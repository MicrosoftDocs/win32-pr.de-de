---
description: Die setdibdata-Methode gibt Informationen über die von diesem Objekt verwaltete GDI-geräteunabhängige Bitmap (DIB) an. Ruft diese Methode auf, um das cimagesample-Objekt zu initialisieren.
ms.assetid: 850fa16b-d4b9-4fe6-b202-7b54c49a4589
title: Cimagesample. setdibdata-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.SetDIBData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 418263da0416b325b1b080713dd6289f3bcc688e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358247"
---
# <a name="cimagesamplesetdibdata-method"></a>Cimagesample. setdibdata-Methode

Die- `SetDIBData` Methode gibt Informationen über die von diesem Objekt verwaltete GDI-geräteunabhängige Bitmap (DIB) an. Ruft diese Methode auf, um das **cimagesample** -Objekt zu initialisieren.

## <a name="syntax"></a>Syntax


```C++
void SetDIBData(
   DIBDATA *pDibData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdibdata* 
</dt> <dd>

Zeiger auf eine [**dibdata**](dibdata.md) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cimagesample-Klasse**](cimagesample.md)
</dt> </dl>

 

 




