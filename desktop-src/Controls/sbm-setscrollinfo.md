---
title: SBM_SETSCROLLINFO (Winuser.h)
description: Die SBM \_ SETSCROLLINFO-Nachricht wird gesendet, um die Parameter einer Bildlaufleiste festlegen.
ms.assetid: e0e42a81-67be-4d40-88c8-77398b068617
keywords:
- SBM_SETSCROLLINFO message Windows Controls
topic_type:
- apiref
api_name:
- SBM_SETSCROLLINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5622371abb86301e1450c9fa0d6864e8db76c9837fca48fe8bcf11cb884f6b5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914290"
---
# <a name="sbm_setscrollinfo-message"></a>SBM \_ SETSCROLLINFO-Meldung

Die **SBM \_ SETSCROLLINFO-Nachricht** wird gesendet, um die Parameter einer Bildlaufleiste festlegen.

Anwendungen sollten diese Nachricht nicht direkt senden. Stattdessen sollten sie die [**SetScrollInfo-Funktion**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) verwenden. Ein Fenster empfängt diese Nachricht über seine [*WindowProc-Funktion.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) Anwendungen, die ein benutzerdefiniertes Scrollleisten-Steuerelement implementieren, müssen auf diese Meldungen reagieren, damit die **SetScrollInfo-Funktion** ordnungsgemäß funktioniert.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, ob die Scrollleiste neu gezeichnet wird, um die position des neuen Bildlauffelds wiederzuerkennen. Wenn dieser Parameter **TRUE ist,** wird die Scrollleiste neu gezeichnet. Wenn der Wert **FALSE ist,** wird die Scrollleiste nicht neu gezeichnet.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**SCROLLINFO-Struktur.**](/windows/win32/api/winuser/ns-winuser-scrollinfo) Legen Sie vor dem Aufrufen von [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)das **cbSize-Element** der -Struktur auf **sizeof**(**SCROLLINFO)** fest, legen Sie das **fMask-Element** fest, um die festzulegenden Parameter anzugeben, und geben Sie die neuen Parameterwerte in den entsprechenden Membern an.

Der **fMask-Member** kann einer oder mehrere der folgenden Werte sein.



| Wert                                                                                                                                                                           | Bedeutung                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIF_DISABLENOSCROLL"></span><span id="sif_disablenoscroll"></span><dl> <dt>**SIF \_ DISABLENOSCROLL**</dt> </dl> | Deaktiviert die Scrollleiste, anstatt sie zu entfernen, wenn die neuen Parameter der Scrollleiste die Scrollleiste unnötig machen.<br/> |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <dt>**\_SIF-SEITE**</dt> </dl>                                  | Legt die Scrollseite auf den im **nPage-Member angegebenen Wert** fest.<br/>                                                |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <dt>**SIF \_ POS**</dt> </dl>                                     | Legt die Bildlaufposition auf den wert fest, der im **nPos-Member angegeben** ist. <br/>                                            |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <dt>**\_SIF-BEREICH**</dt> </dl>                               | Legt den Bildlaufbereich auf den Wert fest, der in den **nMin- und** **nMax-Membern angegeben** ist. <br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die aktuelle Position des Bildlauffelds.

## <a name="remarks"></a>Hinweise

Die Meldungen, die die Position der Scrollleiste [**(WM \_ HSCROLL**](wm-hscroll.md) und [**WM \_ VSCROLL)**](wm-vscroll.md)angeben, stellen nur 16 Bits an Positionsdaten zur Verfügung. Die von [**SBM \_ GETSCROLLINFO,**](sbm-getscrollinfo.md) **SBM \_ SETSCROLLINFO,** [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)und [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) verwendete [**SCROLLINFO-Struktur**](/windows/win32/api/winuser/ns-winuser-scrollinfo) stellt jedoch 32 Bits bildlaufleistenpositionsdaten zur Seite. Sie können diese Nachrichten und Funktionen beim Verarbeiten der **WM \_ HSCROLL-** oder **WM \_ VSCROLL-Nachrichten** verwenden, um 32-Bit-Bildlaufleisten-Positionsdaten zu erhalten.

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

[**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[**SBM \_ GETSCROLLINFO**](sbm-getscrollinfo.md)
</dt> <dt>

[**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 

