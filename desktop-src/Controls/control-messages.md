---
title: Steuern von Nachrichten
description: Dieser Abschnitt enthält Informationen dazu, wie Windows Nachrichten für die Kommunikation mit Steuerelementen verwendet werden.
ms.assetid: 94d34132-25c2-4a1a-bd0e-35e5a666bbfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed60ebb66341332b6248b8427045abc5b62a2311427d56e46b25fe93b3d899ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921100"
---
# <a name="control-messages"></a>Steuern von Nachrichten

Dieser Abschnitt enthält Informationen dazu, wie Windows Nachrichten für die Kommunikation mit Steuerelementen verwendet werden.

Die folgenden Themen werden erläutert.

-   [Meldungen an allgemeine Steuerelemente](#messages-to-common-controls)
-   [Benachrichtigungen von Steuerelementen](#notifications-from-controls)
-   [Zugehörige Themen](#related-topics)

## <a name="messages-to-common-controls"></a>Meldungen an allgemeine Steuerelemente

Da allgemeine Steuerelemente Fenster sind, kann eine Anwendung mit ihnen kommunizieren, indem sie gängige Microsoft Win32-Nachrichten wie [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont) oder [**WM \_ SETTEXT verwendet.**](/windows/desktop/winmsg/wm-settext) Darüber hinaus unterstützt die Fensterklasse jedes allgemeinen Steuerelements einen Satz von steuerelementspezifischen Meldungen. In der Regel verwendet eine Anwendung [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) oder [**SendDlgItemMessage,**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) um Nachrichten an das Steuerelement zu übergeben (häufig werden Informationen im Rückgabewert empfangen).

Einige gängige Steuerelemente verfügen auch über einen Satz von Makros, die eine Anwendung anstelle von [**SendMessage verwenden kann.**](/windows/desktop/api/winuser/nf-winuser-sendmessage) Die Makros sind in der Regel einfacher zu verwenden als die Funktionen. Der folgende Beispielcode ruft den Text des ausgewählten Strukturansichtselements ab, zuerst mithilfe der Unformatiertmeldungen und zweitens mithilfe der entsprechenden Makros. Angenommen, *hwnd* ist das Handle des Steuerelementfensters.


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



Wenn eine Änderung an den Systemfarbeinstellungen vorgenommen wird, sendet Windows [**eine WM \_ SYSCOLORCHANGE-Nachricht**](/windows/desktop/gdi/wm-syscolorchange) an alle Fenster der obersten Ebene. Das Fenster der obersten Ebene muss die **WM \_ SYSCOLORCHANGE-Nachricht** an die allgemeinen Steuerelemente weitersennen. Andernfalls werden die Steuerelemente nicht über die Farbänderung benachrichtigt. Durch das Weiterleiten der Nachricht wird sichergestellt, dass die von Ihren allgemeinen Steuerelementen verwendeten Farben mit denen anderer Benutzeroberflächenobjekte konsistent sind. Beispielsweise verwendet ein Symbolleisten-Steuerelement die Farbe "3D Objects", um seine Schaltflächen zu zeichnen. Wenn der Benutzer die Farbe des 3D-Objekts ändert, die **\_ WM SYSCOLORCHANGE-Meldung** jedoch nicht an die Symbolleiste weitergeleitet wird, bleiben die Symbolleistenschaltflächen in ihrer ursprünglichen Farbe erhalten (oder ändern sich sogar in eine Kombination aus alten und neuen Farben), während sich die Farbe anderer Schaltflächen im System ändert.

## <a name="notifications-from-controls"></a>Benachrichtigungen von Steuerelementen

Steuerelemente sind untergeordnete Fenster, die Benachrichtigungsmeldungen an das übergeordnete Fenster senden, wenn Ereignisse, die in der Regel durch Eingabe des Benutzers ausgelöst werden, im -Steuerelement auftreten. Die Anwendung nutzt diese Benachrichtigungen, um zu bestimmen, welche Aktion der Benutzer ergreifen möchte. Mit Ausnahme von Trackleisten, die die [**WM \_ HSCROLL-**](wm-hscroll.md) und [**WM \_ VSCROLL-Meldungen**](wm-vscroll.md) verwenden, um das übergeordnete Element über Änderungen zu benachrichtigen, senden allgemeine Steuerelemente Benachrichtigungen als [**WM \_ COMMAND-**](/windows/desktop/menurc/wm-command) oder [**WM \_ NOTIFY-Nachrichten,**](wm-notify.md) wie im Referenzthema für die Benachrichtigung angegeben. In der Regel verwenden ältere Benachrichtigungen (die seit langer Zeit in der API enthalten sind) **WM \_ COMMAND**.

Der *lParam-Parameter* von [**WM \_ NOTIFY**](wm-notify.md) ist entweder die Adresse einer [**NMHDR-Struktur**](/windows/desktop/api/richedit/ns-richedit-nmhdr) oder die Adresse einer größeren Struktur, die **NMHDR** als ersten Member enthält. Die -Struktur enthält den Benachrichtigungscode und identifiziert das allgemeine Steuerelement, das die Benachrichtigungsnachricht gesendet hat. Die Bedeutung der verbleibenden Strukturmitglieder variiert je nach Benachrichtigungscode, falls diese elemente sind.

Jeder Typ von allgemeinem Steuerelement verfügt über einen entsprechenden Satz von Benachrichtigungscodes. Die allgemeine Steuerelementbibliothek stellt auch Benachrichtigungscodes zur Verfügung, die von mehr als einem Typ von allgemeinem Steuerelement gesendet werden können. Informationen dazu, welche Benachrichtigungscodes gesendet werden und welches Format sie verwenden, finden Sie in der Dokumentation zur Steuerung von Interesse.

Beispielcode, der zeigt, wie [**WM \_ NOTIFY-Nachrichten**](wm-notify.md) behandelt werden, finden Sie im Referenzthema für diese Nachricht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Allgemeine Steuerelementreferenz](common-control-reference.md)
</dt> </dl>

 

 
