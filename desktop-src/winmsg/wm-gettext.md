---
description: Kopiert den Text, der einem Fenster entspricht, in einen Puffer, der vom Aufrufer bereitgestellt wird.
ms.assetid: 117c3d6d-24cd-462f-bdb0-b65d8914273a
title: WM_GETTEXT Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47f8e2268c1d0ec043e24a001f16abae357bdbdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757824"
---
# <a name="wm_gettext-message"></a>WM- \_ gettext-Nachricht

Kopiert den Text, der einem Fenster entspricht, in einen Puffer, der vom Aufrufer bereitgestellt wird.


```C++
#define WM_GETTEXT                      0x000D
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die maximale Anzahl der zu kopierenden Zeichen, einschließlich des abschließenden NULL-Zeichens.

Bei ANSI-Anwendungen kann die Größe der Zeichenfolge im Puffer (auf mindestens die Hälfte des Werts des *wParam* -Werts) aufgrund der Konvertierung von ANSI in Unicode reduziert werden.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf den Puffer, der den Text empfangen soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Der Rückgabewert ist die Anzahl der kopierten Zeichen, ohne das abschließende Null Zeichen.

## <a name="remarks"></a>Bemerkungen

Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion kopiert den dem Fenster zugeordneten Text in den angegebenen Puffer und gibt die Anzahl der kopierten Zeichen zurück. Beachten Sie, dass für statische nicht-Text-Steuerelemente der Text, mit dem das Steuerelement ursprünglich erstellt wurde, d. h. die ID-Nummer, angezeigt wird. Sie erhalten jedoch die ID des statischen nicht-Text-Steuer Elements, das ursprünglich erstellt wurde. Das heißt, wenn Sie anschließend ein STM-Abbild verwenden, um es zu ändern, wird die ursprüngliche ID weiterhin zurückgegeben. **\_**

Bei einem Bearbeitungs Steuerelement ist der Text, der kopiert werden soll, der Inhalt des Bearbeitungs Steuer Elements. Bei einem Kombinations Feld ist der Text der Inhalt des Bearbeitungs Steuer Elements (oder statischer Text) des Kombinations Felds. Für eine Schaltfläche ist der Text der Schaltflächen Name. Bei anderen Fenstern ist der Text der Fenstertitel. Um den Text eines Elements in einem Listenfeld zu kopieren, kann eine Anwendung die [**lb- \_ gettext**](../controls/lb-gettext.md) -Nachricht verwenden.

Wenn die **WM- \_ gettext** -Nachricht mit dem SS-Symbolstil an ein statisches Steuerelement gesendet wird, wird in den ersten vier Bytes des Puffers, auf die von *LPARAM* verwiesen wird, ein Handle für das Symbol zurückgegeben. **\_** Dies gilt nur, wenn die [**WM- \_ SetText**](wm-settext.md) -Nachricht verwendet wurde, um das Symbol festzulegen.

Umfassende **Bearbeitung:** Wenn der zu kopierende Text 64 KB überschreitet, verwenden Sie entweder die [**EM- \_ StreamOut**](../controls/em-streamout.md) -oder die [**EM \_ GetSelText**](../controls/em-getseltext.md) -Nachricht.

Das Senden einer **WM- \_ gettext** -Nachricht an ein statisches nicht-Text-Steuerelement, z. b. eine statische Bitmap oder ein statisches Symbol Steuerelement, gibt keinen Zeichen folgen Wert zurück. Stattdessen wird 0 (null) zurückgegeben. Außerdem könnten in früheren Versionen von Windows Anwendungen eine **WM- \_ gettext** -Nachricht an ein statisches nicht-Text-Steuerelement senden, um die ID des Steuer Elements abzurufen. Zum Abrufen der ID eines Steuer Elements können Anwendungen [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) mit der **GWL- \_ ID** als Indexwert oder [**getwindowlongptr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) mithilfe der **gwlp- \_ ID** verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
</dt> <dt>

[**Getwindowlongptr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
</dt> <dt>

[**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**Getwindowtextlength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[**WM \_ getTextLength**](wm-gettextlength.md)
</dt> <dt>

[**WM- \_ SetText**](wm-settext.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**EM \_ GetSelText**](../controls/em-getseltext.md)
</dt> <dt>

[**EM- \_ StreamOut**](../controls/em-streamout.md)
</dt> <dt>

[**LB- \_ gettext**](../controls/lb-gettext.md)
</dt> </dl>

 

 
