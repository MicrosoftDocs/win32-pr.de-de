---
description: Die SetRealize-Methode gibt an, ob das Fenster Paletten realisiert.
ms.assetid: ab4a6069-c11f-4126-93bf-6de5277970a1
title: CBaseWindow.SetRealize-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.SetRealize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 825a020b73bc74b38a32daa6f6870b76a009f5b8090e253370c77dfce7d7dc31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954565"
---
# <a name="cbasewindowsetrealize-method"></a>CBaseWindow.SetRealize-Methode

Die `SetRealize` -Methode gibt an, ob das Fenster Paletten realisiert.

## <a name="syntax"></a>Syntax


```C++
void SetRealize(
   BOOL bRealize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bRealize* 
</dt> <dd>

Boolescher Wert, der angibt, ob Paletten realisiert werden. True **gibt an,** dass die [**CBaseWindow::SetPalette-Methode**](cbasewindow-setpalette.md) Paletten realisiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Standardmäßig erkennt die **SetPalette-Methode** die angegebene Palette. Rufen Sie diese Methode auf, um das Standardverhalten zu ändern, sodass Paletten ausgewählt, aber nicht realisiert werden. Diese Methode legt die [**CBaseWindow::m \_ bNoRealize-Membervariable**](cbasewindow-m-bnorealize.md) fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseWindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




