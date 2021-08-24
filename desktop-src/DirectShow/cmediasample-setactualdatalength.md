---
description: Die SetActualDataLength-Methode legt die Länge der gültigen Daten im Puffer fest. Diese Methode implementiert die IMediaSample::SetActualDataLength-Methode.
ms.assetid: a80a67ef-e490-4874-a123-f2d193cec4d7
title: CMediaSample.SetActualDataLength-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetActualDataLength
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: db090ad96f6c53f725aef7864e729b8083bfd1a02b30f0d699d30b5c6f8f71aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634376"
---
# <a name="cmediasamplesetactualdatalength-method"></a>CMediaSample.SetActualDataLength-Methode

Die `SetActualDataLength` -Methode legt die Länge der gültigen Daten im Puffer fest. Diese Methode implementiert die [**IMediaSample::SetActualDataLength-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength)

## <a name="syntax"></a>Syntax


```C++
HRESULT SetActualDataLength(
   long lLen
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lLen* 
</dt> <dd>

Länge der gültigen Daten in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                                             | Beschreibung                                                 |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Erfolg.<br/>                                         |
| <dl> <dt>**VFW \_ E \_ BUFFER \_ OVERFLOW**</dt> </dl> | *lLen* ist größer als die zugeordnete Puffergröße.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode legt die [**Membervariable CMediaSample::m \_ lActual**](cmediasample-m-lactual.md) fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaSample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




