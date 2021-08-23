---
description: Erfahren Sie, wie Sie mithilfe der Clouddatei-API ein Clouddateisynchronisierungsmodul erstellen, das Platzhalterdateien verwendet.
title: Erstellen eines Cloudsynchronisierungsmoduls, das Platzhalterdateien unterstützt
ms.topic: article
ms.date: 11/12/2020
ms.openlocfilehash: d7d1efae4a56e6f52473002953730fb9f1f9459f1ed8dc82e0ba75ddebf05dc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551577"
---
# <a name="build-a-cloud-sync-engine-that-supports-placeholder-files"></a>Erstellen eines Cloudsynchronisierungsmoduls, das Platzhalterdateien unterstützt

Ein Synchronisierungsmodul ist ein Dienst, der Dateien synchronisiert, in der Regel zwischen einem Remotehost und einem lokalen Client. Synchronisierungsmodule auf Windows stellen diese Dateien dem Benutzer häufig über das Windows Dateisystem und den Datei-Explorer vor. Vor Windows 10 Version 1709 war die Unterstützung des Synchronisierungsmoduls in Windows auf szenariounabhängige Ad-hoc-Oberflächen beschränkt, z. B. den Navigationsbereich des Datei-Explorers, die Windows Taskleiste und (für weitere technische Anwendungen) Dateisystemfiltertreiber.

Windows 10 Version 1709 (auch als Fall Creators Update bezeichnet) wurde die *Clouddateien-API* eingeführt. Diese API ist eine neue Plattform, die die Unterstützung für Synchronisierungsmodule formalisiert. Die Clouddateien-API bietet Unterstützung für Synchronisierungs-Engines auf eine Weise, die Entwicklern und Endbenutzern viele neue Vorteile bietet.

Die Clouddateien-API enthält die folgenden nativen Win32-APIs und WinRT-APIs (Windows Runtime):

* [Cloudfilter-API:](cloud-filter-reference.md)Diese native Win32-API bietet Funktionen an der Grenze zwischen dem Benutzermodus und dem Dateisystem. Diese API übernimmt die Erstellung und Verwaltung von Platzhalterdateien und Verzeichnissen.
* [Windows. Storage. Anbieternamespace:](/uwp/api/windows.storage.provider)Mit dieser WinRT-API können Anwendungen den Cloudspeicheranbieter konfigurieren und den Synchronisierungsstamm beim Betriebssystem registrieren.

> [!NOTE]
> Die Clouddateien-API unterstützt derzeit nicht die Implementierung von Cloudsynchronisierungs-Engines in UWP-Apps. Cloudsynchronisierungsmodule müssen in Desktop-Apps implementiert werden.

## <a name="supported-features"></a>Unterstützte Features

Die Clouddateien-API bietet die folgenden Features zum Erstellen von Cloudsynchronisierungs-Engines.

### <a name="placeholder-files"></a>Platzhalterdateien

* Synchronisierungsmodule können Platzhalterdateien erstellen, die nur 1 KB Speicher für den Dateisystemheader belegen und unter normalen Verwendungsbedingungen automatisch in vollständige Dateien hydratisiert werden. Platzhalterdateien, die als typische Dateien für Apps und Endbenutzer in der Windows Shell dargestellt werden.
* Platzhalterdateien werden vertikal vom Windows Kernel bis zur Windows Shell integriert, und die App-Kompatibilität mit Platzhalterdateien ist im Allgemeinen kein Problem. Unabhängig davon, ob Sie Dateisystem-APIs, die Eingabeaufforderung oder einen Desktop oder eine UWP-App verwenden, um auf eine Platzhalterdatei zuzugreifen, wird die Datei ohne zusätzliche Codeänderungen hydratisiert, und diese App kann die Datei normal verwenden.
* Dateien können in drei Zuständen vorhanden sein:
  * **Platzhalterdatei:** Eine leere Darstellung der Datei und nur verfügbar, wenn der Synchronisierungsdienst verfügbar ist.
  * **Vollständige Datei:** Die Datei wurde implizit aktiviert und kann vom System dehydratisiert werden, wenn Speicherplatz benötigt wird.
  * **Angeheftete vollständige Datei:** Die Datei wurde explizit vom Benutzer über den Datei-Explorer aktiviert und ist garantiert offline verfügbar.

Die folgende Abbildung zeigt, wie der Platzhalter, der vollständige und der angeheftete vollständige Dateizustände im Datei-Explorer angezeigt werden.

  ![Beispiel für drei Dateizustände im Datei-Explorer](images/cloud-file-states-file-explorer.png)

### <a name="standardized-sync-root-registration"></a>Standardisierte Synchronisierungsstammregistrierung

* Das Registrieren eines Synchronisierungsstamms ist einfach und standardisiert. Dies schließt die Erstellung eines Knotens mit Branding im Navigationsbereich des Datei-Explorers ein, wie im folgenden Screenshot gezeigt. Stammarten können entweder als einzelne Einträge der obersten Ebene oder als untergeordnete Elemente einer übergeordneten Gruppierung erstellt werden.

  ![Beispiel für einen Synchronisierungsstammeintrag im Datei-Explorer](images/register-sync-root-file-explorer.png)

### <a name="shell-integration"></a>Shellintegration

* Statussymbole:
  * Die Clouddateien-API bietet standardisierte Symbole für den automatischen Zustand der Hydratisierung, die im Datei-Explorer und auf dem Windows Desktop angezeigt werden.
  * Zusätzlich zu den standardmäßigen Windows Zustandssymbolen, die für den Zustand der Hydratisierung verwendet werden, können Sie benutzerdefinierte Zustandssymbole für zusätzliche dienstspezifische Eigenschaften bereitstellen.
  * Ersetzt Legacysymbolüberlagerungs-Shellerweiterungen.
* Statusanzeige:
  * Wenn Sie eine Platzhalterdatei öffnen, deren Hydratisierung mehr als einige Sekunden dauert, wird der Fortschritt der Hydratisierung angezeigt. Der Fortschritt wird je nach Kontext an einigen Stellen angezeigt:
    * In einem Dialogfeld der Kopier-Engine.
    * Der Inlinefortschritt wird neben der Datei im Datei-Explorer angezeigt.
    * Wenn die Datei nicht in der spezifischen Anweisung des Benutzers geöffnet wird, wird eine Popupbenachrichtigung angezeigt, um den Benutzer zu informieren und eine Möglichkeit zum Steuern der unbeabsichtigten Aktivität zur Hydration bereitzustellen.
* Miniaturansichten und Metadaten:
  * Platzhalterdateien können umfassende vom Dienst bereitgestellte Miniaturansichten und erweiterte Dateimetadaten enthalten, um dem Benutzer eine nahtlose Datei-Explorer-Erfahrung zu bieten.
* Navigationsbereich des Datei-Explorers:
  * Das Registrieren eines Synchronisierungsstamms bei der Clouddatei-API bewirkt, dass dieser Synchronisierungsstamm (mit einem Symbol und benutzerdefiniertem Namen) im Navigationsbereich des Datei-Explorers angezeigt wird.
* Kontextmenüs des Datei-Explorers:
  * Das Registrieren eines Synchronisierungsstamms bei der Clouddatei-API stellt automatisch mehrere Verben (Menüeinträge) im Kontextmenü des Datei-Explorers bereit, mit denen der Benutzer den Zustand der Hydratation seiner Datei steuern kann.
  * Diesem Abschnitt des Kontextmenüs können mit Desktop-Brücke kompatiblen APIs zusätzliche Verben hinzugefügt werden.
* Benutzersteuerung der Dateihydratisierung:
  * Benutzer haben immer die Kontrolle über die Dateihydratisierung, auch wenn die Dateien nicht explizit vom Benutzer aktiviert werden. Ein interaktives Popup wird für die Hintergrundhydratisierung angezeigt, um den Benutzer zu warnen und Optionen bereitzustellen. Die folgende Abbildung zeigt eine Popupbenachrichtigung für eine hydratisierende Datei.
    ![Beispiel für ein interaktives Popup für die Hintergrunddateihydratation](images/file-hydration-interactive-toast.png)
  * Wenn ein Benutzer verhindert, dass eine App Dateien über ein interaktives Popup aktiviert, kann er die Blockierung der App auf der Seite **Automatische Dateidownloads** in **Einstellungen** aufheben.
    ![Screenshot der Einstellung für automatische Dateidownloads](images/allow-automatic-file-downloads-setting.png)
* Verknüpfen von Kopiermodulvorgängen (unterstützt in Windows 10 Insider Preview Build 19624 und höher):
  * Cloudspeicheranbieter können einen Shell-Kopierhook zum Überwachen von Dateivorgängen in ihrem Synchronisierungsstamm registrieren.
  * Der Anbieter registriert den Kopierhook, indem er den **CopyHook-Registrierungswert** unter dem Synchronisierungsstammregistrierungsschlüssel auf die CLSID seines lokalen COM-Serverobjekts festlegt. Dieses lokale Serverobjekt implementiert die [IStorageProviderCopyHook-Schnittstelle.](../shell/nn-shobjidl-istorageprovidercopyhook.md)

### <a name="desktop-bridge"></a>Desktop-Brücke

* Synchronisierungsmodule, die cloudbasierte Datei-APIs verwenden, sind so konzipiert, dass sie die [Desktop-Brücke](/windows/uwp/porting/desktop-to-uwp-root) als Implementierungsanforderung verwenden.

## <a name="cloud-mirror-sample"></a>Cloudspiegel-Beispiel

Das [Cloudspiegelungsbeispiel](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/CloudMirror) veranschaulicht, wie Sie eine Lösung erstellen, die die Clouddateien-API verwendet. Sie ist nicht für die Verwendung als Produktionscode vorgesehen. Es fehlt eine stabile Fehlerbehandlung, und sie ist so geschrieben, dass sie so leicht wie möglich verständlich ist. Sie wird als Cloudspiegel bezeichnet, da sie einfach einen lokalen Ordner auf Ihrem lokalen Datenträger spiegelt. Sie geben einen Serverordner an, der ihren Clouddateiserver darstellen soll, und einen Clientordner, der den Stammpfad der Synchronisierung angeben soll. Im Datei-Explorer wird im Navigationsbereich ein Knoten der obersten Ebene mit dem Namen **TestStorageProviderDisplayName** angezeigt, und dieser Knoten wird dem angegebenen Clientordner zugeordnet.

Bei der Synchronisierung muss ein vollständig entwickelter Clouddateisynchronisierungsanbieter Folgendes implementieren:

* Wenn die Synchronisierungsstammdatei nur ein Platzhalter ist, ist der Dienst dafür verantwortlich, den Inhalt der Datei für die Hydration zu kopieren. Dies wird im Beispiel implementiert.
* Wenn es sich bei der Synchronisierungsstammdatei um eine vollständige Datei handelt und sich der Inhalt der Datei im Clouddienst ändert, ist der Dienst dafür verantwortlich, den lokalen Synchronisierungsclient über die Änderung zu benachrichtigen, und der lokale Synchronisierungsclient muss Merges gemäß ihren eigenen Spezifikationen verarbeiten. Dies ist im Beispiel nicht implementiert.
* Wenn es sich bei der Synchronisierungsstammdatei um eine vollständige Datei handelt und sich der Inhalt der Datei im Synchronisierungsstammpfad (der lokale Client) ändert, muss der lokale Synchronisierungsclient den Clouddienst benachrichtigen und Zusammenführungen gemäß ihren eigenen Spezifikationen verarbeiten. Die lokale Dateiänderungsbenachrichtigung wird im Beispiel implementiert, aber sie führt keinerlei Maßnahmen aus.

### <a name="use-the-sample"></a>Verwenden des Beispiels

1. Erstellen Sie zwei Ordner auf Ihrer lokalen Festplatte. Eine davon fungiert als Server und die andere als Client.
2. Fügen Sie dem Serverordner einige Dateien hinzu. Stellen Sie sicher, dass der Clientordner leer ist.
3. Öffnen Sie das Cloudspiegelungs-Beispiel in Visual Studio. Legen Sie das **CloudMirrorPackage-Projekt** als Startprojekt fest, und erstellen Sie dann das Beispiel, und führen Sie es aus. Wenn Sie vom Beispiel dazu aufgefordert werden, geben Sie die beiden Pfade zu Ihrem Server und Ihren Clientordnern ein. Danach wird ein Konsolenfenster mit Diagnoseinformationen angezeigt.
4. Öffnen Sie den Datei-Explorer, und vergewissern Sie sich, dass der Knoten **TestStorageProviderDisplayName** und die Platzhalter für alle Dateien angezeigt werden, die Sie in den Serverordner kopiert haben. Um eine Anwendung zu simulieren, die versucht, Dateien zu öffnen, ohne die Auswahl zu verwenden, kopieren Sie mehrere Bilder in den Serverordner. Doppelklicken Sie auf einen dieser Dateien in Ihrem Synchronisierungsstammordner, und vergewissern Sie sich, dass er aktiviert wird. Öffnen Sie dann die Fotos-App. Die App lädt angrenzende Dateien vorab im Hintergrund, um die Wahrscheinlichkeit zu verbessern, dass der Benutzer beim Durchsehen der anderen Bilder keine Verzögerungen feststellen kann. Sie können die Hintergrunddehydratation über Popups oder im Datei-Explorer beobachten.
5. Klicken Sie im Datei-Explorer mit der rechten Maustaste auf eine Datei, um ein Kontextmenü aufzurufen, und vergewissern Sie sich, dass das Menüelement **TestCommand** angezeigt wird. Wenn Sie auf dieses Menüelement klicken, wird ein Meldungsfeld angezeigt.
6. Um das Beispiel zu beenden, legen Sie den Fokus auf die Konsolenausgabe fest, und drücken **Sie STRG+C.** Dadurch wird die Stammregistrierung der Synchronisierung bereinigt, sodass der Anbieter deinstalliert wird. Wenn das Beispiel abstürzt, bleibt der Synchronisierungsstamm möglicherweise registriert. Dies führt dazu, dass der Datei-Explorer jedes Mal neu gestartet wird, wenn Sie auf etwas klicken, und Sie werden zur Eingabe der falschen Client- und Serverspeicherorte aufgefordert. Deinstallieren Sie in diesem Fall die **CloudMirrorPackage-Beispielanwendung** von Ihrem Computer.

### <a name="sample-architecture"></a>Beispielarchitektur

Das Beispiel ist absichtlich einfach. Sie verwendet statische Klassen, um das Übergeben von Instanzzeigern überflüssig zu machen. Hier sind die Hauptklassen im Beispiel:

* **FakeCloudProvider:** Diese Klasse der obersten Ebene steuert die folgenden Workerklassen:
  * **CloudProviderRegistrar:** Registriert die Synchronisierungsstamminformationen bei der Windows Shell.
  * **Platzhalter:** Generiert die Platzhalterdateien im Stammpfad der Synchronisierung.
  * **ShellServices:** Erstellt die Windows Shell-Anbieter für das Kontextmenü, Miniaturansichten und andere Dienste.
  * **CloudProviderSyncRootWatcher:** Instanziiert einen DirectoryWatcher, um Änderungen am Stammpfad der Synchronisierung zu überwachen und auf Änderungen zu reagieren.
  * **FileCopierWithProgress:** Kopiert Dateien aus dem Serverordner langsam in Blöcke in den Clientordner, um zu simulieren, dass sie von einem echten Cloudserver heruntergeladen werden. Stellt Statusanzeige bereit, damit Popups und die Benutzeroberfläche des Datei-Explorers dem Benutzer etwas Informatives anzeigen.

Zusätzlich zu den oben genannten Klassen stellt das Beispiel auch mehrere Hilfsklassen bereit, um den Benutzer zur Eingabe von Ordnern und einigen Hilfsprogrammen aufzufordern. **TestExplorerCommandHandler,** **CustomStateProvider,** **ThumbnailProvider** und **UriSource** sind Beispiele für Shell-Dienstanbieter.

## <a name="cloud-files-api-architecture"></a>Api-Architektur für Clouddateien

Der Kern des Speicherstapels in der Clouddatei-API ist ein Dateisystem-Minifiltertreiber namens cldflt.sys. Dieser Treiber fungiert als Proxy zwischen den Anwendungen des Benutzers und Ihrem Synchronisierungsmodul. Ihr Synchronisierungsmodul weiß, wie die Daten bei Bedarf heruntergeladen und hochgeladen werden, während es für cldflt.sys verantwortlich ist, mit der Shell zusammenzuarbeiten, um Dateien so darzustellen, als wären die Clouddaten lokal verfügbar.

Cldflt.sys unterstützt derzeit nur NTFS-Volumes, da sie von einigen für NTFS spezifischen Features abhängig sind.

Es gibt viele Dateisystem-Minifiltertreiber in einem System, die gleichzeitig auf einem bestimmten Volume aktiv sein können. Die Treiber, die für die Clouddateien-API am wichtigsten sind, sind die Virenschutz-Dateisystemfilter.

Dateisystem-Minifiltertreiber werden von einer speziellen Kernelmoduskomponente namens Filter-Manager verwaltet und unterstützt. Neben vielen anderen Aufgaben ermöglicht der Filter-Manager die ungefilterte Kommunikation zwischen Filtern und Benutzermoduskomponenten über ein Konstrukt, das als Filtermeldungsport bezeichnet wird.

## <a name="hydration-policies"></a>Richtlinien für die Hydratisierung

Windows unterstützt eine Vielzahl von Richtlinien für [primäre Und](/windows/desktop/api/cfapi/ne-cfapi-cf_hydration_policy_primary) sekundäre Richtlinienmodifizierer für [die Hydratisierung.](/windows/desktop/api/cfapi/ne-cfapi-cf_hydration_policy_modifier) Primäre Richtlinien für die Hydratisierung weisen diese Reihenfolge auf:

  **Immer vollständig > Vollständige > Progressive > Partial**

Sowohl Anwendungen als auch Synchronisierungsmodule können ihre bevorzugte primäre Hydrationsrichtlinie definieren. Wenn keine Angabe erfolgt, ist die Standardmäßige Richtlinie zur Hydratisierung sowohl für Anwendungen als auch für Synchronisierungsmodule progressiv.

Die Hydrationsrichtlinie einer Clouddatei wird zum Zeitpunkt der Dateiöffnung durch diese Formel bestimmt:

  ```File hydration policy = max(app hydration policy, provider hydration policy)```

Nehmen wir beispielsweise an, dass der Benutzer versucht, eine PDF-Datei zu öffnen, die mithilfe des Contoso PDF-Viewers auf Fabrikam Cloud Drive gespeichert ist, der keine bevorzugte Richtlinie für die Hydratisierung angibt. Die Richtlinie für die Anwendungshydratisierung ist daher die progressive Hydration, in diesem Fall standardmäßig. Da Fabrikam Cloud Drive jedoch ein Synchronisierungsmodul für vollständige Hydratisierung ist, wird die endgültige Richtlinie für die Hydratisierung der Datei zu einer vollständigen Hydratisierung, was dazu führt, dass die Datei beim ersten Zugriff vollständig aktiviert wird. Das gleiche Ergebnis tritt in Fällen auf, in denen das Synchronisierungsmodul die progressive Hydration unterstützt, die App jedoch die vollständige Hydration bevorzugt.

Beachten Sie, dass die Dateihydratisierungsrichtlinie nach dem Öffnen der Datei nicht mehr geändert werden kann.

## <a name="compatibility-with-applications-that-use-reparse-points"></a>Kompatibilität mit Anwendungen, die Wiederholungspunkte verwenden

Die Clouddateien-API implementiert das Platzhaltersystem mithilfe von [Wiederholungspunkten.](/windows/desktop/FileIO/reparse-points) Ein häufiges Missverständnis hinsichtlich der Fehler bei der Neuplanung von Punkten ist, dass sie mit symbolischen Verknüpfungen identisch sind. Dieses Missverständnis wird gelegentlich in Anwendungsimplementierungen widergespiegelt, und infolgedessen treten bei vielen vorhandenen Anwendungen Fehler auf, wenn ein Beliebiger Wiederholungspunkt auftritt.

Um dieses Kompatibilitätsproblem zu beheben, blendet die Clouddatei-API ihre Wiederholungspunkte immer in allen Anwendungen aus, mit Ausnahme von Synchronisierungs-Engines und Prozessen, deren Hauptimage sich unter **%systemroot%** befindet. Anwendungen, die die Fehlerpunkte richtig verstehen, können die Plattform zwingen, API-Nachschlagepunkte für Clouddateien mithilfe von [RtlSetProcessPlaceholderCompatibilityMode](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-rtlsetprocessplaceholdercompatibilitymode) oder [RtlSetThreadProcessPlaceholderCompatibilityMode](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-rtlsetthreadplaceholdercompatibilitymode)verfügbar zu machen.