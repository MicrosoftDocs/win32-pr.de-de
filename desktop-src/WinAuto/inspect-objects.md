---
title: Barrierefreiheits Tools-überprüfen
description: Untersuchen (Inspect.exe) ist ein Windows-basiertes Tool, mit dem Sie beliebige Benutzeroberflächen Elemente auswählen und die Barrierefreiheits Daten des Elements anzeigen können.
ms.assetid: 38edacbc-cf24-4818-b029-561b21e3704c
keywords:
- Tool überprüfen
- Eingabehilfen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1770c6c4db812ea7d2880c50fcc72cd0edc15022
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104389960"
---
# <a name="accessibility-tools---inspect"></a>Barrierefreiheits Tools-überprüfen

Unter **Suchen** (Inspect.exe) ist ein Windows-basiertes Tool, mit dem Sie beliebige Benutzeroberflächen Elemente auswählen und die Barrierefreiheits Daten des Elements anzeigen können. Sie können Eigenschaften und Steuerelementmuster der Microsoft-Benutzeroberflächenautomatisierung sowie Microsoft Active Accessibility-Eigenschaften anzeigen. Über **prüfen** ermöglicht außerdem das Testen der Navigationsstruktur der Automatisierungselemente in der Benutzeroberflächenautomatisierungs-Struktur und der barrierefreien Objekte in der Microsoft-Active Accessibility Hierarchie.

Unter **Suchen** wird mit dem Windows Software Development Kit (SDK) installiert. (Sie ist auch in früheren Versionen von Windows SDK verfügbar.) Sie befindet sich im \\ Ordner "bin \\ < *Version* > \\ < *Platform*>" des SDK-Installations Pfads (Inspect.exe).

> [!NOTE]
> Unter **Suchen** ist ein Legacy Tool. Stattdessen wird die [](https://accessibilityinsights.io/) Verwendung von eingabeinsights empfohlen.

## <a name="requirements"></a>Anforderungen

Untersuchen kann verwendet werden, um Barrierefreiheits Daten auf Systemen zu untersuchen, die keine Benutzeroberflächen Automatisierung aufweisen, aber nur die Eigenschaften von Microsoft Active Accessibility unter **suchen können.** Zum Untersuchen der Benutzeroberflächen Automatisierung muss die Benutzeroberflächen Automatisierung auf dem System vorhanden sein. Weitere Informationen finden Sie im Abschnitt "Anforderungen" unter [UI Automation](entry-uiauto-win32.md).

Unter **Suchen** ist als Teil der Gesamtmenge der Tools in der Windows SDK installiert und wird nicht als separater Download bereitgestellt. Die Windows SDK umfasst alle Tools für die Barrierefreiheit, die in diesem Abschnitt dokumentiert sind. [Holen Sie sich den Windows SDK.](https://developer.microsoft.com/) (Es gibt auch ein SDK-Download Archiv, das von dieser Seite verknüpft ist, wenn Sie eine vorherige Version benötigen.)

Zum Ausführen von "über **prüfen**" finden Sie Inspect.exe im \\ Ordner "bin \\ < *Version* > \\ < *Platform*>" und führen ihn aus (Sie müssen in der Regel nicht als Administrator ausgeführt werden).

## <a name="the-inspect-window"></a>Das Fenster überprüfen

Das Fenster über **prüfen** besteht aus mehreren Hauptteilen:

- Titelleiste. Zeigt das **Fenster** handle (HWND) für die Überprüfung an.
- Menüleiste. Bietet Zugriff zum über **prüfen** der Funktionalität.
- Symbolleiste Bietet Zugriff zum über **prüfen** der Funktionalität.
- Strukturansicht. Zeigt die hierarchische Struktur von UI-Elementen als Strukturansicht-Steuerelement an, mit dem Sie zwischen den Elementen navigieren können.
- Datenansicht. Zeigt alle verfügbar gemachten Barrierefreiheits Eigenschaften für das ausgewählte UI-Element an.

Die in der Menüleiste verfügbaren Befehle sind auch auf der Symbolleiste verfügbar. Die folgende Abbildung zeigt das **Inspect**-Tool, mit dem die Benutzeroberflächenautomatisierungseigenschaften des Menübefehls **Bearbeiten** in Editor abgefragt werden.

![Screenshot der Benutzeroberfläche für das Tool "überprüfen"](images/inspect.png)

## <a name="using-inspect"></a>Überprüfen

Wenn Sie **mit der über** Prüfung beginnen, wird in der Strukturansicht der Speicherort des aktuell ausgewählten Benutzeroberflächen Elements in der Element Hierarchie angezeigt, und in der **Daten** **Ansicht werden die** Eigenschafts Informationen für das ausgewählte UI-Element angezeigt. Sie können auf der Benutzeroberfläche navigieren, um Barrierefreiheits Informationen zu allen Elementen in der Benutzeroberfläche anzuzeigen. Standardmäßig wird die Tastatur oder der Mauszeiger von unter **Suchen** nachverfolgt. Wenn sich der Fokus ändert, wird die **Daten** Ansicht mit den Eigenschafts Informationen des Elements mit dem Fokus aktualisiert.

Zum Navigieren zwischen Benutzeroberflächen Elementen können Sie Folgendes verwenden:

- Der Mauszeiger
- Die Tastatur
- Das Strukturansicht-Steuerelement in **der Struktur** Ansicht
- Navigationsoptionen im **Navigations** Menü
- Navigationsoptionen in der Symbolleiste

Die letzten drei Optionen ermöglichen es Ihnen, in der Struktur Hierarchie der Benutzeroberfläche zu navigieren. Die Struktur dieser Struktur kann sich zwischen der Benutzeroberflächenautomatisierungs-und der Microsoft Active Accessibility-Modi leicht unterscheiden.

## <a name="verifying-accessibility-property-information"></a>Informationen zur Barrierefreiheits Eigenschaft werden überprüft

Die **Daten** Ansicht zeigt die Eigenschaften Informationen des Benutzeroberflächen Elements an, das derzeit ausgewählt ist. Sie können die Überprüfung **so konfigurieren, dass Informationen zu allen** Barrierefreiheits Eigenschaften oder eine Teilmenge dieser Eigenschaften angezeigt werden. Sie können auch andere Anzeigeoptionen angeben, z. b **. ob die** Überprüfung auf anderen Benutzeroberflächen verbleiben soll oder ob über **prüfen** ein umschließendes Rechteck um das ausgewählte Element hervorheben soll. Nachdem Sie die Überprüfung **so konfiguriert haben, dass** Sie wie gewünscht funktioniert, können Sie mit dem Navigieren zwischen Benutzeroberflächen Elementen und Anzeigen von Eigenschafts Informationen beginnen. Unter **Suchen** speichert Ihre Konfigurationseinstellungen beim Schließen und verwendet diese zum Initialisieren der nächsten **Prüfungs** Sitzung.

### <a name="configure-property-settings"></a>Konfigurieren von Eigenschaften Einstellungen

1. Wählen Sie im Menü **Optionen die Option** **Einstellungen...** aus, oder klicken Sie auf der Symbolleiste auf **Einstellungen anzeigen** .
2. Wählen Sie in der Liste **in Hauptfenster anzeigen** die Eigenschaften aus, die in der **Daten** Ansicht von über **prüfen** angezeigt werden sollen.
3. Wählen Sie in der **QuickInfo-Liste Anzeige in Informationen** die Eigenschaften aus, die in einer QuickInfo angezeigt werden sollen.
4. Um Eigenschaften anzuzeigen, die das UI-Element möglicherweise nicht unterstützt, aktivieren Sie das Kontrollkästchen **nicht unterstützte Eigenschaften anzeigen** .
5. Klicken Sie auf **OK**.

### <a name="to-configure-viewing-options"></a>So konfigurieren Sie Anzeigeoptionen

- Im Menü **Optionen** oder auf der Symbolleiste können Sie die folgenden Anzeigeoptionen auswählen.

| Wenn diese Option ausgewählt ist | Unter **Suchen** dies                                                                                                                                                                                                              |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Immer im Vordergrund                | Wird oben in jedem anderen Fenster auf dem Bildschirm angezeigt.                                                                                                                                                                                  |
| MSAA-Modus                    | Zeigt Eigenschaften Informationen von Microsoft Active Accessibility an.                                                                                                                                                                      |
| Benutzeroberflächen-Automatisierungs Modus           | Zeigt Eigenschaften Informationen für die Benutzeroberflächen Automatisierung an.                                                                                                                                                                                       |
| Sichtbare Windows-Ansicht    | Nur im MSAA-Modus verfügbar.                                                                                                                                                                                                       |
| Rohdatenansicht                     | Zeigt die [Rohdaten Ansicht](uiauto-treeoverview.md) der Benutzeroberflächenautomatisierungs-Struktur oder der MSAA-Struktur in der **Strukturansicht an** .                                                                                                             |
| Steuerelementansicht                 | Zeigt die [Steuerelement Ansicht](uiauto-treeoverview.md) der Benutzeroberflächenautomatisierungs-Struktur in der **Strukturansicht an** . Nur im Benutzeroberflächenautomatisierungs-Modus verfügbar.                                                                            |
| Inhaltsansicht                 | Zeigt die [Inhaltsansicht](uiauto-treeoverview.md) der Benutzeroberflächenautomatisierungs-Struktur in der **Strukturansicht an** . Nur im Benutzeroberflächenautomatisierungs-Modus verfügbar.                                                                            |
| Aktive Hover-Symbolleiste         | Aktiviert die Symbolleisten Schaltflächen auf dem Mauszeiger, anstatt einen Mausklick zu erfordern.                                                                                                                                                      |
| Bei Fehler bei Fehler                | Gibt an, wenn während einer Benutzeroberflächen Automatisierung oder eines MSAA-Vorgangs ein Fehler erkannt wird.                                                                                                                                                          |
| SPI- \_ Screenreader-Flag       | Geht davon aus, dass ein Bildschirm Reader vorhanden ist. Dieses Flag gibt an, dass eine Anwendung Informationen textueller anstatt grafisch bereitstellen soll. Sie sollten nicht davon ausgehen, dass dieses Flag einfach festgelegt ist, weil eine Bildschirm Sprachausgabe vorhanden ist.         |
| Hervorhebungs Rechteck anzeigen     | Markiert ein Rechteck um das Element mit dem Fokus.                                                                                                                                                                              |
| Hervorhebung von Caretzeichen anzeigen         | Hebt die Einfügemarke hervor. Nur im MSAA-Modus verfügbar.                                                                                                                                                                                 |
| Info Info anzeigen     | Zeigt Eigenschafts Informationen in einer QuickInfo an.                                                                                                                                                                                           |
| Fokus ansehen                  | Folgt dem Tastaturfokus. Wenn diese Option aktiviert ist, wird ein asynchroner Fokus Ereignis Hook installiert, der die Einfügemarke nach oben links vom Element mit dem Fokus verschiebt. Dies bewirkt **, dass die Eigenschaften** in ungefähr einer Sekunde von der Überprüfung aktualisiert werden. |
| Caretzeichen ansehen                  | Folgt der Einfügemarke. Nur im MSAA-Modus verfügbar.                                                                                                                                                                                    |
| Überwachungs Cursor                 | Folgt dem Cursor.                                                                                                                                                                                                                |
| Quick Infos ansehen               | Folgt den Quick Infos.                                                                                                                                                                                                              |
| Struktur anzeigen                    | Zeigt die **Struktur** Ansicht an.                                                                                                                                                                                                        |

## <a name="verifying-accessibility-navigation"></a>Überprüfen der Navigations Navigation

Nachdem Sie mithilfe von überprüfen ein UI-Element ausgewählt haben, können Sie über **prüfen**, ob das Element die richtige Windows-Automatisierungs Navigation für Hilfstechnologieprodukte verfügbar macht.

### <a name="verify-accessibility-navigation"></a>Barrierefreiheits Navigation überprüfen

1. Öffnen Sie über **prüfen** und die Anwendung, die Sie testen möchten.
2. Wählen Sie das UI-Element aus, von dem aus die Navigation gestartet werden soll.
3. Überprüfen Sie in der **Daten** Sicht, ob das-Element die richtigen Navigations bezogenen Eigenschaften verfügbar macht.
4. Verwenden Sie die Strukturansicht, das **Navigations** Menü oder die Navigations Schaltflächen auf der Symbolleiste, **um die Benutzer** Oberfläche zu navigieren und zu überprüfen, ob jedes Element die richtigen Navigations bezogenen Eigenschaften verfügbar macht.
    > [!Note]  
    > Die **Navigations** Menü Optionen und Navigations Symbolleisten-Schaltflächen ändern sich abhängig davon, wo sich das ausgewählte Element in der Struktur befindet.

## <a name="interacting-with-ui-elements"></a>Interagieren mit Benutzeroberflächen Elementen

Windows Automation macht Methoden verfügbar, mit denen Hilfstechnologieprodukte mit einem UI-Element interagieren können, als ob die Maus oder Tastatur verwendet würde (z. b. zum Klicken auf eine Schaltfläche). Mit dem Menü "Aktion über **prüfen** " können Tester Windows-Automatisierungsmethoden auf einem Element aufrufen (z **. b. "aufrufen. aufrufen** " Ruft die [**iuiautomationinvokepattern:: Aufrufen**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) -Methode auf).

### <a name="interact-with-ui-elements"></a>Interagieren mit Benutzeroberflächen Elementen

1. Öffnen Sie über **prüfen** und die Anwendung, die Sie testen möchten.
2. Wählen Sie das UI-Element aus, mit dem Sie interagieren möchten.
3. Wählen Sie im Menü **Aktion** oder auf der Symbolleiste die Aktion aus, die der Windows-Automatisierungs Methode entspricht, die Sie aufrufen möchten.

Das Menü **Aktion** enthält die Elemente **Aktualisieren** und **Fokus** sowie andere Elemente, die abhängig davon variieren, ob der Benutzeroberflächenautomatisierungs-Modus oder der MSAA-Modus ausgewählt ist. Im Benutzeroberflächenautomatisierungs-Modus reflektieren die anderen Elemente die Steuerelement Muster, die vom aktuell ausgewählten Benutzeroberflächen Element unterstützt werden. Im MSAA-Modus bestehen die anderen Elemente immer aus folgendem:

| Aktion                | BESCHREIBUNG                                                                                                           |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------|
| Aktualisieren               | Aktualisiert die Benutzeroberfläche. Verfügbar im MSAA-und Benutzeroberflächenautomatisierungs-Modus.                                               |
| Standardaktion        | Führt die Standardaktion für das-Element aus.                                                                          |
| Fokus                 | Legt den Fokus auf das Element fest. Verfügbar im MSAA-und Benutzeroberflächenautomatisierungs-Modus.                                                  |
| Select                | Wählt das Element aus.                                                                                                  |
| Auswahl erweitern      | Erweitert die Auswahl von Elementen, um alle Elemente zwischen dem ersten ausgewählten Element und dem aktuellen Element einzuschließen. |
| Zur Auswahl hinzufügen      | Wählt das aktuelle Element aus (z. b. ein Listenelement).                                                                    |
| Aus Auswahl entfernen | Entfernt das aktuelle Element aus der Auswahl.                                                                       |
| Setaccvalue           | Legt den Wert von Microsoft Active Accessibility des-Elements auf die angegebene Zeichenfolge fest.                                 |
| Untergeordnetes Element         | Navigiert zum untergeordneten Element des Elements, das gerade den Fokus besitzt.                                                       |
| HitTest bei Cursor     | Navigiert zum untergeordneten Element des Elements, das durch den Maus Cursor angegeben wird.                                                      |
| HitTest...            | Öffnet das Dialogfeld " **HitTest** ".                                                                                     |



 

## <a name="keyboard-shortcuts"></a>Tastenkombinationen

Viele der Menü Elemente können auch mit einer Tastenkombination aufgerufen werden, auch **Wenn die** Überprüfung nicht die aktive Anwendung ist. Beachten Sie jedoch, dass die Tastenkombinationen mit einigen Anwendungen in Konflikt stehen.

Die folgenden Tastenkombinationen aktivieren die verschiedenen Optionen im Menü:



| Aufgabe                                                                                                                                       | Tastenkombination |
|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| Rufen Sie die Standardaktion des-Objekts unter dem Cursor auf (Do default Action). Nur im MSAA-Modus verfügbar.                                       | STRG+UMSCHALT+F2              |
| Wählen Sie das Objekt unter dem Cursor (Select) aus. Nur im MSAA-Modus verfügbar.                                                                        | STRG+UMSCHALT+F3              |
| Legen Sie den Tastaturfokus auf das-Objekt unter dem Cursor (Fokus) fest.                                                                                   | STRG + UMSCHALT + F4              |
| Wechselt zum vorhergehenden neben geordneten Objekt von dem unter dem Cursor. Dieser Befehl navigiert zu Objekten nur innerhalb eines Containers (Vorheriges gleich geordnetes Element). | STRG+UMSCHALT+F5              |
| Wechselt zum übergeordneten Element des Objekts (übergeordnet).                                                                                                            | STRG+UMSCHALT+F6              |
| Wechselt zum ersten untergeordneten Element des aktuellen-Objekts (erstes untergeordnetes Element).                                                                                     | STRG + UMSCHALT + F7              |
| Wechselt zum nächsten neben geordneten Objekt, das sich unter dem Cursor befinden soll. Dieser Befehl navigiert zu Objekten nur innerhalb eines Containers (nächstes neben geordnetes Element).         | STRG + UMSCHALT + F8              |
| Wechselt zum letzten untergeordneten Element des aktuellen-Objekts (letztes untergeordnetes Element).                                                                                       | STRG+UMSCHALT+F9              |
| Wechseln Sie zum-Objekt unter dem Mauszeiger (HitTest bei Cursor). Nur im MSAA-Modus verfügbar.                                                      | STRG+UMSCHALT+1               |
| Kopieren Sie den Inhalt der Datenansicht in die Zwischenablage (alle kopieren).                                                                                  | STRG+UMSCHALT+4               |
| Aktualisieren Sie den Inhalt der Datenansicht (aktualisieren).                                                                                                 | STRG+UMSCHALT+5               |
| Sehen Sie sich das Objekt an, das den Fokus besitzt (Überwachungs Fokus).                                                                                                   | STRG+UMSCHALT+6               |
| Wechselt zum neben geordneten Objekt, das sich auf der linken Seite des Cursors befindet (links). Nur im MSAA-Modus verfügbar.                                        | STRG+UMSCHALT+7               |
| Wechseln Sie zu dem neben geordneten Objekt oberhalb des Objekts, über dem sich der Cursor befindet (aufwärts). Nur im MSAA-Modus verfügbar.                                                | STRG+UMSCHALT+8               |
| Wechseln Sie zu dem neben geordneten Objekt, das sich unter dem befindet, über dem sich der Cursor befindet (unten). Nur im MSAA-Modus verfügbar.                                                 | STRG+UMSCHALT+9               |
| Wechselt zum neben geordneten Objekt rechts vom Cursor, über dem sich der Cursor befindet (rechts). Nur im MSAA-Modus verfügbar.                                      | STRG + UMSCHALT + 0               |

## <a name="related-topics"></a>Zugehörige Themen

- [Überwachung für barrierefreie Ereignisse](accessible-event-watcher.md)
- [TestTools](testing-tools.md)
- [UI Accessibility Checker](ui-accessibility-checker.md)
- [Benutzeroberflächenautomatisierungs-Überprüfung](ui-automation-verify.md)
- [EH-Viewer (AccScope)](accscope.md)
