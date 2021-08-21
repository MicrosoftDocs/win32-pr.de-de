---
description: Die \_ BorderColor-Methode get ruft die aktuelle Rahmenfarbe ab.
ms.assetid: 4b4cae1d-bef7-4f8d-8011-c220fcfb73eb
title: CBaseControlWindow.get_BorderColor -Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BorderColor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a351e794765f3dddb5275d8a588ca54ade06bb789ed720bfb17997fc11e358f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660754"
---
# <a name="cbasecontrolwindowget_bordercolor-method"></a>CBaseControlWindow.get \_ BorderColor-Methode

Die `get_BorderColor` -Methode ruft die aktuelle Rahmenfarbe ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_BorderColor(
   long *Color
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Farbe* 
</dt> <dd>

Zeiger auf die aktuelle Rahmenfarbe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Eine Anwendung kann ein Zielrechteck festlegen, in dem das Video angezeigt werden soll. Dieses Rechteck ist relativ zum Clientbereich für das Fenster. Wenn dies erfolgt (standardmäßig wird immer das gesamte Fenster gestrichen), wird das Video durch einen Rahmen umgrenzt. Diese Eigenschaft wirkt sich auf die farbe aus, die vom Rahmen verwendet wird. Obwohl der -Parameter als **LONG-Typ angegeben** ist, handelt es sich tatsächlich um **einen COLORREF-Wert.**

Diese Memberfunktion soll von externen Objekten über die [**IVideoWindow-Schnittstelle**](/windows/desktop/api/Control/nn-control-ivideowindow) aufgerufen werden und sperrt daher den kritischen Abschnitt für die Synchronisierung mit dem zugeordneten Filter. Rufen Sie [**die CBaseControlWindow::GetBorderColour-Memberfunktion**](cbasecontrolwindow-getbordercolour.md) auf, um diese Eigenschaft abzurufen, wenn sie nicht von einem externen Objekt aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




