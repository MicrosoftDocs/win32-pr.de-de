---
title: Steuern von Meldungen
description: Dieser Abschnitt enthält Informationen darüber, wie Windows-Meldungen für die Kommunikation mit-Steuerelementen verwendet werden.
ms.assetid: 94d34132-25c2-4a1a-bd0e-35e5a666bbfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923a1b47d625a2797a900a6c582d00c5169097f3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103858580"
---
# <a name="control-messages"></a>Steuern von Meldungen

Dieser Abschnitt enthält Informationen darüber, wie Windows-Meldungen für die Kommunikation mit-Steuerelementen verwendet werden.

Die folgenden Themen werden erörtert.

-   [Nachrichten an allgemeine Steuerelemente](#messages-to-common-controls)
-   [Benachrichtigungen von Steuerelementen](#notifications-from-controls)
-   [Zugehörige Themen](#related-topics)

## <a name="messages-to-common-controls"></a>Nachrichten an allgemeine Steuerelemente

Da es sich bei den allgemeinen Steuerelementen um Windows handelt, kann eine Anwendung mit Ihnen kommunizieren, indem allgemeine Microsoft Win32-Nachrichten wie [**WM \_ getFont**](/windows/desktop/winmsg/wm-getfont) oder [**WM \_ SetText**](/windows/desktop/winmsg/wm-settext)verwendet werden. Außerdem unterstützt die Fenster Klasse der einzelnen allgemeinen Steuerelemente eine Reihe von Steuerelement spezifischen Meldungen. In der Regel verwendet eine Anwendung [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) oder [**SendDlgItemMess**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) , um Nachrichten an das Steuerelement zu übergeben (häufig werden Informationen im Rückgabewert empfangen).

Einige allgemeine Steuerelemente verfügen auch über eine Reihe von Makros, die eine Anwendung anstelle von [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)verwenden kann. Die Makros sind in der Regel einfacher zu verwenden als die Funktionen. Der folgende Beispielcode ruft den Text des ausgewählten Struktur Ansichts Elements ab, wobei zuerst die unformatierten Nachrichten verwendet werden, und zweitens, indem die entsprechenden Makros verwendet werden. Nehmen Sie an, dass *HWND* das Handle des Steuerelement Fensters ist.


```
BOOL fSuccess;
WCHAR itemText[99];
TVITEM tvItem = { 0 };
tvItem.mask = TVIF_TEXT;
tvItem.cchTextMax = ARRAYSIZE(itemText);
tvItem.pszText = itemText;

// This...
tvItem.hItem = (HTREEITEM)SendMessage(hwnd, TVM_GETNEXTITEM, TVGN_CARET, NULL);
fSuccess = SendMessage(hwnd, TVM_GETITEM, 0, (LPARAM)&tvItem);

// ... is equivalent to this.
tvItem.hItem = TreeView_GetSelection(hwnd);
fSuccess = TreeView_GetItem(hwnd, &tvItem);
```



Wenn an den System Farbeinstellungen eine Änderung vorgenommen wird, sendet Windows eine [**\_ System-syscolorchange**](/windows/desktop/gdi/wm-syscolorchange) -Meldung an alle Fenster der obersten Ebene. Das Fenster der obersten Ebene muss die **System- \_ syscolorchange** -Nachricht an die allgemeinen Steuerelemente weiterleiten. andernfalls werden die Steuerelemente nicht über die Farbänderung benachrichtigt. Durch Weiterleiten der Nachricht wird sichergestellt, dass die von den allgemeinen Steuerelementen verwendeten Farben mit den von anderen Benutzeroberflächen Objekten verwendeten Farben konsistent sind. Beispielsweise verwendet ein ToolBar-Steuerelement die Farbe "3D-Objekte", um seine Schaltflächen zu zeichnen. Wenn der Benutzer die Farbe des 3D-Objekts ändert, aber die **WM- \_ syscolorchange** -Meldung nicht an die Symbolleiste weitergeleitet wird, bleiben die Schaltflächen der Symbolleiste in der ursprünglichen Farbe (oder sogar in eine Kombination aus alten und neuen Farben geändert), während sich die Farbe anderer Schaltflächen im System ändert.

## <a name="notifications-from-controls"></a>Benachrichtigungen von Steuerelementen

Steuerelemente sind untergeordnete Fenster, die Benachrichtigungs Meldungen an das übergeordnete Fenster senden, wenn Ereignisse, die normalerweise durch eine Eingabe des Benutzers ausgelöst werden, im-Steuerelement auftreten. Die Anwendung nutzt diese Benachrichtigungs Meldungen, um zu bestimmen, welche Aktion der Benutzer ausführen möchte. Mit Ausnahme von trackbars, die die [**"WM \_ HScroll**](wm-hscroll.md) "-und " [**WM \_ VScroll**](wm-vscroll.md) "-Meldungen verwenden, um das übergeordnete Element von Änderungen zu benachrichtigen, senden allgemeine Steuerelemente Benachrichtigungen als [**WM- \_ Befehl**](/windows/desktop/menurc/wm-command) oder [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldungen, wie im Referenz Thema für die Benachrichtigung angegeben. In der Regel verwenden ältere Benachrichtigungen (die für einen langen Zeitraum in der API enthalten waren) **den \_ Befehl WM**.

Der *LPARAM* -Parameter von [**WM \_ Notify**](wm-notify.md) ist entweder die Adresse einer [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur oder die Adresse einer größeren Struktur, die **NMHDR** als ersten Member enthält. Die-Struktur enthält den Benachrichtigungs Code und identifiziert das allgemeine Steuerelement, das die Benachrichtigungs Meldung gesendet hat. Die Bedeutung der übrigen Strukturmember variiert ggf. je nach Benachrichtigungs Code.

Jeder Typ von Common Control verfügt über einen entsprechenden Satz von Benachrichtigungs Codes. Die allgemeine Steuerelement Bibliothek bietet auch Benachrichtigungs Codes, die von mehreren Typen von allgemeinen Steuerelementen gesendet werden können. Sehen Sie sich die Dokumentation für das relevante Steuerelement an, um zu bestimmen, welche Benachrichtigungs Codes gesendet werden und welches Format Sie annehmen.

Beispielcode zum Behandeln von WM- [**\_ Benachrichtigungs**](wm-notify.md) Nachrichten finden Sie im Referenz Thema für diese Nachricht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Allgemeine Steuerungs Referenz](common-control-reference.md)
</dt> </dl>

 

 
