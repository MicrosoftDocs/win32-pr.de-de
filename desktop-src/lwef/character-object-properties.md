---
title: Eigenschaften von Zeichenobjekten
description: Eigenschaften von Zeichenobjekten
ms.assetid: 86748de2-f5c8-4057-bfa4-79d46cac1e62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c80e16bdb35d3fdfd8687eb15f200d2005ab75027e4dcc786f883d21232af4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610690"
---
# <a name="character-object-properties"></a>Eigenschaften von Zeichenobjekten

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Das [**Character-Objekt**](/windows/desktop/lwef/the-characters-object) macht die folgenden Eigenschaften verfügbar:

-   [**Aktiv**](active-property.md)
-   [**AutoPopupMenu**](autopopupmenu-property.md)
-   [**Beschreibung**](description-property.md)
-   [**Extradata**](extradata-property.md)
-   [**GUID**](guid-property.md)
-   [**HasOtherClients**](hasotherclients-property.md)
-   [**Height**](height-property.md)
-   [**Helpcontextid**](helpcontextid-property-ch.md)
-   [**Helpfile**](helpfile-property.md)
-   [**HelpModeOn**](helpmodeon-property.md)
-   [**IdleOn**](idleon-property.md)
-   [**Languageid**](languageid-property.md)
-   [**Links**](left-property.md)
-   [**MoveCause**](movecause-property.md)
-   [**Name**](name-property.md)
-   [**OriginalHeight**](originalheight-property.md)
-   [**OriginalWidth**](originalwidth-property.md)
-   [**Neigung**](pitch-property.md)
-   [**SoundEffectsOn**](soundeffectson-property.md)
-   [**Geschwindigkeit**](speed-property.md)
-   [**SRModeID**](srmodeid-property.md)
-   [**SRStatus**](srstatus-property.md)
-   [**Nach oben**](top-property.md)
-   [**TTSModeID**](ttsmodeid-property.md)
-   [**Version**](version-property.md)
-   [**VisibilityCause**](visibilitycause-property.md)
-   [**Sichtbar**](visible-property-cob.md)
-   [**Width**](width-property-co.md)

Beachten Sie, dass sich die Eigenschaften [**Height,**](height-property.md) [**Left,**](left-property.md) [**Top**](top-property.md)und [**Width**](width-property-co.md) eines Zeichens von denen unterscheiden, die von der Programmierumgebung für die Platzierung des Steuerelements unterstützt werden können. Die [**Zeicheneigenschaften**](/windows/desktop/lwef/the-characters-object) gelten für die sichtbare Darstellung eines Zeichens, nicht für die Position des Microsoft-Agent-Steuerelements.

Wie bei [**Character-Objektmethoden**](/windows/desktop/lwef/the-characters-object) können Sie mithilfe der [**Characters-Auflistung**](/windows/desktop/lwef/the-characters-object) auf die Eigenschaften eines Zeichens zugreifen oder Ihre Syntax vereinfachen, indem Sie eine Objektvariable deklarieren und auf ein Zeichen in der Auflistung festlegen. Im folgenden Beispiel werden Test1 und Test2 auf den gleichen Wert festgelegt:


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



Da der Server ein Zeichen asynchron lädt, stellen Sie sicher, dass das Zeichen geladen wurde, bevor Sie seine Eigenschaften abfragen, z. B. mithilfe des [**RequestComplete-Ereignisses.**](requestcomplete-event.md) Andernfalls geben die Eigenschaften möglicherweise falsche Werte zurück.

 

 