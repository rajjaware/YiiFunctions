YiiFunctions
============

Helper file, a collections of Yii function to make the Yii coding shorten.

The goal of this file is to make more simplication and new way of coding design.

- How to install this file ?
Steps:
    1 ) For you to able to organize the location of the directory, create a subfolder under the 'protected' folder name 'functions'
    
    2 ) On the index.php, insert the line
    
        require_once(dirname(__FILE__) . '/protected/functions/yii.php');
        
        before the line.
        
        Yii::createWebApplication($config)->run();
		
		EX:
			<?php

			// change the following paths if necessary
			$yii=dirname(__FILE__).'/1.1.9/framework/yii.php';
			$config=dirname(__FILE__).'/1.1.9/protected/config/main.php';

			// remove the following lines when in production mode
			defined('YII_DEBUG') or define('YII_DEBUG',true);
			// specify how many levels of call stack should be shown in each log message
			defined('YII_TRACE_LEVEL') or define('YII_TRACE_LEVEL',3);
			
			require_once(dirname(__FILE__) . '/protected/functions/yii.php'); // I insert this new line for my index.php file
			
			require_once($yii);
			Yii::createWebApplication($config)->run();
        
    3 ) That's all, you're now finish installing the functions.
    
    
- How To use this functions? Benefits below:

Before :
	Yii::app()->
	
Now :
	webapp()->
	
	
	
Before :
	Yii::app()->params['params1']['params2']['params3']
	
Now :
	params('params1.params2.params3')
	

	
Before :
	CHtml::link($text, $url, $htmlOptions);
	
Now : 
	hyperlink($text, $url, $htmlOptions)