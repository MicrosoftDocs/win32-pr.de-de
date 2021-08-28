---
title: Die grafische accChecker-Benutzeroberfläche
description: In diesem Thema werden die Elemente beschrieben, die die AccChecker-GUI bilden.
ms.assetid: C8C156F6-AB29-4011-9DCD-74261AC17404
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf645a3afd35bdd906d1ab26453d16672311cb4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473386"
---
# <a name="the-accchecker-graphical-user-interface"></a>Die grafische accChecker-Benutzeroberfläche

In diesem Thema werden die Elemente beschrieben, die die AccChecker-GUI bilden.

-   [Registerkarte "Überprüfungen"](#verifications-tab)
-   [Registerkarte „Ergebnisse“](#results-tab)
-   [MSAA- und UIA-Bildschirmleseregisterkarten](#msaa-and-uia-screen-reader-tabs)
-   [MSAA- und UIA-Strukturregisterkarten](#msaa-and-uia-tree-tabs)
-   [Menü "Datei"](#file-menu)
-   [Zugehörige Themen](#related-topics)

## <a name="verifications-tab"></a>Registerkarte "Überprüfungen"

AccChecker beginnt mit der Standardansicht der Registerkarte **Überprüfungen:**

![Screenshot: Registerkarte "Überprüfungen" in der U I Accessibility Checker](images/accchecker-verifications-tab.png)

Die Registerkarte **Überprüfungen** enthält die folgenden Komponenten.

-   **Auswahl des Überprüfungsziels** Bietet die folgenden Optionen zum Auswählen einer Zielanwendung oder eines Zielsteuerelements.
    -   Wählen Sie ein Ziel aus der vorab ausgefüllten Dropdownliste aus. Diese Liste enthält alle HWNDs der obersten Ebene, die beim Start identifiziert wurden.
    -   Wählen Sie einen HWND basierend auf der Position des Mauszeigers aus (auswählbare Steuerelemente werden mit einem roten Rechteck hervorgehoben). Mit dieser Option können Sie ein beliebiges sichtbares Objekt auswählen, das über ein HWND verfügt.
    -   Geben Sie einen bestimmten HWND ein.
-   **Prüfliste für Überprüfungsroutinen** Bietet die Möglichkeit, die gewünschte Überprüfungsroutine auszuwählen, die für eine Anwendung oder ein Steuerelement ausgeführt werden soll. Weitere Informationen finden Sie unter Überprüfungsroutinen.
-   Auswahl der **Fehler- und Warnungsunterdrückungsdatei** Unterdrückungsdateien werden auf der Registerkarte **Ergebnisse** der Überprüfung generiert. Wenn Sie mit der rechten Maustaste auf eine Fehler- oder Warnmeldung klicken und im Kontextmenü **unterdrücken** auswählen, wird ein Flag für diese Meldung festgelegt. Wenn das Kontrollkästchen **Unterdrückungen** aktiviert ist, werden unterdrückte Einträge in der Liste angezeigt. Ein unterdrückter Eintrag kann mithilfe desselben Kontextmenüs, mit dem er unterdrückt wird, nicht unterdrückt werden.

    Eine Unterdrückungsdatei wird im XML-Format gespeichert, indem Sie im Menü **Datei** die Option **Unterdrückung speichern** auswählen. Diese Datei wird bei nachfolgenden Überprüfungsläufen verwendet, bei denen die Nachrichten ausgeblendet werden. Klicken Sie auf **Löschen,** um die Unterdrückungsdatei zu entfernen. Informationen zu bestimmten Nachrichten finden Sie unter Überprüfungsprotokollmeldungen. Verwenden Sie das Menü **Protokoll speichern** aus dem Menü **Datei,** um die gesamte Liste als Protokolldatei in XML oder als formatierte Textdatei zu speichern.

    ![Registerkarte "Accchecker-Ergebnisse" mit hervorgehobener Option "Kontextelement unterdrücken"](images/accchecker-results-tab-with-suppress.png)

    Das folgende Beispiel zeigt den Inhalt einer Unterdrückungsdatei, die durch Ausführen der **Eigenschaftenüberprüfungen** in der Systemsteuerungsanwendung Windows Firewall generiert wird. Der Fehler mit der ID "ElementHasNoName" wurde für die Unterdrückung in diesem Beispiel ausgewählt.

    ```XML
    <?xml version="1.0" encoding="utf-8"?><ArrayOfLogEvent xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema">
      <LogEvent>
        <EventID>ElementHasNoName</EventID>
        <Text>Element has no name</Text>
        <ParentChain>Windows Firewall.Windows Firewall</ParentChain>
        <VerificationRoutine>VerificationRoutines.CheckName</VerificationRoutine>
        <Classname>ATL:BUTTON</Classname>
        <AccName />
        <AccRole>PushButton</AccRole>
      </LogEvent>
    </ArrayOfLogEvent>
    ```

    

-   **Anzeigen priorisierter Ergebnisse** Bietet die folgenden Optionen zum Filtern der Überprüfungsergebnisse nach Priorität.
    -   **Alle** Schließen Sie alle Ergebnisse unabhängig von der Priorität ein.
    -   **Nur P1** Schließen Sie nur Ergebnisse mit Priorität 0 und Priorität 1 ein.
    -   **Nur P1 P2** Fügen Sie ergebnisse von Priorität 0 bis Priorität 2 ein.
-   **Ausführen ausgewählter Überprüfungen** Stellt die Schaltfläche **Überprüfungen ausführen** bereit, um den Überprüfungsprozess zu starten. Während überprüfungen ausgeführt werden, ändert sich die Schaltfläche in **Überprüfungen abbrechen** und kann verwendet werden, um die Überprüfungen nach Abschluss der aktuellen Überprüfung zu beenden.

## <a name="results-tab"></a>Registerkarte "Ergebnisse"

Die Registerkarte **Ergebnisse** wird aufgefüllt, nachdem die ausgewählten Überprüfungsaufgaben abgeschlossen wurden. Sie besteht aus den folgenden Komponenten.

-   Die Meldungsliste, in der die von den ausgewählten Überprüfungstasks generierten Fehler-, Warnungs- und Informationsmeldungen angezeigt werden. Die angezeigten Nachrichten können mithilfe der Kontrollkästchen oberhalb der Meldungsliste nach Typ gefiltert werden.
-   Die Meldungsdetails und eine Bildschirmaufnahme des Überprüfungsziels. Wenn Sie eine Nachricht aus der Meldungsliste auswählen, werden weitere Details angezeigt und das entsprechende Element im Bildschirmaufnahmebereich hervorgehoben. Über die Schaltfläche **Visualisieren** wird AccChecker zur Registerkarte **MSAA-Struktur** gewechselt. Wenn auf der Registerkarte **Ergebnisse** ein Fehler hervorgehoben ist, wird das entsprechende Element auf der Registerkarte **MSAA-Struktur** hervorgehoben.

Wenn Sie mit der rechten Maustaste auf eine Nachricht klicken, wird ein Kontextmenü mit den folgenden Elementen verfügbar gemacht.

-   **Unterdrücken** Fügt die Meldung der Unterdrückungsliste hinzu.
-   **Kopieren in die Zwischenablage** Kopiert die Nachrichtendetails in die Zwischenablage.
-   **Visualisieren** Wechselt zu AccChecker zur Registerkarte **MSAA-Struktur.** Das Element, das dem ausgewählten Fehler entspricht, wird hervorgehoben.
-   **Hilfe** Zeigt zusätzliche Informationen zur Meldung an.

## <a name="msaa-and-uia-screen-reader-tabs"></a>MSAA- und UIA-Bildschirmleseregisterkarten

Die Registerkarten MSAA-Sprachausgabe und UIA-Sprachausgabe sind ähnlich. Beide zeigen ein Transkript von Elementen an, die in einem simulierten Durchlauf des Überprüfungsziels durch eine Sprachausgabe gefunden wurden, mit der Ausnahme, dass eine die MSAA-Implementierung und die andere die UIA-Implementierung anzeigt.

Elemente werden so navigiert und protokolliert, wie sie von einer Sprachausgabe gelesen werden. Die auf dieser Registerkarte angezeigten Informationen sind wichtig, um zu bestätigen, dass nur nützliche und relevante Informationen angekündigt werden. Ein normal klingender Steuerelementname wie "MenuItem Edit" oder "PushButton Close" ist beispielsweise akzeptabel. Ein Steuerelementname, der keinen Sinn ergibt, z. B. "CPNavPanel22" oder "DefaultValue1", ist jedoch nicht akzeptabel. Die Schaltfläche **Visualisieren** bewirkt, dass AccChecker zur Registerkarte **MSAA-Struktur** oder **UIA-Struktur** wechselt. Wenn ein Element auf der Registerkarte **Sprachausgabe** hervorgehoben ist, wird das entsprechende Element auf der Registerkarte **MSAA-Struktur** oder **UIA-Struktur** hervorgehoben.

Die **ScreenReader-Überprüfungsroutine** unter **Konsistenz** muss auf der Registerkarte **Überprüfungen** ausgewählt werden, damit die **Registerkarte MSAA-Sprachausgabe** angezeigt wird. Auf ähnliche Weise muss die **UiaScreenReader-Überprüfungsroutine** ausgewählt werden, damit die Registerkarte **UIA-Sprachausgabe** angezeigt wird.

Der folgende Screenshot zeigt die Registerkarte UIA Screen reader (UIA-Sprachausgabe) mit einer Beispielüberprüfung von Editor.

![Bildschirmleseregisterkarte "accchecker" mit Beispielüberprüfungsergebnissen](images/accchecker-screen-reader-tab.png)

## <a name="msaa-and-uia-tree-tabs"></a>MSAA- und UIA-Strukturregisterkarten

Das Ausführen einer Überprüfungsroutine bewirkt, dass AccChecker alle sichtbaren Elemente im Überprüfungsziel kompiliert und hierarchisch auf der Registerkarte **MSAA-Struktur** und der Registerkarte **UIA-Struktur** anzeigt. Der folgende Screenshot zeigt die Registerkarte MSAA-Struktur mit der Hierarchie der Elemente für Editor.

![accchecker msaa tree tab](images/accchecker-tree-tab.png)

## <a name="file-menu"></a>Menü „Datei“




| Menü | Befehl | BESCHREIBUNG | 
|------|---------|-------------|
| <strong>Datei</strong>${REMOVE}$<br /> | <strong>Öffnen</strong> | Stellt die folgenden Optionen bereit.<br /><ul><li><strong>Überprüfungs-DLL</strong> Öffnet eine Überprüfungs-DLL. Native AccChecker-Überprüfungen werden in einer eigenständigen DLL (VerificationRoutines.dll) gekapselt. Mit diesem Entwurf können Testteams basierend auf der getesteten Benutzeroberflächenplattform eigene Überprüfungen erstellen.</li><li><strong>Protokolldatei</strong> Hiermit können Sie eine zu öffnende Überprüfungsprotokolldatei auswählen.</li></ul> | 
| <strong>Automatisches Laden verfügbarer Überprüfungen</strong> | Lädt automatisch alle verfügbaren AccChecker-Überprüfungen. | 
| <strong>Protokoll speichern</strong> | Speichern Sie das Überprüfungsprotokoll als XML oder als Nur-Text. Nur-Text ist lesbarer. | 
| <strong>Speichern der Unterdrückung</strong> | Speichern Sie das Unterdrückungsprotokoll als XML. Diese Datei gibt die Überprüfungsmeldungen an, die bei Regressionstests ignoriert werden sollen. | 
| <strong>Beenden</strong> | Schließt das AccChecker-Tool. | 
| <strong>Überprüfungen</strong>${REMOVE}$<br /> | <strong>Run Now</strong> | Führen Sie die Überprüfungsroutinen wie für das ausgewählte Überprüfungsziel angegeben aus. | 
| <strong>Alle aktivieren</strong> | Aktivieren Sie alle Überprüfungsroutinen-Kontrollkästchen. | 
| <strong>Alle deaktivieren</strong> | Deaktivieren Sie alle Überprüfungsroutinen-Kontrollkästchen. | 
| <strong>Optionen</strong> | <strong>Always On Top</strong> | Machen Sie AccChecker zum obersten Fenster in der Z-Reihenfolge. | 
| <strong>Hilfe</strong>${REMOVE}$<br /> | <strong>Hilfe</strong> | Zeigen Sie Hilfeinformationen an. | 
| <strong>Info</strong> | Zeigen Sie die AccChecker-Version und eine E-Mail-Adresse für die Kontaktaufnahme mit Microsoft über AccChecker an. | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 





