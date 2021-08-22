---
description: Die UpdateFormat-Methode füllt einige optionale Member der VIDEOINFO-Struktur aus.
ms.assetid: 5ca34fa0-eef4-44f5-bbcc-e686e5181d86
title: CImageDisplay.UpdateFormat-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.UpdateFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1e46065aae630132a1d7fd38a6d331009a537af18c12687fcbecd22dd7bf78b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119257200"
---
# <a name="cimagedisplayupdateformat-method"></a>CImageDisplay.UpdateFormat-Methode

Die `UpdateFormat` -Methode füllt einige optionale Member der [**VIDEOINFO-Struktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) aus.

## <a name="syntax"></a>Syntax


```C++
HRESULT UpdateFormat(
   VIDEOINFO *pVideoInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVideoInfo* 
</dt> <dd>

Zeiger auf eine **VIDEOINFO-Struktur.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Diese Methode legt die **Member biClrUsed,** **biClrImportant** und **biSizeImage** auf die richtigen Werte fest und gibt die Quell- und Zielrechtecke frei.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CImageDisplay-Klasse**](cimagedisplay.md)
</dt> </dl>

 

 




