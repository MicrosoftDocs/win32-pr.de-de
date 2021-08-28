---
title: SBM_GETSCROLLINFO Meldung (Winuser.h)
description: Die SBM \_ GETSCROLLINFO-Nachricht wird gesendet, um die Parameter einer Scrollleiste abzurufen.
ms.assetid: 3b43430f-b55f-43ec-8558-baf5c953064f
keywords:
- SBM_GETSCROLLINFO Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- SBM_GETSCROLLINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5fde18fe30e9d944e547305094e7ea69e6745d4e1e112d8697367cd82833588
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919470"
---
# <a name="sbm_getscrollinfo-message"></a>SBM \_ GETSCROLLINFO-Nachricht

Die **SBM \_ GETSCROLLINFO-Nachricht** wird gesendet, um die Parameter einer Scrollleiste abzurufen.

Anwendungen sollten diese Nachricht nicht direkt senden. Stattdessen sollten sie die [**GetScrollInfo-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) verwenden. Ein Fenster empfängt diese Meldung über seine [*WindowProc-Funktion.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) Anwendungen, die ein benutzerdefiniertes Scrollleisten-Steuerelement implementieren, müssen auf diese Meldungen reagieren, damit die **GetScrollInfo-Funktion** ordnungsgemäß funktioniert.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**SCROLLINFO-Struktur.**](/windows/win32/api/winuser/ns-winuser-scrollinfo) Legen Sie vor dem Aufrufen von [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)den **cbSize-Member** der -Struktur auf **sizeof****(SCROLLINFO)** fest, und legen Sie den **fMask-Member** fest, um die abzurufenden Scrollleistenparameter anzugeben. Vor der Rückgabe kopiert die Nachricht die angegebenen Parameter in die entsprechenden Member der -Struktur.

Der **fMask-Member** kann einer oder mehrere der folgenden Werte sein.



| Wert                                                                                                                                                      | Bedeutung                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="SIF_ALL"></span><span id="sif_all"></span><dl> <dt>**SIF \_ ALL**</dt> </dl>                | Kombination aus SIF \_ PAGE, SIF \_ POS, SIF \_ RANGE und SIF \_ TRACKPOS.<br/>       |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <dt>**\_SIF-SEITE**</dt> </dl>             | Kopiert die Bildlaufseite in das nPage-Element.<br/>                              |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <dt>**SIF \_ POS**</dt> </dl>                | Kopiert die Bildlaufposition in das nPos-Element. <br/>                          |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <dt>**\_SIF-BEREICH**</dt> </dl>          | Kopiert den Bildlaufbereich in die Member nMin und nMax. <br/>                   |
| <span id="SIF_TRACKPOS"></span><span id="sif_trackpos"></span><dl> <dt>**SIF \_ TRACKPOS**</dt> </dl> | Kopiert die aktuelle Nachverfolgungsposition des Bildlauffelds in das Element nTrackPos.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht Werte abgerufen hat, ist der Rückgabewert **TRUE.** Andernfalls ist es **FALSE.**

## <a name="remarks"></a>Hinweise

Die Meldungen, die die Bildlaufleistenposition [**WM \_ HSCROLL**](wm-hscroll.md) und [**WM \_ VSCROLL**](wm-vscroll.md)angeben, stellen nur 16 Bits an Positionsdaten bereit. Die [**scrollinfo-Struktur,**](/windows/win32/api/winuser/ns-winuser-scrollinfo) die von **SBM \_ GETSCROLLINFO,** [**SBM \_ SETSCROLLINFO,**](sbm-setscrollinfo.md) [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)und [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) verwendet wird, stellt jedoch 32 Bits an Bildlaufleistenpositionsdaten bereit. Sie können diese Nachrichten und Funktionen beim Verarbeiten der **WM \_ HSCROLL-** oder **WM \_ VSCROLL-Nachrichten** verwenden, um 32-Bit-Bildlaufleistenpositionsdaten zu erhalten.

Um die 32-Bit-Position des Bildlauffelds (Thumb) während eines SB \_ THUMBTRACK-Anforderungscodes in einer [**WM \_ HSCROLL-**](wm-hscroll.md) oder [**WM \_ VSCROLL-Nachricht**](wm-vscroll.md) abzurufen, senden Sie **SBM \_ GETSCROLLINFO** mit dem SIF \_ TRACKPOS-Wert im **fMask-Member** der [**SCROLLINFO-Struktur.**](/windows/win32/api/winuser/ns-winuser-scrollinfo) Die Meldung gibt die Nachverfolgungsposition des Bildlauffelds im **nTrackPos-Member** der **SCROLLINFO-Struktur** zurück. Dadurch können Sie die Position des Bildlauffelds abrufen, während der Benutzer es verschiebt. Alternativ können Sie die [**GetScrollInfo-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) verwenden, um die gleichen Informationen abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[**SBM \_ SETSCROLLINFO**](sbm-setscrollinfo.md)
</dt> <dt>

[**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 

