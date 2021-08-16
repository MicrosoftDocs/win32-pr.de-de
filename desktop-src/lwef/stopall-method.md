---
title: StopAll-Methode
description: StopAll-Methode
ms.assetid: 2ce32ff8-4908-45b1-9b83-4d558f67417c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b138be6ea75135d5ddefdea9e1e5cc120d875ae092478ad3147332720e5a0907
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745942"
---
# <a name="stopall-method"></a>StopAll-Methode

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Beendet alle Animationsanforderungen oder angegebenen Anforderungstypen für das angegebene Zeichen.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). StopAll-Typ_ *  \[ \]



| Teil   | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Type* | Optional. Um diesen Parameter zu verwenden, können Sie einen der folgenden Werte verwenden. Sie können auch mehrere Typen angeben, indem Sie sie durch Kommas trennen. <br/> "**Get**" <br/> So beenden Sie alle [**Get-Anforderungen in**](get-method.md) der Warteschlange.<br/> "**NonQueuedGet**" <br/> So beenden Sie alle [](get-method.md) Get-Anforderungen, die sich nicht in der Warteschlange befinden ( Get-Methode, bei der **der Queue-Parameter** auf **False festgelegt ist).**<br/> "**Move**" <br/> So beenden Sie alle [**MoveTo-Anforderungen**](moveto-method.md) in der Warteschlange.<br/> "**Play**" <br/> So beenden Sie alle [**Play-Anforderungen in**](play-method.md) der Warteschlange.<br/> "**Speak**" <br/> So beenden Sie alle [**Speak-Anforderungen in**](speak-method.md) der Warteschlange.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn Sie den **Type-Parameter** nicht festlegen, beendet der Server alle Animationen für [](get-method.md) das Zeichen, einschließlich Get-Anforderungen in der Warteschlange und nicht in der Warteschlange, und entfernt seine Animationswarteschlange. Außerdem wird die Wiedergabe der Animation "Ausblenden" oder "Anzeigen" eines Zeichens beendet.

Diese Methode generiert kein [**Request-Objekt.**](/windows/desktop/lwef/the-request-object)

## <a name="see-also"></a>Weitere Informationen

[**Stop-Methode**](stop-method.md)


 

