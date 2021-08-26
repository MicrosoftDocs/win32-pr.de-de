---
description: Die PHONEBUTTONSTATE-Bitflagkonst constants beschreiben die Positionen der Schaltflächen.
ms.assetid: f1196e31-65c6-4ade-a0b7-c7758ce97be1
title: PHONEBUTTONSTATE_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95070eb24b5189b44f07a8ba2d2d7ed7d8234ec14a97889f09c0fe29ac72eed9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100509"
---
# <a name="phonebuttonstate_-constants"></a>PHONEBUTTONSTATE_ Konstanten

Die **PHONEBUTTONSTATE_** bit-flag-Konstanten beschreiben die Positionen der Schaltfläche.

<dl> <dt>

<span id="PHONEBUTTONSTATE_DOWN"></span><span id="phonebuttonstate_down"></span>**PHONEBUTTONSTATE_DOWN**
</dt> <dd> <dl> <dt>



Die Schaltfläche befindet sich im Zustand "Nach unten" (gedrückt).


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UNAVAIL"></span><span id="phonebuttonstate_unavail"></span>**PHONEBUTTONSTATE_UNAVAIL**
</dt> <dd> <dl> <dt>



Gibt an, dass der Auf- oder Herunter-Zustand der Schaltfläche dem Dienstanbieter nicht bekannt ist und zu einem zukünftigen Zeitpunkt nicht bekannt wird. (TAPI-Versionen 1.4 und höher)


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UNKNOWN"></span><span id="phonebuttonstate_unknown"></span>**PHONEBUTTONSTATE_UNKNOWN**
</dt> <dd> <dl> <dt>



Gibt an, dass der Auf- oder Ab-Zustand der Schaltfläche zu diesem Zeitpunkt nicht bekannt ist, aber zu einem zukünftigen Zeitpunkt bekannt werden kann. (TAPI-Versionen 1.4 und höher)


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONSTATE_UP"></span><span id="phonebuttonstate_up"></span>**PHONEBUTTONSTATE_UP**
</dt> <dd> <dl> <dt>



Die Schaltfläche befindet sich im Zustand "Up".


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Aus Gründen der Abwärtskompatibilität liegt es in der Verantwortung des Dienstanbieters, die ausgehandelte API-Version auf dem Telefon zu untersuchen und diese PHONEBUTTONSTATE_-Werte nicht zu verwenden, die von der ausgehandelten Version nicht unterstützt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




