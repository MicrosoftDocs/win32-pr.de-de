---
title: Interrupt-Methode
description: Interrupt-Methode
ms.assetid: b8442e25-a629-47c7-acdd-1d28e74d78a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e66814963bb3de3db95d60cbc25777244626168e95ceee4bd3d8d76992dd72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749257"
---
# <a name="interrupt-method"></a>Interrupt-Methode

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Unterbricht die Animation für das angegebene Zeichen.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Interruptanforderung_ *  



| Teil      | BESCHREIBUNG                                                                  |
|-----------|------------------------------------------------------------------------------|
| *Anforderung* | Ein [**Request-Objekt**](/windows/desktop/lwef/the-request-object) für einen bestimmten Animationsaufruf. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Damit können Sie Animationen zwischen Zeichen synchronisieren. Wenn sich beispielsweise ein anderes Zeichen in einer Schleifenanimation befindet, beendet diese Methode die Schleife und wechselt zur nächsten Animation in der Warteschlange des Zeichens. Sie können keine Zeichenanimation unterbrechen, die Sie nicht verwenden (die Sie nicht geladen haben).

Um den Anforderungsparameter anzugeben, müssen Sie eine Variable erstellen und die Animationsanforderung zuweisen, die Sie unterbrechen möchten:


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



Sie können die Animation desselben Zeichens, das Sie in dieser Methode angeben, nicht unterbrechen, da der Server die **Interrupt-Methode** in der Animationswarteschlange dieses Zeichens in die Warteschlange einreiht. Daher können Sie **interrupt** nur verwenden, um die Animation eines anderen Zeichens anzuhalten, das Sie geladen haben.

Wenn Sie einen Objektverweis deklarieren und auf diese Methode festlegen, wird ein [**Request-Objekt**](/windows/desktop/lwef/the-request-object) zurückgegeben.

> [!Note]  
> **Interrupt** leert die Warteschlange des Zeichens nicht. Sie hält die vorhandene Animation an und fährt mit der nächsten Animation in der Warteschlange des Zeichens fort. Verwenden Sie die Stop-Methode, um [](stop-method.md) die Warteschlange eines Zeichens anzuhalten und zu leeren.

 

## <a name="see-also"></a>Weitere Informationen

[**Stop-Methode**](stop-method.md)


 

 