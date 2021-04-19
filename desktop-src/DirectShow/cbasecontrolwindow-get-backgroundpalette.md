---
description: Die get \_ backgroundpalette-Methode ruft die realisierte Palette im hintergrundflag ab.
ms.assetid: cc649dbd-d049-4993-b187-4e297bef5152
title: CBaseControlWindow.get_BackgroundPalette-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd06bcec9b3c435370ec3f12340c1c3aede3904c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369971"
---
# <a name="cbasecontrolwindowget_backgroundpalette-method"></a>Cbasecontrolwindow. get \_ backgroundpalette-Methode

Die- `get_BackgroundPalette` Methode ruft die realisierte Palette im hintergrundflag ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_BackgroundPalette(
   long *pBackgroundPalette
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbackgroundpalette* 
</dt> <dd>

Zeiger auf ein boolesches Automatisierungs Flag (0 ist off, 1 ist on).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion implementiert die Methode [**IVideoWindow:: get \_ backgroundpalette**](/windows/desktop/api/Control/nf-control-ivideowindow-get_backgroundpalette) . Wenn ein Video in einer anderen Anwendung oder einem anderen Dokument abgespielt wird, möchte die Anwendung möglicherweise eine eigene Palette verwenden. Es kann gefragt werden, ob das Video die aktuelle Vordergrund Palette anstelle eines eigenen verwendet, indem dieses Flag auf 1 festgelegt wird. Wenn dieser Wert auf 0 festgelegt ist, wird im Fenster eine eigene bevorzugte Palette installiert und erkannt. Beachten Sie, dass die Frage, ob das Fenster eine andere Palette verwendet, zu schwerwiegenden Leistungseinbußen führt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




