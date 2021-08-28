---
title: Ablaufverfolgung
description: Die Ablaufverfolgung verwendet die Ereignisablaufverfolgung für Windows (ETW).
ms.assetid: b008bae2-9423-4e72-ae03-9cd50f73d812
keywords:
- Ablaufverfolgung von Webdiensten für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ace571c2639ddd1eb55ed1e4afd70bcef7318b44
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882306"
---
# <a name="tracing"></a>Ablaufverfolgung

Die Ablaufverfolgung verwendet die Ereignisablaufverfolgung für Windows (ETW). Installieren Sie das Microsoft Windows SDK von der MSDN Downloads-Website, um die in Windows Server 2008 R2 verfügbaren [Ablaufverfolgungstools zu](https://www.microsoft.com/download/details.aspx?id=8279) nutzen.


Es werden drei Ablaufverfolgungsebenen unterstützt:

-   Ausführlich (alle verfügbaren Ablaufverfolgungen).
-   Info (Informationsverfolgungen).
-   Fehler (Fehlerverfolgungen).

Die folgenden Ereignisse werden nachverfolgt:

-   Alle Fehler (Level=Error, Level=Info oder Level=Verbose).
-   Einstieg/Beenden einer API (Level=Info oder Level=Verbose).
-   Start und Abschluss einer E/A (Level=Info oder Level=Verbose)
-   Ausgetauschte SOAP-Nachrichten (Level=Verbose, verfügbar Windows 2003 SP1 und höher)

## <a name="generating-and-viewing-wwsapi-traces"></a>Generieren und Anzeigen von WWSAPI-Ablaufverfolgungen

WWSAPI verwendet die manifestbasierten Ereignisse auf Windows Vista und höher. Daher gibt es bei der Ablaufverfolgung einige Unterschiede, die auf der Betriebssystemversion basieren. Die Generierung von ETW-Ablaufverfolgungen kann mithilfe der etw-Tools auf allen unterstützten Plattformen erfolgen. Zum Anzeigen der ETW-Ablaufverfolgungen in einem guten Format sind jedoch benutzerdefinierte Tools unter Windows XP SP2 und Windows 2003 SP1 erforderlich. Abhängig von der Betriebssystemversion gibt es verschiedene Möglichkeiten, WWSAPI-ETW-Ereignisverfolgungen zu sammeln und zu anzeigen.

## <a name="enabling-and-viewing-wwsapi-traces-in-event-viewer-works-on-windows-vista-and-above"></a>Aktivieren und Anzeigen von WWSAPI-Ablaufverfolgungen in Ereignisanzeige (funktioniert mit Windows Vista und höher)

-   Führen Sie eventvwr.msc über die Befehlszeile oder das Ausführungsmenü aus.
-   Klicken Sie auf der rechten Seite im Bereich Aktionen auf den Link Ansicht, und aktivieren Sie die Option Analytische und Debugprotokolle anzeigen.
-   Navigieren Sie im linken Bereich zu Anwendungs- und Windows Microsoft Windows \\ \\ \\ WebServices-Anbieter.
-   Klicken Sie mit der rechten Maustaste auf den Ablaufverfolgungsanbieter, und wählen Sie Protokoll aktivieren aus.
-   Führen Sie Ihr Szenario aus.
-   Wenn Sie die Seite der Ereignisanzeige aktualisieren, sollten die WWSAPI-Ablaufverfolgungseinträge angezeigt werden.

## <a name="enabling-and-viewing-wwsapi-traces-using-wstracebat-script-works-on-xpsp2-and-above"></a>Aktivieren und Anzeigen von WWSAPI-Ablaufverfolgungen mit Wstrace.bat Script (funktioniert unter XPSP2 und höher)

Die wstrace.bat Batchdatei bietet eine praktische Möglichkeit für:

-   Erstellen eines Ablaufverfolgungsprotokolls
-   Löschen eines Ablaufverfolgungsprotokolls
-   Aktivieren und Deaktivieren der Ablaufverfolgung
-   Aktualisieren der Ablaufverfolgungsebene (info/error/verbose)
-   Konvertieren von Ablaufverfolgungsprotokollen in CSV-Dateien

Die Batchdatei verwendet logman.exe für alle Befehle, mit Ausnahme der Konvertierung der Protokolle in eine CSV-Datei, die ein benutzerdefiniertes Tool (wstracedump.exe.

## <a name="using-tracing-commands"></a>Verwenden von Ablaufverfolgungsbefehlen

Mit dem folgenden Befehl wird ein Protokoll erstellt, das die Ebene "Info", "Fehler" oder "Ausführlich" verwendet. Für diesen Befehl sind erhöhte Rechte erforderlich.

**wstrace.bat ausführlichen \[ Fehler \| beim Erstellen von \| Informationen\]**

Mit dem folgenden Befehl wird das Protokoll gelöscht. Für diesen Befehl sind erhöhte Rechte erforderlich.

**wstrace.bat löschen**

Der folgende Befehl aktiviert die Ablaufverfolgung. Sie müssen zunächst ein Protokoll erstellen.

**wstrace.bat on**

Die Ablaufverfolgungsebene (Info, Fehler oder ausführlich) kann wie folgt geändert werden:

**wstrace.bat update \[ info \| error \| verbose\]**

Verwenden Sie zum Abbilden der Ablaufverfolgungsausgabe den folgenden Befehl:

**wstrace.bat-> temp.csv**

Die Ereignisse werden in der CSV-Datei gespeichert, bis STRG+C gedrückt oder die Ablaufverfolgung deaktiviert wird.

## <a name="tracing-file-format"></a>Ablaufverfolgungsdateiformat

Die von wstrace.bat erstellten CSV-Dateien sind einfache textdateien, die durch Komma getrennt sind. Diese Dateien können in einem Excel, Editor usw. geöffnet werden.

Die Spalten der Datei lauten wie folgt:

-   TimeStamp: Zeitstempel der Aufzeichnung des Ereignisses
-   ProcessID: ULONG-ID des Prozesses, der das Ereignis aufzeichnen
-   ThreadID: ULONG-ID des Threads, der das Ereignis aufzeichnen
-   Ereignis: Der aufzählte Wert des Ereignistyps kann sein ("api enter" \| "api pending" \| "api ExitSyncSuccess" \| "api ExitSyncFailure" \| "api ExitAsyncSuccess" \| "api ExitAsyncFailure" \| "io started" \| "io completed" \| "io failed" \| "error" "received message \| start" "received message" \| \| "received message stop" \| "sending message start" \| "sending message" \| "sending message stop")
-   Vorgang: Der Name des aufgerufenen Vorgangs. Dies ist in der Regel der aufgerufenen API zu sehen.
-   Fehler: Optionale HRESULT-Fehlernummer
-   Info: Optionale Informationen zum Ereignis

## <a name="collecting-wwsapi-etw-trace-file-using-etw-tools-works-on-xpsp2-and-above"></a>Sammeln einer WWSAPI-ETW-Ablaufverfolgungsdatei mit etw-Tools (funktioniert unter XPSP2 und höher)

Aktivieren der ETW-Ablaufverfolgung für WWSAPI

**logman start wstrace -bs 64 -ft 1 -rt -p Microsoft-Windows-WebServices \[ flags \[ level \] \] \[ -o &lt; EtlLogFileName &gt; \] -ets**

, um die ETW-Ablaufverfolgungssitzung zu erstellen und zu starten. Logman.exe ist ein In-Box-ETW-Tool, das auf allen unterstützten Plattformen verfügbar ist. Beachten Sie, dass Sie Microsoft \_ Windows \_ WebServices als Anbieternamen für XPSP2 und W2K3 verwenden müssen. Sie können Logman-Abfrageanbieter ausführen, um die Liste der registrierten Anbieter zu sehen. Der Anbieter Microsoft-Windows-WebServices (oder Microsoft Windows WebServices) sollte aufgeführt werden, es sei denn, \_ \_ er ist nicht registriert. Der Anbieter wird normalerweise während des Setups registriert. Sie kann jedoch auch manuell registriert werden, indem wevtutil.exe im &lt; ManifestFileName (unter Windows Vista und höher) oder &gt; mofcomp.exe &lt; MofFileName &gt; (unter XPSP2 und W2K3) ausgeführt wird.

Flags können verwendet werden, um die Ablaufverfolgungen nach ihrer Art zu filtern. Dabei kann es sich um einen OR'd-Wert der folgenden Ablaufverfolgungsarten aus. Wenn nicht angegeben, sind alle Ablaufverfolgungsarten aktiviert.

-   0x1: API-Eingangs-/Beendigungsverfolgungen.
-   0x2: Fehlerverfolgungen.
-   0x4: E/A-Ablaufverfolgungen.
-   0x8: SOAP-Nachrichtenverfolgungen.
-   0x10: Binäre Nachrichtenverfolgungen.

Level kann verwendet werden, um die Ablaufverfolgungen nach ihrer Ebene zu filtern. Dies sollte einer der folgenden Werte sein. Wenn nicht angegeben, sind alle Ablaufverfolgungsebenen aktiviert.

-   0x1: Schwerwiegende Ablaufverfolgungen.
-   0x2: Fehlerverfolgungen.
-   0x3: Warnungsverfolgungen.
-   0x4: Informationsverfolgungen.
-   0x5: Ausführliche Ablaufverfolgungen.

EtlLogFileName ist der Pfad zur zu erstellenden ETW-Ereignisprotokolldatei (verwenden Sie die Erweiterung .etl). Falls nicht angegeben, wählt ETW einen zufälligen Namen aus, der später abgefragt werden kann. Diese Datei sollte sich nicht im Profilverzeichnis des Benutzers befinden. Die ETW-Ereignisprotokolldatei (ETL-Datei) hat das Binärformat. Sie kann von ETW-Anwendungen verwendet werden, hat jedoch kein lesbares Format. Im nächsten Schritt wird beschrieben, wie der Inhalt angezeigt wird.

Ausführen Ihres Szenarios

Sammeln der ETW-Ereignisprotokolldatei.

**logman stop wstrace -ets**

, um die ETW-Ablaufverfolgungssitzung zu beenden. Dies ist der Fall, wenn ETW die Protokollierung der Ereignisse beendet. Die ETW-Ereignisprotokolldatei (angegeben im EtlLogFileName-Parameter) kann verwendet werden. Sie kann entweder lokal angezeigt werden (anweisungen unten angegeben) oder zur Untersuchung an die Produktgruppe gesendet werden.

End-to-End-Beispiel mit ETW-Tools:

**logman start wstrace -bs 64 -ft 1 -rt -p Microsoft-Windows-WebServices -o mytrace.etl -ets**

**Echo.. Führen Sie Ihr Szenario aus.**

**logman stop wstrace -ets**

**tracerpt mytrace.etl -o mytrace.xml**

**wstrace.htm**

**Echo.. verwenden Sie mytrace.xml und wstrace.xsl auf der geöffneten Seite .**

## <a name="viewing-wwsapi-etw-trace-file-traces-using-wstracedumpexe-tool-works-on-windows-xp-and-above"></a>Anzeigen von WWSAPI ETW-Ablaufverfolgungsdatei-Ablaufverfolgungen mit wstracedump.exe Tool (funktioniert mit Windows XP und höher)

Wstracedump.exe ist ein benutzerdefiniertes entwickeltes ETW-Consumertool, das Ereignisse in der WWSAPI ETW-Ablaufverfolgungsdatei verarbeitet und lesbare Ausgaben für Menschen erzeugt. Die Ausgabe kann von allen unterstützten Plattformen erzeugt werden. Weitere Informationen finden Sie unter verwendung (wstracedump.exe -?).

## <a name="viewing-wwsapi-etw-trace-file-traces-using-etw-tools-works-on-windows-vista-and-above"></a>Anzeigen von WWSAPI ETW-Ablaufverfolgungsdatei-Ablaufverfolgungen mit ETW-Tools (funktioniert mit Windows Vista und höher)

Tracerpt.exe ist das Tool zum Anzeigen des Inhalts einer ETW-Ereignisprotokolldatei, das auf allen unterstützten Plattformen verfügbar ist. Sie kann verwendet werden, um CSV-, EVTX- oder XML-Dumpdateien aus einer ETW-Ereignisprotokolldatei zu generieren. Die generierte Ausgabedatei weist jedoch nur auf Windows Vista und höher lesbare Ablaufverfolgungen auf. In dieser Anleitung wird beschrieben, wie Die XML-Dumpdatei generiert und zusammen mit einer xsl-Datei verwendet wird, um die Ablaufverfolgungen in einem ansprechenden Format anzuzeigen (xsl-Datei ist sehr trivial und kann geändert werden, wenn verschiedene Formate gewünscht werden).

-   Ausführen

    **tracerpt &lt; EtlLogFileName &gt; -o &lt; OutputXMLFileName&gt;**

    , um ein XML-Dump aus der binären ETL-Datei zu erstellen (tracerpt.exe erstellt die Ausgabedatei standardmäßig im XML-Format. Ausführen von tracerpt -? Anzeigen anderer verfügbarer Formate).

-   An diesem Punkt sehen Sie die Ablaufverfolgungsinformationen in der XML-Datei. Darüber hinaus können Sie die wstrace.htm-Datei öffnen und die XML-Dumpdatei und die Datei wstrace.xsl verwenden, um die Ablaufverfolgungen in einem ansprechenderen Format anzuzeigen. Beachten Sie, dass sich die Dateien auf dem lokalen Computer befinden müssen, um diese HTML-Datei in IE verwenden zu können.

## <a name="security"></a>Sicherheit

Beim Aktivieren der Ablaufverfolgung sollten Administratoren berücksichtigen, dass zusätzlicher Speicherplatz und Rechenleistung verbraucht werden. Ein böswilliger Client oder eine Anwendung kann Systemressourcen erschöpfen, es sei denn, Ablaufverfolgungseinstellungen sind mit angemessenen Grenzwerten konfiguriert. Bei Verwendung des Features für die Nachrichtenablaufverfolgung können Nachrichten, die vertrauliche Informationen wie Anmeldeinformationen, persönliche Informationen usw. enthalten, auf dem Datenträger gespeichert oder von jedem Benutzer angezeigt werden, der Zugriff auf die Systemereignisanzeige hat. Um dieses Problem zu beheben, kann die Ablaufverfolgung von System- oder Administratorbenutzern auf Windows 2003 und höher aktiviert werden. Die Nachrichtenablaufverfolgung ist auf Windows XP deaktiviert, auf dem jeder Benutzer die Ablaufverfolgung aktivieren kann.

Die folgende Enumeration wird bei der Ablaufverfolgung verwendet:

-   [**\_WS-ABLAUFVERFOLGUNGS-API \_**](/windows/desktop/api/WebServices/ne-webservices-ws_trace_api)

 

 




