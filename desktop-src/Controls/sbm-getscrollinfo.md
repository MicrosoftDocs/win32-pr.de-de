---
title: SBM_GETSCROLLINFO Meldung (Winuser. h)
description: Die SBM \_ getscrollinfo-Nachricht wird gesendet, um die Parameter einer Schiebe Leiste abzurufen.
ms.assetid: 3b43430f-b55f-43ec-8558-baf5c953064f
keywords:
- Windows-Steuerelemente für SBM_GETSCROLLINFO Meldung
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
ms.openlocfilehash: c4cb05b05ba2686d755c5fa34adcff0016433346
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346766"
---
# <a name="sbm_getscrollinfo-message"></a>SBM \_ getscrollinfo-Meldung

Die **SBM \_ getscrollinfo** -Nachricht wird gesendet, um die Parameter einer Schiebe Leiste abzurufen.

Anwendungen sollten diese Nachricht nicht direkt senden. Stattdessen sollten Sie die [**getscrollinfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) -Funktion verwenden. Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion. Anwendungen, die ein benutzerdefiniertes Bild Lauf leisten-Steuerelement implementieren, müssen auf diese Nachrichten reagieren, damit die Funktion **getscrollinfo** ordnungsgemäß funktioniert.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**ScrollInfo**](/windows/win32/api/winuser/ns-winuser-scrollinfo) -Struktur. Legen Sie vor dem Aufrufen von [**getscrollinfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)den **CBSIZE** -Member der-Struktur auf **sizeof**(**ScrollInfo**) fest, und legen Sie den fmask-Member fest, um die abzurufenden ScrollBar-Parameter anzugeben.  Vor der Rückgabe kopiert die Meldung die angegebenen Parameter in die entsprechenden Member der Struktur.

Der **fmask** -Member kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                      | Bedeutung                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="SIF_ALL"></span><span id="sif_all"></span><dl> <dt>**Alle SIF \_**</dt> </dl>                | Kombination aus SIF \_ -Seite, SIF \_ -POS, SIF \_ -Bereich und SIF- \_ trackpos.<br/>       |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <dt>**SIF- \_ Seite**</dt> </dl>             | Kopiert die scrollseite in den nPage-Member.<br/>                              |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <dt>**SIF \_ Torys**</dt> </dl>                | Kopiert die Scrollposition in den NPOs-Member. <br/>                          |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <dt>**SIF- \_ Bereich**</dt> </dl>          | Kopiert den scrollbereich in die Member nmin und nmax. <br/>                   |
| <span id="SIF_TRACKPOS"></span><span id="sif_trackpos"></span><dl> <dt>**SIF- \_ trackpos**</dt> </dl> | Kopiert die aktuelle nach Verfolgungs Position des Bild Lauf Felds in den ntrackpos-Member.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht Werte abgerufen hat, ist der Rückgabewert " **true**". Andernfalls ist Sie **false**.

## <a name="remarks"></a>Bemerkungen

Die Nachrichten, die die Position der Scrollleiste, [**WM \_ HScroll**](wm-hscroll.md) und [**WM \_ VScroll**](wm-vscroll.md)angeben, stellen nur 16 Bits an Positionsdaten bereit. Die [**ScrollInfo**](/windows/win32/api/winuser/ns-winuser-scrollinfo) -Struktur, die von **SBM \_ getscrollinfo**, [**SBM \_ setScrollInfo**](sbm-setscrollinfo.md), [**getscrollinfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)und [**setScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) verwendet wird, stellt jedoch 32 Bits der Positions leisten Positionsdaten bereit. Sie können diese Nachrichten und Funktionen bei der Verarbeitung der " **WM \_ HScroll** "-oder " **WM \_ VScroll** "-Meldungen zum Abrufen von 32-Bit-Scrollleisten-Positionsdaten verwenden.

Um die 32-Bit-Position des Bild Lauf Felds (Ziehpunkt) während eines SB- \_ thumbrequest-Anforderungs Codes in einer [**WM \_ HScroll**](wm-hscroll.md) -oder [**WM \_ VScroll**](wm-vscroll.md) -Nachricht abzurufen, senden Sie **SBM \_ getscrollinfo** mit dem SIF \_ trackpos-Wert im **fmask** -Member der [**ScrollInfo**](/windows/win32/api/winuser/ns-winuser-scrollinfo) -Struktur. Die Meldung gibt die nach Verfolgungs Position des Bild Lauf Felds im **ntrackpos** -Member der **ScrollInfo** -Struktur zurück. Dadurch können Sie die Position des Bild Lauf Felds beim Verschieben durch den Benutzer erhalten. Alternativ können Sie die [**getscrollinfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) -Funktion verwenden, um dieselben Informationen zu erhalten.

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

[**SBM \_ setScrollInfo**](sbm-setscrollinfo.md)
</dt> <dt>

[**ScrollInfo**](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 

