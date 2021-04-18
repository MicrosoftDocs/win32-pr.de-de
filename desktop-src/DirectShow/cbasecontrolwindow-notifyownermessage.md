---
description: Die notifyownermessage-Methode übergibt bestimmte Nachrichten an das Videofenster.
ms.assetid: 8b27281a-5b8a-46c3-aa66-390d4496f30e
title: Cbasecontrolwindow. notilyownermessage-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.NotifyOwnerMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9073d37987404849ba8aa3acbda9919df840b410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361066"
---
# <a name="cbasecontrolwindownotifyownermessage-method"></a>Cbasecontrolwindow. notif yownermessage-Methode

Die- `NotifyOwnerMessage` Methode übergibt bestimmte Meldungen an das Videofenster.

## <a name="syntax"></a>Syntax


```C++
HRESULT NotifyOwnerMessage(
   long     hwnd,
   long     uMsg,
   LONG_PTR wParam,
   LONG_PTR lParam
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* 
</dt> <dd>

Handle für das Videofenster.

</dd> <dt>

*Umschlag* 
</dt> <dd>

Nachrichten Details.

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

Gibt keinen \_ Fehler zurück.

## <a name="remarks"></a>Bemerkungen

Wenn das Videofenster ein untergeordnetes Element eines anderen Fensters ist, empfängt es bestimmte Fenster Nachrichten der obersten Ebene nicht. Diese Nachrichten können für einen Renderer von Bedeutung sein, da Sie sich auf das Verhalten auswirken könnten. `NotifyOwnerMessage` übergibt eine der folgenden Meldungen an das Videofenster.

-   WM \_ activateapp
-   WM \_ devmodechange
-   WM- \_ Display Change
-   WM \_ palettechanged
-   WM- \_ paletteischanging
-   WM \_ querynewpalette
-   WM- \_ syscolorchange

Sie können anfordern, dass der [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) -Plug-in-Verteiler (PID) ein Fenster einem anderen Fenster untergeordnet wird. Wenn dies auftritt, sucht die PID nach bestimmten Nachrichten, die möglicherweise an das besitzende Fenster gesendet werden. Die PID führt diese Nachrichten dann an das eigene Fenster weiter. Die Standard Verarbeitung für die Nachrichten besteht darin, Sie synchron an die eigene Fenster Prozedur zu senden, indem Sie die Win32 **SendMessage** -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




