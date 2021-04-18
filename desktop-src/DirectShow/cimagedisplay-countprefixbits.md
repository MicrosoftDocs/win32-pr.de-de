---
description: Die Methode "count prefixbits" berechnet die Anzahl der Bits (0) am Anfang eines angegebenen Bitfelds.
ms.assetid: 36fc5c5f-dc64-4588-9130-1b0740d03be1
title: Cimagedisplay. countrytprefixbits-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CountPrefixBits
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4333e1b0826b4fac7bfff463531b5d2e10704418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371423"
---
# <a name="cimagedisplaycountprefixbits-method"></a>Cimagedisplay. countrytprefixbits-Methode

Die- `CountPrefixBits` Methode berechnet die Anzahl der Bits (0) am Anfang eines angegebenen Bitfelds.

## <a name="syntax"></a>Syntax


```C++
DWORD CountPrefixBits(
   const DWORD Field
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Feld* 
</dt> <dd>

Gibt ein Bitfeld als **DWORD** -Wert an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl von Null Bits zurück, die vor dem ersten 1 Bit auftreten, oder 0x80000000, wenn alle Bits 0 (null) sind.

## <a name="remarks"></a>Bemerkungen

Diese Methode eignet sich für die Arbeit mit Farb Masken in [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) -Strukturen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cimagedisplay-Klasse**](cimagedisplay.md)
</dt> </dl>

 

 




