---
description: Bestimmt die Länge des einem Fenster zugeordneten Texts in Zeichen.
ms.assetid: 9e185435-a624-4380-adfd-be4f3645ee5d
title: WM_GETTEXTLENGTH Meldung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bc01f6f7a2b74df41e97a84bb4d7e17d9c3e21966215fcbcca04222d1d5537f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710390"
---
# <a name="wm_gettextlength-message"></a>WM \_ GETTEXTLENGTH-Nachricht

Bestimmt die Länge des einem Fenster zugeordneten Texts in Zeichen.


```C++
#define WM_GETTEXTLENGTH                0x000E
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Der Rückgabewert ist die Länge des Texts in Zeichen, ohne das abschließende NULL-Zeichen.

## <a name="remarks"></a>Hinweise

Bei einem Bearbeitungssteuerelement ist der zu kopierende Text der Inhalt des Bearbeitungssteuerelements. Bei einem Kombinationsfeld ist der Text der Inhalt des Bearbeitungssteuerelements (oder des statischen Texts) des Kombinationsfelds. Bei einer Schaltfläche ist der Text der Schaltflächenname. Bei anderen Fenstern ist der Text der Fenstertitel. Um die Länge eines Elements in einem Listenfeld zu bestimmen, kann eine Anwendung die [**LB \_ GETTEXTLEN-Nachricht**](../controls/lb-gettextlen.md) verwenden.

Wenn die **WM \_ GETTEXTLENGTH-Nachricht** gesendet wird, gibt die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) die Länge des Texts in Zeichen zurück. Unter bestimmten Bedingungen gibt die **DefWindowProc-Funktion** einen Wert zurück, der größer als die tatsächliche Länge des Texts ist. Dies tritt bei bestimmten Mischungen von ANSI und Unicode auf und ist darauf zurückzuführen, dass das System das mögliche Vorhandensein von Doppel-Byte-Zeichensatzzeichen (Double-Byte Character Set, DBCS) im Text zulässt. Der Rückgabewert ist jedoch immer mindestens so groß wie die tatsächliche Länge des Texts. Sie können es daher immer verwenden, um die Pufferzuordnung zu steuern. Dieses Verhalten kann auftreten, wenn eine Anwendung sowohl ANSI-Funktionen als auch allgemeine Dialoge verwendet, die Unicode verwenden.

Um die genaue Länge des Texts abzurufen, verwenden Sie die [**WM \_ GETTEXT-,**](wm-gettext.md) [**LB \_ GETTEXT-**](../controls/lb-gettext.md)oder [**CB \_ GETLBTEXT-Nachrichten**](../controls/cb-getlbtext.md) oder die [**GetWindowText-Funktion.**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)

Das Senden einer **WM \_ GETTEXTLENGTH-Nachricht** an ein statisches Steuerelement ohne Text, z. B. eine statische Bitmap oder ein statisches Symbolsteuerelement, gibt keinen Zeichenfolgenwert zurück. Stattdessen wird 0 (null) zurückgegeben.

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

[**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[**WM \_ GETTEXT**](wm-gettext.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**CB \_ GETLBTEXT**](../controls/cb-getlbtext.md)
</dt> <dt>

[**LB \_ GETTEXT**](../controls/lb-gettext.md)
</dt> <dt>

[**LB \_ GETTEXTLEN**](../controls/lb-gettextlen.md)
</dt> </dl>

 

 
