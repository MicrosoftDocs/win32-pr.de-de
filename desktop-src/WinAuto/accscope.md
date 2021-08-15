---
title: Barrierefreiheitstools – AccScope
description: Mit dem AccScope-Tool können Entwickler und Tester den Zugriff auf ihre App während der Entwicklung und des Entwurfs der App bewerten, anstatt in den späteren Testphasen des Entwicklungszyklus einer App.
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

Mit **dem AccScope-Tool** können Entwickler und Tester den Zugriff auf ihre App während der Entwicklung und des Entwurfs der App bewerten, anstatt in den späteren Testphasen des Entwicklungszyklus einer App. Tests können auch in einem frühen Stadium der Prototypphasen begonnen werden. **AccScope** kann visualisieren, wie eine Sprachausgabe die Benutzeroberflächenautomatisierung von einer App zur Verfügung stellt, und Bereiche anzeigen, in denen Sie Ihrer App möglicherweise Informationen oder Unterstützung hinzufügen möchten, um die Barrierefreiheit zu verbessern.

> [!NOTE]
> **AccScope** ist ein Legacytool. Es wird empfohlen, [stattdessen Insights](https://accessibilityinsights.io/) Barrierefreiheit zu verwenden.

## <a name="about-accscope"></a>Informationen zu AccScope

**AccScope** wird mit dem Windows Software Development Kit (SDK) installiert. Sie befindet sich im Ordner \\ \\ < accScope *der Bin-Versionsplattform* > \\ <  > \\ des SDK-Installationspfads. Führen Sie das Programm AccScope.exe.

**AccScope** ist eine Desktop-App, keine Windows Store App. Sie können damit jede App anzeigen, die als Fenster angezeigt wird, einschließlich einer Desktop-App oder einer Windows Store App.

Möglicherweise müssen Sie **AccScope** bei der ersten Verwendung als Administrator ausführen, um den Sprachausgabemodus zu aktivieren.

**AccScope** ist als Teil der Binärdateien für Barrierefreiheitstools im Windows SDK verfügbar. Es wird nicht als separater EXE-Download verteilt und ist in vorherigen SDKs nicht vorhanden.

## <a name="file-menu-options"></a>Menüoptionen für Dateien

- Wählen **Sie Aktualisieren** aus, um alle Informationen in **AccScope** zu aktualisieren, damit sie mit dem aktuellen Status des Zielfensters übereinstimmen. Für eine Benutzeroberfläche, die eine große Anzahl von Elementen enthält, kann dies einige Sekunden dauern.
- Aktivieren oder deaktivieren Sie **Always On Top,** um das Fensterverhalten der **AccScope-Benutzeroberfläche zu** ändern. **Always On Top** aktiviert ist die Standardeinstellung.
- Wählen Sie **Beenden aus,** um **AccScope zu beenden.**

## <a name="view-options"></a>Anzeigen der Optionen

- Wählen **Sie Vollbild** aus, um **das AccScope-Tool** in einer Vollbildansicht ausführen zu können (und verwenden Sie dann die Tabulatoren, um das Zielfenster anzuzeigen). Wenn **sowohl AccScope** als auch die Ziel-App vollbildig ausgeführt werden, entsprechen die Platzierung, die begrenzungsgebundenen Rechtecke und die gesamte Visualisierung von Elementen zwischen Ihrer App und **der AccScope-Ansicht.**
    > [!Note]  
    > **AccScope** und sein Ziel sollten auf derselben Anzeige ausgeführt werden.

     

- Wählen **Sie Automatischer Fokus** aus, damit AccScope das Zielfenster ändern kann, wenn ein Benutzer den Fokus auf das Fenster verschiebt (per Maus oder Tastatur).
- Wählen **Sie Automatische Aktualisierung** aus, um den **AccScope-Modus** zu aktivieren, der alle 5 Sekunden alle Barrierefreiheitsdaten des Zielfensters aktualisiert. Dies ist hilfreich, wenn sich Benutzeroberflächenautomatisierung Daten des Zielfensters ständig ändern.
- Wählen **Sie Liveregionen** aus, um alle Liveregionen hervorzuheben, die Benachrichtigungen im Zielfenster senden. Ein Livebereichsereignis, das ein rotes Popup mit Informationen über den Livebereich einschließlich seines Namens und des aria-live-Werts (oder den entsprechenden ARIA-Wert analog für Apps enthält, die nicht direkt HTML verwenden, sondern das Konzept der Liveregionen in der Benutzeroberflächenautomatisierung-Unterstützung verwenden).

## <a name="element-mode"></a>Elementmodus

Sie können ein Zielfenster über einen der folgenden Modi anzeigen:

- **Blattsteuerelemente:** Zeigt eine Benutzeroberflächenautomatisierung Ansicht von **Steuerelementelementen** mit über- und untergeordneten Beziehungen an, d. h. eine Ansicht der interaktiven Steuerelemente auf Blattebene. Verwenden Sie diese Option, um zu sehen, ob alle interaktiven Steuerelemente ordnungsgemäß in der Benutzeroberflächenautomatisierung für eine **Steuerelementansicht angezeigt** werden.
- **Textmuster:** Zeigt sichtbare Textbereiche der **TextPattern-Container** aus dem Zielfenster an. Verwenden Sie diese Option, um die sichtbaren Textbereiche der **TextPattern Benutzeroberflächenautomatisierung visuell** zu darstellen.
- **Sprachausgabe:** Zeigt die Benutzeroberflächenautomatisierung, die die Sprachausgabe mithilfe der Sprachausgabemetapher "Elementnavigation" identifizieren kann.
- **Benutzerdefinierter Filter:** Zeigt eine gefilterte Steuerelementstruktur mit einer Auswahl von Steuerelementteilmengen **an:** **Schaltfläche,** **Kontrollkästchen,** Kombinationsfeld, Raster, **Link,** **Liste,** **Menü** oder **Tabelle**.

Wenn Sie die **Einstellung Elementmodus** ändern, wird eine Aktualisierung der Visualisierung ausgelöst. Für eine Benutzeroberfläche, die eine große Anzahl von Elementen enthält, kann dies einige Sekunden dauern.

## <a name="layout-options"></a>Layoutoptionen

Sie können entweder **Visual oder** **Liste** als Visualisierungsmodus für das **AccScope-Layout** auswählen. **Visual** platziert die Elemente im Koordinatenbereich in derselben Beziehung wie das Zielfenster. **List** ordnet die Elemente in einer absteigenden Liste an, die im **AccScope-Fenster** linksbündig ausgerichtet ist, und die Listen reihenfolge entspricht der Reihenfolge der Registerkarten oder der Lese reihenfolge.

- Wählen Sie  unter Bilder anzeigen eine Option aus, um zu steuern, wann die einfachen Rechtecke für Bildelemente durch das tatsächliche Bild ersetzt werden (oder einen kleinen Viewport dieses Bilds, da die Rechtecke häufig kleiner als das tatsächliche Bild sind). Der Standardwert ist **On Hover**, wodurch das Bild angezeigt wird, wenn Sie in **AccScope** navigieren und mit der Maus auf das Rechteck für ein Bildelement zeigen. Alternative Optionen sind **Immer oder** **Nie.**
- Wählen **Sie QuickInfo anzeigen aus,** um grundlegende Elementinformationen immer dann zu zeigen, wenn Sie mit dem Mauszeiger auf ein Element in der **AccScope-Visualisierung** zeigen. Wenn der **Elementmodus** **Blattsteuerelement** oder **Textmuster** ist, sind die in der QuickInfo angezeigten Informationen die Elementebene mit der höchsten Priorität Benutzeroberflächenautomatisierung Eigenschaften. Wenn der **Elementmodus die** **Sprachausgabe ist,** enthalten die Informationen den Text, den die Sprachausgabe für das Element lesen würde.
- Wählen **Sie Zahlen anzeigen aus,** um Sequenznummern anzuzeigen, die die Renderreihenfolge des Steuerelements im Layout angeben. Das Zahlenschema basiert auf der **Einstellung Elementmodus:**
    - **Blattsteuerelemente:** Die Zahlen geben die Reihenfolge an, in der Blattsteuerelemente in der Struktur Benutzeroberflächenautomatisierung werden.
    - **Textmuster:** Die Zahlen geben die Reihenfolge an, in der Textbereiche in einem Dokumentbereich angezeigt werden.
    - **Sprachausgabe:** Die Zahl gibt die Reihenfolge an, in der die Elemente in der Elementnavigation der Sprachausgabe navigiert werden.

## <a name="choosing-a-window"></a>Auswählen eines Fensters

Unter der Bezeichnung **Fenster** finden Sie eine Dropdownliste mit allen HWND-Fenstern, die derzeit im System aktiv sind. Der Text für jedes Fenster, das in der Dropdownliste angezeigt wird, ist der Fenstertitel und eine hexadezimale Fenster-ID in eckigen Klammern. Wählen Sie eine dieser Einstellungen aus, um das Zielfenster zu ändern, über das **AccScope** berichtet. Sie können dasselbe Element erneut auswählen, um das gleiche Verhalten wie bei einer expliziten **Aktualisierung zu erhalten.**

## <a name="using-the-accscope-visualization"></a>Verwenden der AccScope-Visualisierung

Die abbildung unten ist ein Screenshot der **AccScope-Visualisierung.** Dieser spezielle Screenshot zeigt das **AccScope-Tool,** das das Fenster der obersten Ebene für die [Beispielausgabe](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/XAML%20accessibility%20sample) der XAML-Barrierefreiheit anschaut und als App auf demselben Computer ausgeführt wird. Dieser Screenshot zeigt den Standardelementmodus des **Blattsteuerelements und** den **Visuellen** Wert für **Layout**.

![Screenshot der AccScope-Visualisierung](images/accscopescreenshot.png)

Beachten Sie, wie diese Visualisierung die Steuerelemente im ungefähren Koordinatenbereich darstellt, den Sie in der App sehen würden. Anstatt ihnen jedoch die XAML-Visuals oder den vollständigen Text  von Textsteuerelementen zu zeigen, werden die Name-Eigenschaftswerte angezeigt, die aus jedem Steuerelement stammen, indem Benutzeroberflächenautomatisierung.

Zusätzlich zu den zuvor beschriebenen Menüoptionen können Sie auch diese Techniken verwenden:

- Klicken Sie in visual-  oder  List-Visualisierungen auf das Rechteck eines elements, um ein **Popup mit UIA-Eigenschaften** anzuzeigen. Hier werden einige wichtige eigenschaften Benutzeroberflächenautomatisierung für dieses Element aufgeführt, darunter einige der [**IUIAutomationElement-Standardeigenschaften**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) und andere Informationen wie ARIA-Werte und eine **Anbieterbeschreibung.**
- Klicken Sie in visual- oder  List-Visualisierungen mit der rechten Maustaste auf das Rechteck eines Elements, um ein Kontextmenü für die Vom Element unterstützten Muster anzuzeigen.  Wenn ein Element beispielsweise [**InvokePattern unterstützt,**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern)enthält das Kontextmenü ein Element für **Invoke**. Wählen Sie dieses Element aus, und die entsprechende Muster-API wird in der entsprechenden App verwendet. **AccScope** unterstützt dieses Feature für die folgenden Muster: **Invoke**, **ExpandCollapse**, **Toggle**, **SelectionItem**, **ScrollItem**.
- Passen Sie den **Schieberegler** Transparenz an, um die Deckkraft/Transparenz des **AccScope-Fensters zu** ändern. Standardmäßig wird sie als Durchlässigkeit von 100 % angezeigt. Das Fenster teilweise transparent zu gestalten, kann nützlich sein, um die Teile des Zielfensters über die **AccScope-Benutzeroberfläche** anzuzeigen, während sie den modus Always On **Top** verwenden.
- Wenn sie angezeigt werden, verwenden Sie die horizontalen und vertikalen Bildlaufleisten, um die Ansichtsmitte der Visualisierung zu ändern. Dies ist hilfreich, wenn  Sie die Option  Visuelles Layout verwenden, aber nicht die Option Vollbildansicht verwenden, während das **AccScope-Fenster** im Vergleich zum Zielfenster klein ist.

## <a name="testing-the-narrator-scenario"></a>Testen des Sprachausgabeszenarios

Das Szenario "Sprachausgabe" ist der wichtigste Aspekt, der bei Verwendung von **AccScope** zu testen ist. Es wurde speziell entwickelt, um zu visualisieren, wie die grundlegende Navigation von Sprachausgabeelement funktioniert, wenn sie auf Ihre App angewendet wird.

Verwenden Sie zum Testen des Sprachausgabeszenarios die folgenden **AccScope-Konfigurationsoptionen:**

- **Elementmodus:** **Sprachausgabe**
- **Layout:** **Visual**
- **Layoutoptionen:** **QuickInfo anzeigen und** **Zahlen anzeigen** beide ausgewählt

Im Folgenden finden Sie einige bestimmte Bereiche Ihrer App, die Sie für das Sprachausgabeszenario testen können:

- **Element reihenfolge:** Stellen Sie sicher, dass die Reihenfolge, in der die Sprachausgabe Ihre Steuerelemente liest, gemäß den Zahlen (grünen Kreisen), die in den Visualisierungen angezeigt werden, korrekt ist. Wenn Elemente nicht in der Reihenfolge sind, die Sie zum Lesen erwarten, ändern Sie die Benutzeroberflächenstruktur der App und die resultierende Benutzeroberflächenautomatisierung-Struktur, und testen Sie erneut, bis Sie überprüft haben, ob ihre Elemente in der erwarteten Lesefolge sind.
- **Gesprochener Text:** Bewegen Sie die Maus innerhalb der Visualisierung, und zeigen Sie auf jedes der Elementrechtecke, um die Tooltipps für jedes Element anzuzeigen. Im Sprachausgabemodus zeigen die Tooltipps einen **Texteintrag für die** Sprachausgabe an, bei dem es sich tatsächlich um den Text handelt, den die Sprachausgabe liest. Im Allgemeinen besteht dieser Text aus dem **Namen und** dem **Steuerelementtyp**. Stellen Sie sicher, dass dies die richtigen Informationen für jedes Steuerelement in Ihrer Benutzeroberfläche ist. Wenn informationen falsch sind, ändern Sie Benutzeroberflächenautomatisierung eigenschaften mit den Techniken, die von Ihrem bestimmten Benutzeroberflächenframework dafür aktiviert werden. (Wenn **der Steuerelementtyp** unerwartet ist, müssen Sie möglicherweise ein anderes Steuerelement verwenden, da dies häufig ausschließlich von den Steuerelementimplementierungen eines Benutzeroberflächenframework gesteuert wird.) Testen Sie dann erneut, und überprüfen Sie, **ob der Text der Sprachausgabe** korrekt ist.
- **Elementlayout:** Überprüfen Sie jeden dieser Fälle:
    - Stellen Sie sicher, dass redundante Elemente nicht von der Sprachausgabe verfügbar gemacht werden. Ein Beispiel für ein redundantes Element ist das Ratings-Steuerelement in jedem Windows Store Kachelelement.
    - Überprüfen Sie, ob wichtige Elemente (Elemente, die der Benutzer benötigt, um wichtige Aufgaben in der App auszuführen) jeweils in der Navigation der Sprachausgabeelemente angezeigt werden.
    - Wenn Sie das **visuelle** Layout verwenden und ein Element fehlt, da steuerelemente sich überlappen, wechseln Sie zu **Listenlayout,** um die Sequenz anzuzeigen, die die Sprachausgabe meldet.
    - Vergewissern Sie sich, dass die Benutzeroberflächenautomatisierung Struktur insgesamt korrekt und für Ihre App erwartet ist.

## <a name="related-topics"></a>Zugehörige Themen

- [Überwachung für barrierefreie Ereignisse](accessible-event-watcher.md)
- [Testtools](testing-tools.md)
- [UI Accessibility Checker](ui-accessibility-checker.md)
- [Benutzeroberflächenautomatisierungs-Überprüfung](ui-automation-verify.md)
- [Microsoft Accessibility (Microsoft-Barrierefreiheit)](https://www.microsoft.com/accessibility/)
