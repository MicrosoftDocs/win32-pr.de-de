---
title: WM_DRAWITEM (Winuser.h)
description: Wird an das übergeordnete Fenster einer vom Besitzer gezeichneten Schaltfläche, eines Kombinationsfelds, eines Listenfelds oder eines Menüs gesendet, wenn sich ein visueller Aspekt der Schaltfläche, des Kombinationsfelds, des Listenfelds oder des Menüs geändert hat.
ms.assetid: e54bae5e-10d6-43b0-a766-1b270c8873a9
keywords:
- WM_DRAWITEM meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- WM_DRAWITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f5d4b2addfa2de5f8c76ded636ca29a96fb3af7e0ab4157d25ac26a78c462c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957519"
---
# <a name="wm_drawitem-message"></a>WM \_ DRAWITEM-Nachricht

Wird an das übergeordnete Fenster einer vom Besitzer gezeichneten Schaltfläche, eines Kombinationsfelds, eines Listenfelds oder eines Menüs gesendet, wenn sich ein visueller Aspekt der Schaltfläche, des Kombinationsfelds, des Listenfelds oder des Menüs geändert hat.

Ein Fenster empfängt diese Nachricht über seine [*WindowProc-Funktion.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
WM_DRAWITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den Bezeichner des Steuerelements an, das die **WM \_ DRAWITEM-Nachricht gesendet** hat. Wenn die Nachricht von einem Menü gesendet wurde, ist dieser Parameter 0 (null).

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**DRAWITEMSTRUCT-Struktur,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) die Informationen über das zu zeichnende Element und den erforderlichen Zeichnungstyp enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie **TRUE zurückgeben.**

## <a name="remarks"></a>Hinweise

Standardmäßig zeichnet die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) das Fokusrechteck für ein vom Besitzer gezeichnetes Listenfeldelement.

Der *itemAction-Member* der [**DRAWITEMSTRUCT-Struktur**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) gibt den Zeichnungsvorgang an, den eine Anwendung ausführen soll.

Bevor eine Anwendung von der Verarbeitung dieser Nachricht zurückkehrt, sollte sie sicherstellen, dass sich der vom *hDC-Member* der [**DRAWITEMSTRUCT-Struktur**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) identifizierte Gerätekontext im Standardzustand befindet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

