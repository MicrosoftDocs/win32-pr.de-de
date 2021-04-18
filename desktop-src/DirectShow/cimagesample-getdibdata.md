---
description: Die getdibdata-Methode ruft Informationen über das von diesem Objekt verwaltete GDI-geräteunabhängige Bitmap (DIB) ab.
ms.assetid: ec337336-69ec-47ff-a522-42c0388f9bc0
title: Cimagesample. getdibdata-Methode (winutil. h)
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
ms.openlocfilehash: 0fd198152e7c0042a6d48cf942a48745540960d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364810"
---
# <a name="cimagesamplegetdibdata-method"></a>Cimagesample. getdibdata-Methode

Die- `GetDIBData` Methode ruft Informationen über die von diesem-Objekt verwaltete GDI-geräteunabhängige Bitmap (DIB) ab.

## <a name="syntax"></a>Syntax


```C++
DIBDATA* GetDIBData();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf eine [**dibdata**](dibdata.md) -Struktur zurück.

## <a name="remarks"></a>Bemerkungen

Der Aufrufer muss die **dibdata** -Struktur initialisieren, bevor diese Methode aufgerufen wird. Überprüfen Sie den Wert von **cimagesample:: m \_ binit**. Um die Struktur zu initialisieren, müssen Sie die [**cimagesample:: setdibdata**](cimagesample-setdibdata.md) -Methode aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cimagesample-Klasse**](cimagesample.md)
</dt> </dl>

 

 




