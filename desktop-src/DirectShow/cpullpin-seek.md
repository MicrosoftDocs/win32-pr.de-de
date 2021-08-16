---
description: Die Seek-Methode legt die Start- und Stopppositionen des Streams fest.
ms.assetid: d84476f5-688c-429d-a51b-7020a6316e35
title: CPullPin.Seek-Methode (Pullpin.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Seek
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 65ea4deddd000d1064adf8b8caf5a636eed87105856d506191d677e70978d096
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953989"
---
# <a name="cpullpinseek-method"></a>CPullPin.Seek-Methode

Die `Seek` -Methode legt die Start- und Stopppositionen des Streams fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT Seek(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*tStart* 
</dt> <dd>

Gibt die Startposition in Bytes multipliziert mit 10.000.000 an.

</dd> <dt>

*tStop* 
</dt> <dd>

Gibt die Stoppposition in Bytes multipliziert mit 10.000.000 an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn die Methode erfolgreich ist, andernfalls ein Fehlercode.

## <a name="remarks"></a>Hinweise

Wenn der Arbeitsthread ausgeführt wird, hält die Methode den Thread an, leert das Filterdiagramm und setzt den Thread wieder auf. Der Thread beginnt mit dem Pullen von Daten von der neuen Startposition. Andernfalls werden die neuen Positionswerte wirksam, sobald der Thread gestartet wird.

Positionen sind relativ zum Anfang der ursprünglichen Quelle. Multiplizieren Sie die gewünschten Byteoffsets mit der Konstanten UNITS, die in der Basisklassenbibliothek als 10.000.000 definiert ist.

Wenn der Pin zum ersten Mal eine Verbindung herstellt, werden die Stopp- und Startpositionen standardmäßig auf den Anfang und das Ende des Streams festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CPullPin-Klasse**](cpullpin.md)
</dt> </dl>

 

 




