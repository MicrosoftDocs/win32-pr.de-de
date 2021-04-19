---
description: 'Die setactualdatalength-Methode legt die Länge der gültigen Daten im Puffer fest. Diese Methode implementiert die imediasample:: setactualdatalength-Methode.'
ms.assetid: a80a67ef-e490-4874-a123-f2d193cec4d7
title: Cmediasample. setactualdatalength-Methode (amfilter. h)
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
ms.openlocfilehash: 825b02f43195424f9ceb5ecd23c4dcf26727ef8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360313"
---
# <a name="cmediasamplesetactualdatalength-method"></a>Cmediasample. setactualdatalength-Methode

Die- `SetActualDataLength` Methode legt die Länge der gültigen Daten im Puffer fest. Diese Methode implementiert die [**imediasample:: setactualdatalength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetActualDataLength(
   long lLen
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Verdammten* 
</dt> <dd>

Länge der gültigen Daten in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                                             | Beschreibung                                                 |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Erfolg.<br/>                                         |
| <dl> <dt>**VFW \_ E- \_ Puffer \_ Überlauf**</dt> </dl> | *lLen* ist größer als die zugeordnete Puffergröße.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode legt die Element Variable [**cmediasample: \_ : m**](cmediasample-m-lactual.md) fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediasample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




