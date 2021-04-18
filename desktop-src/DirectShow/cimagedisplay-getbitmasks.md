---
description: Die getBitMasks-Methode ruft die Farb Masken für ein angegebenes videoinfo-Format ab.
ms.assetid: 72a9ba44-96de-4fff-a3fb-675d3dd080d8
title: Cimagedisplay. getBitMasks-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetBitMasks
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2defe5e80a0d7311adcd19dca67119019623993
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371776"
---
# <a name="cimagedisplaygetbitmasks-method"></a>Cimagedisplay. getBitMasks-Methode

Die- `GetBitMasks` Methode ruft die Farb Masken für ein angegebenes [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Format ab.

## <a name="syntax"></a>Syntax


```C++
const DWORD* GetBitMasks(
   const VIDEOINFO *pVideoInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pvideoinfo* 
</dt> <dd>

Ein Zeiger auf die **videoinfo** -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein Array von drei **DWORD** -Werten zurück.

## <a name="remarks"></a>Bemerkungen

Wenn der **bicompression** -Member BI- \_ Bitfields ist, gibt die Methode einen Zeiger auf die Farb Masken zurück, die im **dwbitmasks** -Member bereitgestellt werden. Wenn der **bicompression** -Member BI \_ RGB ist, gibt die Methode die Farb Masken zurück, die der Bittiefe entsprechen. Wenn die Methode fehlschlägt (z. b. die Bittiefe ist kleiner als 16), gibt die Methode das Array zurück {0,0,0} .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cimagedisplay-Klasse**](cimagedisplay.md)
</dt> </dl>

 

 




