---
description: Die OnSize-Methode verarbeitet WM \_ SIZE-Nachrichten.
ms.assetid: 21d867a4-4321-478a-9beb-5d3053569369
title: CBaseWindow.OnSize-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bf6c7793af3cb7866ddaaaae8823acd91ed10ac71d939af8bc9e71eff768d75f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657655"
---
# <a name="cbasewindowonsize-method"></a>CBaseWindow.OnSize-Methode

Die `OnSize` -Methode verarbeitet WM \_ SIZE-Meldungen.

## <a name="syntax"></a>Syntax


```C++
virtual BOOL OnSize(
   LONG Width,
   LONG Height
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Width* 
</dt> <dd>

Breite des Clientbereichs in Pixel.

</dd> <dt>

*Height* 
</dt> <dd>

Höhe des Clientbereichs in Pixel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück.**

## <a name="remarks"></a>Hinweise

Diese Methode speichert die neue Breite und Höhe. Rufen Sie zum Abrufen dieser Werte die [**Methoden CBaseWindow::GetWindowHeight**](cbasewindow-getwindowheight.md) und [**CBaseWindow::GetWindowWidth**](cbasewindow-getwindowwidth.md) auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseWindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




