How to use this Plugin
===

Introduction
---

This code snipped shows how to use the FirePHP Plugin for AdoDB Lite.

Code Snipped
---

	$debug = true;
	
	require_once('lib/FirePHPCore/fb.php');
	
	$firephp = FirePHP::getInstance(true);
	
	if($debug)
	{
		ob_start(); // requiered by FirePHP
		$firephp->setEnabled(true);
	}
	else
	{
		$firephp->setEnabled(false);
	}
	
	require_once('lib/adodb_lite/adodb.inc.php');
	require_once('lib/adodb_lite/adodb-firephp.inc.php'); 
	
	$db = NewADOConnection($DATABASE_DNS);
	$db->debug = $debug;
	
	//...


License
---

See [license](master/license) file.
