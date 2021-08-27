---
description: Kopiert den Text, der einem Fenster entspricht, in einen vom Aufrufer bereitgestellten Puffer.
ms.assetid: 117c3d6d-24cd-462f-bdb0-b65d8914273a
title: WM_GETTEXT Meldung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e1bc6a8a77c51b3ab5b84f5cce700e65b180b357c932b4044a2b65cb49fc8e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089890"
---
# <a name="wm_gettext-message"></a>WM \_ GETTEXT-Nachricht

Kopiert den Text, der einem Fenster entspricht, in einen vom Aufrufer bereitgestellten Puffer.


```C++
#define WM_GETTEXT                      0x000D
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die maximale Anzahl der zu kopierenden Zeichen, einschließlich des abschließenden NULL-Zeichens.

Bei ANSI-Anwendungen kann die Größe der Zeichenfolge im Puffer aufgrund der Konvertierung von ANSI in Unicode auf mindestens die Hälfte des *wParam-Werts* reduziert werden.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf den Puffer, der den Text empfangen soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Der Rückgabewert ist die Anzahl der kopierten Zeichen, ohne das abschließende NULL-Zeichen.

## <a name="remarks"></a>Hinweise

Die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) kopiert den dem Fenster zugeordneten Text in den angegebenen Puffer und gibt die Anzahl der kopierten Zeichen zurück. Beachten Sie, dass Sie bei statischen Steuerelementen ohne Text den Text erhalten, mit dem das Steuerelement ursprünglich erstellt wurde, d. h. die ID-Nummer. Sie erhalten jedoch die ID des statischen Steuerelements ohne Text, wie es ursprünglich erstellt wurde. Das heißt, wenn Sie später ein **STM \_ SETIMAGE** verwendet haben, um es zu ändern, wird die ursprüngliche ID weiterhin zurückgegeben.

Bei einem Bearbeitungssteuerelement ist der zu kopierende Text der Inhalt des Bearbeitungssteuerelements. Bei einem Kombinationsfeld ist der Text der Inhalt des Bearbeitungssteuerelements (oder des statischen Texts) des Kombinationsfelds. Bei einer Schaltfläche ist der Text der Schaltflächenname. Bei anderen Fenstern ist der Text der Fenstertitel. Um den Text eines Elements in ein Listenfeld zu kopieren, kann eine Anwendung die [**LB \_ GETTEXT-Nachricht**](../controls/lb-gettext.md) verwenden.

Wenn die **WM \_ GETTEXT-Nachricht** an ein statisches Steuerelement mit dem **SS \_ ICON-Format** gesendet wird, wird in den ersten vier Bytes des Puffers, auf den *von lParam* gezeigt wird, ein Handle für das Symbol zurückgegeben. Dies gilt nur, wenn die [**WM \_ SETTEXT-Meldung**](wm-settext.md) zum Festlegen des Symbols verwendet wurde.

**Rich Edit:** Wenn der zu kopierende Text 64 KB überschreitet, verwenden Sie entweder die [**EM \_ STREAMOUT-**](../controls/em-streamout.md) oder [**EM \_ GETSELTEXT-Nachricht.**](../controls/em-getseltext.md)

Das Senden einer **WM \_ GETTEXT-Nachricht** an ein statisches Steuerelement ohne Text, z. B. eine statische Bitmap oder ein statisches Symbolsteuerelement, gibt keinen Zeichenfolgenwert zurück. Stattdessen wird 0 (null) zurückgegeben. Darüber hinaus könnten Anwendungen in frühen Versionen von Windows eine **WM \_ GETTEXT-Nachricht** an ein statisches Steuerelement senden, das keinen Text enthält, um die ID des Steuerelements abzurufen. Um die ID eines Steuerelements abzurufen, können Anwendungen [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) verwenden, um die **\_ GWL-ID** als Indexwert zu übergeben, oder [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) mithilfe der **\_ GWLP-ID**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
</dt> <dt>

[**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
</dt> <dt>

[**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[**WM \_ GETTEXTLENGTH**](wm-gettextlength.md)
</dt> <dt>

[**WM \_ SETTEXT**](wm-settext.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**EM \_ GETSELTEXT**](../controls/em-getseltext.md)
</dt> <dt>

[**EM \_ STREAMOUT**](../controls/em-streamout.md)
</dt> <dt>

[**LB \_ GETTEXT**](../controls/lb-gettext.md)
</dt> </dl>

 

 
