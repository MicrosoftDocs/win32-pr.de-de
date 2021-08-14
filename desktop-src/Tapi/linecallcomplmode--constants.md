---
description: Die \_ LINECALLCOMPLMODE-Bitflagkonst constants beschreiben verschiedene Möglichkeiten, wie ein Aufruf abgeschlossen werden kann.
ms.assetid: 68f755a1-586b-4c5b-b8e8-c8b40eb71685
title: LINECALLCOMPLMODE_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d43f76c9b8012f9ecb60c6b0ffd787d5a0bad87794eb833cc4095c276ba983f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761754"
---
# <a name="linecallcomplmode_-constants"></a>LINECALLCOMPLMODE-Konstanten \_

Die **\_ LINECALLCOMPLMODE-Bitflags-Konstanten** beschreiben verschiedene Möglichkeiten, wie ein Aufruf abgeschlossen werden kann.

<dl> <dt>

<span id="LINECALLCOMPLMODE_CALLBACK"></span><span id="linecallcomplmode_callback"></span>**LINECALLCOMPLMODE-RÜCKRUF \_**
</dt> <dd> <dl> <dt>



Fordert die aufgerufene Station auf, den Aufruf zurückgibt, wenn sie in den Leerlauf zurückkehrt.


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_CAMPON"></span><span id="linecallcomplmode_campon"></span>**LINECALLCOMPLMODEZEILEN \_**
</dt> <dd> <dl> <dt>



Reiht den Aufruf in die Warteschlange ein, bis der Aufruf abgeschlossen werden kann.


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_INTRUDE"></span><span id="linecallcomplmode_intrude"></span>**LINECALLCOMPLMODE \_ INTRUDE**
</dt> <dd> <dl> <dt>



Fügt die Anwendung dem vorhandenen Aufruf an der aufgerufenen Station (Barge in) hinzu.


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_MESSAGE"></span><span id="linecallcomplmode_message"></span>**LINECALLCOMPLMODE-NACHRICHT \_**
</dt> <dd> <dl> <dt>



Hinterlässt eine kurze vordefinierte Nachricht für die aufgerufene Station (Word Calling verlassen). Die zu sendende Nachricht wird separat angegeben.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




