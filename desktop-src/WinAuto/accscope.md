---
title: Barrierefreiheitstools – AccScope
description: Das AccScope-Tool ermöglicht Es Entwicklern und Testern, die Barrierefreiheit ihrer App während der Entwicklung und des Entwurfs der App zu bewerten, anstatt in den phasenweise späteren Tests des Entwicklungszyklus einer App.
ms.assetid: 7C4D78CD-CDDA-8369-B747-6224C152A997
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4e55aa40822b786ee69185abe753bb0bacd65345d042526a126b4c8343a2639
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327721"
---
# <a name="accessibility-tools---accscope"></a>Barrierefreiheitstools – AccScope

Das **AccScope-Tool** ermöglicht Es Entwicklern und Testern, die Barrierefreiheit ihrer App während der Entwicklung und des Entwurfs der App zu bewerten, anstatt in den phasenweise späteren Tests des Entwicklungszyklus einer App. Tests können auch in einem frühen Stadium der Prototypphasen begonnen werden. **AccScope** kann visualisieren, wie eine Sprachausgabe die Benutzeroberflächenautomatisierung Informationen verfügbar macht, die eine App bereitstellt, und Bereiche anzeigen, in denen Sie Informationen oder Unterstützung zu Ihrer App hinzufügen möchten, um ihre Barrierefreiheit zu verbessern.

> [!NOTE]
> **AccScope** ist ein Legacytool. Es wird empfohlen, stattdessen [Barrierefreiheit Insights](https://accessibilityinsights.io/) zu verwenden.

## <a name="about-accscope"></a>Informationen zu AccScope

**AccScope** wird mit dem Windows Software Development Kit (SDK) installiert. Sie befindet sich im \\ Ordner bin \\ < *version* > \\ < *platform* > \\ AccScope des SDK-Installationspfads. Führen Sie das Programm AccScope.exe aus.

**AccScope** ist eine Desktop-App, keine Windows Store App. Sie können damit eine beliebige App anzeigen, die als Fenster angezeigt wird, einschließlich einer Desktop-App oder einer Windows Store App.

Möglicherweise müssen Sie **AccScope** bei der ersten Verwendung als Administrator ausführen, um den Sprachausgabemodus zu aktivieren.

**AccScope** ist als Teil der Binärdateien der Barrierefreiheitstools im Windows SDK verfügbar. Sie wird nicht als separater Exe-Download verteilt und ist in vorherigen SDKs nicht vorhanden.

## <a name="file-menu-options"></a>Optionen im Menü "Datei"

- Wählen Sie **Aktualisieren** aus, um alle Informationen in **AccScope** entsprechend dem aktuellen Status des Zielfensters zu aktualisieren. Für eine Benutzeroberfläche, die eine große Anzahl von Elementen enthält, kann dies einige Sekunden dauern.
- Aktivieren oder deaktivieren Sie **Always On Top,** um das Fensterverhalten der **AccScope-Benutzeroberfläche** zu ändern. **Das** Aktivierte Always On Top-Kontrollkästchen ist die Standardeinstellung.
- Wählen Sie **Beenden** aus, um **AccScope** zu beenden.

## <a name="view-options"></a>Anzeigen der Optionen

- Wählen Sie **Vollbild** aus, um das **AccScope-Tool** in einer Vollbildansicht auszuführen (verwenden Sie dann tabbing, um das Zielfenster anzuzeigen). Wenn **sowohl AccScope** als auch die Ziel-App im Vollbildmodus ausgeführt werden, entspricht die Platzierung, die begrenzungsenden Rechtecke und die allgemeine Visualisierung von Elementen zwischen Ihrer App und der **AccScope-Ansicht.**
    > [!Note]  
    > **AccScope** und sein Ziel sollten auf der gleichen Anzeige ausgeführt werden.

     

- Wählen Sie **Auto Focus (Automatischer Fokus)** aus, damit AccScope das Zielfenster ändern kann, wenn ein Benutzer den Fokus auf das Fenster verschiebt (per Maus oder Tastatur).
- Wählen Sie **Automatische Aktualisierung** aus, um den **AccScope-Modus** zu aktivieren, der alle 5 Sekunden alle Barrierefreiheitsdaten des Zielfensters aktualisiert. Dies ist nützlich, wenn sich die Microsoft Benutzeroberflächenautomatisierung Daten des Zielfensters ständig ändern.
- Wählen Sie **Liveregionen aus,** um alle Liveregionen hervorzuheben, die im Zielfenster Benachrichtigungen ausstellen. Ein Livebereichsereignis, das ausgelöst wird, zeigt ein rotes Popup mit Informationen zur Liveregion an, einschließlich des Namens und des zugehörigen "aria-live"-Werts (oder des entsprechenden ARIA-Werts analog für Apps, die nicht direkt HTML verwenden, sondern das Live regions-Konzept in der Benutzeroberflächenautomatisierung-Unterstützung verwenden).

## <a name="element-mode"></a>Elementmodus

Sie können ein Zielfenster über einen der folgenden Modi anzeigen:

- **Blattsteuerelement:** Zeigt eine Benutzeroberflächenautomatisierung Ansicht von **Steuerelementelementen** mit über- und untergeordneten Beziehungen an, d. h. eine Ansicht von interaktiven Steuerelementen auf Blattebene. Verwenden Sie diese Option, um festzustellen, ob alle interaktiven Steuerelemente in der Benutzeroberflächenautomatisierung Struktur für eine **Steuerelementansicht** ordnungsgemäß angezeigt werden.
- **Textmuster:** Zeigt sichtbare Textbereiche der **TextPattern-Container** aus dem Zielfenster an. Verwenden Sie diese Option, um die sichtbaren Textbereiche von Benutzeroberflächenautomatisierung **TextPattern-Elementen** visuell darzustellen.
- **Sprachausgabe:** Zeigt die Benutzeroberflächenautomatisierung Elemente an, die die Sprachausgabe mithilfe der Metapher "Elementnavigation" der Sprachausgabe identifizieren kann.
- **Benutzerdefinierter Filter:** Zeigt eine gefilterte Steuerelementstruktur mit einer Auswahl von Steuerelementteilmengen an: **Schaltfläche,** **Kontrollkästchen,** **Kombinationsfeld,** **Raster,** **Hyperlink,** **Liste,** **Menü** oder **Tabelle.**

Wenn Sie die Einstellung **Elementmodus** ändern, wird eine Aktualisierung der Visualisierung ausgelöst. Für eine Benutzeroberfläche, die eine große Anzahl von Elementen enthält, kann dies einige Sekunden dauern.

## <a name="layout-options"></a>Layoutoptionen

Sie können entweder **Visual** oder **List** als Visualisierungsmodus für das **AccScope-Layout** auswählen. **Visual** platziert die Elemente im Koordinatenbereich in derselben Beziehung wie das Zielfenster. **List** ordnet die Elemente in einer absteigenden Liste an, die linksbündig im **AccScope-Fenster** ausgerichtet ist, und die Listenreihenfolge entspricht der Tabstopp- oder Lesereihenfolge.

- Wählen Sie unter **Bilder anzeigen** eine Option aus, um zu steuern, wann die einfachen Rechtecke für Bildelemente durch das tatsächliche Bild (oder einen kleinen Viewport dieses Bilds) ersetzt werden, da die Rechtecke häufig kleiner als das tatsächliche Bild sind. Der Standardwert ist **On Hover (Ein Hover),** der das Bild anzeigt, wenn Sie in **AccScope** navigieren und mit der Maus auf das Rechteck für ein Bildelement zeigen. Alternative Optionen sind **Always** oder **Never.**
- Wählen Sie **QuickInfo anzeigen** aus, um grundlegende Elementinformationen anzuzeigen, wenn Sie mit der Maus auf ein Element in der **AccScope-Visualisierung** zeigen. Wenn der **Elementmodus** **Blattsteuerelement** oder **Textmuster** ist, sind die in der QuickInfo angezeigten Informationen die Benutzeroberflächenautomatisierung Eigenschaften auf Elementebene mit der höchsten Priorität. Wenn der **Elementmodus** **die Sprachausgabe** ist, enthält die Information den Text, den die Sprachausgabe für das Element lesen würde.
- Wählen Sie **Zahlen anzeigen** aus, um Sequenznummern anzuzeigen, die die Renderreihenfolge des Steuerelements im Layout angeben. Das Zahlenschema basiert auf der Einstellung **Elementmodus:**
    - **Blattsteuerelement:** Die Zahlen geben die Reihenfolge an, in der Blattsteuerelemente in der Benutzeroberflächenautomatisierung-Struktur angezeigt werden.
    - **Textmuster:** Die Zahlen geben die Reihenfolge an, in der Textbereiche in einem Dokumentbereich angezeigt werden.
    - **Sprachausgabe:** Die Zahl gibt die Reihenfolge an, in der die Elemente in der Elementnavigation der Sprachausgabe navigiert werden.

## <a name="choosing-a-window"></a>Auswählen eines Fensters

Unter der Bezeichnung **Fenster** finden Sie eine Dropdownliste mit allen HWND-Fenstern, die derzeit im System aktiv sind. Der Text für jedes Fenster, das in der Dropdownliste angezeigt wird, ist der Fenstertitel und eine hexadezimale Fenster-ID in eckigen Klammern. Wählen Sie eines dieser Fenster aus, um das Zielfenster zu ändern, über das **AccScope** Berichte meldet. Sie können dasselbe Element erneut auswählen, um das gleiche Verhalten wie bei einer expliziten **Aktualisierung zu erhalten.**

## <a name="using-the-accscope-visualization"></a>Verwenden der AccScope-Visualisierung

Die folgende Abbildung zeigt einen Screenshot der **AccScope-Visualisierung.** Dieser Screenshot zeigt das **AccScope-Tool,** das das Fenster der obersten Ebene für die Beispielausgabe für [XAML-Barrierefreiheit](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/XAML%20accessibility%20sample) anzeigt und als App auf demselben Computer ausgeführt wird. Dieser Screenshot zeigt den Standardelementmodus des **Blattsteuerelements** und den **Visuellen** Wert für **Layout**.

![Screenshot der AccScope-Visualisierung](images/accscopescreenshot.png)

Beachten Sie, dass diese Visualisierung die Steuerelemente im ungefähren Koordinatenbereich darstellt, den Sie in der App sehen würden. Anstatt ihnen jedoch die XAML-Visuals oder den vollständigen Text von Textsteuerelementen zu zeigen, werden die **Name-Eigenschaftswerte** angezeigt, die aus jedem Steuerelementelement stammen, wobei Benutzeroberflächenautomatisierung verwendet wird.

Zusätzlich zu den zuvor beschriebenen Menüoptionen können Sie auch diese Techniken verwenden:

- Klicken Sie in **Visual-** oder  Listenvisualisierungen auf das Rechteck eines Elements, um ein Popupfenster für **UIA-Eigenschaften** anzuzeigen. Dies listet eine Reihe der wichtigen Benutzeroberflächenautomatisierung Eigenschaften für dieses Element auf, einschließlich einiger der [**IUIAutomationElement-Standardeigenschaften**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) und anderer Informationen wie ARIA-Werte und einer **Anbieterbeschreibung.**
- Klicken Sie mit der rechten Maustaste auf das Rechteck eines Elements in **Visual-** oder Listenvisualisierungen, um ein Kontextmenü für die Muster anzuzeigen, die das Element unterstützt.  Wenn ein Element beispielsweise [**InvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern)unterstützt, enthält das Kontextmenü ein Element für **Invoke**. Wählen Sie dieses Element aus, und die entsprechende Muster-API wird in der entsprechenden App trainiert. **AccScope** unterstützt dieses Feature für die folgenden Muster: **Invoke**, **ExpandCollapse**, **Toggle**, **SelectionItem**, **ScrollItem**.
- Passen Sie den **Schieberegler Transparenz** an, um die Deckkraft/Transparenz des **AccScope-Fensters** zu ändern. Standardmäßig wird sie als Durchlässigkeit von 100 % angezeigt. Das Fenster teilweise transparent zu machen, kann nützlich sein, um die Teile des Zielfensters über die **AccScope-Benutzeroberfläche** anzuzeigen, während sie den **Always On Top-Modus** verwenden.
- Wenn sie angezeigt werden, verwenden Sie die horizontalen und vertikalen Bildlaufleisten, um die Ansichtsmitte der Visualisierung zu ändern. Dies ist nützlich, wenn Sie die Option **Visuelles** Layout verwenden, aber nicht die **Option Vollbildansicht** verwenden, während das **AccScope-Fenster** im Vergleich zum Zielfenster klein bleibt.

## <a name="testing-the-narrator-scenario"></a>Testen des Sprachausgabeszenarios

Das Sprachausgabeszenario ist der wichtigste Aspekt, der bei der Verwendung von **AccScope** getestet werden muss. Dieses Ist speziell darauf ausgelegt, zu visualisieren, wie die grundlegende Navigation von Sprachausgabeelement funktioniert, wenn sie auf Ihre App angewendet wird.

Verwenden Sie zum Testen des  Sprachausgabeszenarios die folgenden AccScope-Konfigurationsoptionen:

- **Elementmodus:** **Sprachausgabe**
- **Layout:** **Visual**
- **Layoutoptionen:** **QuickInfo anzeigen** und **Zahlen anzeigen** beide ausgewählt

Im Folgenden finden Sie einige spezifische Bereiche Ihrer App, die sie für das Sprachausgabeszenario testen können:

- **Elementreihenfolge:** Überprüfen Sie, ob die Reihenfolge, in der die Sprachausgabe Ihre Steuerelemente liest, gemäß den zahlen (grünen Kreisen) in den Visualisierungen korrekt ist. Wenn elemente sich nicht in der Reihenfolge befinden, die Sie für das Lesen erwarten, ändern Sie die Ui-Struktur der App und die resultierende Benutzeroberflächenautomatisierung Struktur, und testen Sie erneut, bis Sie überprüft haben, ob Ihre Elemente in der erwarteten Lesereihenfolge sind.
- **Gesprochener Text:** Bewegen Sie die Maus innerhalb der Visualisierung, und zeigen Sie auf jedes der Elementrechtecke, um die QuickInfos für jedes Element anzuzeigen. Im Sprachausgabemodus zeigen die QuickInfos einen Texteintrag der **Sprachausgabe** an, der den Text darstellt, den die Sprachausgabe liest. Im Allgemeinen besteht dieser Text aus dem **Namen** und dem **Steuerelementtyp**. Vergewissern Sie sich, dass dies die richtigen Informationen für jedes Steuerelement in Der Benutzeroberfläche sind. Wenn informationen falsch sind, ändern Sie die Benutzeroberflächenautomatisierung Eigenschaften mithilfe der Techniken, die von Ihrem speziellen Benutzeroberflächenframework dafür aktiviert werden. (Wenn **der Steuerelementtyp** unerwartet ist, müssen Sie möglicherweise ein anderes Steuerelement verwenden, da dies häufig ausschließlich durch die Steuerelementimplementierungen eines Benutzeroberflächenframeworks gesteuert wird.) Testen Sie dann erneut, und überprüfen Sie, ob der Text der **Sprachausgabe** korrekt ist.
- **Elementlayout:** Überprüfen Sie jeden dieser Fälle:
    - Stellen Sie sicher, dass redundante Elemente nicht von der Sprachausgabe verfügbar gemacht werden. Ein Beispiel für ein redundantes Element ist das Ratings-Steuerelement in jedem Windows Store Kachelelement.
    - Vergewissern Sie sich, dass wichtige Elemente (Elemente, die der Benutzer benötigt, um wichtige Aufgaben in der App auszuführen) jeweils in der Navigation des Sprachausgabeelements angezeigt werden.
    - Wenn Sie das  visuelle Layout verwenden und ein Element fehlt,  da Sich-Steuerelemente überlappen, wechseln Sie zu Listenlayout, um die von der Sprachausgabe gemeldete Sequenz zu sehen.
    - Vergewissern Sie sich Benutzeroberflächenautomatisierung dass die Struktur der Struktur für Ihre App korrekt ist und erwartet wird.

## <a name="related-topics"></a>Zugehörige Themen

- [Überwachung für barrierefreie Ereignisse](accessible-event-watcher.md)
- [Testtools](testing-tools.md)
- [UI Accessibility Checker](ui-accessibility-checker.md)
- [Benutzeroberflächenautomatisierungs-Überprüfung](ui-automation-verify.md)
- [Microsoft Accessibility (Microsoft-Barrierefreiheit)](https://www.microsoft.com/accessibility/)
