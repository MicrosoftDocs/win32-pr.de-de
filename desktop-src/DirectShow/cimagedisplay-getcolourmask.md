---
description: Die GetColourMask-Methode ruft die Farbmasken für das aktuelle Anzeigeformat ab.
ms.assetid: 386d0439-8502-411d-935c-3c2153a8b5b4
title: CImageDisplay.GetColourMask-Methode (Winutil.h)
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
ms.openlocfilehash: 018bdaf96e5b6508e13893290449d77041c453b3b28bb4c4d794cc5cc85fb945
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655941"
---
# <a name="cimagedisplaygetcolourmask-method"></a>CImageDisplay.GetColourMask-Methode

Die `GetColourMask` -Methode ruft die Farbmasken für das aktuelle Anzeigeformat ab.

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

*pMaskRed* 
</dt> <dd>

Zeiger auf eine Variable, die die rote Komponentenmaske empfängt.

</dd> <dt>

*pMaskGreen* 
</dt> <dd>

Zeiger auf eine Variable, die die grüne Komponentenmaske empfängt.

</dd> <dt>

*pMaskBlue* 
</dt> <dd>

Zeiger auf eine Variable, die die blaue Komponentenmaske empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, andernfalls **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CImageDisplay-Klasse**](cimagedisplay.md)
</dt> </dl>

 

 




