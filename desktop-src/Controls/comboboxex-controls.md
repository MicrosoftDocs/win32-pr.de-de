---
title: Informationen zu ComboBoxEx-Steuerelementen
description: ComboBoxEx-Steuerelemente sind Kombinationsfeld-Steuerelemente, die native Unterstützung für Elementbilder bereitstellen.
ms.assetid: a4b1aa79-40c4-4eff-801c-4f308d86fb35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993fa8db73246c62f8ceee805e767c13ffdcc15a12d0222e09f308324cc97bab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831836"
---
# <a name="about-comboboxex-controls"></a>Informationen zu ComboBoxEx-Steuerelementen

ComboBoxEx-Steuerelemente sind Kombinationsfeld-Steuerelemente, die native Unterstützung für Elementbilder bereitstellen. Damit Elementbilder leicht zugänglich sind, bietet das Steuerelement Unterstützung für Bildlisten. Mit diesem Steuerelement können Sie die Funktionalität eines Kombinationsfelds bereitstellen, ohne Elementgrafiken manuell zeichnen zu müssen.

Dieses Thema enthält folgende Abschnitte:

-   [Erstellen von ComboBoxEx-Steuerelementen](#creating-comboboxex-controls)
-   [ComboBoxEx-Steuerelementstile](#comboboxex-control-styles)
-   [ComboBoxEx-Steuerelementelemente](#comboboxex-control-items)
-   [Rückrufelemente](#callback-items)
-   [Bildlisten des ComboBoxEx-Steuerelements](#comboboxex-control-image-lists)
-   [Informationen zu ComboBoxEx-Steuerelementbenachrichtigungsmeldungen](#about-comboboxex-control-notification-messages)
-   [ComboBoxEx-Steuerungsnachrichtenweiterleitung](#comboboxex-control-message-forwarding)

## <a name="creating-comboboxex-controls"></a>Erstellen von ComboBoxEx-Steuerelementen

Effektiv erstellt ein ComboBoxEx-Steuerelement ein untergeordnetes Kombinationsfeld und führt Aufgaben zum Zeichnen des Besitzers für Sie basierend auf einer zugewiesenen Bildliste aus. Daher wird der [**CBS \_ OWNERDRAWFIXED-Stil**](combo-box-styles.md) impliziert, und es ist nicht erforderlich, ihn beim Erstellen des Steuerelements zu verwenden. Da Bildlisten zum Bereitstellen von Elementgrafiken verwendet werden, kann [**der CBS \_ OWNERDRAWVARIABLE-Stil**](combo-box-styles.md) nicht verwendet werden.

Ein ComboBoxEx-Steuerelement muss initialisiert werden, indem die [**InitCommonControlsEx-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) aufruft und DABEI INITCOMMONCONTROLSEX CLASSES in der zugehörigen \_ \_ [**INITCOMMONCONTROLSEX-Struktur angegeben**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) wird.

Sie können ein ComboBoxEx-Steuerelement erstellen, indem Sie die [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) verwenden und [**WC \_ COMBOBOXEX**](common-control-window-classes.md) als Fensterklasse angeben. Die -Klasse wird registriert, wenn [**die InitCommonControlsEx-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) wie oben beschrieben aufgerufen wird.

ComboBoxEx-Steuerelemente werden ohne Standardbildliste erstellt. Um Elementbilder zu verwenden, müssen Sie eine Bildliste für das ComboBoxEx-Steuerelement erstellen und dem Steuerelement mithilfe der [**CBEM \_ SETIMAGELIST-Nachricht**](cbem-setimagelist.md) zuweisen. Wenn Sie dem ComboBoxEx-Steuerelement keine Bildliste zuweisen, zeigt das Steuerelement nur Elementtext an.

## <a name="comboboxex-control-styles"></a>ComboBoxEx-Steuerelementstile

ComboBoxEx-Steuerelemente unterstützen nur die folgenden ComboBox-Stile:

-   CBS \_ SIMPLE
-   \_CBS-DROPDOWNLISTE
-   \_CBS-DROPDOWNLISTE
-   WS \_ CHILD

Es gibt auch mehrere [erweiterte ComboBoxEx-Steuerelementstile,](comboboxex-control-extended-styles.md) die nur von ComboBoxEx verwendet werden.

> [!Note]  
> Der [**CBS \_ SIMPLE-Stil**](combo-box-styles.md) funktioniert in einigen Fällen möglicherweise nicht ordnungsgemäß.

 

Da das ComboBoxEx-Steuerelement Besitzerzeichnungsaufgaben für Sie basierend auf einer zugewiesenen Bildliste ausführt, wird der [**CBS \_ OWNERDRAWFIXED-Stil**](combo-box-styles.md) impliziert. Sie müssen ihn beim Erstellen des Steuerelements nicht verwenden. Da Bildlisten zum Bereitstellen von Elementgrafiken verwendet werden, kann [**der CBS \_ OWNERDRAWVARIABLE-Stil**](combo-box-styles.md) nicht verwendet werden. Das ComboBoxEx-Steuerelement unterstützt auch [erweiterte ComboBoxEx-Steuerelementstile,](comboboxex-control-extended-styles.md) die zusätzliche Funktionen bereitstellen.

## <a name="comboboxex-control-items"></a>ComboBoxEx-Steuerelementelemente

ComboBoxEx-Steuerelemente verwalten Elementinformationen mithilfe einer [**COMBOBOXEXITEM-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) Diese Struktur umfasst Member für Elementindizes, Bildindizes (normal, Auswahlzustand und Überlagerung), Einzugswerte, Textzeichenfolgen und elementspezifische Werte.

Das ComboBoxEx-Steuerelement ermöglicht den einfachen Zugriff auf elemente und deren Bearbeitung durch Messaging. Um ein Element hinzuzufügen oder zu löschen, senden Sie die [**CBEM \_ INSERTITEM-**](cbem-insertitem.md) oder [**CBEM \_ DELETEITEM-Nachricht.**](cbem-deleteitem.md) Sie können elemente, die sich derzeit im -Steuerelement befindet, mithilfe der [**CBEM \_ SETITEM-Nachricht**](cbem-setitem.md) ändern.

## <a name="callback-items"></a>Rückrufelemente

ComboBoxEx-Steuerelemente unterstützen Rückrufelementattribute. Sie können ein Element als Rückrufelement angeben, wenn Sie es dem Steuerelement mit [**CBEM \_ INSERTITEM hinzufügen.**](cbem-insertitem.md) Wenn Sie der [**COMBOBOXEXITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) eines Elements Werte zuweisen, müssen Sie die entsprechenden Rückrufflagwerte angeben. Im Folgenden finden Sie **COMBOBOXEXITEM-Strukturmitglieder** und die entsprechenden Rückrufflagwerte.



| Member             | Rückrufwert      |
|--------------------|---------------------|
| **pszText**        | LPSTR \_ TEXTCALLBACK |
| **iImage**         | I \_ IMAGECALLBACK    |
| **iSelectedImage** | I \_ IMAGECALLBACK    |
| **iOverlay**       | I \_ IMAGECALLBACK    |
| **iIndent**        | I \_ INDENTCALLBACK   |



 

Das Steuerelement fordert Informationen zu Rückrufelementen an, indem [es CBEN \_ GETDISPINFO-Benachrichtigungscodes](cben-getdispinfo.md) sendet. Diese Benachrichtigung wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. Wenn Ihre Anwendung diese Nachricht verarbeitet, muss sie die angeforderten Informationen für das Steuerelement bereitstellen. Wenn Sie den **Maskenelement** der zugehörigen [**COMBOBOXEXITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) auf CBEIF \_ DI SETITEM festlegen, werden die Elementdaten vom Steuerelement gespeichert und nicht \_ erneut anfordern.

## <a name="comboboxex-control-image-lists"></a>Bildlisten des ComboBoxEx-Steuerelements

Wenn ein ComboBoxEx-Steuerelement Symbole mit Elementen anzeigen soll, müssen Sie eine Bildliste bereitstellen. ComboBoxEx-Steuerelemente unterstützen bis zu drei Bilder für ein Element – eines für den ausgewählten Zustand, eines für den nicht ausgewählten Zustand und eines für ein Überlagerungsbild. Weisen Sie einem ComboBoxEx-Steuerelement mithilfe der [**CBEM \_ SETIMAGELIST-Nachricht eine**](cbem-setimagelist.md) vorhandene Bildliste zu.

Die [**COMBOBOXEXITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) enthält Member, die die Bildindizes für jede Bildliste darstellen (ausgewählt, nicht ausgewählt und Überlagerung). Legen Sie für jedes Element diese Elemente so fest, dass die gewünschten Bilder angezeigt werden. Es ist nicht erforderlich, Bildindizes für jeden Imagetyp anzugeben. Sie können Bildtypen nach Be willen mischen  und ab suchen, aber immer den Masken-Member der **COMBOBOXEXITEM-Struktur** festlegen, um anzugeben, welche Member verwendet werden. Das -Steuerelement ignoriert Member, die nicht als gültig gekennzeichnet wurden.

> [!Note]  
> Wenn Sie den [**CBS \_ SIMPLE-Stil**](combo-box-styles.md) verwenden, werden keine Symbole angezeigt.

 

## <a name="about-comboboxex-control-notification-messages"></a>Informationen zu ComboBoxEx-Steuerelementbenachrichtigungsmeldungen

Ein ComboBoxEx-Steuerelement sendet Benachrichtigungsmeldungen, um Änderungen an sich selbst zu melden oder Rückrufelementinformationen an anforderungsaufgerufen. Das übergeordnete Element des Steuerelements empfängt alle [**WM \_ COMMAND-Meldungen**](/windows/desktop/menurc/wm-command) aus dem Kombinationsfeld, das im ComboBoxEx-Steuerelement enthalten ist. Das ComboBoxEx-Steuerelement sendet seine eigenen Benachrichtigungen mithilfe von [**WM \_ NOTIFY-Nachrichten.**](wm-notify.md) Daher muss der Besitzer des Steuerelements darauf vorbereitet sein, beide Formen von Benachrichtigungsmeldungen zu verarbeiten.

Im Folgenden finden Sie die ComboBoxEx-spezifischen Benachrichtigungscodes, die über [**WM \_ NOTIFY-Nachrichten gesendet**](wm-notify.md) werden.



| Benachrichtigung                              | **Beschreibung**                                                                                                            |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [CBEN \_ BEGINEDIT](cben-beginedit.md)     | Signalisiert, dass der Benutzer die Dropdownliste aktiviert oder auf das Bearbeitungsfeld des Steuerelements geklickt hat.                               |
| [CBEN \_ ENDEDIT](cben-endedit.md)         | Signalisiert, dass der Benutzer ein Element aus der Dropdownliste ausgewählt oder einen Bearbeitungsvorgang innerhalb des Bearbeitungsfelds abgeschlossen hat. |
| [CBEN \_ DELETEITEM](cben-deleteitem.md)   | Meldet, dass ein Element gelöscht wurde.                                                                                          |
| [CBEN \_ GETDISPINFO](cben-getdispinfo.md) | Fordert Informationen zu den Attributen eines Elements an.                                                                           |
| [CBEN \_ INSERTITEM](cben-insertitem.md)   | Signalisiert, dass ein Element in das Steuerelement eingefügt wurde.                                                                          |



 

## <a name="comboboxex-control-message-forwarding"></a>ComboBoxEx-Steuerungsnachrichtenweiterleitung

Im Folgenden finden Sie die Standard-Kombinationsfeldmeldungen, die ein ComboBoxEx-Steuerelement an das untergeordnete Kombinationsfeld weiterleiten. Einige dieser Nachrichten können vom ComboBoxEx-Steuerelement verarbeitet werden, bevor oder nachdem die Nachricht weitergeleitet wurde.

-   [**CB \_ DELETESTRING**](cb-deletestring.md)
-   [**CB \_ FINDSTRINGEXACT**](cb-findstringexact.md)
-   [**CB \_ GETCOUNT**](cb-getcount.md)
-   [**CB \_ GETCURSEL**](cb-getcursel.md)
-   [**CB \_ GETDROPPEDCONTROLRECT**](cb-getdroppedcontrolrect.md)
-   [**CB \_ GETDROPPEDSTATE**](cb-getdroppedstate.md)
-   [**CB \_ GETITEMDATA**](cb-getitemdata.md)
-   [**CB \_ GETITEMHEIGHT**](cb-getitemheight.md)
-   [**CB \_ GETLBTEXT**](cb-getlbtext.md)
-   [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md)
-   [**CB \_ GETEXTENDEDUI**](cb-getextendedui.md)
-   [**CB \_ LIMITTEXT**](cb-limittext.md)
-   [**CB \_ RESETCONTENT**](cb-resetcontent.md)
-   [**CB \_ SETCURSEL**](cb-setcursel.md)
-   [**CB \_ SETDROPPEDWIDTH**](cb-setdroppedwidth.md)
-   [**CB \_ SETEXTENDEDUI**](cb-setextendedui.md)
-   [**CB \_ SETITEMDATA**](cb-setitemdata.md)
-   [**CB \_ SETITEMHEIGHT**](cb-setitemheight.md)
-   [**CB \_ SHOWDROPDOWN**](cb-showdropdown.md)

Im Folgenden sind die Windows-Meldungen aufgeführt, die ein ComboBoxEx-Steuerelement an das übergeordnete Fenster weiterleitet:

-   [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) (Dies schließt alle \_ CBN-Benachrichtigungen ein.)
-   [**WM \_ NOTIFY**](wm-notify.md)

 

 