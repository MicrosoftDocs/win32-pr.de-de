---
description: Die Methode "Methode" gibt an, ob im Fenster Paletten realisiert werden.
ms.assetid: ab4a6069-c11f-4126-93bf-6de5277970a1
title: Cbasewindow. ontrealize-Methode (winutil. h)
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
ms.openlocfilehash: 587e54cdbbbf57ddb4cf52e2d5dfb916acaee22d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361057"
---
# <a name="cbasewindowsetrealize-method"></a>Cbasewindow. abtrealize-Methode

Die- `SetRealize` Methode gibt an, ob im Fenster Paletten realisiert werden.

## <a name="syntax"></a>Syntax


```C++
void SetRealize(
   BOOL bRealize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*zu brealisieren* 
</dt> <dd>

Boolescher Wert, der angibt, ob Paletten erkannt werden sollen. **True** gibt an, dass die [**cbasewindow:: SetPalette**](cbasewindow-setpalette.md) -Methode Paletten erkennt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Standardmäßig erkennt die **SetPalette** -Methode die angegebene Palette. Diese Methode wird aufgerufen, um das Standardverhalten zu ändern, sodass die Paletten ausgewählt, aber nicht realisiert werden. Diese Methode legt die Element Variable [**cbasewindow:: m \_ bnorealize**](cbasewindow-m-bnorealize.md) fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasewindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




