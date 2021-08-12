---
description: Die OnReceiveMessage-Methode verarbeitet Fenstermeldungen.
ms.assetid: 0f074f9b-00e5-42ff-a491-020d441acad1
title: CBaseWindow.OnReceiveMessage-Methode (Winutil.h)
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
ms.openlocfilehash: 1a5dbfb84edef1f5257cfda8cae08d27b219909f47a7d88fd29580ae12e48b3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657963"
---
# <a name="cbasewindowonreceivemessage-method"></a>CBaseWindow.OnReceiveMessage-Methode

Die `OnReceiveMessage` -Methode verarbeitet Fenstermeldungen.

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

*Hwnd* 
</dt> <dd>

Handle zum Fenster.

</dd> <dt>

*uMsg* 
</dt> <dd>

Nachrichtenbezeichner.

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

Gibt 0 zurück, wenn die Nachricht verarbeitet wurde, oder 1, wenn die Nachricht nicht verarbeitet wurde.

## <a name="remarks"></a>Hinweise

Die Basisklasse verarbeitet die folgenden Nachrichten:

-   WM \_ CLOSE
-   WM \_ MOVE
-   WM \_ PALETTECHANGED
-   WM \_ QUERYNEWPALETTE
-   \_WM-GRÖßE
-   WM \_ SYSCOLORCHANGE

Eine abgeleitete Klasse kann diese Methode überschreiben, um andere Nachrichten zu verarbeiten. Die abgeleitete Klasse sollte die Basisklassenmethode aufrufen, um alle Nachrichten zu behandeln, die von der abgeleiteten Klasse ignoriert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseWindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




