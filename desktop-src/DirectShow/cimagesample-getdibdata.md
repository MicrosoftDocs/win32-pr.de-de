---
description: Die GetDIBData-Methode ruft Informationen über die geräteunabhängige GDI-Bitmap (DEVICE-Independent Bitmap, DIB) ab, die von diesem Objekt verwaltet wird.
ms.assetid: ec337336-69ec-47ff-a522-42c0388f9bc0
title: CImageSample.GetDIBData-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.GetDIBData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 894d75512c6c7909f617e13999e7290efea663fa843bf64424aad8371965de75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655599"
---
# <a name="cimagesamplegetdibdata-method"></a>CImageSample.GetDIBData-Methode

Die `GetDIBData` -Methode ruft Informationen über die geräteunabhängige GDI-Bitmap (DEVICE-Independent Bitmap, DIB) ab, die von diesem Objekt verwaltet wird.

## <a name="syntax"></a>Syntax


```C++
DIBDATA* GetDIBData();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf eine [**DIBDATA-Struktur**](dibdata.md) zurück.

## <a name="remarks"></a>Hinweise

Der Aufrufer muss die **DIBDATA-Struktur** initialisieren, bevor er diese Methode aufruft. überprüfen Sie den Wert von **CImageSample::m \_ bInit**. Um die -Struktur zu initialisieren, rufen Sie die [**CImageSample::SetDIBData-Methode**](cimagesample-setdibdata.md) auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CImageSample-Klasse**](cimagesample.md)
</dt> </dl>

 

 




