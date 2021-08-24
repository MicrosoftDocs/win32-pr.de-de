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
ms.openlocfilehash: da2bcd5c07c2c5ebf3a28620e39efe3034d3c2bc024ac487caaec38e3c69fca9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707260"
---
# <a name="tracing"></a>Ablaufverfolgung

Die Ablaufverfolgung verwendet die Ereignisablaufverfolgung für Windows (ETW). Um die mit Windows Server 2008 R2 verfügbaren Ablaufverfolgungstools nutzen zu können, installieren Sie das Microsoft Windows SDK von der [MSDN Downloads-Website.](https://www.microsoft.com/download/details.aspx?id=8279)


Es werden drei Ablaufverfolgungsebenen unterstützt:

-   Ausführlich (alle verfügbaren Ablaufverfolgungen).
-   Info (Informationsablaufverfolgungen).
-   Fehler (Fehlerablaufverfolgungen).

Die folgenden Ereignisse werden nachverfolgt:

-   Alle Fehler (Level=Error, Level=Info oder Level=Verbose).
-   Eintrag/Beendigung einer API (Level=Info oder Level=Verbose).
-   Start und Abschluss einer beliebigen E/A (Level=Info oder Level=Verbose)
-   Ausgetauschte SOAP-Nachrichten (Level=Verbose, verfügbar ab Windows 2003 SP1)

## <a name="generating-and-viewing-wwsapi-traces"></a>Generieren und Anzeigen von WWSAPI-Ablaufverfolgungen

WWSAPI verwendet die manifestbasierten Ereignisse für Windows Vista und höher. Daher weist die Ablaufverfolgung einige Unterschiede basierend auf der Betriebssystemversion auf. Das Generieren von ETW-Ablaufverfolgungen kann mithilfe der in der Box ausgeführten ETW-Tools auf allen unterstützten Plattformen erfolgen. Das Anzeigen der ETW-Ablaufverfolgungen in einem ansprechenden Format erfordert jedoch benutzerdefinierte Tools für Windows XP SP2 und Windows 2003 SP1. Je nach Betriebssystemversion gibt es verschiedene Möglichkeiten zum Sammeln und Anzeigen von WWSAPI-ETW-Ereignisablaufverfolgungen.

## <a name="enabling-and-viewing-wwsapi-traces-in-event-viewer-works-on-windows-vista-and-above"></a>Aktivieren und Anzeigen von WWSAPI-Ablaufverfolgungen in Ereignisanzeige (funktioniert mit Windows Vista und höher)

-   Führen Sie eventvwr.msc über die Befehlszeile oder das Ausführungsmenü aus.
-   Klicken Sie auf den Link Ansicht im Bereich Aktionen auf der rechten Seite, und aktivieren Sie die Option Analyse- und Debugprotokolle anzeigen.
-   Navigieren Sie im linken Bereich zu Anwendungs- und Dienstprotokolle \\ Microsoft \\ Windows \\ WebServices-Anbieter.
-   Klicken Sie mit der rechten Maustaste auf den Ablaufverfolgungsanbieter, und wählen Sie Protokoll aktivieren aus.
-   Führen Sie Ihr Szenario aus.
-   Wenn Sie die Ereignisanzeigeseite aktualisieren, sollten die WWSAPI-Ablaufverfolgungseinträge angezeigt werden.

## <a name="enabling-and-viewing-wwsapi-traces-using-wstracebat-script-works-on-xpsp2-and-above"></a>Aktivieren und Anzeigen von WWSAPI-Ablaufverfolgungen mit Wstrace.bat Script (funktioniert unter XPSP2 und höher)

Die wstrace.bat Batchdatei bietet eine praktische Möglichkeit für Folgendes:

-   Erstellen eines Ablaufverfolgungsprotokolls
-   Löschen eines Ablaufverfolgungsprotokolls
-   Aktivieren und Deaktivieren der Ablaufverfolgung
-   Aktualisieren der Ablaufverfolgungsebene (Info/Fehler/ausführlich)
-   Konvertieren von Ablaufverfolgungsprotokollen in CSV-Dateien

Die Batchdatei verwendet logman.exe für alle Befehle, mit Ausnahme der Konvertierung der Protokolle in eine CSV-Datei, die ein benutzerdefiniertes Tool (wstracedump.exe) erfordert.

## <a name="using-tracing-commands"></a>Verwenden von Ablaufverfolgungsbefehlen

Mit dem folgenden Befehl wird ein Protokoll erstellt, das Informationen, Fehler oder ausführliche Informationen verwendet. Für diesen Befehl sind erhöhte Rechte erforderlich.

**wstrace.bat Fehler beim Erstellen von \[ Informationen \| \| ausführlich\]**

Mit dem folgenden Befehl wird das Protokoll gelöscht. Für diesen Befehl sind erhöhte Rechte erforderlich.

**wstrace.bat löschen**

Der folgende Befehl aktiviert die Ablaufverfolgung. Sie müssen zunächst ein Protokoll erstellen.

**wstrace.bat ein**

Die Ablaufverfolgungsebene (Info, Fehler oder ausführlich) kann wie folgt geändert werden:

**wstrace.bat \[ \| Updateinformationsfehler \| ausführlich\]**

Verwenden Sie den folgenden Befehl, um die Ablaufverfolgungsausgabe zu dumpen:

**wstrace.bat dump > temp.csv**

Die Ereignisse werden in die CSV-Datei ausgegeben, bis STRG+C gedrückt oder die Ablaufverfolgung deaktiviert ist.

## <a name="tracing-file-format"></a>Format der Ablaufverfolgungsdatei

Die von wstrace.bat erstellten CSV-Dateien sind einfache Textdateien mit kommastrennten Variablen. Diese Dateien können in Excel, Editor usw. geöffnet werden.

Die Spalten der Datei sind wie folgt:

-   TimeStamp: Zeitstempel der Aufzeichnung des Ereignisses
-   ProcessID: ULONG-ID des Prozesses, der das Ereignis aufzeichnet
-   ThreadID: ULONG-ID des Threads, der das Ereignis aufzeichnet
-   Ereignis: Der aufzählende Wert des Ereignistyps kann sein("api enter" \| "api pending" \| "api ExitSyncSuccess" \| "api ExitSyncFailure" \| "api ExitAsyncSuccess" \| "api ExitAsyncFailure" \| "io started" \| "io completed" \| "io failed" \| "error" \| "received message start" \| "received message" \| "received message stop" \| "sending message start" "sending message start" \| \| "sending message stop")
-   Vorgang: Der Name des vorgangs, der aufgerufen wird. In der Regel wird dies der aufgerufenen API zugeordnet.
-   Fehler: Optionale HRESULT-Fehlernummer
-   Info: Optionale Informationen zum Ereignis

## <a name="collecting-wwsapi-etw-trace-file-using-etw-tools-works-on-xpsp2-and-above"></a>Sammeln der WWSAPI-ETW-Ablaufverfolgungsdatei mit ETW-Tools (funktioniert unter XPSP2 und höher)

Aktivieren der ETW-Ablaufverfolgung für WWSAPI

**logman start wstrace -bs 64 -ft 1 -rt -p Microsoft-Windows-WebServices \[ flags \[ level \] \] \[ -o <EtlLogFileName> \] -ets**

, um die ETW-Ablaufverfolgungssitzung zu erstellen und zu starten. Logman.exe ist ein sofort einsatzbereites ETW-Tool, das auf allen unterstützten Plattformen verfügbar ist. Beachten Sie, dass Sie Microsoft \_ Windows \_ WebServices als Anbieternamen für XPSP2 und W2K3 verwenden müssen. Sie können logman-Abfrageanbieter ausführen, um die Liste der registrierten Anbieter anzuzeigen. Der Anbieter Microsoft-Windows-WebServices (oder Microsoft \_ Windows \_ WebServices) sollte aufgeführt werden, es sei denn, er ist nicht registriert. Der Anbieter wird normalerweise während des Setups registriert. Sie kann jedoch auch manuell registriert werden, indem Sie wevtutil.exe im <ManifestFileName> (auf Windows Vista und höher) oder mofcomp.exe <MofFileName> (auf XPSP2 und W2K3) ausführen.

Flags können verwendet werden, um die Ablaufverfolgungen nach ihrer Art zu filtern. Dies kann der WERT OR der folgenden Ablaufverfolgungsarten sein. Wenn sie nicht angegeben wird, sind alle Ablaufverfolgungsarten aktiviert.

-   0x1: API-Ablaufverfolgungen zum Ein-/Beenden.
-   0x2: Fehlerablaufverfolgungen.
-   0x4: E/A-Ablaufverfolgungen.
-   0x8: SOAP-Nachrichtenablaufverfolgungen.
-   0x10: Binäre Nachrichtenablaufverfolgungen.

Die Ebene kann verwendet werden, um die Ablaufverfolgungen nach ihrer Ebene zu filtern. Dies sollte einer der folgenden Werte sein. Wenn sie nicht angegeben wird, sind alle Ablaufverfolgungsebenen aktiviert.

-   0x1: Schwerwiegende Ablaufverfolgungen.
-   0x2: Fehlerablaufverfolgungen.
-   0x3: Warnungsablaufverfolgungen.
-   0x4: Informationsablaufverfolgungen.
-   0x5: Ausführliche Ablaufverfolgungen.

EtlLogFileName ist der Pfad zur etw-Ereignisprotokolldatei, die erstellt werden soll (verwenden Sie die Erweiterung .etl). Wenn keine Angabe erfolgt, wählt ETW einen zufälligen Namen aus, der später abgefragt werden kann. Diese Datei sollte sich nicht im Profilverzeichnis des Benutzers befinden. Die ETW-Ereignisprotokolldatei (ETL-Datei) hat das Binärformat. Sie kann von ETW-Anwendungen genutzt werden, hat aber kein lesbares Format. Im nächsten Schritt wird beschrieben, wie der Inhalt angezeigt wird.

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

Wstracedump.exe ist ein benutzerdefiniertes entwickeltes ETW-Consumertool, das Ereignisse in der WWSAPI-ETW-Ablaufverfolgungsdatei verarbeitet und lesbare Ausgaben erzeugt. Die Ausgabe kann von allen unterstützten Plattformen erzeugt werden. Weitere Informationen finden Sie unter verwendung (wstracedump.exe -?).

## <a name="viewing-wwsapi-etw-trace-file-traces-using-etw-tools-works-on-windows-vista-and-above"></a>Anzeigen von WWSAPI ETW-Ablaufverfolgungsdatei-Ablaufverfolgungen mit ETW-Tools (funktioniert mit Windows Vista und höher)

Tracerpt.exe ist das Tool zum Anzeigen des Inhalts einer ETW-Ereignisprotokolldatei, das auf allen unterstützten Plattformen verfügbar ist. Sie kann verwendet werden, um CSV-, EVTX- oder XML-Dumpdateien aus einer ETW-Ereignisprotokolldatei zu generieren. Die generierte Ausgabedatei verfügt jedoch nur über lesbare Ablaufverfolgungen für Windows Vista und höher. In dieser Anleitung wird beschrieben, wie Die XML-Dumpdatei generiert und zusammen mit einer xsl-Datei verwendet wird, um die Ablaufverfolgungen in einem ansprechenden Format anzuzeigen (xsl-Datei ist sehr trivial und kann geändert werden, wenn verschiedene Formate gewünscht werden).

-   Ausführen

    **tracerpt <EtlLogFileName> -o <OutputXMLFileName>**

    , um ein XML-Dump aus der binären ETL-Datei zu erstellen (tracerpt.exe erstellt die Ausgabedatei standardmäßig im XML-Format. Ausführen von tracerpt -? Anzeigen anderer verfügbarer Formate).

-   An diesem Punkt sehen Sie die Ablaufverfolgungsinformationen in der XML-Datei. Darüber hinaus können Sie die wstrace.htm-Datei öffnen und die XML-Dumpdatei und die Datei wstrace.xsl verwenden, um die Ablaufverfolgungen in einem ansprechenderen Format anzuzeigen. Beachten Sie, dass sich die Dateien auf dem lokalen Computer befinden müssen, um diese HTML-Datei in IE verwenden zu können.

## <a name="security"></a>Sicherheit

Beim Aktivieren der Ablaufverfolgung sollten Administratoren berücksichtigen, dass zusätzlicher Speicherplatz und Rechenleistung verbraucht werden. Ein böswilliger Client oder eine Anwendung kann Systemressourcen erschöpfen, es sei denn, Ablaufverfolgungseinstellungen sind mit angemessenen Grenzwerten konfiguriert. Bei Verwendung des Features für die Nachrichtenablaufverfolgung können Nachrichten, die vertrauliche Informationen wie Anmeldeinformationen, persönliche Informationen usw. enthalten, auf dem Datenträger gespeichert oder von jedem Benutzer angezeigt werden, der Zugriff auf die Systemereignisanzeige hat. Um dieses Problem zu beheben, kann die Ablaufverfolgung von System- oder Administratorbenutzern auf Windows 2003 und höher aktiviert werden. Die Nachrichtenablaufverfolgung ist auf Windows XP deaktiviert, auf dem jeder Benutzer die Ablaufverfolgung aktivieren kann.

Die folgende Enumeration wird bei der Ablaufverfolgung verwendet:

-   [**\_WS-ABLAUFVERFOLGUNGS-API \_**](/windows/desktop/api/WebServices/ne-webservices-ws_trace_api)

 

 




