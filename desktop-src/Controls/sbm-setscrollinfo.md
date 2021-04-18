---
title: SBM_SETSCROLLINFO Meldung (Winuser. h)
description: Die SBM- \_ setScrollInfo-Nachricht wird gesendet, um die Parameter einer Schiebe Leiste festzulegen.
ms.assetid: e0e42a81-67be-4d40-88c8-77398b068617
keywords:
- Windows-Steuerelemente für SBM_SETSCROLLINFO Meldung
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
ms.openlocfilehash: e98abbca2d53d4b104caea22954472a17dfd5c1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345494"
---
# <a name="sbm_setscrollinfo-message"></a>SBM- \_ setScrollInfo-Meldung

Die **SBM- \_ setScrollInfo** -Nachricht wird gesendet, um die Parameter einer Schiebe Leiste festzulegen.

Anwendungen sollten diese Nachricht nicht direkt senden. Stattdessen sollten Sie die [**setScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) -Funktion verwenden. Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion. Anwendungen, die ein benutzerdefiniertes Bild Lauf leisten-Steuerelement implementieren, müssen auf diese Nachrichten reagieren, damit die Funktion **setScrollInfo** ordnungsgemäß funktioniert.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, ob die Schiebe Leiste neu gezeichnet wird, um die neue Position des Bild Lauf Felds widerzuspiegeln. Wenn dieser Parameter **true** ist, wird die Scrollleiste neu gezeichnet. Wenn der Wert **false** ist, wird die Scrollleiste nicht neu gezeichnet.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**ScrollInfo**](/windows/win32/api/winuser/ns-winuser-scrollinfo) -Struktur. Legen Sie vor dem Aufrufen von [**setScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)den **CBSIZE** -Member der-Struktur auf **sizeof**(**ScrollInfo**) fest, legen Sie den **fmask** -Member fest, um die festzulegenden Parameter anzugeben, und geben Sie die neuen Parameterwerte in den entsprechenden Membern an.

Der **fmask** -Member kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                           | Bedeutung                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIF_DISABLENOSCROLL"></span><span id="sif_disablenoscroll"></span><dl> <dt>**SIF \_ DisableNoScroll**</dt> </dl> | Deaktiviert die Schiebe Leiste, anstatt Sie zu entfernen, wenn die neuen Parameter der Scrollleiste die Bild Lauf Leiste unnötig machen.<br/> |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <dt>**SIF- \_ Seite**</dt> </dl>                                  | Legt die scrollseite auf den im **nPage** -Member angegebenen Wert fest.<br/>                                                |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <dt>**SIF \_ Torys**</dt> </dl>                                     | Legt die Scrollposition auf den im **NPOs** -Member angegebenen Wert fest. <br/>                                            |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <dt>**SIF- \_ Bereich**</dt> </dl>                               | Legt den scrollbereich auf den Wert fest, der in den **nmin** -und **nmax** -Membern angegeben ist. <br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die aktuelle Position des Bild Lauf Felds.

## <a name="remarks"></a>Bemerkungen

Die Nachrichten, die die Position der Scrollleiste, [**WM \_ HScroll**](wm-hscroll.md) und [**WM \_ VScroll**](wm-vscroll.md)angeben, stellen nur 16 Bits an Positionsdaten bereit. Die [**ScrollInfo**](/windows/win32/api/winuser/ns-winuser-scrollinfo) -Struktur, die von [**SBM \_ getscrollinfo**](sbm-getscrollinfo.md), **SBM \_ setScrollInfo**, [**getscrollinfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)und [**setScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) verwendet wird, stellt jedoch 32 Bits der Positions leisten Positionsdaten bereit. Sie können diese Nachrichten und Funktionen bei der Verarbeitung der " **WM \_ HScroll** "-oder " **WM \_ VScroll** "-Meldungen zum Abrufen von 32-Bit-Scrollleisten-Positionsdaten verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**Getscrollinfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[**SBM \_ getscrollinfo**](sbm-getscrollinfo.md)
</dt> <dt>

[**ScrollInfo**](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 

