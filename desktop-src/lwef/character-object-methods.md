---
title: Zeichenobjektmethoden
description: Zeichenobjektmethoden
ms.assetid: 0f926b7b-c1cf-4bd6-ba8c-1b2877eb1d24
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 141c0fbcfe26e198984fd4a4d8c6c67858085e41178786d2cb78d2938231fdf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118480314"
---
# <a name="character-object-methods"></a>Zeichenobjektmethoden

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Der Server macht auch Methoden für jedes Zeichen in einer [**Characters-Auflistung**](/windows/desktop/lwef/the-characters-object) verfügbar. Folgende Methoden werden unterstützt:

-   [**Aktivieren**](activate-method.md)
-   [**GestureAt**](gestureat-method.md)
-   [**Erhalten**](get-method.md)
-   [**Ausblenden**](hide-method.md)
-   [**Interrupt**](interrupt-method.md)
-   [**Hören**](listen-method.md)
-   [**Moveto**](moveto-method.md)
-   [**Abspielen**](play-method.md)
-   [**Zeigen**](show-method.md)
-   [**ShowPopupMenu**](showpopupmenu-method.md)
-   [**Speak**](speak-method.md)
-   [**Beenden**](stop-method.md)
-   [**StopAll**](stopall-method.md)
-   [**Denke**](think-method.md)
-   [**Wait**](wait-method.md)

Um eine Methode zu verwenden, verweisen Sie auf das Zeichen in der Auflistung. In VBScript und Visual Basic geben Sie dazu die ID für ein Zeichen an:


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



Um die Syntax Ihres Codes zu vereinfachen, können Sie eine Objektvariable definieren und festlegen, um auf ein Zeichenobjekt in der [**Characters-Auflistung**](/windows/desktop/lwef/the-characters-object) zu verweisen. dann können Sie ihre Variable verwenden, um auf Methoden oder Eigenschaften des Zeichens zu verweisen. Im folgenden Beispiel wird veranschaulicht, wie Sie dies mithilfe der set-Anweisung Visual Basic:


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



In Visual Basic 5.0 können Sie den Verweis auch erstellen, indem Sie Ihre Variable als [**Zeichenobjekt**](/windows/desktop/lwef/the-characters-object)deklarieren:


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



Das Deklarieren ihres Objekts vom Typ IAgentCtlCharacterEx ermöglicht eine frühe Bindung des Objekts, was zu einer besseren Leistung führt.

In VBScript können Sie einen Verweis nicht als bestimmten Typ deklarieren. Sie können jedoch einfach den Variablenverweis deklarieren:


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



Einige Programmiersprachen unterstützen keine Sammlungen. Sie können jedoch mit der [**Character-Methode**](/windows/desktop/lwef/the-characters-object) auf die Methoden eines [**Character-Objekts**](character-method.md) zugreifen:


```
   agent.Characters.Character("CharacterID").method
```



Darüber hinaus können Sie auch einen Verweis auf das [**Character-Objekt**](/windows/desktop/lwef/the-characters-object) erstellen, damit Ihr Skriptcode leichter zu befolgen ist:


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



 

 