---
title: Zeichen Objekteigenschaften
description: Zeichen Objekteigenschaften
ms.assetid: 86748de2-f5c8-4057-bfa4-79d46cac1e62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6212d6f0539b7fcb29faa883e6d88101952c12f5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390142"
---
# <a name="character-object-properties"></a>Zeichen Objekteigenschaften

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Das [**Character**](/windows/desktop/lwef/the-characters-object) -Objekt macht die folgenden Eigenschaften verfügbar:

-   [**Aktiv**](active-property.md)
-   [**Autopopupmenu**](autopopupmenu-property.md)
-   [**Beschreibung**](description-property.md)
-   [**ExtraData**](extradata-property.md)
-   [**GUID**](guid-property.md)
-   [**Hasotherclients**](hasotherclients-property.md)
-   [**Höhe**](height-property.md)
-   [**HelpContextID**](helpcontextid-property-ch.md)
-   [**HelpFile**](helpfile-property.md)
-   [**Helpmudeon**](helpmodeon-property.md)
-   [**Idleon**](idleon-property.md)
-   [**LanguageID**](languageid-property.md)
-   [**Linken**](left-property.md)
-   [**"Muvecause"**](movecause-property.md)
-   [**Name**](name-property.md)
-   [**OriginalHeight**](originalheight-property.md)
-   [**OriginalWidth**](originalwidth-property.md)
-   [**Neigung**](pitch-property.md)
-   [**Sounentffectson**](soundeffectson-property.md)
-   [**Geschwindigkeit**](speed-property.md)
-   [**Srmodeid**](srmodeid-property.md)
-   [**Srstatus**](srstatus-property.md)
-   [**Nach oben**](top-property.md)
-   [**Ttsmodeid**](ttsmodeid-property.md)
-   [**Version**](version-property.md)
-   [**Visibilitycause**](visibilitycause-property.md)
-   [**Sichtbar**](visible-property-cob.md)
-   [**Breite**](width-property-co.md)

Beachten Sie, dass sich die Eigenschaften [**height**](height-property.md), [**left**](left-property.md), [**Top**](top-property.md)und [**Width**](width-property-co.md) eines Zeichens von denen unterscheiden, die möglicherweise von der Programmierumgebung für die Platzierung des Steuer Elements unterstützt werden. Die [**Zeichen**](/windows/desktop/lwef/the-characters-object) Eigenschaften gelten für die sichtbare Darstellung eines Zeichens, nicht für den Speicherort des Microsoft-Agent-Steuer Elements.

Wie bei [**Zeichen**](/windows/desktop/lwef/the-characters-object) Objektmethoden können Sie mithilfe der [**Zeichen**](/windows/desktop/lwef/the-characters-object) Auflistung auf die Eigenschaften eines Zeichens zugreifen oder die Syntax vereinfachen, indem Sie eine Objekt Variable deklarieren und Sie auf ein Zeichen in der Auflistung festlegen. Im folgenden Beispiel werden Test1 und test2 auf denselben Wert festgelegt:


```
   Dim Genie 
   Dim MyRequest
   
   Sub window_Onload

   Agent.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent.Characters("Genie")

   Genie.MoveTo 15,15
   Set MyRequest = Genie.Show()

   End Sub

   Sub Agent_RequestComplete(ByVal Request)

   If Request = MyRequest Then 
      Test1 = Agent.Characters("Genie").Top
      Test2 = Genie.Top
      MsgBox "Test 1 is " + cstr(Test1) + "and Test 2 is " + cstr(Test2)
   End If

   End Sub
```



Da der Server ein Zeichen asynchron lädt, stellen Sie sicher, dass das Zeichen vor dem Abfragen der Eigenschaften geladen wurde, z. b. mit dem [**requestcomplete**](requestcomplete-event.md) -Ereignis. Andernfalls können die Eigenschaften falsche Werte zurückgeben.

 

 