---
description: Die SetDIBData-Methode gibt Informationen über die geräteunabhängige GDI-Bitmap (DIB) an, die von diesem Objekt verwaltet wird. Rufen Sie diese Methode auf, um das CImageSample-Objekt zu initialisieren.
ms.assetid: 850fa16b-d4b9-4fe6-b202-7b54c49a4589
title: CImageSample.SetDIBData-Methode (Winutil.h)
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
ms.openlocfilehash: 367fed37545e9498f9f6e753a57a7eeeb2ce8767779241284be9109676fafd38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655524"
---
# <a name="cimagesamplesetdibdata-method"></a>CImageSample.SetDIBData-Methode

Die `SetDIBData` -Methode gibt Informationen über die geräteunabhängige GDI-Bitmap (DIB) an, die von diesem Objekt verwaltet wird. Rufen Sie diese Methode auf, um das **CImageSample-Objekt** zu initialisieren.

## <a name="syntax"></a>Syntax


```C++
void SetDIBData(
   DIBDATA *pDibData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDibData* 
</dt> <dd>

Zeiger auf eine [**DIBDATA-Struktur.**](dibdata.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CImageSample-Klasse**](cimagesample.md)
</dt> </dl>

 

 




