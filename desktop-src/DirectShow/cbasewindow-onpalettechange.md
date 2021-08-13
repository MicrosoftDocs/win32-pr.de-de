---
description: Die OnPaletteChange-Methode verarbeitet Palettenänderungsmeldungen.
ms.assetid: 2abae4f1-fbd0-4a32-8772-012fa96b6d6c
title: CBaseWindow.OnPaletteChange-Methode (Winutil.h)
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
ms.openlocfilehash: c881c519706ca0288847a7dc603cf513a99cdd76e4c83f0e53bec16df840e509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657953"
---
# <a name="cbasewindowonpalettechange-method"></a>CBaseWindow.OnPaletteChange-Methode

Die `OnPaletteChange` -Methode verarbeitet Palettenänderungsmeldungen.

## <a name="syntax"></a>Syntax


```C++
virtual LRESULT OnPaletteChange(
   HWND hwnd,
   UINT Message
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Hwnd* 
</dt> <dd>

Handle zum Fenster.

</dd> <dt>

*Meldung* 
</dt> <dd>

Nachrichtenbezeichner.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 zurück, wenn die Nachricht verarbeitet wurde, oder 1, wenn die Nachricht nicht verarbeitet wurde.

## <a name="remarks"></a>Hinweise

Diese Methode verarbeitet WM \_ PALETTECHANGED- und WM \_ QUERYNEWPALETTE-Meldungen. Sie ruft die [**CBaseWindow::D oRealisePalette-Methode**](cbasewindow-dorealisepalette.md) auf, um die neue Palette zu realisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseWindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




