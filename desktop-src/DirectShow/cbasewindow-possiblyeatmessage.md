---
description: Mit der possiblyeatmessage-Methode kann eine abgeleitete Klasse Nachrichten an ein anderes Fenster weiterleiten.
ms.assetid: d8775182-44ed-4df2-b4b8-1fdf289e2c1a
title: Cbasewindow. possiblyeatmessage-Methode (winutil. h)
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
ms.openlocfilehash: f218b62ac5464da27b8596992c34ce7ae5efde46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365968"
---
# <a name="cbasewindowpossiblyeatmessage-method"></a>Cbasewindow. possiblyeatmessage-Methode

Mit der- `PossiblyEatMessage` Methode kann eine abgeleitete Klasse Nachrichten an ein anderes Fenster weiterleiten.

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

*Umschlag* 
</dt> <dd>

Nachrichten-ID.

</dd> <dt>

*wParam* 
</dt> <dd>

Der erste Message-Parameter.

</dd> <dt>

*lParam* 
</dt> <dd>

Der zweite Meldungs Parameter.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn die Nachricht weitergeleitet wurde, andernfalls **false** . Die Basisklasse gibt **false** zurück.

## <a name="remarks"></a>Bemerkungen

Bevor die [**cbasewindow:: onreceivemess**](cbasewindow-onreceivemessage.md) -Methode eine Nachricht verarbeitet, ruft Sie auf `PossiblyEatMessage` . Wenn `PossiblyEatMessage` **true** zurückgibt, wird die Nachricht von **onreceivemess** ignoriert. Eine abgeleitete Klasse kann `PossiblyEatMessage` überschreiben, sodass einige Nachrichten an ein Besitzer Fenster weitergeleitet werden. Beispielsweise leitet die [**cbasecontrolwindow**](cbasecontrolwindow.md) -Klasse, die von **cbasewindow** abgeleitet wird, Tastatur-und Maus Nachrichten weiter.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasewindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




