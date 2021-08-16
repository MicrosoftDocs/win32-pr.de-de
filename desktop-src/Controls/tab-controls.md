---
title: Informationen zu Registerkartensteuerelementen
description: Ein Registerkarten-Steuerelement entspricht in etwa einem Trennblatt in einem Notizbuch den Beschriftungen in einer Hängeregistratur. Durch Verwenden eines Registerkarten-Steuerelements können in einer Anwendung mehrere Seiten für denselben Bereich in einem Fenster oder Dialogfeld definiert werden.
ms.assetid: 55ed2863-7f8d-43ce-a0f9-6f6d41e3f947
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 512955ec2b3426227366ef109669c52a6c07c8882374d935023123182de194ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670424"
---
# <a name="about-tab-controls"></a>Informationen zu Registerkartensteuerelementen

Ein Registerkarten-Steuerelement entspricht in etwa einem Trennblatt in einem Notizbuch den Beschriftungen in einer Hängeregistratur. Durch Verwenden eines Registerkarten-Steuerelements können in einer Anwendung mehrere Seiten für denselben Bereich in einem Fenster oder Dialogfeld definiert werden. Jede Seite besteht aus einer bestimmten Art von Informationen oder einer Gruppe von Steuerelementen, die die Anwendung anzeigt, wenn der Benutzer die entsprechende Registerkarte auswählt.

Der folgende Screenshot zeigt ein einfaches Registerkarten-Steuerelement, das Registerkarten für Wochentage enthält. Die Registerkarte Dienstag wurde ausgewählt.

![Screenshot eines Eigenschaftenblatts mit fünf Registerkarten, eine für jeden Wochentag](images/tab-simple.png)

Das Thema enthält folgende Abschnitte:

-   [Erstellen von Registerkartensteuerelementen](#creating-tab-controls)
-   [Registerkarten-Steuerelementstile](#tab-control-styles)
-   [Registerkarten und Registerkartenattribute](#tabs-and-tab-attributes)
-   [Anzeigebereich](#display-area)
-   [Registerkartenauswahl](#tab-selection)
-   [Registerkarten-Steuerelement – Bildlisten](#tab-control-image-lists)
-   [Registerkartengröße und -position](#tab-size-and-position)
-   [Vom Besitzer gezeichnete Registerkarten](#owner-drawn-tabs)
-   [QuickInfos für Das Registerkartensteuerprogramm](#tab-control-tooltips)
-   [Standard-Registerkarten-Steuerelement Nachrichtenverarbeitung](#default-tab-control-message-processing)

## <a name="creating-tab-controls"></a>Erstellen von Registerkartensteuerelementen

Sie können ein Registerkarten-Steuerelement erstellen, indem Sie die [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) aufrufen und die [**Fensterklasse WC \_ TABCONTROL**](common-control-window-classes.md) angeben. Diese Fensterklasse wird registriert, wenn die ALLGEMEINE STEUERELEMENT-DLL geladen wird. Um sicherzustellen, dass die DLL geladen wird, verwenden Sie die [**InitCommonControlsEx-Funktion.**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex)

In Microsoft Visual Studio können Sie mithilfe der Toolbox ein Registerkartensteuerelement erstellen.

Sie senden Nachrichten an ein Registerkarten-Steuerelement, um Registerkarten hinzuzufügen, und wirken sich andernfalls auf die Darstellung und das Verhalten des Steuerelements aus. Jede Nachricht verfügt über ein entsprechendes Makro, das Sie verwenden können, anstatt die Nachricht explizit zu senden. Sie können eine einzelne Registerkarte in einem Registerkarten-Steuerelement nicht deaktivieren. Sie können jedoch ein Registerkarten-Steuerelement in einem Eigenschaftenblatt deaktivieren, indem Sie die entsprechende Seite deaktivieren.

## <a name="tab-control-styles"></a>Registerkarten-Steuerelementstile

Sie können bestimmte Merkmale auf Registerkartensteuerelemente anwenden, indem Sie Stile für Registerkartensteuerelemente angeben, wenn das Steuerelement erstellt wird. Beispielsweise können Sie die Ausrichtung und allgemeine Darstellung der Registerkarten in einem Registerkarten-Steuerelement angeben.

Sie können dazu führen, dass die Registerkarten wie Schaltflächen aussehen, indem Sie das [**\_ TCS-Schaltflächenformat**](tab-control-styles.md) angeben. Registerkarten in dieser Art von Registerkartensteuerelementen sollten die gleiche Funktion wie Schaltflächensteuerelemente erfüllen. Wenn Sie also auf eine Registerkarte klicken, sollte ein Befehl ausgeführt werden, anstatt eine Seite anzuzeigen. Da der Anzeigebereich in einem Schaltflächen-Registerkarten-Steuerelement in der Regel nicht verwendet wird, wird kein Rahmen um ihn gezeichnet.

Sie können bewirken, dass eine Registerkarte beim Klicken den Eingabefokus erhält, indem Sie den [**TCS \_ FOCUSONBUTTONDOWN-Stil**](tab-control-styles.md) angeben. Dieser Stil wird in der Regel nur mit dem [**TCS \_ BUTTONS-Stil**](tab-control-styles.md) verwendet. Sie können angeben, dass eine Registerkarte beim Klicken keinen Eingabefokus erhält, indem Sie [**das FORMAT TCS \_ FOCUSNEVER**](tab-control-styles.md) verwenden.

Standardmäßig zeigt ein Registerkarten-Steuerelement nur eine Zeile mit Registerkarten an. Wenn nicht alle Registerkarten gleichzeitig angezeigt werden können, zeigt das Registerkarten-Steuerelement ein Nach-unten-Steuerelement an, damit der Benutzer weitere Registerkarten in die Ansicht scrollen kann. Sie können dazu führen, dass ein Registerkarten-Steuerelement bei Bedarf mehrere Zeilen mit Registerkarten zeigt, indem Sie den [**TCS \_ MULTILINE-Stil**](tab-control-styles.md) angeben. Mit diesem Stil können alle Registerkarten gleichzeitig angezeigt werden. Die Registerkarten werden innerhalb jeder Zeile linksbündig ausgerichtet, es sei denn, Sie geben den [**STIL TCS \_ RIGHTJUSTIFY**](tab-control-styles.md) an. In diesem Fall wird die Breite jeder Registerkarte erhöht, sodass jede Zeile mit Registerkarten die gesamte Breite des Registerkarten-Steuerelements ausfüllt.

Ein Registerkarten-Steuerelement passt automatisch die Größe jeder Registerkarte an ihr Symbol (sofern verfügbar) und die Bezeichnung an. Um allen Registerkarten die gleiche Breite zu geben, können Sie das [**TCS \_ FIXEDWIDTH-Format**](tab-control-styles.md) angeben. Das Steuerelement passt die Größe aller Registerkarten an die breiteste Bezeichnung an, oder Sie können mithilfe der [**\_ TCM-Meldung SETITEMSIZE**](tcm-setitemsize.md) eine bestimmte Breite und Höhe zuweisen. Auf jeder Registerkarte centert das Steuerelement das Symbol und die Bezeichnung und platziert das Symbol links neben der Bezeichnung. Sie können das Symbol auf der linken Seite erzwingen und die Bezeichnung zentriert lassen, indem Sie den [**TCS \_ FORCEICONLEFT-Stil**](tab-control-styles.md) angeben. Sie können sowohl das Symbol als auch die Bezeichnung mithilfe des [**TCS \_ FORCELABELLEFT-Stils**](tab-control-styles.md) nach links ausrichten. Sie können den **TCS \_ FIXEDWIDTH-Stil** nicht mit [**dem TCS \_ RIGHTJUSTIFY-Stil**](tab-control-styles.md) verwenden.

Sie können angeben, dass das übergeordnete Fenster die Registerkarten im Steuerelement zeichnet, indem Sie das [**TCS \_ OWNERDRAWFIXED-Format**](tab-control-styles.md) verwenden. Weitere Informationen finden Sie unter [Owner-Drawn Tabs](#owner-drawn-tabs).

Sie können angeben, dass ein Registerkarten-Steuerelement ein QuickInfo-Steuerelement mithilfe des [**TCS-QuickInfos-Stils \_ erstellt.**](tab-control-styles.md) Weitere Informationen hierzu finden Sie unter [QuickInfos für die Registerkartensteuerung.](#tab-control-tooltips)

## <a name="tabs-and-tab-attributes"></a>Registerkarten und Registerkartenattribute

Jede Registerkarte in einem Registerkarten-Steuerelement besteht aus einem Symbol, einer Bezeichnung und anwendungsdefinierten Daten. Diese Informationen werden von einer [**T VERDRM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tcitema) angegeben. Sie können einem Registerkarten-Steuerelement Registerkarten hinzufügen, die Anzahl der Registerkarten abrufen, den Inhalt einer Registerkarte abrufen und festlegen und Registerkarten löschen. Registerkarten werden durch ihren nullbasierten Index identifiziert.

Verwenden Sie zum Hinzufügen von Registerkarten zu einem Registerkartensteuerelement die [**TCM \_ INSERTITEM-Meldung,**](tcm-insertitem.md) und geben Sie dabei die Position des Elements und die Adresse einer [**TULATORM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tcitema) an. Sie können den Inhalt einer vorhandenen Registerkarte mithilfe der [**TCM \_ GETITEM-**](tcm-getitem.md) und [**TCM \_ SETITEM-Meldungen**](tcm-setitem.md) abrufen und festlegen. Für jede Registerkarte können Sie ein Symbol, eine Bezeichnung oder beides angeben. Sie können auch anwendungsdefinierte Daten angeben, die der Registerkarte zugeordnet werden.

Sie können die aktuelle Anzahl von Registerkarten abrufen, indem Sie die [**TCM \_ GETITEMCOUNT-Nachricht**](tcm-getitemcount.md) verwenden, eine Registerkarte mithilfe der [**TCM \_ DELETEITEM-Meldung**](tcm-deleteitem.md) löschen und alle Registerkarten in einem Registerkarten-Steuerelement löschen, indem Sie die [**TCM \_ DELETEALLITEMS-Meldung**](tcm-deleteallitems.md) verwenden.

Sie können jeder Registerkarte anwendungsdefinierte Daten zuordnen. Beispielsweise können Sie Informationen zu jeder Seite mit der entsprechenden Registerkarte speichern. Standardmäßig ordnet ein Registerkarten-Steuerelement vier zusätzliche Bytes pro Registerkarte für anwendungsdefinierte Daten zu. Sie können die Anzahl zusätzlicher Bytes pro Registerkarte ändern, indem Sie die [**\_ TCM-Nachricht SETITEMEXTRA**](tcm-setitemextra.md) verwenden. Sie können diese Meldung nur verwenden, wenn das Registerkarten-Steuerelement leer ist.

Die anwendungsdefinierten Daten werden vom **lParam-Member** der [**TSTELLUNGM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tcitema) angegeben. Wenn Sie mehr als 4 Byte anwendungsdefinierter Daten verwenden, müssen Sie ihre eigene Struktur definieren und anstelle von **T VERDR verwenden.** Sie können anwendungsdefinierte Daten auf die gleiche Weise abrufen und festlegen, wie Sie andere Informationen zu einer Registerkarte abrufen und festlegen – mithilfe der [**TCM \_ GETITEM-**](tcm-getitem.md) und [**TCM \_ SETITEM-Meldungen.**](tcm-setitem.md)

Das erste Member der -Struktur muss eine [**TCALCMHEADER-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) sein, und die verbleibenden Member müssen anwendungsdefinierte Daten angeben. **TCALCMHEADER** ist identisch mit [**T VERDRM,**](/windows/win32/api/commctrl/ns-commctrl-tcitema)verfügt jedoch nicht über **den lParam-Member.** Der Unterschied zwischen der Größe Ihrer Struktur und der Größe von **TULATORMHEADER** sollte der Anzahl zusätzlicher Bytes pro Registerkarte entspricht.

## <a name="display-area"></a>Anzeigebereich

Der Anzeigebereich eines Registerkarten-Steuerelements ist der Bereich, in dem eine Anwendung die aktuelle Seite anzeigt. In der Regel erstellt eine Anwendung ein untergeordnetes Fenster oder Dialogfeld, indem die Fenstergröße und -position an den Anzeigebereich anpasst. Anhand des Fensterrechtecks für ein Registerkarten-Steuerelement können Sie das umgebundene Rechteck des Anzeigebereichs mithilfe der [**\_ TCM-Meldung ADJUSTRECT**](tcm-adjustrect.md) berechnen.

Manchmal muss der Anzeigebereich eine bestimmte Größe haben, z. B. die Größe eines nicht moduslosen untergeordneten Dialogfelds. Angesichts des umgebundenen Rechtecks für den Anzeigebereich können Sie [**TCM \_ ADJUSTRECT**](tcm-adjustrect.md) verwenden, um das entsprechende Fensterrechteck für das Registerkarten-Steuerelement zu berechnen.

## <a name="tab-selection"></a>Registerkartenauswahl

Wenn der Benutzer eine Registerkarte auswählt, sendet ein Registerkarten-Steuerelement die Benachrichtigungscodes des übergeordneten Fensters in Form von [**WM \_ NOTIFY-Nachrichten.**](wm-notify.md) Der [TCN \_ SELCHANGING-Benachrichtigungscode](tcn-selchanging.md) wird gesendet, bevor sich die Auswahl ändert, und der [TCN SELCHANGE-Benachrichtigungscode \_ ](tcn-selchange.md) wird gesendet, nachdem die Auswahl geändert wurde.

Sie können [TCN \_ SELCHANGING verarbeiten,](tcn-selchanging.md) um den Status der ausgehenden Seite zu speichern. Sie können **TRUE zurückgeben,** um zu verhindern, dass sich die Auswahl ändert. Sie möchten z. B. nicht von einem untergeordneten Dialogfeld wegwechseln, in dem ein Steuerelement eine ungültige Einstellung auf hat.

Sie müssen [TCN \_ SELCHANGE verarbeiten,](tcn-selchange.md) um die eingehende Seite im Anzeigebereich anzuzeigen. Dies kann einfach das Ändern der Informationen beinhalten, die in einem untergeordneten Fenster angezeigt werden. Häufiger besteht jede Seite aus einem untergeordneten Fenster oder Dialogfeld. In diesem Fall kann eine Anwendung diese Benachrichtigung verarbeiten, indem das ausgehende untergeordnete Fenster oder Dialogfeld zerstört oder verborgen wird und das eingehende untergeordnete Fenster oder Dialogfeld erstellt oder angezeigt wird.

Sie können die aktuelle Auswahl mithilfe der [**TCM-Meldungen \_ GETCURSEL**](tcm-getcursel.md) und [**TCM \_ SETCURSEL**](tcm-setcursel.md) abrufen und festlegen.

## <a name="tab-control-image-lists"></a>Registerkarten-Steuerelement – Bildlisten

Jeder Registerkarte kann ein Symbol zugeordnet sein, das durch einen Index in der Bildliste für das Registerkarten-Steuerelement angegeben wird. Wenn ein Registerkarten-Steuerelement erstellt wird, ist ihm keine Bildliste zugeordnet. Eine Anwendung kann mithilfe der [**ImageList \_ Create-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) eine Bildliste erstellen und sie dann mithilfe der [**\_ TCM-Nachricht SETIMAGELIST**](tcm-setimagelist.md) einem Registerkartensteuersatz zuweisen.

Sie können der Bildliste eines Registerkarten-Steuerelements Bilder wie jede andere Bildliste hinzufügen. Eine Anwendung sollte images jedoch mithilfe der [**TCM \_ REMOVEIMAGE-Meldung**](tcm-removeimage.md) anstelle der [**ImageList \_ Remove-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_remove) entfernen. Diese Meldung stellt sicher, dass jede Registerkarte dem gleichen Bild wie zuvor zugeordnet bleibt.

Das Zerstören eines Registerkarten-Steuerelements zerstört keine bildliste, die ihm zugeordnet ist. Sie müssen die Imageliste separat zerstören. Dies ist nützlich, wenn Sie mehreren Registerkartensteuerelementen dieselbe Bildliste zuweisen möchten.

Um das Handle für die Bildliste abzurufen, die derzeit einem Registerkartensteuerelement zugeordnet ist, können Sie die [**TCM \_ GETIMAGELIST-Nachricht**](tcm-getimagelist.md) verwenden.

## <a name="tab-size-and-position"></a>Registerkartengröße und -position

Jede Registerkarte in einem Registerkartensteuerelement hat eine Größe und Position. Sie können die Größe von Registerkarten festlegen, das umgrenzende Rechteck einer Registerkarte abrufen oder bestimmen, welche Registerkarte sich an einer angegebenen Position befindet.

Für Steuerelemente mit fester Breite und vom Besitzer gezeichnete Registerkarten können Sie die genaue Breite und Höhe von Registerkarten mithilfe der [**TCM \_ SETITEMSIZE-Meldung**](tcm-setitemsize.md) festlegen. In anderen Registerkartensteuerelementen wird die Größe jeder Registerkarte basierend auf dem Symbol und der Bezeichnung für die Registerkarte berechnet. Das Registerkartensteuerelement enthält Platz für einen Rahmen und einen zusätzlichen Rand. Sie können die Stärke des Rands mithilfe der [**TCM \_ SETPADDING-Nachricht**](tcm-setpadding.md) festlegen.

Sie können das aktuelle umgrenzende Rechteck für eine Registerkarte mithilfe der [**TCM \_ GETITEMRECT-Nachricht**](tcm-getitemrect.md) bestimmen. Sie können mithilfe der [**TCM \_ HITTEST-Nachricht**](tcm-hittest.md) ermitteln, welche Registerkarte sich an einem angegebenen Speicherort befindet.

In einem Registerkartensteuerelement mit dem [**TCS \_ MULTILINE-Stil**](tab-control-styles.md) können Sie die aktuelle Anzahl von Zeilen von Registerkarten mithilfe der [**TCM \_ GETROWCOUNT-Nachricht**](tcm-getrowcount.md) bestimmen.

## <a name="owner-drawn-tabs"></a>registerkarten Owner-Drawn

Wenn ein Registerkartensteuerelement über den [**TCS \_ OWNERDRAWFIXED-Stil**](tab-control-styles.md) verfügt, muss das übergeordnete Fenster Registerkarten zeichnen, indem die [**WM \_ DRAWITEM-Meldung**](wm-drawitem.md) verarbeitet wird. Das Registerkartensteuerelement sendet diese Meldung immer dann, wenn eine Registerkarte gezeichnet werden muss. Der *lParam-Parameter* gibt die Adresse einer [**DRAWITEMSTRUCT-Struktur**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) an, die den Index der Registerkarte, das umgebende Rechteck und den Gerätekontext (DC) enthält, in dem gezeichnet werden soll.

Standardmäßig enthält der **itemData-Member** von [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) den Wert des **lParam-Members** der [**TCITEM-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-tcitema) Wenn Sie jedoch die Menge der anwendungsdefinierte Daten pro Registerkarte ändern, enthält **itemData** stattdessen die Adresse der Daten. Sie können die Menge der anwendungsdefinierte Daten pro Registerkarte ändern, indem Sie die [**TCM \_ SETITEMEXTRA-Nachricht**](tcm-setitemextra.md) verwenden.

Um die Größe der Elemente in einem Registerkartensteuerelement anzugeben, muss das übergeordnete Fenster die [**WM \_ MEASUREITEM-Meldung**](wm-measureitem.md) verarbeiten. Da alle Registerkarten in einem vom Besitzer gezeichneten Registerkartensteuerelement dieselbe Größe haben, wird diese Meldung nur einmal gesendet. Es gibt kein Registerkartensteuerelementformat für vom Besitzer gezeichnete Registerkarten unterschiedlicher Größe. Sie können die Breite und Höhe von Registerkarten auch mithilfe der [**TCM \_ SETITEMSIZE-Meldung**](tcm-setitemsize.md) festlegen.

## <a name="tab-control-tooltips"></a>QuickInfos für Registerkartensteuerelement

Sie können ein QuickInfo-Steuerelement verwenden, um eine kurze Beschreibung jeder Registerkarte in einem Registerkartensteuerelement bereitzustellen. Ein Registerkartensteuerelement mit dem [**TCS \_ TOOLTIPS-Stil**](tab-control-styles.md) erstellt beim Erstellen ein QuickInfo-Steuerelement und zerstört das QuickInfo-Steuerelement, wenn es zerstört wird. Sie können auch ein QuickInfo-Steuerelement erstellen und es einem Registerkartensteuerelement zuweisen.

Wenn Sie ein QuickInfo-Steuerelement mit einem Registerkartensteuerelement verwenden, muss das übergeordnete Fenster den [TTN \_ GETDISPINFO-Benachrichtigungscode](ttn-getdispinfo.md) verarbeiten, um eine Beschreibung jeder Registerkarte auf Anforderung bereitzustellen.

Um dasselbe QuickInfo-Steuerelement mit mehreren Registerkartensteuerelement zu verwenden, erstellen Sie das QuickInfo-Steuerelement selbst, und weisen Sie es dem Registerkartensteuerelement mithilfe der [**TCM \_ SETTOOLTIPS-Meldung**](tcm-settooltips.md) zu. Sie können das Handle zum aktuellen QuickInfo-Steuerelement eines Registerkartensteuerelements abrufen, indem Sie die [**TCM \_ GETTOOLTIPS-Nachricht**](tcm-gettooltips.md) verwenden. Wenn Sie ein eigenes QuickInfo-Steuerelement erstellen, sollten Sie nicht den [**TCS \_ TOOLTIPS-Stil**](tab-control-styles.md) verwenden.

## <a name="default-tab-control-message-processing"></a>Standardmeldungsverarbeitung des Registerkartensteuerelements

In diesem Abschnitt wird die Nachrichtenverarbeitung beschrieben, die von einem Registerkartensteuerelement ausgeführt wird. Meldungen, die für Registerkartensteuerelemente spezifisch sind, werden in anderen Abschnitten dieser Dokumentation erläutert.



| `Message`                                                  | Verarbeitung erfolgt                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CAPTURECHANGED**](/windows/desktop/inputdev/wm-capturechanged) | Führt nichts aus, wenn das Registerkartensteuerelement die Mausaufnahme selbst freigegeben hat. Wenn ein anderes Fenster die Maus erfasst hat und eine Schaltfläche gedrückt gehalten wird, gibt der Befehl die Schaltfläche frei.                                                                                                                                                                                                                                                                                                                |
| [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create)                 | Ordnet eine interne Datenstruktur zu und initialisiert sie. Das Steuerelement erstellt ein QuickInfo-Steuerelement, wenn der [**TCS \_ TOOLTIPS-Stil**](tab-control-styles.md) angegeben ist.                                                                                                                                                                                                                                                                                                    |
| [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)               | Gibt während der [**WM \_ CREATE-Verarbeitung**](/windows/desktop/winmsg/wm-create) zugeordnete Ressourcen frei.                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)         | Gibt eine Kombination der WERTE DLGC \_ WANTGC UND DLGC \_ WANTCHARS zurück.                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)               | Gibt das Handle für die Schriftart zurück, die für Bezeichnungen verwendet wird.                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)               | Verarbeitet Richtungsschlüssel und ändert ggf. die Auswahl.                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus)           | Erklärt die Registerkarte, die den Fokus besitzt, für ungültig, sodass sie neu gepackt wird, um einen nicht fokussierten Zustand widerzuspiegeln.                                                                                                                                                                                                                                                                                                                                                                                      |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)       | Leitet die Nachricht ggf. an das QuickInfo-Steuerelement weiter und ändert die Auswahl, wenn der Benutzer auf eine Registerkarte klickt. Wenn der Benutzer auf eine Schaltfläche klickt, zeichnet das Steuerelement die Schaltfläche neu, um ein versenktes Aussehen zu geben, und erfasst die Maus. Wenn der Benutzer auf eine Registerkarte oder Schaltfläche klickt und der [**TCS \_ FOCUSONBUTTONDOWN-Stil**](tab-control-styles.md) angegeben ist, legt das Steuerelement den Fokus auf sich selbst fest.                                                     |
| [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)           | Gibt die Maus frei, wenn eine Schaltfläche gedrückt wurde. Wenn sich der Cursor über der Schaltfläche befindet und gedrückt gehalten wird, ändert das Steuerelement die Auswahl entsprechend und zeichnet die Schaltfläche neu.                                                                                                                                                                                                                                                                                                         |
| [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)           | Leitet die Nachricht ggf. an das QuickInfo-Steuerelement weiter. Wenn der [**TCS \_ BUTTONS-Stil**](tab-control-styles.md) angegeben ist und die Maustaste nach dem Klicken gedrückt gehalten wird, kann das Steuerelement die betroffene Schaltfläche auch neu zeichnen, um ihr eine erhöhte oder abgesenkte Darstellung zu geben.                                                                                                                                                                                            |
| [**WM \_ NOTIFY**](wm-notify.md)                          | Leitet vom QuickInfo-Steuerelement gesendete Benachrichtigungscodes weiter.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint)                            | Zeichnet einen Rahmen um den Anzeigebereich (es sei denn, der [**TCS \_ BUTTONS-Stil**](tab-control-styles.md) ist angegeben) und zeichnet alle Registerkarten, die das ungültige Rechteck überschneiden. Für jede Registerkarte zeichnet sie den Text der Registerkarte (oder sendet eine [**WM \_ DRAWITEM-Nachricht**](wm-drawitem.md) an das übergeordnete Fenster) und zeichnet dann einen Rahmen um die Registerkarte. Wenn der *wParam-Parameter* ungleich NULL ist, geht das Steuerelement davon aus, dass der Wert ein HDC ist und zeichnet mit diesem Gerätekontext. |
| [**WM \_ RBUTTONDOWN**](/windows/desktop/inputdev/wm-rbuttondown)       | Sendet einen [ \_ NM-RCLICK-Benachrichtigungscode](nm-rclick-tab.md) an das übergeordnete Fenster.                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)             | Erklärt die Registerkarte mit dem Fokus für ungültig, sodass sie neu maliert wird, um einen fokussierten Zustand widerzuspiegeln.                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)               | Legt die Schriftart fest, die für Bezeichnungen verwendet wird.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**WM \_ SETREDRAW**](/windows/desktop/gdi/wm-setredraw)                    | Legt den Zustand eines internen Flags fest, das bestimmt, ob das Steuerelement neu maliert wird, wenn Elemente eingefügt und gelöscht werden, wenn die Schriftart geändert wird usw.                                                                                                                                                                                                                                                                                                                      |
| [**\_WM-GRÖßE**](/windows/desktop/winmsg/wm-size)                     | Berechnet die Positionen von Registerkarten neu und macht möglicherweise einen Teil des Registerkartensteuerelements ungültig, um das erneute Anstrichen einiger oder aller Registerkarten zu erzwingen.                                                                                                                                                                                                                                                                                                                                                             |



 

 

 