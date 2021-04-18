---
description: Die Methode "possiblyeatmessage" leitet Tastatur-und Maus Meldungen an das Fenster "Nachrichten Ausgleich" weiter.
ms.assetid: 8e344c5d-2f94-454f-89b7-45c539b6e833
title: Cbasecontrolwindow. possiblyeatmessage-Methode (ctlutil. h)
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
ms.openlocfilehash: 9bfadcfbbd6833d8f3e9b65bd39d0cdbef4a006e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351291"
---
# <a name="cbasecontrolwindowpossiblyeatmessage-method"></a>Cbasecontrolwindow. possiblyeatmessage-Methode

Die `PossiblyEatMessage` -Methode leitet Tastatur-und Maus Meldungen an das Fenster für die Nachrichten Ableitung weiter.

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

*Umschlag* 
</dt> <dd>

Fenster Meldung.

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

Gibt **true** zurück, wenn die Nachricht an das Fenster weitergeleitet wurde, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Das Fenster für die Nachrichten Ableitung ist ein Fenster, das für den Empfang bestimmter Maus-und Tastatur Meldungen vorgesehen ist. Anfänglich ist das Fenster **null**. Sie kann durch Aufrufen von [**cbasecontrolwindow::p UT \_ messagedrain**](cbasecontrolwindow-put-messagedrain.md)festgelegt werden.

Wenn das Fenster für die Nachrichten Ableitung nicht **null** ist, werden `PossiblyEatMessage` die folgenden Meldungen an dieses Fenster gesendet:

-   WM \_ -Zeichen
-   WM \_ deadchar
-   WM- \_ KeyDown
-   WM- \_ KeyUp
-   WM \_ lbuttondblclk
-   WM \_ lbuttondown
-   WM- \_ lbuttonup
-   WM- \_ mbuttondblclk
-   WM- \_ mbuttondown
-   WM- \_ mbuttonup
-   WM- \_ moueinaktivierung
-   WM- \_ mouseelmove
-   WM \_ nclbuttondblclk
-   WM- \_ nclbuttondown
-   WM- \_ nclbuttonup
-   WM \_ ncmbuttondblclk
-   WM \_ ncmbuttondown
-   WM \_ ncmbuttonup
-   WM- \_ ncmouummove
-   WM \_ ncrbuttondblclk
-   WM- \_ ncrbuttondown
-   WM- \_ ncrbuttonup
-   WM- \_ rbuttondblclk
-   WM- \_ rbuttondown
-   WM- \_ rbuttonup
-   WM- \_ syschar
-   WM \_ sysdeadchar
-   WM \_ syskeydown
-   WM- \_ syskeyup

Andere Meldungen werden ignoriert. Wenn das Fenster für die Nachrichten Ableitung **null** ist, ignoriert die Methode alle Fenster Meldungen. Die Methode gibt " **true** " zurück, wenn Sie die Nachricht sendet, andernfalls " **false** ". Die **cbasewindow** -Klasse ruft diese Methode auf, wenn Sie eine Fenster Meldung empfängt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




