---
description: Die GetDisplayFormat-Methode ruft ein Videoformat ab, das den aktuellen Anzeigemodus beschreibt.
ms.assetid: 98134704-0453-4090-94de-d92cdf324538
title: CImageDisplay.GetDisplayFormat-Methode (Winutil.h)
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
ms.openlocfilehash: f8841e95f4097d043e7ef01abdb067c248f43b9295a8c8466ba50f07d23bd7dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074144"
---
# <a name="cimagedisplaygetdisplayformat-method"></a>CImageDisplay.GetDisplayFormat-Methode

Die `GetDisplayFormat` -Methode ruft ein Videoformat ab, das den aktuellen Anzeigemodus beschreibt.

## <a name="syntax"></a>Syntax


```C++
const VIDEOINFO* GetDisplayFormat();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf eine [**VIDEOINFO-Struktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CImageDisplay-Klasse**](cimagedisplay.md)
</dt> </dl>

 

 




