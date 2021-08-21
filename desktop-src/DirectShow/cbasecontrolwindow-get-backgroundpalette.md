---
description: Die get \_ BackgroundPalette-Methode ruft die realisierte Palette im Hintergrundflag ab.
ms.assetid: cc649dbd-d049-4993-b187-4e297bef5152
title: CBaseControlWindow.get_BackgroundPalette -Methode (Ctlutil.h)
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
ms.openlocfilehash: 63ea3fa8ecbc6e644ccc5f4b1fac7a2fcd9c18270474f45dc08faa164f76cbec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660775"
---
# <a name="cbasecontrolwindowget_backgroundpalette-method"></a>CBaseControlWindow.get \_ BackgroundPalette-Methode

Die `get_BackgroundPalette` -Methode ruft die realisierte Palette im Hintergrundflag ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_BackgroundPalette(
   long *pBackgroundPalette
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pBackgroundPalette* 
</dt> <dd>

Zeiger auf ein boolesches Automation-Flag (0 ist deaktiviert, 1 ist ein).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion implementiert die [**IVideoWindow::get \_ BackgroundPalette-Methode.**](/windows/desktop/api/Control/nf-control-ivideowindow-get_backgroundpalette) Wenn ein Video in einer anderen Anwendung oder einem anderen Dokument abgespielt wird, möchte die Anwendung möglicherweise eine eigene Palette verwenden. Sie kann das Video auffordern, die aktuelle Vordergrundpalette anstelle einer eigenen zu verwenden, indem dieses Flag auf 1 festlegen. Wenn dies auf 0 festgelegt ist, installiert und realisiert das Fenster seine eigene bevorzugte Palette. Beachten Sie, dass das Bitten des Fensters, eine andere Palette zu verwenden, zu schwerwiegenden Leistungsbehinderung führen kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




