## The Text Plugin ##

The text plugin is used by the version plugin to show its content

### Options ###
  1. Text for the menu tab
  1. Text for the content panel

### Contents in the menu tab ###
  * Your text

### Contents in the content panel ###
  * Your text


### Details ###
Its an easy an fast way to publish information

```
class BarController extends Zend_Controller_Action
{
    ...
    FooAction()
    {
        $important = 'Internal Variable';
        $debugText = new ZFDebug_Controller_Plugin_Debug_Plugin_Text();
        $debugText->setTab('My Information')
                  ->setPanel('Data :' . $important');
        $debug = $this->getPlugin('ZFDebug_Controller_Plugin_Debug');
        $debug->registerPlugin($debugText);
    }
}

```