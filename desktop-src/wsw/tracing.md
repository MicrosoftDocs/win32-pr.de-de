---
title: Ablaufverfolgung
description: Die Ablauf Verfolgung verwendet die Ereignis Ablauf Verfolgung für Windows (ETW).
ms.assetid: b008bae2-9423-4e72-ae03-9cd50f73d812
keywords:
- Ablauf Verfolgung von Webdiensten für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c660884667cefae8067376075a30cbc41f70d4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104391238"
---
# <a name="tracing"></a>Ablaufverfolgung

Die Ablauf Verfolgung verwendet die Ereignis Ablauf Verfolgung für Windows (ETW). Wenn Sie die in Windows Server 2008 R2 verfügbaren Ablauf Verfolgungs Tools nutzen möchten, installieren Sie die Microsoft Windows SDK von der [MSDN-Download](https://www.microsoft.com/download/details.aspx?id=8279) Website.


Es werden drei Ablauf Verfolgungs Ebenen unterstützt:

-   Ausführlich (alle verfügbaren Ablauf Verfolgungen).
-   Info (Informations Ablauf Verfolgungen).
-   Fehler (Fehler Ablauf Verfolgungen).

Die folgenden Ereignisse werden nachverfolgt:

-   Alle Fehler (Level = Error, Level = Info oder Level = verbose).
-   Eingang/Ende einer API (Level = Info oder Level = verbose).
-   Start und Abschluss aller e/a-Vorgänge (Level = Info oder Level = verbose)
-   Ausgetauschte SOAP-Nachrichten (Level = Verbose, verfügbar unter Windows 2003 SP1 und höher)

## <a name="generating-and-viewing-wwsapi-traces"></a>Erstellen und Anzeigen von wwsapi-Ablauf Verfolgungen

Wwsapi verwendet die Manifest-basierten Ereignisse unter Windows Vista und höher. Folglich hat die Ablauf Verfolgung einige Unterschiede basierend auf der Betriebssystemversion. Etw-Ablauf Verfolgungen können mithilfe der in-Box-etw-Tools auf allen unterstützten Plattformen erstellt werden. Das Anzeigen der etw-Ablauf Verfolgungen in einem netten Format erfordert jedoch benutzerdefinierte Tools unter Windows XP SP2 und Windows 2003 SP1. Abhängig von der Betriebssystemversion gibt es verschiedene Methoden zum Erfassen und Anzeigen von wwsapi-ETW-Ereignis Ablauf Verfolgungen.

## <a name="enabling-and-viewing-wwsapi-traces-in-event-viewer-works-on-windows-vista-and-above"></a>Aktivieren und Anzeigen von wwsapi-Ablauf Verfolgungen in Ereignisanzeige (funktioniert unter Windows Vista und höher)

-   Führen Sie eventvwr. msc über die Befehlszeile oder das Menü ausführen aus.
-   Klicken Sie im Aktionsbereich auf der rechten Seite auf den Link Ansicht, und aktivieren Sie die Option analytische und Debugprotokolle anzeigen.
-   Navigieren Sie im linken Bereich zu Anwendungs-und Dienst Protokolle \\ Microsoft \\ Windows- \\ Webdienste-Anbieter.
-   Klicken Sie mit der rechten Maustaste auf den Ablauf Verfolgungs Anbieter und wählen Sie Protokoll
-   Führen Sie das Szenario aus.
-   Wenn Sie die Seite Ereignisanzeige aktualisieren, sollten Sie die wwsapi-Ablauf Verfolgungs Einträge sehen.

## <a name="enabling-and-viewing-wwsapi-traces-using-wstracebat-script-works-on-xpsp2-and-above"></a>Aktivieren und Anzeigen von wwsapi-Ablauf Verfolgungen mithilfe Wstrace.bat Skripts (funktioniert auf XP SP2 und höher)

Die wstrace.bat Batchdatei bietet eine bequeme Möglichkeit, Folgendes zu tun:

-   Erstellen eines Ablauf Verfolgungs Protokolls
-   Löschen eines Ablauf Verfolgungs Protokolls
-   Aktivieren und Deaktivieren der Ablauf Verfolgung
-   Aktualisieren der Ablauf Verfolgungs Ebene (Info/Fehler/verbose)
-   Umstellen von Ablauf Verfolgungs Protokollen in CSV-Dateien

Die Batchdatei verwendet logman.exe für alle Befehle, mit der Ausnahme, dass die Protokolle in eine CSV-Datei umgerechnet werden, die ein benutzerdefiniertes Tool (wstracedump.exe) erfordert.

## <a name="using-tracing-commands"></a>Verwenden von Ablauf Verfolgungs Befehlen

Mit dem folgenden Befehl wird ein Protokoll erstellt, das die Ebene Info, Error oder ausführliche verwendet. Dieser Befehl erfordert erhöhte Berechtigungen.

**Fehler bei derwstrace.bat Create \[ Info- \| Fehler \|\]**

Der folgende Befehl löscht das Protokoll. Dieser Befehl erfordert erhöhte Berechtigungen.

**wstrace.bat löschen**

Der folgende Befehl aktiviert die Ablauf Verfolgung. Sie müssen zuerst ein Protokoll erstellen.

**wstrace.bat**

Die Ablauf Verfolgungs Ebene (Info, Error oder verbose) kann wie folgt geändert werden:

**Fehler bei derwstrace.bat Update \[ Informationen \| \|\]**

Verwenden Sie den folgenden Befehl, um die Ausgabe der Ablauf Verfolgung zu speichern:

**wstrace.bat > temp.csv**

Die Ereignisse werden in die CSV-Datei gekippt, bis STRG + C gedrückt wird oder die Ablauf Verfolgung deaktiviert ist.

## <a name="tracing-file-format"></a>Format der Ablauf Verfolgungs Datei

Die von wstrace.bat erstellten CSV-Dateien sind einfache Textdateien mit Komma getrennter Variable. Diese Dateien können in Excel, Notepad usw. geöffnet werden.

Die Spalten der Datei lauten wie folgt:

-   Zeitstempel-Zeitstempel des Zeitrahmens, zu dem das Ereignis aufgezeichnet wurde
-   ProcessID-ULONG-ID des Prozesses, der das Ereignis aufzeichnen soll.
-   ThreadID-ULONG-ID des Threads, der das Ereignis aufzeichnen hat
-   Der ereignisenumerationswert des Ereignis Typs ist möglicherweise ("API Enter" "API Enter", API Pending "" API \| \| exitsyncsuccess " \| " API exitsyncfailure " \| " API exitasyncsuccess "" API exitasyncfailure "" IO Started "" e/a-Vorgang abgeschlossen "" e/a- \| \| \| \| Fehler "" \| Fehler " \| " empfangener Nachrichten Start " \| \| \| \| \| " empfangene Meldung "" empfangene Nachricht wird beendet
-   Operation: der Name des aufgerufenen Vorgangs. In der Regel wird dies der API zugeordnet, die aufgerufen wird.
-   Fehler: optionale HRESULT-Fehlernummer
-   Info: optionale Informationen zum Ereignis

## <a name="collecting-wwsapi-etw-trace-file-using-etw-tools-works-on-xpsp2-and-above"></a>Sammeln einer wwsapi-etw-Ablauf Verfolgungs Datei mithilfe von etw-Tools (funktioniert auf XP SP2 und höher)

Aktivieren der etw-Ablauf Verfolgung für wwsapi

**logman Start wstrace-SB 64-ft 1-RT-p Microsoft-Windows-Webservices \[ Flags \[ Level \] \] \[ -o <EtlLogFileName> \] -ETS**

, um die ETW-Ablauf Verfolgungs Sitzung zu erstellen und zu starten. Logman.exe ist ein in-Box-etw-Tool, das auf allen unterstützten Plattformen verfügbar ist. Beachten Sie, dass Sie Microsoft \_ Windows \_ -Webdienste als Anbieter Namen auf XP SP2 und W2K3 verwenden müssen. Sie können Logman Query Providers ausführen, um die Liste der registrierten Anbieter anzuzeigen. Der Anbieter Microsoft-Windows-Webservices (oder Microsoft \_ Windows \_ Webservices) sollte aufgeführt werden, es sei denn, er ist nicht registriert. Der Anbieter wird normalerweise während des Setups registriert. Sie kann jedoch auch manuell durch Ausführen von wevtutil.exe im <ManifestFileName> (unter Windows Vista und höher) oder mofcomp.exe <MofFileName> (auf XP SP2 und W2K3) registriert werden.

Flags können verwendet werden, um die Ablauf Verfolgungen nach ihrer Art zu filtern. Der Wert kann oder ein Wert der folgenden Ablauf Verfolgungs Arten sein. Wenn keine Angabe erfolgt, werden alle Ablauf Verfolgungs Arten aktiviert.

-   0x1-API-Eintrags-und Beendigungs Ablauf Verfolgungen.
-   0x2-Fehler Ablauf Verfolgungen.
-   0x4-e/a-Ablauf Verfolgungen.
-   0x8: SOAP-Nachrichten Ablauf Verfolgungen.
-   0x10-binäre Nachrichten Ablauf Verfolgungen.

Die Ebene kann verwendet werden, um die Ablauf Verfolgungen nach ihrer Ebene zu filtern. Es muss sich um einen der folgenden Werte handeln: Wenn keine Angabe erfolgt, werden alle Ablauf Verfolgungs Ebenen aktiviert.

-   0x1-schwerwiegende Ablauf Verfolgungen.
-   0x2-Fehler Ablauf Verfolgungen.
-   0x3-Warnungs Ablauf Verfolgungen.
-   0x4-Informations Ablauf Verfolgungen.
-   0x5-ausführliche Ablauf Verfolgungen.

Etllogfilename ist der Pfad zu der zu erstellenden etw-Ereignisprotokoll Datei (ETL-Erweiterung verwenden). Wenn kein Wert angegeben wird, wählt etw einen zufälligen Namen aus, der später abgefragt werden kann. Diese Datei darf sich nicht im Profilverzeichnis des Benutzers befinden. Die ETW-Ereignisprotokoll Datei (ETL-Datei) liegt im Binärformat vor. Sie kann von etw-Anwendungen genutzt werden, ist aber nicht in einem lesbaren Format. Im nächsten Schritt wird beschrieben, wie der Inhalt angezeigt wird.

Ausführen Ihres Szenarios

Die ETW-Ereignisprotokoll Datei wird gesammelt.

**logman stoppt wstrace-ETS.**

zum Abbrechen der etw-Ablauf Verfolgungs Sitzung. Dies ist der Fall, wenn etw die Protokollierung der Ereignisse beendet. Die ETW-Ereignisprotokoll Datei (angegeben im etllogfilename-Parameter) ist einsatzbereit. Sie können entweder lokal (Anweisungen unten) angezeigt oder zur Untersuchung an die Produktgruppe gesendet werden.

End-to-End-Beispiel mit etw-Tools:

**logman Start wstrace-b 64-ft 1-RT-p Microsoft-Windows-Webservices-o mytrace. ETL-ETS**

**Echo. Führen Sie das Szenario aus.**

**logman stoppt wstrace-ETS.**

**tracerpt mytrace. ETL-o mytrace.xml**

**wstrace.htm**

**Echo. Verwenden Sie in der geöffneten Seite mytrace.xml und wstrace. Xsl.**

## <a name="viewing-wwsapi-etw-trace-file-traces-using-wstracedumpexe-tool-works-on-windows-xp-and-above"></a>Anzeigen von Ablauf Verfolgungen der wwsapi-etw-Ablauf Verfolgungs Datei mit wstracedump.exe Tool (funktioniert unter Windows XP und höher)

Wstracedump.exe ist ein benutzerdefiniertes etw-consumertool, das Ereignisse in der wwsapi-etw-Ablauf Verfolgungs Datei verarbeitet und eine lesbare Ausgabe erzeugt. Sie kann die Ausgabe von allen unterstützten Plattformen liefern. Weitere Informationen finden Sie in der Verwendung (wstracedump.exe-?).

## <a name="viewing-wwsapi-etw-trace-file-traces-using-etw-tools-works-on-windows-vista-and-above"></a>Anzeigen von wwsapi-etw-Ablauf Verfolgungs Datei-Ablauf Verfolgungen mit etw-Tools (funktioniert unter Windows Vista und höher)

Tracerpt.exe ist das Tool, um den Inhalt einer etw-Ereignisprotokoll Datei anzuzeigen und auf allen unterstützten Plattformen verfügbar zu sein. Es kann zum Generieren von CSV-, evtx-oder XML-Dumpdateien aus einer etw-Ereignisprotokoll Datei verwendet werden. Die generierte Ausgabedatei enthält jedoch nur in Windows Vista und höher lesbare Ablauf Verfolgungen. In diesen Anweisungen wird beschrieben, wie die XML-Dumpdatei generiert und zusammen mit einer XSL-Datei verwendet wird, um die Ablauf Verfolgungen in einem schönen Format anzuzeigen (die XSL-Datei ist sehr trivial und kann geändert werden, wenn verschiedene Formate gewünscht werden).

-   Ausführen

    **tracerpt <EtlLogFileName> -o <OutputXMLFileName>**

    zum Erstellen eines XML-Dumps aus der binären ETL-Datei (tracerpt.exe erstellt die Ausgabedatei standardmäßig im XML-Format. Führen Sie tracerpt-? aus. Um andere verfügbare Formate anzuzeigen).

-   An diesem Punkt können Sie die Ablauf Verfolgungs Informationen in der XML-Datei sehen. Außerdem können Sie die wstrace.htm Datei öffnen und die XML-Dumpdatei und die wstrace. XSL-Datei verwenden, um die Ablauf Verfolgungen in einem günstigeren Format anzuzeigen. Beachten Sie, dass sich die Dateien auf dem lokalen Computer befinden müssen, damit diese HTML-Datei auf IE verwendet werden kann.

## <a name="security"></a>Sicherheit

Beim Aktivieren der Ablauf Verfolgung sollten Administratoren berücksichtigen, dass Sie zusätzlichen Speicherplatz und Rechenleistung beansprucht. Ein böswilliger Client oder eine Anwendung kann Systemressourcen abschöpfen, es sei denn, die Ablauf Verfolgungs Einstellungen sind mit angemessenen Beschränkungen Bei Verwendung der Nachrichten Ablauf Verfolgung können Nachrichten, die vertrauliche Informationen wie Anmelde Informationen, persönliche Informationen usw. verwenden, auf dem Datenträger persistent gespeichert werden oder von jedem Benutzer mit Zugriff auf die System Ereignisanzeige angezeigt werden. Um dieses Problem zu beheben, kann die Ablauf Verfolgung von System-oder Administrator Benutzern unter Windows 2003 und höher aktiviert werden. Die Nachrichten Ablauf Verfolgung ist unter Windows XP deaktiviert, auf der alle Benutzer die Ablauf Verfolgung aktivieren können.

Die folgende Enumeration wird für die Ablauf Verfolgung verwendet:

-   [**WS- \_ Trace- \_ API**](/windows/desktop/api/WebServices/ne-webservices-ws_trace_api)

 

 




