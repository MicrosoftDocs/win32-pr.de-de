---
description: Die CountPrefixBits-Methode berechnet die Anzahl der Nullbits am Anfang eines angegebenen Bitfelds.
ms.assetid: 36fc5c5f-dc64-4588-9130-1b0740d03be1
title: CImageDisplay.CountPrefixBits-Methode (Winutil.h)
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
ms.openlocfilehash: 510ac01baab55fbf45e3441296018426335a8f50061f06400872fd7275d3e273
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108480"
---
# <a name="cimagedisplaycountprefixbits-method"></a>CImageDisplay.CountPrefixBits-Methode

Die `CountPrefixBits` -Methode berechnet die Anzahl der Nullbits am Anfang eines angegebenen Bitfelds.

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

Gibt ein Bitfeld als **DWORD-Wert** an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Nullbits zurück, die vor dem ersten 1 Bit auftreten, oder 0x80000000, wenn alle Bits 0 (null) sind.

## <a name="remarks"></a>Hinweise

Diese Methode ist nützlich für die Arbeit mit Farbmasken in [**VIDEOINFO-Strukturen.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CImageDisplay-Klasse**](cimagedisplay.md)
</dt> </dl>

 

 




