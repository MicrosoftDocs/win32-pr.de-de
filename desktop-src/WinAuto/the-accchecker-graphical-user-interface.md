---
title: Die grafische Benutzeroberfläche der Zugriffs Überprüfung
description: In diesem Thema werden die Elemente beschrieben, aus denen die Benutzeroberfläche für die Zugriffs Prüfung besteht.
ms.assetid: C8C156F6-AB29-4011-9DCD-74261AC17404
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26d847d1bc198958ca28dd77d67b0e99b9d7745
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "104562106"
---
# <a name="the-accchecker-graphical-user-interface"></a>Die grafische Benutzeroberfläche der Zugriffs Überprüfung

In diesem Thema werden die Elemente beschrieben, aus denen die Benutzeroberfläche für die Zugriffs Prüfung besteht.

-   [Registerkarte Überprüfungen](#verifications-tab)
-   [Registerkarte „Ergebnisse“](#results-tab)
-   [MSAA-und UIA-Bildschirm Lese Registerkarten](#msaa-and-uia-screen-reader-tabs)
-   [Registerkarten für MSAA und UIA-Struktur](#msaa-and-uia-tree-tabs)
-   [Menü "Datei"](#file-menu)
-   [Zugehörige Themen](#related-topics)

## <a name="verifications-tab"></a>Registerkarte Überprüfungen

Die Zugriffs Prüfung wird mit der Standardansicht der Registerkarte über **Prüfungen** gestartet:

![Screenshot, der die Registerkarte "verifications" in der eingabezugriffsüberprüfung von U I anzeigt](images/accchecker-verifications-tab.png)

Die Registerkarte über **Prüfungen** enthält die folgenden Komponenten.

-   **Überprüfungs Zielauswahl** Bietet die folgenden Optionen für die Auswahl einer Zielanwendung oder eines-Steuer Elements.
    -   Wählen Sie ein Ziel aus der vordefinierten Dropdown Liste aus. Diese Liste enthält alle HWNDs der obersten Ebene, die beim Start identifiziert werden.
    -   Wählen Sie ein HWND basierend auf der Position des Mauszeigers aus (auswählbare Steuerelemente werden mit einem roten Rechteck hervorgehoben). Mit dieser Option können Sie ein beliebiges sichtbares Objekt auswählen, das über ein HWND verfügt.
    -   Geben Sie ein bestimmtes HWND ein.
-   **Checkliste für Überprüfungs Routinen** Bietet die Möglichkeit, die gewünschte Überprüfungs Routine auszuwählen, die für eine Anwendung oder ein Steuerelement ausgeführt werden soll. Weitere Informationen finden Sie unter Überprüfungs Routinen.
-   **Fehler-und Warnungs Unterdrückungs Dateiauswahl** Unterdrückungs Dateien werden auf der Registerkarte Überprüfungs **Ergebnisse** generiert. Wenn Sie mit der rechten Maustaste auf einen Fehler oder eine Warnmeldung Klicken und im Kontextmenü unter **drücken** auswählen, wird für diese Nachricht ein Flag festgelegt. Wenn das Kontrollkästchen **Unterdrückungen** aktiviert ist, werden unterdrückte Einträge in der Liste angezeigt. Ein unterdrückter Eintrag kann unterdrückt werden, indem das gleiche Kontextmenü verwendet wird, um ihn zu unterdrücken.

    Eine Unterdrückungs Datei wird im XML-Format gespeichert, indem im Menü **Datei** die Option **Unterdrückung speichern** ausgewählt wird. Diese Datei wird bei nachfolgenden Überprüfungs Läufen verwendet, bei denen die Nachrichten ausgeblendet werden. Um die Unterdrückungs Datei zu entfernen, klicken Sie auf **Löschen**. Informationen zu bestimmten Nachrichten finden Sie unter Verifizierungsprotokoll Meldungen. Verwenden Sie im Menü **Datei** die Option **Protokoll speichern** , um die gesamte Liste als Protokolldatei in XML oder als formatierte Textdatei zu speichern.

    ![Registerkarte "accchecker-Ergebnisse" mit hervorgehobenem Kontext Element](images/accchecker-results-tab-with-suppress.png)

    Das folgende Beispiel zeigt den Inhalt einer Unterdrückungs Datei, die durch Ausführen der **Eigenschaften** Überprüfungen in der System Steuerungsanwendung der Windows-Firewall generiert wird. Der Fehler mit der ID "elementhasnoname" wurde in diesem Beispiel zur Unterdrückung ausgewählt.

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

    

-   **Priorisierte Ergebnisse anzeigen** Bietet die folgenden Optionen zum Filtern der Überprüfungs Ergebnisse nach Priorität.
    -   **Alle** Alle Ergebnisse unabhängig von der Priorität einbeziehen.
    -   **Nur P1** Nur Ergebnisse mit Priorität 0 und Priorität 1 einschließen.
    -   **Nur P1 P2** Ergebnisse mit Priorität 0 und Priorität 2 einschließen.
-   **Ausgewählte Verifizierungen ausführen** Stellt die Schaltfläche über **Prüfungen ausführen** zum Starten des Überprüfungsprozesses bereit. Während die Überprüfung ausgeführt wird, ändert sich die Schaltfläche, um über **Prüfungen abzubrechen** , und kann verwendet werden, um die Überprüfungen zu beenden, nachdem der aktuelle abgeschlossen wurde.

## <a name="results-tab"></a>Registerkarte "Ergebnisse"

Die Registerkarte **Ergebnisse** wird aufgefüllt, nachdem die ausgewählten Überprüfungs Aufgaben fertiggestellt wurden. Sie besteht aus den folgenden Komponenten:

-   Die Meldungs Liste, in der die Fehler-, Warnungs-und Informationsmeldungen angezeigt werden, die von den ausgewählten Überprüfungs Tasks generiert wurden. Die angezeigten Meldungen können mithilfe der Kontrollkästchen oberhalb der Meldungs Liste nach Typ gefiltert werden.
-   Die Nachrichten Details und eine Bildschirmaufnahme des Überprüfungs Ziels. Wenn Sie eine Meldung aus der Liste Nachricht auswählen, werden weitere Details angezeigt, und das entsprechende Element wird im Bereich Bildschirmaufnahme hervorgehoben. Die Schaltfläche **visualisieren** , schaltet die Zugriffstaste auf die Registerkarte **MSAA** -Struktur. Wenn ein Fehler auf der Registerkarte **Ergebnisse** hervorgehoben ist, wird das entsprechende Element auf der Registerkarte **MSAA** -Struktur hervorgehoben.

Wenn Sie mit der rechten Maustaste auf eine Nachricht klicken, wird ein Kontextmenü mit den folgenden Elementen angezeigt.

-   Unter **drücken** Fügt die Meldung der Unterdrückungs Liste hinzu.
-   **In Zwischenablage kopieren** Kopiert die Nachrichten Details in die Zwischenablage.
-   **Visualisieren** Schaltet die Zugriffstaste auf die Registerkarte **MSAA** -Struktur. Das Element, das dem ausgewählten Fehler entspricht, wird hervorgehoben.
-   **Hilfe** Zeigt zusätzliche Informationen zur Meldung an.

## <a name="msaa-and-uia-screen-reader-tabs"></a>MSAA-und UIA-Bildschirm Lese Registerkarten

Die Registerkarten "MSAA Screen Reader" und "UIA Screen Reader" ähneln einander. Beide zeigen eine Aufzeichnung von Elementen an, die in einem simulierten Durchlauf des Überprüfungs Ziels durch eine Bildschirm Sprachausgabe gefunden wurden, mit dem Unterschied, dass die MSAA-Implementierung und die andere die UIA-Implementierung anzeigt.

Elemente werden navigiert und protokolliert, so wie Sie von einer Bildschirmausgabe gelesen werden. Die auf dieser Registerkarte dargestellten Informationen sind wichtig, um zu bestätigen, dass nur nützliche und relevante Informationen angekündigt werden. Beispielsweise ist ein normaler Name eines Steuer Elements, z. b. "MenuItem Edit" oder "Push Button Close", zulässig. ein Steuerelement Name, der nicht sinnvoll ist, z. b. "CPNavPanel22" oder "DefaultValue1", ist jedoch nicht zulässig. Die Schaltfläche **visualisieren** bewirkt, dass die Zugriffs Prüfung zur Registerkarte **MSAA** -Struktur oder **UIA** -Struktur wechselt. Wenn ein Element auf der Registerkarte **Bildschirmleser** hervorgehoben ist, wird das entsprechende Element auf der Registerkarte **MSAA** -Struktur oder **UIA** -Struktur hervorgehoben.

Die **Screenreader** -Überprüfungs Routine **muss auf** der Registerkarte über **Prüfungen** ausgewählt sein, damit die **Registerkarte "MSAA-Bildschirmleser** " angezeigt wird. Ebenso muss die **uiaskreeinreader** -Überprüfungs Routine ausgewählt werden, damit die Registerkarte " **UIA-Bildschirmleser** " angezeigt wird.

Der folgende Screenshot zeigt die Registerkarte "User Screen Reader" (UIA) mit einer Beispiel Überprüfung von Notepad.

![Bildschirm Lese Registerkarte "accchecker" zeigt Beispiel Überprüfungs Ergebnisse an](images/accchecker-screen-reader-tab.png)

## <a name="msaa-and-uia-tree-tabs"></a>Registerkarten für MSAA und UIA-Struktur

Das Ausführen einer Überprüfungs Routine bewirkt, dass accchecker alle sichtbaren Elemente im Überprüfungs Ziel kompiliert und hierarchisch auf der Registerkarte " **MSAA** -Struktur" und der Registerkarte " **UIA** -Struktur" anzeigt. Der folgende Screenshot zeigt die Registerkarte MSAA-Struktur mit der Hierarchie der Elemente für Notepad.

![Registerkarte "accchecker-Struktur"](images/accchecker-tree-tab.png)

## <a name="file-menu"></a>Menü „Datei“



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Menü</th>
<th>Get-Help</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="5"><strong>Datei</strong>$ {Remove} $<br />
</td>
<td><strong>Öffnen</strong></td>
<td>Bietet die folgenden Optionen.<br/>
<ul>
<li><strong>Verifications-dll</strong> Öffnet eine Überprüfungs-dll. Native accchecker-Verifizierungen werden in einer eigenständigen dll (VerificationRoutines.dll) gekapselt. Mit diesem Entwurf können Testteams basierend auf der UI-Plattform, die getestet wird, ihren eigenen Satz von Überprüfungen erstellen.</li>
<li><strong>Protokolldatei</strong> Ermöglicht das Auswählen einer zu öffnenden Überprüfungsprotokoll Datei.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Verfügbare Überprüfungen automatisch laden</strong></td>
<td>Alle verfügbaren accessüberprüfungs Überprüfungen werden automatisch geladen.</td>

</tr>
<tr class="odd">
<td><strong>Protokoll speichern</strong></td>
<td>Speichern Sie das Überprüfungsprotokoll als XML oder als Klartext. Nur-Text ist besser lesbar.</td>

</tr>
<tr class="even">
<td><strong>Unterdrückung speichern</strong></td>
<td>Speichern Sie das Unterdrückungs Protokoll als XML. Diese Datei gibt die Überprüfungs Meldungen an, die bei Regressionstests ignoriert werden.</td>

</tr>
<tr class="odd">
<td><strong>Beenden</strong></td>
<td>Schließt das accchecker-Tool.</td>

</tr>
<tr class="even">
<td rowspan="3"><strong>Verifizierungen</strong>$ {Remove} $<br />
</td>
<td><strong>Run Now</strong></td>
<td>Führen Sie die Überprüfungs Routinen aus, die für das ausgewählte Überprüfungs Ziel angegeben sind.</td>
</tr>
<tr class="odd">
<td><strong>Alle aktivieren</strong></td>
<td>Aktivieren Sie die Kontrollkästchen Alle Überprüfungs Routine.</td>

</tr>
<tr class="even">
<td><strong>Alle deaktivieren</strong></td>
<td>Deaktivieren Sie die Kontrollkästchen Alle Überprüfungs Routine.</td>

</tr>
<tr class="odd">
<td><strong>Optionen</strong></td>
<td><strong>Always on oben</strong></td>
<td>Erstellen Sie das oberste Fenster in der z-Reihenfolge.</td>
</tr>
<tr class="even">
<td rowspan="2"><strong>Hilfe</strong>$ {Remove} $<br />
</td>
<td><strong>Hilfe</strong></td>
<td>Anzeigen von Hilfe Informationen.</td>
</tr>
<tr class="odd">
<td><strong>Info</strong></td>
<td>Anzeigen der accchecker-Version und einer e-Mail-Adresse für die Kontaktaufnahme mit Microsoft zur Zugriffs Überprüfung.</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 





