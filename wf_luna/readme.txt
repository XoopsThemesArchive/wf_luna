*************************************************
*						*
* 		Theme 1.0		*
*						*
*		    Xoops v2.0.x		*
*		Theme design by solo		*
*	   visit us : www.wolfpackclan.com	*
*						*
*************************************************
Theme 1.0

Attention : pour afficher l'ic�ne signalant les nouveaux messages, il faut remplacer le fichier 'header.php' par celui fourni.
Ce fichier est adapt� pour la version 2.0.5.1 de Xoops. 

Autrement eff�ctuez la modification suivante dans le fichier header.php � la racine de votre site :

Apr�s la 2i�me ligne : 

if ($xoopsUser != '') { 


//D�but Hack PM anim�
$pm_handler =& xoops_gethandler('privmessage');
$criteria = new CriteriaCompo(new Criteria('read_msg', 0));
$criteria->add(new Criteria('to_userid', $xoopsUser->getVar('uid')));
$xoopsTpl->assign('nbrepm', $pm_handler->getCount($criteria));
//Fin Hack PM anim�

Bon Xoops

-----------------------
Theme 1.0

Attention : to show the new PM button button, you must replace the 'header.php' by the current one.
This hack is adapted for the 2.0.5.1 version of Xoops. 

Otherwise, apply the following modification to the 'header.php' file on the site root.

After the 2nd line : 

if ($xoopsUser != '') { 


//Start hack animated PM
$pm_handler =& xoops_gethandler('privmessage');
$criteria = new CriteriaCompo(new Criteria('read_msg', 0));
$criteria->add(new Criteria('to_userid', $xoopsUser->getVar('uid')));
$xoopsTpl->assign('nbrepm', $pm_handler->getCount($criteria));
//End hack animated PM


Enjoy !

-----------------------


Solo (aka solo71 - www.wolfpackclan.com)

