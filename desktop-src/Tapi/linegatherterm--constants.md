---
description: Die bitflagkonstanten von linegatherterm \_ beschreiben die Bedingungen, unter denen die pufferte Ziffern Erfassung beendet wird.
ms.assetid: 409e1984-e5a4-4636-ab53-5973fe7b78ea
title: LINEGATHERTERM_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968492a584024c7750b417a9fd03b68ac1df42ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354830"
---
# <a name="linegatherterm_-constants"></a>Linegatherterm- \_ Konstanten

Die bitflagkonstanten von **linegatherterm \_** beschreiben die Bedingungen, unter denen die pufferte Ziffern Erfassung beendet wird.

<dl> <dt>

<span id="LINEGATHERTERM_BUFFERFULL"></span><span id="linegatherterm_bufferfull"></span>**linegatherterm \_ bufferfull**
</dt> <dd> <dl> <dt>



Die angeforderte Anzahl von Ziffern wurde gesammelt. Der Puffer ist voll.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_CANCEL"></span><span id="linegatherterm_cancel"></span>**linegatherterm \_ Abbrechen**
</dt> <dd> <dl> <dt>



Die Anforderung wurde von dieser Anwendung, von einer anderen Anwendung oder von der Beendigung des Aufrufes abgebrochen.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_FIRSTTIMEOUT"></span><span id="linegatherterm_firsttimeout"></span>**linegatherterm \_ firsttimeout**
</dt> <dd> <dl> <dt>



Das erste Ziffern Timeout ist abgelaufen. Der Puffer enthält keine Ziffern.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_INTERTIMEOUT"></span><span id="linegatherterm_intertimeout"></span>**linegatherterm- \_ intertimeout**
</dt> <dd> <dl> <dt>



Das zwischen Ziffern Timeout ist abgelaufen. Der Puffer enthält mindestens eine Ziffer.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_TERMDIGIT"></span><span id="linegatherterm_termdigit"></span>**linegatherterm \_ termdigit**
</dt> <dd> <dl> <dt>



Eine der Beendigungs Ziffern entsprach einer empfangenen Ziffer. Die übereinstimmende Abbruch Ziffer ist die letzte Ziffer im Puffer.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




