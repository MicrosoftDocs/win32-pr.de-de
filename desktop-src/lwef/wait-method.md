---
title: Wait-Methode
description: Wait-Methode
ms.assetid: 968a3f19-6953-473b-ba98-0dc93696e703
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f2e94b0f765a9861c30b254761fbc4dc2e72763
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106341923"
---
# <a name="wait-method"></a>Wait-Methode

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Bewirkt, dass die Animations Warteschlange für das angegebene Zeichen wartet, bis die angegebene Animations Anforderung abgeschlossen ist.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("*** Merkmal-ID ***"). Warte*** Anforderung*



| Teil      | BESCHREIBUNG                                                                     |
|-----------|---------------------------------------------------------------------------------|
| *Anforderung* | Ein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt, das eine bestimmte Animation angibt. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Methode nur, wenn Sie mehrere (gleichzeitige) Zeichen unterstützen und versuchen, die Interaktion von Zeichen zu sequenzieren. (Bei einem einzelnen Zeichen wird jede Animations Anforderung sequenziell wiedergegeben, nachdem die vorherige Anforderung abgeschlossen wurde.) Wenn Sie zwei Zeichen haben und die Animations Anforderung eines Zeichens warten soll, bis die Animation des anderen Zeichens abgeschlossen ist, legen Sie die **Wait** -Methode auf das Animations [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt für das andere Zeichen fest. Um den Anforderungs Parameter anzugeben, müssen Sie eine Variable erstellen und die Animations Anforderung zuweisen, die Sie unterbrechen möchten:


```
   Dim GenieRequest 
   Dim RobbyRequest 
   Dim Genie 
   Dim Robby 

   Sub window_Onload

   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"
   Agent1.Characters.Load "Robby", "https://agent.microsoft.com/characters/v2/robby/robby.acf"

   Set Genie = Agent1.Characters("Genie")
   Set Robby = Agent1.Characters("Robby")

   Genie.Get "State", "Showing"
   Robby.Get "State", "Showing"

   Genie.Get "Animation", "Announce, AnnounceReturn, Pleased, _ 
      PleasedReturn"
   
   Robby.Get "Animation", "Confused, ConfusedReturn, Sad, SadReturn"

   Set Genie = Agent1.Characters ("Genie")
   Set Robby = Agent1.Characters ("Robby")

   Genie.MoveTo 100,100
   Genie.Show

   Robby.MoveTo 250,100
   Robby.Show

   Genie.Play "Announce"
   Set GenieRequest = Genie.Speak ("Why did the chicken cross the road?")
   
   Robby.Wait GenieRequest
   Robby.Play "Confused"
   Set RobbyRequest = Robby.Speak ("I don't know. Why did the chicken _
      cross the road?")
   
   Genie.Wait RobbyRequest
   Genie.Play "Pleased"
   Set GenieRequest = Genie.Speak ("To get to the other side.")
   
   Robby.Wait GenieRequest
   Robby.Play "Sad"
   Robby.Speak "I never should have asked."

   End Sub
```



Sie können den Code auch optimieren, indem Sie einfach **Wait** direkt aufrufen, indem Sie eine bestimmte Animations Anforderung verwenden.


```
   Robby.Wait Genie.Play "GestureRight"
```



Dadurch ist es nicht erforderlich, ein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt explizit zu deklarieren.

 

 