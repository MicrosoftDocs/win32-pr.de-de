---
description: Die Put \_ backgroundpalette-Methode legt ein Flag fest, um die Palette im Hintergrund zu erkennen.
ms.assetid: db420e75-e300-41fa-bae4-fb267cc99c7c
title: CBaseControlWindow.put_BackgroundPalette-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04aeb445be91426e7995ecd01c9326cda586a447
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371125"
---
# <a name="cbasecontrolwindowput_backgroundpalette-method"></a>Cbasecontrolwindow. Put \_ backgroundpalette-Methode

Die- `put_BackgroundPalette` Methode legt ein Flag fest, um die Palette im Hintergrund zu erkennen.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_BackgroundPalette(
   long BackgroundPalette
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Backgroundpalette* 
</dt> <dd>

Boolesches Automatisierungs Flag (0 ist off, 1 ist on).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Zum Abspielen eines Videos in einer anderen Anwendung oder einem anderen Dokument möchte die Anwendung möglicherweise eine eigene Palette verwenden. Das Video kann die aktuelle Vordergrund Palette anstelle seiner eigenen als Hintergrund Palette verwenden, indem dieses Flag auf 1 festgelegt wird. Wenn dieser Wert auf 0 festgelegt ist, wird im Fenster eine eigene bevorzugte Palette installiert und erkannt. Wenn Sie das Fenster zur Verwendung einer anderen Palette auffordern, werden schwerwiegende Leistungseinbußen verursacht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




