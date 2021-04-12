---
title: Interrupt-Methode
description: Interrupt-Methode
ms.assetid: b8442e25-a629-47c7-acdd-1d28e74d78a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58050e181525cc4a4b9f35ec169e92d91ab28e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390323"
---
# <a name="interrupt-method"></a>Interrupt-Methode

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Unterbricht die Animation für das angegebene Zeichen.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("*** Merkmal-ID * * *"). Interrupt*- *  *Anforderung*



| Teil      | BESCHREIBUNG                                                                  |
|-----------|------------------------------------------------------------------------------|
| *Anforderung* | Ein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt für einen bestimmten Animations Aufruf. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Damit können Sie die Animation zwischen Zeichen synchronisieren. Wenn sich z. b. ein anderes Zeichen in einer Schleifen Animation befindet, beendet diese Methode die Schleife und wechselt zur nächsten Animation in der Warteschlange des Zeichens. Eine Zeichen Animation, die Sie nicht verwenden (die Sie nicht geladen haben), kann nicht unterbrochen werden.

Um den Anforderungs Parameter anzugeben, müssen Sie eine Variable erstellen und die Animations Anforderung zuweisen, die Sie unterbrechen möchten:


```
   Dim GenieRequest as Object
   Dim RobbyRequest as Object
   Dim Genie as Object
   Dim Robby as Object

   Sub FormLoad()

      MyAgent1.Characters.Load "Genie", "Genie.acs"

      MyAgent1.Characters.Load "Robby", "Robby.acs"

      Set Genie = MyAgent1.Characters ("Genie")
      Set Robby = MyAgent1.Characters ("Robby")

      Genie.Show

      Genie.Speak "Just a moment"

      Set GenieRequest = Genie.Play ("Processing")

      Robby.Show
      Robby.Play "confused"
      Robby.Speak "Hey, Genie. What are you doing?"
      Robby.Interrupt GenieRequest

      Genie.Speak "I was just checking on something."

   End Sub
```



Sie können die Animation desselben Zeichen, das Sie in dieser Methode angeben, nicht unterbrechen, da der Server die **Interrupt** -Methode in die Animations Warteschlange dieses Zeichens eingereiht. Daher können Sie nur **Interrupt** verwenden, um die Animation eines anderen Zeichens anzuhalten, das Sie geladen haben.

Wenn Sie einen Objekt Verweis deklarieren und diesen auf diese Methode festlegen, wird ein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt zurückgegeben.

> [!Note]  
> Der **Interrupt** leert die Warteschlange des Zeichens nicht. Sie hält die vorhandene Animation an und wechselt zur nächsten Animation in der Warteschlange des Zeichens. Verwenden Sie die Stop-Methode, um die Warteschlange eines Zeichens [**anzuhalten**](stop-method.md) und zu leeren.

 

## <a name="see-also"></a>Weitere Informationen

[**Stop-Methode**](stop-method.md)


 

 