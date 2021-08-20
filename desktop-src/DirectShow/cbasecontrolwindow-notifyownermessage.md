---
description: Die NotifyOwnerMessage-Methode übergibt bestimmte Nachrichten an das Videofenster.
ms.assetid: 8b27281a-5b8a-46c3-aa66-390d4496f30e
title: CBaseControlWindow.NotifyOwnerMessage-Methode (Ctlutil.h)
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
ms.openlocfilehash: 35d71057027bd8fbd572dffd714f761ff101ba0de95dd42dcf058009b0cb1b04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526850"
---
# <a name="cbasecontrolwindownotifyownermessage-method"></a>CBaseControlWindow.NotifyOwnerMessage-Methode

Die `NotifyOwnerMessage` -Methode übergibt bestimmte Nachrichten an das Videofenster.

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

*Hwnd* 
</dt> <dd>

Handle für das Videofenster.

</dd> <dt>

*uMsg* 
</dt> <dd>

Meldungsdetails.

</dd> <dt>

*wParam* 
</dt> <dd>

Erster Nachrichtenparameter.

</dd> <dt>

*lParam* 
</dt> <dd>

Zweiter Nachrichtenparameter.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt NO \_ ERROR zurück.

## <a name="remarks"></a>Hinweise

Wenn das Videofenster ein untergeordnetes Element eines anderen Fensters ist, empfängt es keine bestimmten Fenstermeldungen der obersten Ebene. Diese Nachrichten können für einen Renderer nützlich sein, da sie sich auf sein Verhalten auswirken können. `NotifyOwnerMessage` übergibt eine der folgenden Meldungen an das Videofenster.

-   WM \_ ACTIVATEAPP
-   WM \_ DEVMODECHANGE
-   WM \_ DISPLAYCHANGE
-   WM \_ PALETTECHANGED
-   WM \_ PALETTEISCHANGING
-   WM \_ QUERYNEWPALETTE
-   WM \_ SYSCOLORCHANGE

Sie können anfordern, dass der [**IVideoWindow-Plug-In-Verteiler**](/windows/desktop/api/Control/nn-control-ivideowindow) (PID) ein Fenster zu einem untergeordneten Element eines anderen Fensters macht. In diesem Fall sucht die PID nach bestimmten Nachrichten, die möglicherweise an das besitzende Fenster gesendet werden. Die PID leitet diese Nachrichten dann an das eigene Fenster weiter. Die Standardverarbeitung für die Nachrichten besteht darin, sie synchron an die Prozedur des eigenen Fensters zu senden, indem die Win32 **SendMessage-Funktion** aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




