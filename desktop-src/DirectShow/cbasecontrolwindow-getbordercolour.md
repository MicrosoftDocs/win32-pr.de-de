---
description: Die GetBorderColour-Methode ruft die aktuelle Fensterrahmenfarbe m \_ BorderColour ab.
ms.assetid: 5cd9b834-5438-475e-9671-ee9917f9a485
title: CBaseControlWindow.GetBorderColour-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetBorderColour
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9b5b94e0fa58c95e74fd140c04710e8aaacef9402397fa475983c0e01e586528
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017368"
---
# <a name="cbasecontrolwindowgetbordercolour-method"></a>CBaseControlWindow.GetBorderColour-Methode

Die `GetBorderColour` -Methode ruft die aktuelle Fensterrahmenfarbe **m \_ BorderColour ab.**

## <a name="syntax"></a>Syntax


```C++
COLORREF GetBorderColour();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt die Farbe des Rahmens zurück.

## <a name="remarks"></a>Hinweise

Eine Anwendung kann ein Zielrechteck festlegen, um das Video anzuzeigen. Dieses Rechteck sollte relativ zum Clientbereich für das Fenster sein. Wenn dies erfolgt (standardmäßig wird immer das gesamte Fenster ge zeichnet), gibt es einen Bereich, der das Video umgibt. das heißt, der Rahmen. Die Rahmenfarbe kann über die [**Memberfunktion CBaseControlWindow::p ut \_ BorderColor**](cbasecontrolwindow-put-bordercolor.md) festgelegt werden. Diese Eigenschaft wirkt sich auf die Farbe des Rahmens aus. Verwenden Sie diese Memberfunktion anstelle [**von CBaseControlWindow::get \_ BorderColor,**](cbasecontrolwindow-get-bordercolor.md)es sei denn, Sie rufen diese extern über die [**IVideoWindow::get \_ BorderColor-Methode**](/windows/desktop/api/Control/nf-control-ivideowindow-get_bordercolor) auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




