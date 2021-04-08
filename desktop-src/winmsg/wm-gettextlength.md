---
description: Bestimmt die Länge des Texts, der einem Fenster zugeordnet ist, in Zeichen.
ms.assetid: 9e185435-a624-4380-adfd-be4f3645ee5d
title: WM_GETTEXTLENGTH Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0efc058033f9c4939137414d305d0717b54bef54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960171"
---
# <a name="wm_gettextlength-message"></a>WM \_ getTextLength-Meldung

Bestimmt die Länge des Texts, der einem Fenster zugeordnet ist, in Zeichen.


```C++
#define WM_GETTEXTLENGTH                0x000E
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss NULL sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Der Rückgabewert ist die Länge des Texts in Zeichen, ohne das abschließende Null Zeichen.

## <a name="remarks"></a>Bemerkungen

Bei einem Bearbeitungs Steuerelement ist der Text, der kopiert werden soll, der Inhalt des Bearbeitungs Steuer Elements. Bei einem Kombinations Feld ist der Text der Inhalt des Bearbeitungs Steuer Elements (oder statischer Text) des Kombinations Felds. Für eine Schaltfläche ist der Text der Schaltflächen Name. Bei anderen Fenstern ist der Text der Fenstertitel. Zum Ermitteln der Länge eines Elements in einem Listenfeld kann eine Anwendung die [**\_ gettextlen**](../controls/lb-gettextlen.md) -Nachricht des lb-Elements verwenden.

Wenn die **WM \_ getTextLength** -Nachricht gesendet wird, gibt die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion die Länge des Texts in Zeichen zurück. Unter bestimmten Bedingungen gibt die **defwindowproc** -Funktion einen Wert zurück, der größer ist als die tatsächliche Textlänge. Dies tritt bei bestimmten Kombinationen von ANSI und Unicode auf und ist darauf zurückzuführen, dass das System das vorhanden sein von DBCS-Zeichen (Double-Byte Character Set) im Text zulässt. Der Rückgabewert ist jedoch immer mindestens so groß wie die tatsächliche Textlänge. Sie können Sie daher immer verwenden, um die Puffer Zuordnung zu steuern. Dieses Verhalten kann auftreten, wenn eine Anwendung sowohl ANSI-Funktionen als auch allgemeine Dialogfelder verwendet, die Unicode verwenden.

Um die genaue Länge des Texts zu erhalten, verwenden Sie die Nachrichten [**WM \_ gettext**](wm-gettext.md), [**lb \_ gettext**](../controls/lb-gettext.md)oder [**CB \_ getlbtext**](../controls/cb-getlbtext.md) oder die Funktion [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta) .

Das Senden einer **WM- \_ getTextLength** -Nachricht an ein statisches, nicht-Text-Steuerelement, z. b. eine statische Bitmap oder ein statisches Symbol, gibt keinen Zeichen folgen Wert zurück. Stattdessen wird 0 (null) zurückgegeben.

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

[**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**Getwindowtextlength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[**WM \_ gettext**](wm-gettext.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**CB \_ getlbtext**](../controls/cb-getlbtext.md)
</dt> <dt>

[**LB- \_ gettext**](../controls/lb-gettext.md)
</dt> <dt>

[**LB- \_ gettextlen**](../controls/lb-gettextlen.md)
</dt> </dl>

 

 
