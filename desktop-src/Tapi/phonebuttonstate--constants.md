---
description: Die "phonebuttonstate"-bitflagkonstanten beschreiben die Positionen der Schaltflächen.
ms.assetid: f1196e31-65c6-4ade-a0b7-c7758ce97be1
title: PHONEBUTTONSTATE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b1cc2f669fb5c1171834f46e11a161e9390eab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365439"
---
# <a name="phonebuttonstate_-constants"></a>PHONEBUTTONSTATE_ Konstanten

Die **PHONEBUTTONSTATE_** bitflagkonstanten beschreiben die Positionen der Schaltfläche.

<dl> <dt>

<span id="PHONEBUTTONSTATE_DOWN"></span><span id="phonebuttonstate_down"></span>**PHONEBUTTONSTATE_DOWN**
</dt> <dd> <dl> <dt>



Die Schaltfläche befindet sich im Zustand "nach unten" (gedrückt).


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UNAVAIL"></span><span id="phonebuttonstate_unavail"></span>**PHONEBUTTONSTATE_UNAVAIL**
</dt> <dd> <dl> <dt>



Gibt an, dass der Status der Schaltfläche für den Dienstanbieter nicht bekannt ist und zu einem späteren Zeitpunkt nicht bekannt wird. (TAPI-Versionen 1,4 und höher)


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UNKNOWN"></span><span id="phonebuttonstate_unknown"></span>**PHONEBUTTONSTATE_UNKNOWN**
</dt> <dd> <dl> <dt>



Gibt an, dass der Zustand der Schaltfläche zurzeit nicht bekannt ist, aber zu einem späteren Zeitpunkt bekannt werden kann. (TAPI-Versionen 1,4 und höher)


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UP"></span><span id="phonebuttonstate_up"></span>**PHONEBUTTONSTATE_UP**
</dt> <dd> <dl> <dt>



Die Schaltfläche befindet sich im Status "up".


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Aus Gründen der Abwärtskompatibilität liegt es in der Verantwortung des Dienstanbieters, die ausgehandelte API-Version auf dem Telefon zu untersuchen und diese PHONEBUTTONSTATE_ Werte zu verwenden, die von der ausgehandelten Version nicht unterstützt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




