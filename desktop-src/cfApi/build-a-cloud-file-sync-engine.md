---
description: Erfahren Sie, wie Sie eine Cloud Files-Synchronisierungs-Engine erstellen, die Platzhalter Dateien mithilfe der Cloud Files-API verwendet.
title: Erstellen einer Cloud-Synchronisierungs-Engine, die Platzhalter Dateien unterstützt
ms.topic: article
ms.date: 11/12/2020
ms.openlocfilehash: 4f1330285d0c8ef0359639f2be84162f8bc2ef3b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104561419"
---
# <a name="build-a-cloud-sync-engine-that-supports-placeholder-files"></a>Erstellen einer Cloud-Synchronisierungs-Engine, die Platzhalter Dateien unterstützt

Ein Synchronisierungs Modul ist ein Dienst zum Synchronisieren von Dateien, normalerweise zwischen einem Remote Host und einem lokalen Client. Synchronisierungs-Engines unter Windows stellen diese Dateien häufig über das Windows-Dateisystem und den Datei-Explorer für den Benutzer zur Verfügung. Vor Windows 10, Version 1709, wurde die Synchronisierung von Synchronisierungs Modulen in Windows auf szenariounabhängige Ad-hoc-Oberflächen, wie z. b. Navigationsbereich des Datei-Explorers, Windows-Systemleiste und (für weitere technische Anwendungen), als Dateisystem Filter-Treiber beschränkt.

In Windows 10, Version 1709 (auch als Fall Creators Update bezeichnet), wurde die *Cloud Files-API* eingeführt. Diese API ist eine neue Plattform, die die Unterstützung für Synchronisierungs-Engines formalisiert. Die Cloud Files-API bietet Unterstützung für Synchronisierungs Module auf eine Weise, die Entwicklern und Endbenutzern viele neue Vorteile bietet.

Die Cloud Files-API enthält die folgenden nativen Win32-APIs und Windows-Runtime (WinRT)-APIs:

* [Cloud Filter-API](cloud-filter-reference.md): diese Native Win32-API bietet Funktionen an der Grenze zwischen dem Benutzermodus und dem Dateisystem. Diese API behandelt die Erstellung und Verwaltung von Platzhalter Dateien und Verzeichnissen.
* [Windows. Storage. Provider-Namespace](/uwp/api/windows.storage.provider): Diese WinRT-API ermöglicht es Anwendungen, den cloudspeicheranbieter zu konfigurieren und den Synchronisierungs Stamm beim Betriebssystem zu registrieren.

> [!NOTE]
> Die Cloud Files-API unterstützt derzeit nicht die Implementierung von Cloud Sync Engines in UWP-apps. Cloud Sync Engines müssen in Desktop-Apps implementiert werden.

## <a name="supported-features"></a>Unterstützte Features

Die Cloud Files-API bietet die folgenden Features zum Entwickeln von Cloud-Synchronisierungs Modulen.

### <a name="placeholder-files"></a>Platzhalter Dateien

* Mithilfe von Synchronisierungs Modulen können Platzhalter Dateien erstellt werden, die für den File System-Header nur 1 KB Speicher beanspruchen und unter normalen Verwendungsbedingungen automatisch in vollständige Dateien unterteilt werden. Platzhalter Dateien, die als typische Dateien für apps und Endbenutzer in der Windows-Shell vorhanden sind.
* Platzhalter Dateien sind vertikal aus dem Windows-Kernel in die Windows-Shell integriert, und die APP-Kompatibilität mit Platzhalter Dateien ist in der Regel kein Problem. Unabhängig davon, ob Sie Dateisystem-APIs, die Eingabeaufforderung oder eine Desktop-oder UWP-App verwenden, um auf eine Platzhalter Datei zuzugreifen, wird die Datei ohne zusätzliche Codeänderungen einfriert, und die Datei kann normalerweise von der APP verwendet werden.
* Dateien können in drei Zuständen vorhanden sein:
  * **Platzhalter Datei**: eine leere Darstellung der Datei und nur verfügbar, wenn der Synchronisierungs Dienst verfügbar ist.
  * **Vollständige Datei**: die Datei wurde implizit in die Datei aufgelöst, und Sie könnte durch das System aufgeschbe werden, wenn Speicherplatz benötigt wird.
  * Angeheftete **vollständige Datei**: die Datei wurde im Datei-Explorer explizit vom Benutzer bereitgestellt und ist garantiert offline verfügbar.

In der folgenden Abbildung wird veranschaulicht, wie der Platzhalter, vollständige und angeheftete vollständige Dateistatus im Datei-Explorer angezeigt wird.

  ![Beispiel für drei Datei Zustände im Datei-Explorer](images/cloud-file-states-file-explorer.png)

### <a name="standardized-sync-root-registration"></a>Standardisierte Synchronisierungs Stamm Registrierung

* Das Registrieren eines Synchronisierungs Stamms ist unkompliziert und standardisiert. Dies schließt die Erstellung eines Branding-Knotens im Navigationsbereich des Datei-Explorers ein, wie im folgenden Screenshot gezeigt. Stämme können entweder als einzelne Einträge der obersten Ebene oder als untergeordnete Elemente einer übergeordneten Gruppierung erstellt werden.

  ![Beispiel für einen Synchronisierungs Stamm Eintrag im Datei-Explorer](images/register-sync-root-file-explorer.png)

### <a name="shell-integration"></a>Shellintegration

* Zustands Symbole:
  * Die Cloud Files-API stellt standardisierte, automatische Aktivierungs Zustands Symbole bereit, die im Datei-Explorer und auf dem Windows-Desktop angezeigt werden.
  * Zusätzlich zu den Standardsymbolen für den Windows-Status, die für den Aktivierungszustand verwendet werden, können Sie benutzerdefinierte Zustands Symbole für zusätzliche Dienst spezifische Eigenschaften bereitstellen.
  * Ersetzt Legacy-Shellerweiterungen für Symbol Überlagerung.
* Fortschrittsanzeige:
  * Wenn Sie eine Platzhalter Datei öffnen, die mehr als ein paar Sekunden für das Hydrat benötigt, wird der Aktivierungs Fortschritt angezeigt. Der Fortschritt wird in Abhängigkeit vom Kontext an einigen Orten angezeigt:
    * Im Dialogfenster "Kopier-Engine".
    * Der Inline Fortschritt wird neben der Datei im Datei-Explorer angezeigt.
    * Wenn die Datei nicht in der spezifischen Anweisung des Benutzers geöffnet ist, wird eine Popup Benachrichtigung angezeigt, um den Benutzer zu informieren und eine Möglichkeit zur Steuerung der unbeabsichtigten Aktivierungs Aktivität bereitzustellen.
* Miniaturansichten und Metadaten:
  * Platzhalter Dateien können über umfangreiche, vom Dienst bereitgestellte Miniaturansichten und erweiterte Datei Metadaten verfügen, um dem Benutzer eine nahtlose Datei-Explorer-Benutzerfunktion bereitzustellen.
* Navigationsbereich des Datei-Explorers:
  * Das Registrieren eines Synchronisierungs Stamms mit der Cloud Files-API bewirkt, dass der Synchronisierungs Stamm (mit einem Symbol und einem benutzerdefinierten Namen) im Navigationsbereich des Datei-Explorers angezeigt wird.
* Kontextmenüs im Datei-Explorer:
  * Wenn Sie einen Synchronisierungs Stamm mit der Cloud Files-API registrieren, werden im Kontextmenü des Datei-Explorers automatisch mehrere Verben (Menüeinträge) bereitstellt, mit denen der Benutzer den Aktivierungszustand der Datei steuern können.
  * Diesem Abschnitt des Kontextmenüs können zusätzliche Verben mithilfe von Desktop Bridge kompatiblen APIs hinzugefügt werden.
* Benutzer Steuerelement der Datei Aktivierung:
  * Benutzer haben immer die Kontrolle über die Datei Aktivierung, auch wenn die Dateien nicht explizit vom Benutzer aktiviert werden. Ein interaktiver Popup wird angezeigt, um den Benutzer zu warnen und Optionen anzugeben. In der folgenden Abbildung wird eine Popup Benachrichtigung für eine Metadatendatei veranschaulicht.
    ![Beispiel für einen interaktiven Toast, der für die Aktivierung der Hintergrund Datei angezeigt wird](images/file-hydration-interactive-toast.png)
  * Wenn ein Benutzer eine APP daran hindert, Dateien durch einen interaktiven Toast zu durchlaufen, kann er die Blockierung der APP auf der Seite **Automatische Dateidownloads** in den **Einstellungen** entsperren.
    ![Screenshot der Einstellung zum automatischen Herunterladen von Dateien](images/allow-automatic-file-downloads-setting.png)
* Einbinden von Kopier-Engine-Vorgängen (unterstützt in Windows 10 Insider Preview Build 19624 und höher):
  * Cloudspeicheranbieter können einen shellkopierhook zum Überwachen von Datei Vorgängen in Ihrem Synchronisierungs Stamm registrieren.
  * Der Anbieter registriert seinen kopierhook, indem er den **copyhook** -Registrierungs Wert unter Ihrem Synchronisierungs Stamm-Registrierungsschlüssel auf eine CLSID seines lokalen com-Server Objekts festlegt. Dieses lokale Server Objekt implementiert die [istorageprovidercopyhook](../shell/nn-shobjidl-istorageprovidercopyhook.md) -Schnittstelle.

### <a name="desktop-bridge"></a>Desktop-Brücke

* Synchronisierungs-Engines, die die Cloud Files-APIs verwenden, sind darauf ausgelegt, die [Desktop Bridge](/windows/uwp/porting/desktop-to-uwp-root) als Implementierungs Anforderung zu verwenden.

## <a name="cloud-mirror-sample"></a>Cloud-Spiegelungs Beispiel

Das [cloudspiegelungs Beispiel](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/CloudMirror) veranschaulicht, wie Sie eine Lösung erstellen, die die Cloud Files-API verwendet. Sie ist nicht für die Verwendung als Produktionscode vorgesehen. Es fehlt eine robuste Fehlerbehandlung und wird so geschrieben, dass es so leicht verständlich wie möglich ist. Es wird als cloudspiegelung bezeichnet, da es einfach einen lokalen Ordner auf dem lokalen Datenträger widerspiegelt. Sie geben einen Server Ordner an, der Ihren clouddateiserver und einen Client Ordner darstellen soll, der den Synchronisierungs Stamm Pfad angeben soll. Ein Knoten der obersten Ebene wird im Navigationsbereich des Datei-Explorers namens **teststorageproviderdisplayname** angezeigt, und dieser Knoten wird dem angegebenen Client Ordner zugeordnet.

Bei der Synchronisierung müssen diese Funktionen von einem vollständig entwickelten clouddateisynchronisierungs-Anbieter implementiert werden:

* Wenn die Synchronisierungs Stammdatei nur ein Platzhalter ist, ist der Dienst dafür verantwortlich, den Inhalt der Datei zur Aktivierung zu kopieren. Dies wird im Beispiel implementiert.
* Wenn die Synchronisierungs Stammdatei eine vollständige Datei ist und sich der Inhalt der Datei im clouddienst ändert, ist der Dienst für die Benachrichtigung des lokalen Synchronisierungs Clients der Änderung zuständig, und der lokale Synchronisierungs Client muss Zusammenführungen gemäß ihren eigenen Spezifikationen verarbeiten. Dies ist im Beispiel nicht implementiert.
* Wenn es sich bei der Synchronisierungs Stammdatei um eine vollständige Datei handelt und der Inhalt der Datei im Synchronisierungs Stamm Pfad (der lokale Client) geändert wird, muss der lokale Synchronisierungs Client den clouddienst Benachrichtigen und Zusammenführungen gemäß ihren eigenen Spezifikationen verarbeiten. Die Benachrichtigung über lokale Dateiänderungen ist im Beispiel implementiert, aber es wird nichts unternommen.

### <a name="use-the-sample"></a>Verwenden des Beispiels

1. Erstellen Sie zwei Ordner auf der lokalen Festplatte. Einer davon fungiert als Server und der andere als Client.
2. Fügen Sie dem Server Ordner einige Dateien hinzu. Stellen Sie sicher, dass der Client Ordner leer ist.
3. Öffnen Sie das Cloud-Spiegel Beispiel in Visual Studio. Legen Sie das Projekt **cloudmirrorpackage** als Startprojekt fest, und erstellen Sie das Beispiel, und führen Sie es aus. Wenn Sie durch das Beispiel dazu aufgefordert werden, geben Sie die beiden Pfade zu Ihren Server-und Client Ordnern ein. Anschließend wird ein Konsolenfenster mit Diagnoseinformationen angezeigt.
4. Öffnen Sie den Datei-Explorer, und vergewissern Sie sich, dass der Knoten **teststorageproviderdisplayname** und die Platzhalter für alle Dateien angezeigt werden, die Sie in den Server Ordner kopiert haben. Um eine Anwendung zu simulieren, die versucht, Dateien zu öffnen, ohne die Auswahl zu verwenden, kopieren Sie mehrere Images in den Server Ordner. Doppelklicken Sie in ihrem Stamm Ordner für die Synchronisierung auf eine dieser Elemente, und vergewissern Sie sich, dass Sie in der Öffnen Sie dann die Fotos-app. Die APP lädt benachbarte Dateien vorab in den Hintergrund, um die Wahrscheinlichkeit zu erhöhen, dass der Benutzer bei der Betrachtung der anderen Bilder keine Verzögerungen hat. Sie können sehen, dass die Hintergrund Aktivierung über ein-oder im Datei-Explorer erfolgt.
5. Klicken Sie mit der rechten Maustaste auf eine Datei im Datei-Explorer, um ein Kontextmenü anzuzeigen, und vergewissern Sie sich, dass das Menü Element **TestCommand** angezeigt wird. Wenn Sie auf dieses Menü Element klicken, wird ein Meldungs Feld angezeigt.
6. Um das Beispiel anzuhalten, legen Sie den Fokus auf die Konsolenausgabe fest, und drücken Sie **STRG + C**. Dadurch wird die Synchronisierung der Stamm Registrierung bereinigt, sodass der Anbieter deinstalliert wird. Wenn das Beispiel abstürzt, ist es möglich, dass der Synchronisierungs Stamm registriert bleibt. Dies bewirkt, dass der Datei-Explorer jedes Mal neu startet, wenn Sie auf etwas klicken, und Sie werden aufgefordert, die falschen Client-und Server Speicherorte zu erhalten. Wenn dies der Fall ist, deinstallieren Sie die **cloudmirrorpackage** -Beispielanwendung von Ihrem Computer.

### <a name="sample-architecture"></a>Beispiel Architektur

Das Beispiel ist absichtlich einfach. Statische Klassen werden verwendet, um die Übergabe von instanzzeigern unnötig zu machen. Im Beispiel sind die Hauptklassen aufgeführt:

* **Fakecloudprovider**: Diese Klasse der obersten Ebene steuert die folgenden Workerklassen:
  * **Cloudproviderregistrar**: registriert die Informationen des Synchronisierungs Stamms bei der Windows-Shell.
  * **Platz** Halter: generiert die Platzhalter Dateien im Synchronisierungs Stammpfad.
  * **Shellservices**: erstellt die Windows Shell-Anbieter für das Kontextmenü, die Miniaturansichten und andere Dienste.
  * **Cloudprovidersyncrootwatcher**: instanziiert einen Director-Watcher, um Änderungen am Synchronisierungs Stamm Pfad zu überwachen und Änderungen vorzunehmen.
  * **Filecopierwithprogress**: kopiert Dateien aus dem Server Ordner langsam in den Client Ordner, um das Herunterladen von einem echten cloudserver zu simulieren. Gibt die Statusanzeige an, sodass der Benutzer von den-und Datei-Explorer-Benutzeroberflächen etwas informativ angezeigt wird.

Zusätzlich zu den oben genannten Klassen bietet das Beispiel auch mehrere Hilfsklassen, um den Benutzer zur Eingabe von Ordnern und einigen Dienstprogrammen aufzufordern. **Testexplorercommandhandler**, **customstateprovider**, **thumbnailprovider** und **UriSource** sind Beispiele für shelldienstanbieter.

## <a name="cloud-files-api-architecture"></a>Cloud Files-API-Architektur

Der Kern des Speicher Stapels in der Cloud Files-API ist ein Dateisystem-Minifilter-Treiber namens "cldflt.sys". Dieser Treiber fungiert als Proxy zwischen den Anwendungen des Benutzers und dem Synchronisierungs Modul. Das Synchronisierungs Modul weiß, wie die Daten bei Bedarf heruntergeladen und hochgeladen werden. in diesem Fall ist es cldflt.sys, mit der Shell zu arbeiten, um Dateien so darzustellen, als wären die clouddaten lokal verfügbar.

Cldflt.sys unterstützt derzeit nur NTFS-Volumes, da es von einigen Features abhängig ist, die für NTFS spezifisch sind.

Es gibt viele Minifilter-Treiber für Dateisysteme in einem System, die auf einem bestimmten Volume gleichzeitig aktiv sein können. Die Treiber, die für die Cloud Files-API am meisten von Interesse sind, sind die antivirendateisystemfilter.

Minifilter-Treiber für Dateisysteme werden von einer speziellen Kernelmoduskomponente mit dem Namen Filter-Manager verwaltet und unterstützt. Unter vielen anderen Aufgaben ermöglicht der Filter-Manager die ungefilterte Kommunikation zwischen Filtern und Benutzermoduskomponenten über ein Konstrukt, das als filternachrichtenport bezeichnet wird.

## <a name="hydration-policies"></a>Aktivierungs Richtlinien

Windows unterstützt eine Vielzahl von [primären Aktivierungs Richtlinien](/windows/desktop/api/cfapi/ne-cfapi-cf_hydration_policy_primary) und die richtlinienmodifiziererer für [sekundäre Maßnahmen](/windows/desktop/api/cfapi/ne-cfapi-cf_hydration_policy_modifier) . Primäre Aktivierungs Richtlinien haben folgende Reihenfolge:

  **Immer voll > vollständige > Progressive > partiell**

Sowohl Anwendungen als auch Synchronisierungs Module können Ihre bevorzugte primäre Aktivierungs Richtlinie definieren. Wenn nicht angegeben, ist die standardmäßige Aktivierungs Richtlinie für Anwendungen und Synchronisierungs Module progressiv.

Die Richtlinie für die Einlösung einer Cloud-Datei wird durch die folgende Formel am Datei Öffnungs Zeitpunkt bestimmt:

  ```File hydration policy = max(app hydration policy, provider hydration policy)```

Nehmen wir beispielsweise an, dass der Benutzer versucht, eine PDF-Datei zu öffnen, die auf dem Fabrikam-cloudlaufwerk mithilfe von "Configuration Manager-Viewer" gespeichert ist, die keine bevorzugte Aktivierungs Richtlinie angibt. Die Richtlinie zur Anwendungs Aktivierung ist folglich progressiv, in diesem Fall standardmäßig. Da es sich bei Fabrikam Cloud Drive jedoch um ein vollständiges Synchronisierungs Modul handelt, wird die endgültige Aktivierungs Richtlinie für die Datei vollständig aktiviert, was dazu führt, dass die Datei beim ersten Zugriff vollständig aktiviert wird. Das gleiche Ergebnis tritt in Fällen auf, in denen das Synchronisierungs Modul eine progressive Aktivierung unterstützt, aber die bevorzugte APP ist vollständig.

Beachten Sie, dass die Datei-Aktivierungs Richtlinie nicht geändert werden kann, nachdem die Datei geöffnet wurde.

## <a name="compatibility-with-applications-that-use-reparse-points"></a>Kompatibilität mit Anwendungen, die Analyse Punkte verwenden

Die Cloud Files-API implementiert das Platzhalter System mithilfe von Analyse [Punkten](/windows/desktop/FileIO/reparse-points). Ein gängiges Missverständnis bei Analyse Punkten ist, dass Sie mit symbolischen Verknüpfungen identisch sind. Dieses fehl Konzept wird gelegentlich in Anwendungs Implementierungen widergespiegelt, und infolgedessen stoßen viele vorhandene Anwendungen beim Auftreten eines Analyse Punkts auf Fehler.

Um dieses Kompatibilitätsproblem zu mindern, verbirgt die Cloud Files-API immer Ihre Analyse Punkte aus allen Anwendungen, mit Ausnahme von Synchronisierungs Modulen und Prozessen, deren Hauptimage unter **% systemroot%** liegt. Anwendungen, die Analyse Punkte korrekt verstehen, können erzwingen, dass die Plattform clouddateien-API-Analyse Punkte mithilfe von [rtlsetprocessplaceholdercompatibilitymode](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-rtlsetprocessplaceholdercompatibilitymode) oder [rtlsetthreadprocessplaceholdercompatibilitymode](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-rtlsetthreadplaceholdercompatibilitymode)verfügbar macht.