---
description: Die SetFormatType-Methode gibt den Formattyp an.
ms.assetid: e8ed9190-7169-4d51-ace7-597f43ff083e
title: CMediaType.SetFormatType-Methode (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormatType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f6a0582a882ffe40a9bd889ff48e70a52a4048bad57e01077263e607f13d9898
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954419"
---
# <a name="cmediatypesetformattype-method"></a>CMediaType.SetFormatType-Methode

Die SetFormatType-Methode gibt den Formattyp an.

## <a name="syntax"></a>Syntax


```C++
void SetFormatType(
   const GUID *pformattype
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pformattype* 
</dt> <dd>

Zeiger auf eine **GUID,** die den Formattyp angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode legt den **formattype-Member** fest. Der Formattyp definiert das Layout des Formatblocks. Wenn der Formattyp beispielsweise FORMAT \_ VideoInfo ist, sollte der Formatblock eine **VIDEOINFOHEADER-Struktur** enthalten. Rufen Sie zum Festlegen des Formatblocks die [**CMediaType::SetFormat-Methode**](cmediatype-setformat.md) auf. Der Aufrufer ist dafür verantwortlich, sicherzustellen, dass der Formatblock dem Formattyp entspricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaType-Klasse**](cmediatype.md)
</dt> </dl>

 

 


``
