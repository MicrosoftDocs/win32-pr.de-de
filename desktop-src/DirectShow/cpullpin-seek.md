---
description: Die Seek-Methode legt die Anfangs-und Endposition des Streams fest.
ms.assetid: d84476f5-688c-429d-a51b-7020a6316e35
title: Cpullpin. Seek-Methode (pullpin. h)
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
ms.openlocfilehash: 6f1a82ec549b5ceb888acc194a7abc2cd3eace47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362045"
---
# <a name="cpullpinseek-method"></a>Cpullpin. Seek-Methode

Die `Seek` -Methode legt die Anfangs-und Endposition des Streams fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT Seek(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*tSTART* 
</dt> <dd>

Gibt die Startposition in Bytes multipliziert mit 10 Millionen an.

</dd> <dt>

*tstopps* 
</dt> <dd>

Gibt die Position des Stopps in Bytes multipliziert mit 10 Millionen an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn die Methode erfolgreich ist, andernfalls einen Fehlercode.

## <a name="remarks"></a>Bemerkungen

Wenn der Arbeits Thread ausgeführt wird, hält die Methode den Thread an, leert das Filter Diagramm und setzt den Thread fort. Der Thread beginnt mit dem Abrufen von Daten von der neuen Startposition. Andernfalls werden die neuen Positionswerte immer dann wirksam, wenn der Thread gestartet wird.

Positionen sind relativ zum Anfang der ursprünglichen Quelle. Multiplizieren Sie die gewünschten Byte Offsets um die Konstanten Einheiten, die in der Basisklassen Bibliothek als 10 Millionen definiert sind.

Wenn die PIN zum ersten Mal eine Verbindung herstellt, werden die Start-und Startpositionen standardmäßig auf den Anfang und das Ende des Streams eingestellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpullpin-Klasse**](cpullpin.md)
</dt> </dl>

 

 




