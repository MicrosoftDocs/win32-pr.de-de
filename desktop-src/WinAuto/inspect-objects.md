---
title: Barrierefreiheitstools – Überprüfen
description: Inspect (Inspect.exe) ist ein Windows-basiertes Tool, mit dem Sie ein beliebiges Benutzeroberflächenelement auswählen und die Barrierefreiheitsdaten des Elements anzeigen können.
ms.assetid: 38edacbc-cf24-4818-b029-561b21e3704c
keywords:
- Tool "Überprüfen"
- Zugriff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c72fba29a409fdce60c026c832f68ff6d182bcd9c8a53e1918e7ac847f4332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118828708"
---
# <a name="accessibility-tools---inspect"></a>Barrierefreiheitstools – Überprüfen

> [!Important]
> **Inspect** ist ein Legacytool. Es wird empfohlen, [stattdessen Insights](https://accessibilityinsights.io/) Barrierefreiheit zu verwenden.

**Inspect** (Inspect.exe) ist ein Windows-basiertes Tool, mit dem Sie ein beliebiges Benutzeroberflächenelement auswählen und die Barrierefreiheitsdaten des Elements anzeigen können. Sie können Eigenschaften und Steuerelementmuster der Microsoft-Benutzeroberflächenautomatisierung sowie Microsoft Active Accessibility-Eigenschaften anzeigen. **Mit Inspect** können Sie auch die Navigationsstruktur der Automatisierungselemente in der Benutzeroberflächenautomatisierung struktur und die zugänglichen Objekte in der Microsoft Active Accessibility testen.

## <a name="requirements"></a>Anforderungen

Um die Benutzeroberflächenautomatisierung, Benutzeroberflächenautomatisierung auf dem System vorhanden sein. Weitere Informationen finden Sie im Abschnitt "Anforderungen" [Benutzeroberflächenautomatisierung](entry-uiauto-win32.md).

**Inspect** wird als Teil der gesamten Tools im Windows Software Development Kit (SDK) installiert und nicht als separater Download verteilt. Das Windows SDK enthält alle in diesem Abschnitt dokumentierten Tools zur Barrierefreiheit.

[Laden Sie das Windows SDK herunter.](https://developer.microsoft.com/en-us/windows/downloads/windows-10-sdk/)

> [!NOTE]
> Informationen zu älteren Versionen des Windows SDK finden Sie im Windows [SDK und Emulatorarchiv](https://developer.microsoft.com/en-us/windows/downloads/sdk-archive/).

**Inspect.exe** befindet sich im Ordner bin version platform> des SDK-Installationspfads (sie müssen in der Regel \\ \\ <  > \\ <  nicht als Administrator ausgeführt werden).

## <a name="the-inspect-window"></a>Das Fenster "Überprüfen"

Das **Fenster** Überprüfen besteht aus mehreren Hauptteilen:

- Titelleiste. Zeigt das **Fensterhand** handle überprüfen (HWND) an.
- Menüleiste. Ermöglicht den Zugriff auf **die Funktion "Überprüfen".**
- Symbolleiste Ermöglicht den Zugriff auf **die Funktion "Überprüfen".**
- Strukturansicht. Stellt die hierarchische Struktur von Benutzeroberflächenelementen als Strukturansicht-Steuerelement vor, mit dem Sie zwischen den Elementen navigieren können.
- Datenansicht Zeigt alle verfügbar gemachten Barrierefreiheitseigenschaften für das ausgewählte Benutzeroberflächenelement an.

Die auf der Menüleiste verfügbaren Befehle sind auch auf der Symbolleiste verfügbar. Die folgende Abbildung zeigt das **Inspect**-Tool, mit dem die Benutzeroberflächenautomatisierungseigenschaften des Menübefehls **Bearbeiten** in Editor abgefragt werden.

![Screenshot der Benutzeroberfläche für das Überprüfungstool](images/inspect.png)

## <a name="using-inspect"></a>Verwenden von Inspect

Wenn Sie Untersuchen **starten,** zeigt die **Strukturansicht** den Speicherort des aktuell  ausgewählten Benutzeroberflächenelements in der Elementhierarchie an, und die Datenansicht zeigt die Eigenschafteninformationen für das ausgewählte Benutzeroberflächenelement an. Sie können in der Benutzeroberfläche navigieren, um Barrierefreiheitsinformationen zu jedem Element in der Benutzeroberfläche anzuzeigen. Standardmäßig verfolgt **Inspect den** Tastatur- oder Mausfokus nach. Wenn sich der Fokus ändert, **wird die** Datenansicht mit den Eigenschafteninformationen des Elements mit Fokus aktualisiert.

Um zwischen Benutzeroberflächenelementen zu navigieren, können Sie eines der folgenden Elemente verwenden:

- Die Maus
- Die Tastatur
- Das Strukturansicht-Steuerelement in der **Strukturansicht**
- Die Navigationsoptionen im **Navigationsmenü**
- Die Navigationsoptionen auf der Symbolleiste

Mit den letzten drei Optionen können Sie durch die Strukturhierarchie der Benutzeroberfläche navigieren. Die Struktur dieser Struktur kann sich zwischen den Modi Benutzeroberflächenautomatisierung und Microsoft Active Accessibility unterscheiden.

## <a name="verifying-accessibility-property-information"></a>Überprüfen von Informationen zur Barrierefreiheitseigenschaft

Die **Datenansicht** zeigt die Eigenschafteninformationen des benutzeroberflächenelements an, das derzeit ausgewählt ist. Sie können **Inspect** so konfigurieren, dass Informationen zu allen Barrierefreiheitseigenschaften oder einer Teilmenge dieser Eigenschaften gezeigt werden. Sie können auch andere Anzeigeoptionen angeben, z. B. ob **Inspect** auf anderen Benutzeroberflächen verbleiben soll oder ob **Inspect** ein um das ausgewählte Element umendes Rechteck hervorheben soll. Nachdem Sie Inspect so **konfiguriert** haben, dass es ihren Wünschen entsprechend funktioniert, können Sie zwischen Benutzeroberflächenelementen navigieren und Eigenschafteninformationen anzeigen. **Inspect** speichert Ihre Konfigurationseinstellungen, wenn sie geschlossen werden, und verwendet sie, um Ihre nächste **Inspect-Sitzung zu** initialisieren.

### <a name="configure-property-settings"></a>Konfigurieren der Einstellungen

1. Wählen Sie **im Menü** Optionen **Einstellungen...** aus, oder wählen Sie **Einstellungen der** Symbolleiste anzeigen aus.
2. Wählen Sie **in der Liste Im Hauptfenster anzeigen**  die Eigenschaften aus, die in der Datenansicht von Überprüfen **angezeigt werden.**
3. Wählen Sie **in der Liste QuickInfo anzeigen** die Eigenschaften aus, die in einer QuickInfo angezeigt werden.
4. Aktivieren Sie das Kontrollkästchen Nicht unterstützte Eigenschaften anzeigen, um Eigenschaften anzuzeigen, die das **Benutzeroberflächenelement möglicherweise nicht** unterstützt.
5. Klicken Sie auf **OK**.

### <a name="to-configure-viewing-options"></a>So konfigurieren Sie Anzeigeoptionen

- Im Menü **Optionen** oder auf der Symbolleiste können Sie die folgenden Anzeigeoptionen auswählen.

| Wenn diese Option ausgewählt ist | **Inspect** führt dies aus.                                                                                                                                                                                                              |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Always on Top                | Wird über einem beliebigen anderen Fenster auf dem Bildschirm angezeigt.                                                                                                                                                                                  |
| MSAA-Modus                    | Zeigt Microsoft Active Accessibility Eigenschafteninformationen an.                                                                                                                                                                      |
| Benutzeroberflächenautomatisierung Modus           | Zeigt Benutzeroberflächenautomatisierung Eigenschafteninformationen an.                                                                                                                                                                                       |
| Nur Windows Ansicht sichtbar    | Nur im MSAA-Modus verfügbar.                                                                                                                                                                                                       |
| Rohdatenansicht                     | Zeigt die [rohe Ansicht](uiauto-treeoverview.md) der Benutzeroberflächenautomatisierung struktur oder MSAA-Struktur in der **Strukturansicht** an.                                                                                                             |
| Steuerelementansicht                 | Stellt die [Steuerelementansicht der](uiauto-treeoverview.md) Benutzeroberflächenautomatisierung Struktur in der **Strukturansicht** vor. Nur im Benutzeroberflächenautomatisierung verfügbar.                                                                            |
| Inhaltsansicht                 | Stellt die [Inhaltsansicht der](uiauto-treeoverview.md) Benutzeroberflächenautomatisierung Struktur in der **Strukturansicht** vor. Nur im Benutzeroberflächenautomatisierung verfügbar.                                                                            |
| Symbolleiste mit aktivem Hover         | Aktiviert Symbolleistenschaltflächen beim Mauszeigerzeiger, anstatt einen Mausklick zu erfordern.                                                                                                                                                      |
| Signalton bei Fehler                | Signalt, wenn während eines vorgangs- oder msaa-Vorgangs Benutzeroberflächenautomatisierung erkannt wird.                                                                                                                                                          |
| SPI \_ SCREENREADER-Flag       | Setzt voraus, dass eine Sprachausgabe vorhanden ist. Dieses Flag gibt an, dass eine Anwendung Informationen nicht grafisch, sondern textlich bereitstellen soll. Sie sollten nicht davon ausgehen, dass dieses Flag einfach festgelegt ist, weil eine Sprachausgabe vorhanden ist.         |
| Hervorhebungsrechte anzeigen     | Hebt ein Rechteck um das Element mit dem Fokus hervor.                                                                                                                                                                              |
| Caret highlight anzeigen         | Hebt das Caret-Caret- hervor. Nur im MSAA-Modus verfügbar.                                                                                                                                                                                 |
| QuickInfo "Informationen anzeigen"     | Zeigt Eigenschaftsinformationen in einer QuickInfo an.                                                                                                                                                                                           |
| Watch Focus                  | Folgt dem Tastaturfokus. Wenn diese Option ausgewählt ist, wird ein asynchroner Fokusereignishook installiert, der das Caret-Caret-Element an die linke obere Ecke des Elements mit dem Fokus verschiebt. Dies **bewirkt, dass Inspect** seine Eigenschaften in etwa einer Sekunde aktualisiert. |
| Caretuhr                  | Folgt dem Caret-Caret. Nur im MSAA-Modus verfügbar.                                                                                                                                                                                    |
| Überwachungscursor                 | Folgt dem Cursor.                                                                                                                                                                                                                |
| QuickInfos ansehen               | Folgt den QuickInfos.                                                                                                                                                                                                              |
| Struktur anzeigen                    | Zeigt die **Strukturansicht** an.                                                                                                                                                                                                        |

## <a name="verifying-accessibility-navigation"></a>Überprüfen der Barrierefreiheitsnavigation

Nachdem Sie mit **Inspect** ein Benutzeroberflächenelement ausgewählt haben, können Sie überprüfen, ob das -Element die richtige Windows Automation-Navigation für Hilfstechnologieprodukte verfügbar macht.

### <a name="verify-accessibility-navigation"></a>Überprüfen der Barrierefreiheitsnavigation

1. Öffnen **Sie Überprüfen** und die Anwendung, die Sie testen möchten.
2. Wählen Sie das Benutzeroberflächenelement aus, über das Sie die Navigation starten möchten.
3. Überprüfen Sie in der **Datenansicht,** ob das Element die richtigen navigationsbezogenen Eigenschaften verfügbar macht.
4. Verwenden Sie die **Strukturansicht,** das **Navigationsmenü** oder die Navigationsschaltflächen auf der Symbolleiste, um in der Benutzeroberfläche zu navigieren und zu überprüfen, ob jedes Element die richtigen navigationsbezogenen Eigenschaften verfügbar macht.
    > [!Note]  
    > Die Optionen des **Navigationsmenüs** und die Schaltflächen der Navigationssymbolleiste ändern sich abhängig davon, wo sich das ausgewählte Element in der Struktur befindet.

## <a name="interacting-with-ui-elements"></a>Interagieren mit Benutzeroberflächenelementen

Windows Automation macht Methoden verfügbar, mit denen Hilfstechnologieprodukte mit einem Benutzeroberflächenelement interagieren können, als ob die Maus oder Tastatur verwendet würde (z. B. um auf eine Schaltfläche zu klicken). Im Menü **Aktion überprüfen** können Tester Windows Automation-Methoden für ein Element aufrufen **(z.B. ruft Invoke.Invoke** die [**IUIAutomationInvokePattern::Invoke-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) auf).

### <a name="interact-with-ui-elements"></a>Interagieren mit Benutzeroberflächenelementen

1. Öffnen **Sie Überprüfen** und die Anwendung, die Sie testen möchten.
2. Wählen Sie das Benutzeroberflächenelement aus, mit dem Sie interagieren möchten.
3. Wählen Sie im Menü **Aktion** oder auf der Symbolleiste die Aktion aus, die Windows Automation-Methode entspricht, die Sie aufrufen möchten.

Das Menü **Aktion** enthält die Elemente **Aktualisieren** und **Fokus** sowie andere Elemente, die abhängig davon variieren, ob Benutzeroberflächenautomatisierung Modus oder msaa-Modus ausgewählt ist. Im Benutzeroberflächenautomatisierung Modus spiegeln die anderen Elemente die Steuerelementmuster wider, die vom derzeit ausgewählten Benutzeroberflächenelement unterstützt werden. Im MSAA-Modus bestehen die anderen Elemente immer aus folgenden Elementen:

| Aktion                | BESCHREIBUNG                                                                                                           |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------|
| Aktualisieren               | Aktualisiert die Benutzeroberfläche. Verfügbar im MSAA- und Benutzeroberflächenautomatisierung-Modus.                                               |
| Standardaktion        | Führt die Standardaktion für das Element aus.                                                                          |
| Fokus                 | Legt den Fokus auf das Element fest. Verfügbar im MSAA- und Benutzeroberflächenautomatisierung-Modus.                                                  |
| Select                | Wählt das Element aus.                                                                                                  |
| Auswahl erweitern      | Erweitert die Auswahl von Elementen, um alle Elemente zwischen dem ersten ausgewählten Element und dem aktuellen Element einzuschließt. |
| Zur Auswahl hinzufügen      | Wählt das aktuelle Element (z. B. ein Listenelement) aus.                                                                    |
| Aus Auswahl entfernen | Entfernt das aktuelle Element aus der Auswahl.                                                                       |
| SetAccValue           | Legt den Microsoft Active Accessibility Wert des Elements auf die angegebene Zeichenfolge fest.                                 |
| Fokussiertes untergeordnetes Element         | Navigiert zum untergeordneten Element des Elements, das derzeit den Fokus besitzt.                                                       |
| HitTest am Cursor     | Navigiert zum untergeordneten Element des vom Mauscursor angegebenen Elements.                                                      |
| Hittest...            | Öffnet das Dialogfeld **HitTest.**                                                                                     |



 

## <a name="keyboard-shortcuts"></a>Tastenkombinationen

Viele der Menüelemente können mit einer Tastenkombination aufgerufen werden, auch wenn **Inspect** nicht die aktive Anwendung ist. Beachten Sie jedoch, dass die Tastenkombinationen mit einigen Anwendungen in Konflikt geraten.

Die folgenden Tastenkombinationen aktivieren die verschiedenen Optionen im Menü:



| Aufgabe                                                                                                                                       | Tastenkombination |
|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| Rufen Sie die Standardaktion des Objekts unter dem Cursor auf (Standardaktion durchführen). Nur im MSAA-Modus verfügbar.                                       | STRG+UMSCHALT+F2              |
| Wählen Sie das Objekt unter dem Cursor aus (Auswählen). Nur im MSAA-Modus verfügbar.                                                                        | STRG+UMSCHALT+F3              |
| Legen Sie den Tastaturfokus auf das Objekt unter dem Cursor (Fokus) fest.                                                                                   | STRG+UMSCHALT+F4              |
| Wechseln Sie von dem Objekt unter dem Cursor zum vorherigen nebengeordneten Objekt. Dieser Befehl navigiert nur zu Objekten innerhalb eines Containers (Previous Sibling). | STRG+UMSCHALT+F5              |
| Wechseln Sie zum übergeordneten (übergeordneten) Objekt.                                                                                                            | STRG+UMSCHALT+F6              |
| Wechseln Sie zum ersten untergeordneten Element des aktuellen Objekts (Erstes untergeordnetes Element).                                                                                     | STRG+UMSCHALT+F7              |
| Wechseln Sie zum nächsten nebengeordneten Objekt von dem Objekt unter dem Cursor. Dieser Befehl navigiert nur innerhalb eines Containers zu Objekten (Next Sibling).         | STRG+UMSCHALT+F8              |
| Wechseln Sie zum letzten untergeordneten Element des aktuellen Objekts (Letztes untergeordnetes Element).                                                                                       | STRG+UMSCHALT+F9              |
| Wechseln Sie zum Objekt unter dem Mauszeiger (HitTest bei Cursor). Nur im MSAA-Modus verfügbar.                                                      | STRG+UMSCHALT+1               |
| Kopieren Sie den Inhalt der Datenansicht in die Zwischenablage (Alle kopieren).                                                                                  | STRG+UMSCHALT+4               |
| Aktualisieren Sie den Inhalt der Datenansicht (Aktualisieren).                                                                                                 | STRG+UMSCHALT+5               |
| Sehen Sie sich das Objekt an, das den Fokus besitzt (Fokus ansehen).                                                                                                   | STRG+UMSCHALT+6               |
| Wechseln Sie zum nebengeordneten Objekt links neben dem Objekt, über dem sich der Cursor befindet (Links). Nur im MSAA-Modus verfügbar.                                        | STRG+UMSCHALT+7               |
| Wechseln Sie zum nebengeordneten Objekt über dem Objekt, über dem sich der Cursor befindet (Nach oben). Nur im MSAA-Modus verfügbar.                                                | STRG+UMSCHALT+8               |
| Wechseln Sie zum nebengeordneten Objekt unter dem Objekt, über dem sich der Cursor befindet (Nach unten). Nur im MSAA-Modus verfügbar.                                                 | STRG+UMSCHALT+9               |
| Wechseln Sie zum nebengeordneten Objekt rechts neben dem Objekt, über dem sich der Cursor befindet (rechts). Nur im MSAA-Modus verfügbar.                                      | STRG+UMSCHALT+0               |

## <a name="related-topics"></a>Zugehörige Themen

- [Überwachung für barrierefreie Ereignisse](accessible-event-watcher.md)
- [Testtools](testing-tools.md)
- [UI Accessibility Checker](ui-accessibility-checker.md)
- [Benutzeroberflächenautomatisierungs-Überprüfung](ui-automation-verify.md)
- [EH-Viewer (AccScope)](accscope.md)
