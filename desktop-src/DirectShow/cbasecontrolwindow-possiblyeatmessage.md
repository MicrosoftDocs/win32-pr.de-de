---
description: Die Methode PossiblyEatMessage gibt Tastatur- und Mausnachrichten an das Fenster zum Leeren von Nachrichten weiter.
ms.assetid: 8e344c5d-2f94-454f-89b7-45c539b6e833
title: CBaseControlWindow.PossiblyEatMessage-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.PossiblyEatMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 403fb4d170f9c3cf0b7d68d3ac6ce1fdcc9c81a14b1c76d74e67bb64d4d9cc8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017338"
---
# <a name="cbasecontrolwindowpossiblyeatmessage-method"></a>CBaseControlWindow.PossiblyEatMessage-Methode

Die `PossiblyEatMessage` -Methode gibt Tastatur- und Mausnachrichten an das Fenster zum Leeren von Nachrichten weiter.

## <a name="syntax"></a>Syntax


```C++
BOOL PossiblyEatMessage(
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*uMsg* 
</dt> <dd>

Fenstermeldung.

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

Gibt **TRUE zurück,** wenn die Nachricht an das Fenster weitergeleitet wurde, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Das Fenster zum Leeren von Nachrichten ist ein Fenster, das für den Empfang bestimmter Maus- und Tastaturmeldungen vorgesehen ist. Anfangs ist das Fenster **NULL.** Sie kann durch Aufrufen von [**CBaseControlWindow::p ut \_ MessageDrain festgelegt werden.**](cbasecontrolwindow-put-messagedrain.md)

Wenn das Fenster zum Leeren von Nachrichten nicht **NULL ist,** `PossiblyEatMessage` werden die folgenden Meldungen an dieses Fenster gesendet:

-   WM \_ CHAR
-   WM \_ DEADCHAR
-   WM \_ KEYDOWN
-   WM \_ KEYUP
-   WM \_ LBUTTONDBLCLK
-   WM \_ LBUTTONDOWN
-   WM \_ LBUTTONUP
-   WM \_ MBUTTONDBLCLK
-   WM \_ MBUTTONDOWN
-   WM \_ MBUTTONUP
-   WM \_ MOUSEACTIVATE
-   WM \_ MOUSEMOVE
-   WM \_ NCLBUTTONDBLCLK
-   WM \_ NCLBUTTONDOWN
-   WM \_ NCLBUTTONUP
-   WM \_ NCMBUTTONDBLCLK
-   WM \_ NCMBUTTONDOWN
-   WM \_ NCMBUTTONUP
-   WM \_ NCMOUSEMOVE
-   WM \_ NCRBUTTONDBLCLK
-   WM \_ NCRBUTTONDOWN
-   WM \_ NCRBUTTONUP
-   WM \_ RBUTTONDBLCLK
-   WM \_ RBUTTONDOWN
-   WM \_ RBUTTONUP
-   WM \_ SYSCHAR
-   WM \_ SYSDEADCHAR
-   WM \_ SYSKEYDOWN
-   WM \_ SYSKEYUP

Andere Nachrichten werden ignoriert. Wenn das Fenster zum Leeren von Nachrichten **NULL ist,** ignoriert die -Methode alle Fenstermeldungen. Die Methode gibt **TRUE zurück,** wenn sie die Nachricht veröffentlicht, andernfalls **FALSE.** Die **CBaseWindow-Klasse** ruft diese Methode auf, wenn sie eine Fensternachricht empfängt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




