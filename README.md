# SharePractice

Shares data with implicit intents

override fun onOptionsItemSelected(item: MenuItem): Boolean {
        // Handle action bar item clicks here. The action bar will
        // automatically handle clicks on the Home/Up button, so long
        // as you specify a parent activity in AndroidManifest.xml.
        return when (item.itemId) {
            R.id.action_settings -> true
            R.id.action_share -> share()
            else -> super.onOptionsItemSelected(item)
        }
    }

    private fun share(): Boolean {

        val intent = Intent().apply {
            action = Intent.ACTION_SEND
            putExtra(Intent.EXTRA_TEXT, "Hello SharePractice")
            type = "text/plain"
        }
        startActivity(intent)
        return true
    }
