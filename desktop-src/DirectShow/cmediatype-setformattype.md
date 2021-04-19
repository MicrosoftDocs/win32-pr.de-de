---
description: Die setformattype-Methode gibt den Formattyp an.
ms.assetid: e8ed9190-7169-4d51-ace7-597f43ff083e
title: Cmediatype. setformattype-Methode (mtype. h)
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
ms.openlocfilehash: 7843c5a9788545909ef4297accfa342c08b71e88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362012"
---
# <a name="cmediatypesetformattype-method"></a>Cmediatype. setformattype-Methode

Die setformattype-Methode von ' ' gibt den Formattyp an.

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

Zeiger auf eine **GUID** , die den Formattyp angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode legt den **Format Type** -Member fest. Der Formattyp definiert das Layout des Format Blocks. Wenn der Formattyp beispielsweise Format \_ videoinfo ist, sollte der Format Block eine **videoinfoheader** -Struktur enthalten. Um den Format Block festzulegen, müssen Sie die [**cmediatype:: SetFormat**](cmediatype-setformat.md) -Methode aufrufen. Der Aufrufer ist dafür verantwortlich, sicherzustellen, dass der Format Block mit dem Formattyp übereinstimmt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediatype-Klasse**](cmediatype.md)
</dt> </dl>

 

 


``
