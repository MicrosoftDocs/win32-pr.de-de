---
title: Barrierefreiheits Tools-accscope
description: Das accscope-Tool ermöglicht Entwicklern und Testern, die Barrierefreiheit Ihrer APP während der Entwicklung und des Entwurfs der APP zu evaluieren, und nicht in den Phasen, in denen der Entwicklungszeitraum einer APP verzögert ist.
ms.assetid: 7C4D78CD-CDDA-8369-B747-6224C152A997
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d057e818a0fe01ef6f219f1a03d82190d21ac14
ms.sourcegitcommit: 305298a7727a428310fa138b45a933bcd7ef2532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/25/2020
ms.locfileid: "104562455"
---
# <a name="accessibility-tools---accscope"></a>Barrierefreiheits Tools-accscope

Das **accscope** -Tool ermöglicht Entwicklern und Testern, die Barrierefreiheit Ihrer APP während der Entwicklung und des Entwurfs der APP zu evaluieren, und nicht in den Phasen, in denen der Entwicklungszeitraum einer APP verzögert ist. Tests können auch in einem frühen Stadium der Prototypphasen begonnen werden. **Accscope** kann visualisieren, wie eine Sprachausgabe die Informationen zur Benutzeroberflächenautomatisierung verfügbar macht, die eine APP bereitstellt. Darüber hinaus können Sie Bereiche anzeigen, in denen Sie Ihrer APP Informationen oder Unterstützung hinzufügen möchten, um deren Barrierefreiheit zu verbessern

> [!NOTE]
> **Accscope** ist ein Legacy Tool. Stattdessen wird die [](https://accessibilityinsights.io/) Verwendung von eingabeinsights empfohlen.

## <a name="about-accscope"></a>Informationen zu accscope

**Accscope** wird mit dem Windows Software Development Kit (SDK) installiert. Sie befindet sich im \\ Ordner "bin \\ < *Version* > \\ < *Platform* > \\ accscope" des SDK-Installations Pfads. Führen Sie das Programm AccScope.exe aus.

**Accscope** ist eine Desktop-App, keine Windows Store-App. Sie können es verwenden, um jede APP, die als Fenster angezeigt wird, einschließlich einer Desktop-App oder einer Windows Store-App, zu untersuchen.

Wenn Sie das erste Mal verwenden, müssen Sie **accscope** als Administrator ausführen, um den Sprachausgabe Modus zu aktivieren.

**Accscope** steht als Teil der Binärdateien der Barrierefreiheits Tools im Windows SDK zur Verfügung. Er wird nicht als separater Download der exe-Datei verteilt und ist in früheren sDas nicht vorhanden.

## <a name="file-menu-options"></a>Datei Menü Optionen

- Wählen Sie **Aktualisieren** aus, um alle Informationen in **accscope** zu aktualisieren, damit Sie mit dem aktuellen Zustand des Zielfensters identisch sind. Bei einer Benutzeroberfläche, die eine große Anzahl von Elementen enthält, kann dies einige Sekunden in Anspruch nehmen.
- Aktivieren oder deaktivieren Sie **Always on Top** , um das Fenster Verhalten der **accscope** -Benutzeroberfläche zu ändern. **Always on-Top** aktiviert ist die Standardeinstellung.
- Wählen Sie **Beenden** , um **accscope** zu beenden.

## <a name="view-options"></a>Anzeigen der Optionen

- Wählen Sie **Vollbild** aus, um das **accessscope** -Tool in einer Vollbildansicht auszuführen (verwenden Sie dann die Tab-Taste, um das Zielfenster anzuzeigen). Wenn sowohl **accscope** als auch die Ziel-App den Vollbildmodus ausführen, entsprechen die Platzierung, Begrenzungs Rechtecke und die allgemeine Visualisierung von Elementen zwischen Ihrer APP und der **accscope** -Ansicht.
    > [!Note]  
    > **Accscope** und sein Ziel sollten auf der gleichen Anzeige ausgeführt werden.

     

- Wählen Sie **automatisch Fokus** aus, um das Zielfenster zu aktivieren, wenn ein Benutzer den Fokus auf das Fenster (mit der Maus oder der Tastatur) verschiebt.
- Wählen Sie **automatisch aktualisieren** aus, um den **accscope** -Modus zu aktivieren, der alle 5 Sekunden alle Barrierefreiheits Daten des Zielfensters aktualisiert. Dies ist hilfreich, wenn sich die Daten der Microsoft-Benutzeroberflächen Automatisierung des Zielfensters ständig ändern.
- Wählen Sie **Live Bereiche** aus, um alle Live Bereiche hervorzuheben, die Benachrichtigungen im Zielfenster ausgeben. Ein Live Regions Ereignis, das ausgelöst wird, zeigt ein rotes Popup an, das Informationen über den aktiven Bereich enthält, einschließlich des Namens und seines "Aria-Live"-Werts (oder der äquivalente Aria-Wert für apps, die nicht direkt mit HTML, aber mit dem Live Regions Konzept in der Benutzeroberflächenautomatisierungs-Unterstützung

## <a name="element-mode"></a>Element Modus

Sie können ein Zielfenster über einen der folgenden Modi anzeigen:

- **Blatt Steuer** Element: zeigt eine Benutzeroberflächenautomatisierungs-Ansicht von Steuerelementen mit über-und untergeordneten Beziehungen an, d. h. eine Ansicht von interaktiven **Steuer** Elementen auf Blatt Ebene. Mit dieser Option können Sie überprüfen, ob alle interaktiven Steuerelemente in der Benutzeroberflächenautomatisierungs-Struktur für eine **Steuer** Element Ansicht ordnungsgemäß angezeigt werden
- **Text Muster**: zeigt sichtbare Text Bereiche der **TextPattern** -Container aus dem Zielfenster an. Verwenden Sie diese Option, um die sichtbaren Textbereiche von **TextPattern** -Elementen für die Benutzeroberflächen Automatisierung visuell darzustellen.
- Sprach **Ausgabe: zeigt** die Benutzeroberflächenautomatisierungs-Elemente, die die Sprachausgabe mithilfe der-Sprachausgabe "Element Navigation" identifizieren kann.
- **Custom Filter**: zeigt eine gefilterte Steuerelement Struktur mit einer Auswahl von Steuerelement Teilmengen an: **Schaltfläche**, **CheckBox**, **ComboBox**, **Raster**, **Hyperlink**, **Liste**, **Menü** oder **Tabelle**.

Wenn Sie die Einstellung für den **Element Modus** ändern, wird eine Aktualisierung der Visualisierung ausgelöst. Bei einer Benutzeroberfläche, die eine große Anzahl von Elementen enthält, kann dies einige Sekunden in Anspruch nehmen.

## <a name="layout-options"></a>Layoutoptionen

Sie können entweder **Visual** oder **List** als Visualisierungs Modus für das **accessscope** -Layout auswählen. In der **Visualisierung** werden die Elemente im Koordinaten Bereich in derselben Beziehung wie das Zielfenster platziert. **Auflisten** ordnet die Elemente in einer absteigenden Liste, die linksbündig ausgerichtet ist, im Fenster **accscope** und die Reihenfolge der Aktivier Reihenfolge oder der Lesefolge zu.

- Wählen Sie eine Option aus Bild **anzeigen** aus, um zu steuern, wann die einfachen Rechtecke für Bildelemente durch das tatsächliche Bild (oder einen kleinen Viewport des Bilds) ersetzt werden, da die Rechtecke häufig kleiner als das tatsächliche Bild sind. Der Standardwert ist **on Hover**, der das Bild anzeigt, wenn Sie innerhalb von **accscope** navigieren und mit der Maus auf das Rechteck für ein Bildelement zeigen. Alternative Optionen sind **immer** oder **nie**.
- Wählen Sie QuickInfo **anzeigen** aus, um grundlegende Element Informationen anzuzeigen, wenn Sie mit der Maus auf das Element in der **accscope** -Visualisierung zeigen. Wenn der **Element Modus** ein **Blatt Steuer** Element oder **Text Muster** ist, sind die in der QuickInfo angezeigten Informationen die Eigenschaften der Benutzeroberflächen Automatisierung mit der höchsten Priorität. Wenn der **Element Modus** eine Sprachausgabe ist, enthält die Info den Text **, den die** Sprachausgabe für das Element lesen würde.
- Wählen Sie **Zahlen anzeigen** aus, um Sequenznummern anzuzeigen, die die Reihenfolge der Steuerungselemente im Layout angeben. Das Zahlen Schema basiert auf der Einstellung für den **Element Modus** :
    - **Blatt Steuer** Element: die Zahlen gibt die Reihenfolge an, in der Blatt Steuerelemente in der Benutzeroberflächenautomatisierungs-Struktur angezeigt werden
    - **Text Muster**: die Zahlen geben die Reihenfolge an, in der Text Bereiche in einem Dokumentbereich angezeigt werden.
    - Sprach **Ausgabe: die** Zahl gibt die Reihenfolge an, in der die Elemente in der Element Navigation der Sprachausgabe navigiert werden.

## <a name="choosing-a-window"></a>Auswählen eines Fensters

Im **Fenster** Bezeichnung finden Sie eine Dropdown Liste, in der alle HWND-Fenster aufgelistet sind, die derzeit im System aktiv sind. Der Text für jedes Fenster, das in der Dropdown Liste angezeigt wird, ist der Fenstertitel und auch eine hexadezimale Fenster-ID in eckigen Klammern. Wählen Sie eine dieser Optionen aus, um das Zielfenster zu ändern, für das **accscope** Bericht erstattet. Sie können dasselbe Element erneut auswählen, um das gleiche Verhalten wie bei einer expliziten **Aktualisierung** zu erhalten.

## <a name="using-the-accscope-visualization"></a>Verwenden der accscope-Visualisierung

Die Abbildung unten zeigt einen Screenshot der **accscope** -Visualisierung. Dieser Screenshot zeigt das **accscope** -Tool, das das Fenster der obersten Ebene für die Beispielausgabe für die [XAML-Barrierefreiheit](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/XAML%20accessibility%20sample) anzeigt, das als APP auf dem gleichen Computer ausgeführt wird. Dieser Screenshot zeigt den Standardelement Modus des **Blatt Steuer** Elements und den **visuellen** Wert für das **Layout**.

![Screenshot der accscope-Visualisierung](images/accscopescreenshot.png)

Beachten Sie, dass diese Visualisierung die Steuerelemente im ungefähren Koordinaten Bereich darstellt, den Sie in der app sehen. Anstatt Ihnen jedoch die XAML-Visuals oder den vollständigen Text der Text Steuerelemente anzuzeigen, werden die **Name** -Eigenschaftswerte, die von jedem Steuerelement stammen, mithilfe der Benutzeroberflächen Automatisierung angezeigt.

Zusätzlich zu den zuvor beschriebenen Menü Optionen können Sie auch die folgenden Techniken verwenden:

- Klicken Sie in Visualisierungen von **Visual** oder **List** auf das Rechteck eines beliebigen Elements, um das Popup Fenster **UIA-Eigenschaften** anzuzeigen. Dies listet eine Reihe wichtiger Benutzeroberflächenautomatisierungs-Eigenschaften für dieses Element auf, einschließlich einiger der standardmäßigen [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Eigenschaften und anderer Informationen, wie z. b. Aria-Werte und eine **Anbieter Beschreibung**.
- Klicken Sie mit der rechten Maustaste auf das Rechteck eines Elements in **visuellen** oder **Listen** Visualisierungen, um ein Kontextmenü anzuzeigen, in dem die vom Element unterstützten Muster angezeigt werden. Wenn z. b. ein Element [**InvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern)unterstützt, enthält das Kontextmenü ein Element zum **aufrufen**. Wählen Sie dieses Element aus, und die entsprechende Muster-API wird in der entsprechenden app ausgeführt. **Accscope** unterstützt diese Funktion für die folgenden Muster: **aufrufen**, **ExpandCollapse**, **Umschalten**, **SelectionItem**, **ScrollItem**.
- Passen Sie den Schieberegler für **Transparenz** an, um die Deckkraft/Transparenz des Fensters **accscope** zu ändern. Standardmäßig wird es als 100%-Deckkraft angezeigt. Wenn das Fenster teilweise transparent ist, kann es hilfreich sein, die Teile des Zielfensters über die Benutzeroberfläche des **Zugriffsbereichs** zu sehen, während der **Always on oberen** Modus verwendet wird.
- Wenn Sie angezeigt werden, verwenden Sie die horizontale und vertikale Bild Lauf leisten, um den Ansichts Mittelpunkt der Visualisierung zu ändern. Dies ist hilfreich, wenn Sie die Option **visuelles** Layout verwenden, aber nicht die Option **Vollbild** -Ansicht verwenden, während das Fenster **accscope** im Vergleich zum Zielfenster klein ist.

## <a name="testing-the-narrator-scenario"></a>Testen des Sprachausgabe Szenarios

Das Sprachausgabe Szenario ist der wichtigste Aspekt bei der Verwendung von **accscope**, das speziell darauf ausgelegt ist, zu veranschaulichen, wie die einfache Navigation in der Sprachausgabe funktioniert, wenn Sie auf Ihre APP angewendet wird.

Um das Sprachausgabe Szenario zu testen, verwenden Sie diese **accscope** -Konfigurationsoptionen:

- **Element Modus**: **sprach** Ausgabe
- **Layout**: **Visualisierung**
- **Layoutoptionen** : QuickInfo **anzeigen** und **Zahlen anzeigen** beide ausgewählt

Im folgenden finden Sie einige spezifische Bereiche Ihrer APP zum Testen des Sprachausgabe Szenarios:

- **Element Reihenfolge:** Vergewissern Sie sich, dass die Reihenfolge, in der die Sprachausgabe die Steuerelemente liest, gemäß den in den Visualisierungen angezeigten Zahlen (grüne Kreise) korrekt ist. Wenn sich die Elemente nicht in der Reihenfolge befinden, in der Sie das Lesen erwarten, ändern Sie die Benutzeroberflächen Struktur der APP und die resultierende Benutzeroberflächenautomatisierungs-Struktur, und testen Sie Sie erneut, bis Sie überprüft haben, ob die Elemente in der
- **Gesprochener Text:** Bewegen Sie die Maus innerhalb der Visualisierung, und bewegen Sie den Mauszeiger über die einzelnen Element Rechtecke, um die QuickInfo für die einzelnen Elemente anzuzeigen. Im Sprachausgabe Modus zeigen die QuickInfo einen **Text** Eintrag für die Sprachausgabe an Dieser Text besteht im Allgemeinen aus dem **Namen** und dem **Steuerelement Typ**. Vergewissern Sie sich, dass es sich um die richtigen Informationen für jedes Steuerelement in der Benutzeroberfläche handelt Wenn eine der Informationen falsch ist, ändern Sie die Eigenschaften der Benutzeroberflächenautomatisierung mithilfe der Techniken, die von Ihrem speziellen UI-Framework für dies aktiviert werden. (Wenn der **Steuerungstyp** unerwartet ist, müssen Sie möglicherweise ein anderes Steuerelement verwenden, da dies häufig exklusiv durch die Steuerelemente eines Benutzeroberflächen-Frameworks gesteuert wird.) Testen Sie dann erneut, und überprüfen Sie, ob der Sprachausgabe **Text** richtig
- **Element Layout:** Überprüfen Sie jeden der folgenden Fälle:
    - Überprüfen Sie, ob redundante Elemente von der Sprachausgabe nicht verfügbar gemacht Ein Beispiel für ein redundantes Element ist das Bewertungs Steuerelement in jedem Windows Store-Kachel Element.
    - Überprüfen Sie, ob alle wichtigen Elemente (Elemente, die der Benutzer zum Ausführen wichtiger Aufgaben in der APP benötigt) in der Sprachausgabe für Sprachausgabe angezeigt werden.
    - Wenn Sie das **visuelle** Layout verwenden und ein Element fehlt, weil sich die Steuerelemente einander überlappen, wechseln Sie zum **Listen** Layout, um die Reihenfolge anzuzeigen, in der die Sprachausgabe meldet.
    - Überprüfen Sie, ob die Gesamtstruktur der Benutzeroberflächenautomatisierungs-Struktur genau und für Ihre APP erwartet wird.

## <a name="related-topics"></a>Zugehörige Themen

- [Überwachung für barrierefreie Ereignisse](accessible-event-watcher.md)
- [TestTools](testing-tools.md)
- [UI Accessibility Checker](ui-accessibility-checker.md)
- [Benutzeroberflächenautomatisierungs-Überprüfung](ui-automation-verify.md)
- [Microsoft Accessibility (Microsoft-Barrierefreiheit)](https://www.microsoft.com/accessibility/)
