---
title: WM_CTLCOLORLISTBOX Meldung (Winuser.h)
description: Wird an das übergeordnete Fenster eines Listenfelds gesendet, bevor das System das Listenfeld zeichnet. Durch Reagieren auf diese Meldung kann das übergeordnete Fenster den Text und die Hintergrundfarben des Listenfelds mithilfe des angegebenen Anzeigegerätekontexthandle festlegen.
ms.assetid: e128e77f-e966-44c4-9f0e-efcf421b6c82
keywords:
- WM_CTLCOLORLISTBOX Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- WM_CTLCOLORLISTBOX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1713c7251dfe837d5796b708fa5b77f0aa5e372c031c251199cb871dbd7c5608
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077664"
---
# <a name="wm_ctlcolorlistbox-message"></a>WM \_ CTLCOLORLISTBOX-Meldung

Wird an das übergeordnete Fenster eines Listenfelds gesendet, bevor das System das Listenfeld zeichnet. Durch Reagieren auf diese Meldung kann das übergeordnete Fenster den Text und die Hintergrundfarben des Listenfelds mithilfe des angegebenen Anzeigegerätekontexthandle festlegen.


```C++
WM_CTLCOLORLISTBOX

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Behandeln Sie den Gerätekontext für das Listenfeld.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das Listenfeld.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, muss sie ein Handle an einen Pinsel zurückgeben. Das System verwendet den Pinsel, um den Hintergrund des Listenfelds zu zeichnen.

## <a name="remarks"></a>Hinweise

Standardmäßig wählt die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) die Standardsystemfarben für das Listenfeld aus.

Die **WM \_ CTLCOLORLISTBOX-Nachricht** wird nie zwischen Threads gesendet. Er wird nur innerhalb eines Threads gesendet.

Wenn eine Dialogfeldprozedur diese Nachricht verarbeitet, sollte sie den gewünschten Rückgabewert in einen **INT \_ PTR-Wert** konvertieren und den Wert direkt zurückgeben. Wenn die Dialogfeldprozedur **FALSE** zurückgibt, wird die Standardmäßige Nachrichtenverarbeitung ausgeführt. Der von der [**SetWindowLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) festgelegte **\_ DWL-MSGRESULT-Wert** wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Andere Ressourcen**
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**Wählen SiePalette aus.**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

