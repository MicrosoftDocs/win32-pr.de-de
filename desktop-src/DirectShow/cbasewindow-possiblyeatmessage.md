---
description: Die PossiblyEatMessage-Methode ermöglicht einer abgeleiteten Klasse, Nachrichten an ein anderes Fenster weiter zu senden.
ms.assetid: d8775182-44ed-4df2-b4b8-1fdf289e2c1a
title: CBaseWindow.PossiblyEatMessage-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PossiblyEatMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 851f46d14f949a49c9422256f9b2bda1ba314e5789773121387e89c011f7a424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016458"
---
# <a name="cbasewindowpossiblyeatmessage-method"></a>CBaseWindow.PossiblyEatMessage-Methode

Die `PossiblyEatMessage` -Methode ermöglicht es einer abgeleiteten Klasse, Nachrichten an ein anderes Fenster weiter zu senden.

## <a name="syntax"></a>Syntax


```C++
virtual BOOL PossiblyEatMessage(
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*uMsg* 
</dt> <dd>

Nachrichtenbezeichner.

</dd> <dt>

*wParam* 
</dt> <dd>

Erster Meldungsparameter.

</dd> <dt>

*lParam* 
</dt> <dd>

Zweiter Meldungsparameter.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn die Nachricht weitergeleitet wurde, andernfalls **FALSE.** Die Basisklasse gibt **FALSE zurück.**

## <a name="remarks"></a>Hinweise

Bevor die [**CBaseWindow::OnReceiveMessage-Methode**](cbasewindow-onreceivemessage.md) eine Nachricht verarbeitet, ruft sie `PossiblyEatMessage` auf. Wenn `PossiblyEatMessage` **TRUE zurückgibt,** **ignoriert OnReceiveMessage** die Nachricht. Eine abgeleitete Klasse kann `PossiblyEatMessage` überschreiben, sodass sie einige Nachrichten an ein Besitzerfenster weiter leitet. Beispielsweise leitet die [**CBaseControlWindow-Klasse,**](cbasecontrolwindow.md) die von **CBaseWindow** ableitung, Tastatur- und Mausnachrichten weiter.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseWindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




