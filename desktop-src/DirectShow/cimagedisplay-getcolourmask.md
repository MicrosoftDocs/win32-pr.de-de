---
description: Die getColorMask-Methode ruft die Farb Masken für das aktuelle Anzeige Format ab.
ms.assetid: 386d0439-8502-411d-935c-3c2153a8b5b4
title: Cimagedisplay. getColorMask-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetColourMask
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 499b3677cd68444b58514d692d87cd4f631350b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365810"
---
# <a name="cimagedisplaygetcolourmask-method"></a>Cimagedisplay. getColorMask-Methode

Die- `GetColourMask` Methode ruft die Farb Masken für das aktuelle Anzeige Format ab.

## <a name="syntax"></a>Syntax


```C++
BOOL GetColourMask(
   DWORD *pMaskRed,
   DWORD *pMaskGreen,
   DWORD *pMaskBlue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmaskred* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die rote Komponenten Maske empfängt.

</dd> <dt>

*pmaskgreen* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die grüne Komponenten Maske empfängt.

</dd> <dt>

*pmaskblue* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die blaue Komponenten Maske empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cimagedisplay-Klasse**](cimagedisplay.md)
</dt> </dl>

 

 




