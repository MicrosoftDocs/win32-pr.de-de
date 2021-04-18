---
description: Die getdisplayformat-Methode ruft ein Videoformat ab, das den aktuellen Anzeigemodus beschreibt.
ms.assetid: 98134704-0453-4090-94de-d92cdf324538
title: Cimagedisplay. getdisplayformat-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetDisplayFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 901d61f3597156853b0f2d6f93b43c3cf99ec5e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352060"
---
# <a name="cimagedisplaygetdisplayformat-method"></a>Cimagedisplay. getdisplayformat-Methode

Die- `GetDisplayFormat` Methode ruft ein Videoformat ab, das den aktuellen Anzeigemodus beschreibt.

## <a name="syntax"></a>Syntax


```C++
const VIDEOINFO* GetDisplayFormat();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf eine [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Struktur zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cimagedisplay-Klasse**](cimagedisplay.md)
</dt> </dl>

 

 




