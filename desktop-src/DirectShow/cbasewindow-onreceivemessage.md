---
description: Die onreceivemess Age-Methode verarbeitet Fenster Meldungen.
ms.assetid: 0f074f9b-00e5-42ff-a491-020d441acad1
title: Cbasewindow. onreceivemess Age-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnReceiveMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: defef9a7ca24d6875eda508989615f308a2385b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366927"
---
# <a name="cbasewindowonreceivemessage-method"></a>Cbasewindow. onreceivemess Age-Methode

Die- `OnReceiveMessage` Methode verarbeitet Fenster Meldungen.

## <a name="syntax"></a>Syntax


```C++
virtual LRESULT OnReceiveMessage(
   HWND   hwnd,
   INT    uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* 
</dt> <dd>

Handle für das Fenster.

</dd> <dt>

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

Gibt 0 zurück, wenn die Meldung verarbeitet wurde, oder 1, wenn die Meldung nicht verarbeitet wurde.

## <a name="remarks"></a>Bemerkungen

Die-Basisklasse verarbeitet die folgenden Meldungen:

-   WM \_ Schließen
-   WM \_ verschieben
-   WM \_ palettechanged
-   WM \_ querynewpalette
-   WM- \_ Größe
-   WM- \_ syscolorchange

Eine abgeleitete Klasse kann diese Methode überschreiben, um andere Nachrichten zu verarbeiten. Die abgeleitete Klasse sollte die Basisklassen Methode zum Verarbeiten von Nachrichten, die von der abgeleiteten Klasse ignoriert werden, aufruft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasewindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




