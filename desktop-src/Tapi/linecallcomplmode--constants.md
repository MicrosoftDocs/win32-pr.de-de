---
description: Die Bit-Flag-Konstanten von linecallcomplmode \_ beschreiben verschiedene Methoden, mit denen ein-Vorgang abgeschlossen werden kann.
ms.assetid: 68f755a1-586b-4c5b-b8e8-c8b40eb71685
title: LINECALLCOMPLMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 373a66b6ce13b7bfba00303bea824f542bf0016a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372346"
---
# <a name="linecallcomplmode_-constants"></a>Linecallcomplmode- \_ Konstanten

Die Bit-Flag-Konstanten von **linecallcomplmode \_** beschreiben verschiedene Methoden, mit denen ein-Vorgang abgeschlossen werden kann.

<dl> <dt>

<span id="LINECALLCOMPLMODE_CALLBACK"></span><span id="linecallcomplmode_callback"></span>**linecallcomplmode- \_ Rückruf**
</dt> <dd> <dl> <dt>



Fordert an, dass die aufgerufene Station den Aufruf zurückgibt, wenn Sie in den Leerlauf kehrt.


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_CAMPON"></span><span id="linecallcomplmode_campon"></span>**linecallcomplmode- \_ Campon**
</dt> <dd> <dl> <dt>



Fügt den-aufruder in die Warteschlange ein, bis der-


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_INTRUDE"></span><span id="linecallcomplmode_intrude"></span>**Eingriff in linecallcomplmode \_**
</dt> <dd> <dl> <dt>



Fügt die Anwendung dem vorhandenen Aufruf an der aufgerufenen Station hinzu (Barge in).


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_MESSAGE"></span><span id="linecallcomplmode_message"></span>**linecallcomplmode- \_ Meldung**
</dt> <dd> <dl> <dt>



Hinterlässt eine kurze vordefinierte Meldung für die aufgerufene Station (Wort Aufruf durchlassen). Die zu sendende Nachricht wird separat angegeben.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




