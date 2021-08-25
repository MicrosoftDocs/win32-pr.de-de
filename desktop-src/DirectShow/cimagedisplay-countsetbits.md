---
description: Die CountSetBits-Methode gibt die Anzahl der Bits zurück, die in einem angegebenen Bitfeld auf 1 festgelegt sind.
ms.assetid: fc5701b8-88ff-4c23-9d26-854bb65cc55c
title: CImageDisplay.CountSetBits-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CountSetBits
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d334111c18c2c94c79a8b49ed7c0601efabb2bd13922a68c292970d4d2c379bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824070"
---
# <a name="cimagedisplaycountsetbits-method"></a>CImageDisplay.CountSetBits-Methode

Die -Methode gibt die Anzahl der Bits zurück, `CountSetBits` die in einem angegebenen Bitfeld auf 1 festgelegt sind.

## <a name="syntax"></a>Syntax


```C++
DWORD CountSetBits(
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

Gibt die Anzahl der Bits zurück, die auf 1 festgelegt sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CImageDisplay-Klasse**](cimagedisplay.md)
</dt> </dl>

 

 




