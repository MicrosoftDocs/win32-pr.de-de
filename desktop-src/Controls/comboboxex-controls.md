---
title: Informationen zu ComboBoxEx-Steuerelementen
description: ComboBoxEx-Steuerelemente sind Kombinations Feld-Steuerelemente, die native Unterstützung für Element Bilder bereitstellen.
ms.assetid: a4b1aa79-40c4-4eff-801c-4f308d86fb35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 427abef015474047d1842d13e5fb40640d0406c5
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103858509"
---
# <a name="about-comboboxex-controls"></a>Informationen zu ComboBoxEx-Steuerelementen

ComboBoxEx-Steuerelemente sind Kombinations Feld-Steuerelemente, die native Unterstützung für Element Bilder bereitstellen. Damit Element Bilder problemlos zugänglich sind, bietet das-Steuerelement Unterstützung für Bildlisten. Mithilfe dieses Steuer Elements können Sie die Funktionalität eines Kombinations Felds bereitstellen, ohne die Element Grafiken manuell zeichnen zu müssen.

Dieses Thema enthält folgende Abschnitte:

-   [Erstellen von ComboBoxEx-Steuerelementen](#creating-comboboxex-controls)
-   [ComboBoxEx-Steuerelement Stile](#comboboxex-control-styles)
-   [ComboBoxEx-Steuerelement Elemente](#comboboxex-control-items)
-   [Rückruf Elemente](#callback-items)
-   [Bildlisten des ComboBoxEx-Steuer Elements](#comboboxex-control-image-lists)
-   [Informationen zu ComboBoxEx-Steuerelement Benachrichtigungs Meldungen](#about-comboboxex-control-notification-messages)
-   [Nachrichten Weiterleitung durch ComboBoxEx-Steuerelement](#comboboxex-control-message-forwarding)

## <a name="creating-comboboxex-controls"></a>Erstellen von ComboBoxEx-Steuerelementen

Effektiv erstellt ein ComboBoxEx-Steuerelement ein untergeordnetes Kombinations Feld und führt auf der Grundlage einer zugewiesenen Bildliste für Sie Besitzer Zeichnungs Aufgaben aus. Aus diesem Grund ist der Stil des [**CBS- \_ Besitzers**](combo-box-styles.md) "," impliziert, und es ist nicht notwendig, ihn beim Erstellen des Steuer Elements zu verwenden. Da Bildlisten verwendet werden, um Element Grafiken bereitzustellen, kann der [**CBS \_**](combo-box-styles.md) -Besitzer von "Besitzer" nicht verwendet werden.

Ein ComboBoxEx-Steuerelement muss initialisiert werden, indem die [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) -Funktion aufgerufen wird, wobei die "ICC \_ userex"- \_ Klassen in der zugehörigen [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) -Struktur angegeben werden.

Sie können ein ComboBoxEx-Steuerelement erstellen, indem Sie die Funktion "up- [**windowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " verwenden und " [**WC \_ ComboBoxEx**](common-control-window-classes.md) " als Fenster Klasse angeben. Die-Klasse wird registriert, wenn die [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) -Funktion aufgerufen wird, wie oben erläutert.

ComboBoxEx-Steuerelemente werden ohne eine Standard Bildliste erstellt. Wenn Sie Element Bilder verwenden möchten, müssen Sie eine Bildliste für das ComboBoxEx-Steuerelement erstellen und es dem Steuerelement mithilfe der [**CBEM \_ SetImageList**](cbem-setimagelist.md) -Nachricht zuweisen. Wenn Sie dem ComboBoxEx-Steuerelement keine Bildliste zuweisen, zeigt das Steuerelement nur Element Text an.

## <a name="comboboxex-control-styles"></a>ComboBoxEx-Steuerelement Stile

ComboBoxEx-Steuerelemente unterstützen nur die folgenden ComboBox-Stile:

-   CBS \_ Simple
-   CBS- \_ Dropdown
-   CBS- \_ Dropdown Liste
-   untergeordnetes Element \_

Es gibt auch mehrere [erweiterbare Stile des ComboBoxEx-Steuer](comboboxex-control-extended-styles.md) Elements, die nur von ComboBoxEx verwendet werden.

> [!Note]  
> Der [**\_ einfache CBS**](combo-box-styles.md) -Stil funktioniert in einigen Fällen möglicherweise nicht ordnungsgemäß.

 

Da das ComboBoxEx-Steuerelement auf der Grundlage einer zugewiesenen Bildliste für Sie Besitzer zeichnen-Aufgaben ausführt, wird der " [**CBS Owner \_ drawfixed**](combo-box-styles.md) "-Stil impliziert; Sie müssen ihn bei der Erstellung des Steuer Elements nicht verwenden. Da Bildlisten verwendet werden, um Element Grafiken bereitzustellen, kann der [**CBS \_**](combo-box-styles.md) -Besitzer von "Besitzer" nicht verwendet werden. Das ComboBoxEx-Steuerelement unterstützt auch das [ComboBoxEx](comboboxex-control-extended-styles.md) -Steuerelement erweiterte Stile, die zusätzliche Funktionen bereitstellen.

## <a name="comboboxex-control-items"></a>ComboBoxEx-Steuerelement Elemente

ComboBoxEx-Steuerelemente verwalten Element Informationen mithilfe einer [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) -Struktur. Diese Struktur schließt Elemente für Element Indizes, Bild Indizes (normal, Auswahl Zustand und Overlay), Einzugs Werte, Text Zeichenfolgen und Element spezifische Werte ein.

Das ComboBoxEx-Steuerelement ermöglicht den einfachen Zugriff auf und die Bearbeitung von Elementen über Messaging. Um ein Element hinzuzufügen oder zu löschen, senden Sie die Nachricht [**CBEM \_ InsertItem**](cbem-insertitem.md) oder [**CBEM \_ DeleteItem**](cbem-deleteitem.md) . Sie können Elemente, die sich derzeit im Steuerelement befinden, mithilfe der [**CBEM \_ -Nachricht "CBEM**](cbem-setitem.md) " ändern.

## <a name="callback-items"></a>Rückruf Elemente

ComboBoxEx-Steuerelemente unterstützen Rückruf Element Attribute. Sie können ein Element als Rückruf Element angeben, wenn Sie es mithilfe von [**CBEM \_ InsertItem**](cbem-insertitem.md)dem Steuerelement hinzufügen. Wenn Sie der [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) -Struktur eines Elements Werte zuweisen, müssen Sie die entsprechenden Rückruf Flagwerte angeben. Folgendes sind **COMBOBOXEXITEM** -Strukturmember und ihre entsprechenden Rückruf Kennzeichen-Werte.



| Member             | Rückruf Wert      |
|--------------------|---------------------|
| **Member pszText**        | LPSTR- \_ textcallback |
| **iImage**         | I \_ imagecallback    |
| **iSelectedImage** | I \_ imagecallback    |
| **IOverlay**       | I \_ imagecallback    |
| **iIndent**        | I \_ Einzug Rückruf   |



 

Das-Steuerelement fordert Informationen zu Rückruf Elementen an, indem [cben \_ getdispinfo](cben-getdispinfo.md) -Benachrichtigungs Codes gesendet werden. Diese Benachrichtigung wird in Form einer WM-Benachrichtigungs Meldung gesendet. [**\_**](wm-notify.md) Wenn die Anwendung diese Nachricht verarbeitet, muss Sie die angeforderten Informationen für das Steuerelement bereitstellen. Wenn Sie das **Mask** -Element der zugehörigen [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) -Struktur auf cbeif \_ di \_ SetItem festlegen, speichert das-Steuerelement die Elementdaten und fordert Sie nicht erneut an.

## <a name="comboboxex-control-image-lists"></a>Bildlisten des ComboBoxEx-Steuer Elements

Wenn Sie möchten, dass ein ComboBoxEx-Steuerelement Symbole mit Elementen anzeigt, müssen Sie eine Bildliste bereitstellen. ComboBoxEx-Steuerelemente unterstützen bis zu drei Bilder für ein Element – eine für den ausgewählten Zustand, eine für den nicht ausgewählten Zustand und eine für ein Überlagerungs Bild. Weisen Sie mithilfe der [**CBEM \_ SetImageList**](cbem-setimagelist.md) -Nachricht eine vorhandene Bildliste einem ComboBoxEx-Steuerelement zu.

Die [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) -Struktur enthält Elemente, die die Bild Indizes für jede Bildliste darstellen (ausgewählt, nicht ausgewählt und überlagern). Legen Sie für jedes Element diese Member fest, um die gewünschten Bilder anzuzeigen. Es ist nicht erforderlich, für jeden Bildtyp Bild Indizes anzugeben. Sie können Bild Typen beliebig kombinieren, aber immer den **Mask** -Member der **COMBOBOXEXITEM** -Struktur festlegen, um anzugeben, welche Member verwendet werden. Das-Steuerelement ignoriert Member, die nicht als gültig gekennzeichnet wurden.

> [!Note]  
> Wenn Sie den [**\_ einfachen CBS**](combo-box-styles.md) -Stil verwenden, werden keine Symbole angezeigt.

 

## <a name="about-comboboxex-control-notification-messages"></a>Informationen zu ComboBoxEx-Steuerelement Benachrichtigungs Meldungen

Ein ComboBoxEx-Steuerelement sendet Benachrichtigungs Meldungen, um Änderungen in sich selbst zu melden oder Rückruf Element Informationen anzufordern. Das übergeordnete Element des-Steuer Elements empfängt alle [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldungen aus dem Kombinations Feld, das im ComboBoxEx-Steuerelement enthalten ist. Das ComboBoxEx-Steuerelement sendet seine eigenen Benachrichtigungen mithilfe von [**WM- \_ Benachrichtigungs**](wm-notify.md) Nachrichten. Folglich muss der Besitzer des Steuer Elements darauf vorbereitet sein, beide Formen von Benachrichtigungs Meldungen zu verarbeiten.

Im folgenden finden Sie die ComboBoxEx-spezifischen Benachrichtigungs Codes, die über die WM-Benachrichtigungs Nachrichten gesendet werden. [**\_**](wm-notify.md)



| Benachrichtigung                              | **Beschreibung**                                                                                                            |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [cben \_ BeginEdit](cben-beginedit.md)     | Signalisiert, dass der Benutzer die Dropdown Liste aktiviert hat oder auf das Bearbeitungsfeld des Steuer Elements geklickt hat.                               |
| [cben \_ EndEdit](cben-endedit.md)         | Signalisiert, dass der Benutzer ein Element aus der Dropdown Liste ausgewählt hat oder einen Bearbeitungsvorgang innerhalb des Bearbeitungs Felds abgeschlossen hat. |
| [cben \_ DeleteItem](cben-deleteitem.md)   | Meldet, dass ein Element gelöscht wurde.                                                                                          |
| [cben \_ getdispinfo](cben-getdispinfo.md) | Fordert Informationen zu den Attributen eines Elements an.                                                                           |
| [cben \_ InsertItem](cben-insertitem.md)   | Signalisiert, dass ein Element in das Steuerelement eingefügt wurde.                                                                          |



 

## <a name="comboboxex-control-message-forwarding"></a>Nachrichten Weiterleitung durch ComboBoxEx-Steuerelement

Im folgenden finden Sie die standardmäßigen Kombinations Feld Meldungen, die ein ComboBoxEx-Steuerelement an das untergeordnete Kombinations Feld weiterleitet. Einige dieser Nachrichten können vom ComboBoxEx-Steuerelement entweder vor oder nach der Weiterleitung der Nachricht verarbeitet werden.

-   [**CB \_ deletestring**](cb-deletestring.md)
-   [**CB- \_ FindStringExact**](cb-findstringexact.md)
-   [**CB- \_ GetCount**](cb-getcount.md)
-   [**CB \_ getcurrsel**](cb-getcursel.md)
-   [**CB \_ getdroppedcontrolrect**](cb-getdroppedcontrolrect.md)
-   [**CB \_ getdroppedstate**](cb-getdroppedstate.md)
-   [**CB \_ GetItemData**](cb-getitemdata.md)
-   [**CB- \_ GetItemHeight**](cb-getitemheight.md)
-   [**CB \_ getlbtext**](cb-getlbtext.md)
-   [**CB \_ getlbtextlen**](cb-getlbtextlen.md)
-   [**CB \_ getextendedui**](cb-getextendedui.md)
-   [**CB- \_ limittext**](cb-limittext.md)
-   [**CB \_ resetcontent**](cb-resetcontent.md)
-   [**CB \_ setcurrsel**](cb-setcursel.md)
-   [**CB \_ setdroppeer-DTH**](cb-setdroppedwidth.md)
-   [**CB- \_ textendedui**](cb-setextendedui.md)
-   [**CB- \_ Daten**](cb-setitemdata.md)
-   [**CB- \_ sitztemheight**](cb-setitemheight.md)
-   [**CB- \_ ShowDropDown**](cb-showdropdown.md)

Die folgenden Windows-Meldungen werden von einem ComboBoxEx-Steuerelement an das übergeordnete Fenster weitergeleitet:

-   [**WM \_ (Dies**](/windows/desktop/menurc/wm-command) schließt alle CBN-Benachrichtigungen ein \_ .)
-   [**WM- \_ Benachrichtigung**](wm-notify.md)

 

 