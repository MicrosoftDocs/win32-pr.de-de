---
description: Die onpalettechange-Methode verarbeitet palettenänderungs Meldungen.
ms.assetid: 2abae4f1-fbd0-4a32-8772-012fa96b6d6c
title: Cbasewindow. onpalettechange-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnPaletteChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9abcb2d9f5cdc875f70f5c1db1fd2f625ce911f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369441"
---
# <a name="cbasewindowonpalettechange-method"></a>Cbasewindow. onpalettechange-Methode

Die `OnPaletteChange` -Methode verarbeitet palettenänderungs Meldungen.

## <a name="syntax"></a>Syntax


```C++
virtual LRESULT OnPaletteChange(
   HWND hwnd,
   UINT Message
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* 
</dt> <dd>

Handle für das Fenster.

</dd> <dt>

*Meldung* 
</dt> <dd>

Nachrichten-ID.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 zurück, wenn die Meldung verarbeitet wurde, oder 1, wenn die Meldung nicht verarbeitet wurde.

## <a name="remarks"></a>Bemerkungen

Diese Methode verarbeitet die \_ Nachrichten "WM palettechanged" und "WM \_ querynewpalette". Die [**cbasewindow::D orealisetpalette**](cbasewindow-dorealisepalette.md) -Methode wird aufgerufen, um die neue Palette zu erkennen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasewindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




