---
title: Zeichen Objektmethoden
description: Zeichen Objektmethoden
ms.assetid: 0f926b7b-c1cf-4bd6-ba8c-1b2877eb1d24
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19bb0dbb256c99660cbce1613c9fdd27d85a92dc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948606"
---
# <a name="character-object-methods"></a>Zeichen Objektmethoden

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Der Server macht auch Methoden für jedes Zeichen in einer [**Zeichen**](/windows/desktop/lwef/the-characters-object) Auflistung verfügbar. Folgende Methoden werden unterstützt:

-   [**Aktivieren**](activate-method.md)
-   [**Gestureat**](gestureat-method.md)
-   [**Erhalten**](get-method.md)
-   [**Ausblenden**](hide-method.md)
-   [**Interrupt**](interrupt-method.md)
-   [**Lauschen**](listen-method.md)
-   [**MoveTo**](moveto-method.md)
-   [**Abspielen**](play-method.md)
-   [**Auftritt**](show-method.md)
-   [**ShowPopupMenu**](showpopupmenu-method.md)
-   [**Speak**](speak-method.md)
-   [**Stop**](stop-method.md)
-   [**StopAll**](stopall-method.md)
-   [**Meiner**](think-method.md)
-   [**Wait**](wait-method.md)

Um eine Methode zu verwenden, verweisen Sie auf das Zeichen in der Auflistung. In VBScript und Visual Basic müssen Sie dazu die ID für ein Zeichen angeben:


```
   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", "Genie.acs"

   'Display the character
   Agent1.Characters("Genie").Show
   Agent1.Characters("Genie").Play "Greet"
   Agent1.Characters("Genie").Speak "Hello. "

   End Sub
```



Um die Syntax des Codes zu vereinfachen, können Sie eine Objekt Variable definieren und Sie so festlegen, dass Sie auf ein Zeichen Objekt in der [**Zeichen**](/windows/desktop/lwef/the-characters-object) Auflistung verweist. Anschließend können Sie die Variable verwenden, um auf Methoden oder Eigenschaften des Zeichens zu verweisen. Im folgenden Beispiel wird veranschaulicht, wie Sie dies mit der Visual Basic Set-Anweisung erreichen können:


```
   'Define a global object variable
   Dim Genie as Object

   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", " Genie.acs"

   'Create a reference to the character
   Set Genie = Agent1.Characters("Genie")

   'Display the character
   Genie.Show

   'Get the Restpose animation
   Genie.Get "animation", "RestPose"

   'Make the character say Hello
   Genie.Speak "Hello."

   End Sub
```



In Visual Basic 5,0 können Sie auch den Verweis erstellen, indem Sie die Variable als [**Zeichen**](/windows/desktop/lwef/the-characters-object)Objekt deklarieren:


```
   Dim Genie as IAgentCtlCharacterEx

   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", "Genie.acs"

   'Create a reference to the character
   Set Genie = Agent1.Characters("Genie")

   'Display the character
   Genie.Show

   End Sub
```



Durch das Deklarieren Ihres Objekts vom Typ iagentctlcharakteriex wird eine frühe Bindung für das Objekt ermöglicht, was zu einer besseren Leistung führt.

In VBScript können Sie keinen Verweis als bestimmten Typ deklarieren. Sie können jedoch einfach den Variablen Verweis deklarieren:


```
<SCRIPT LANGUAGE = "VBSCRIPT">
<!—--

   Dim Genie
   
   Sub window_OnLoad
   
   'Load the character
   AgentCtl.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   'Create an object reference to the character in the collection
   set Genie= AgentCtl.Characters ("Genie")

   'Get the Showing state animation
   Genie.Get "state", "Showing"

   'Display the character
   Genie.Show

   End Sub

-->
   </SCRIPT>
```



Einige Programmiersprachen unterstützen keine Auflistungen. Allerdings können Sie mit der [**Zeichen**](character-method.md) Methode auf die Methoden eines [**Zeichen**](/windows/desktop/lwef/the-characters-object) Objekts zugreifen:


```
   agent.Characters.Character("CharacterID").method
```



Darüber hinaus können Sie auch einen Verweis auf das [**Zeichen**](/windows/desktop/lwef/the-characters-object) Objekt erstellen, damit der Skriptcode leichter befolgt werden kann:


```
<SCRIPT LANGUAGE="JScript" FOR="window" EVENT="onLoad()">
<!--
   
   //Load the character's data
   AgentCtl.Characters.Load ("Genie", _
      "https://agent.microsoft.com/characters/v2/genie/genie.acf");   

   //Create a reference to this object
   Genie = AgentCtl.Characters.Character("Genie");
   
   //Get the Showing state animation
   Genie.Get("state", "Showing");

   //Display the character
   Genie.Show();

-->
</SCRIPT>
```



 

 