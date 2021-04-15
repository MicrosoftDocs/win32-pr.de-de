---
title: 'Szenario 1: Beispiel für http-Timeout mit etw-Ablauf Verfolgung und Netsh-Befehlen'
description: Mithilfe der etw-Ablauf Verfolgung kann der Datenfluss über die HTTP-Server-API-Komponente überprüft werden, um Probleme zu diagnostizieren.
ms.assetid: b6b24161-c3da-4972-b49f-c545da2fc81e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa50f438aca664651b24db822f2b9e3a30da4682
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104554609"
---
# <a name="scenario-1-http-timeout-example-using-etw-tracing-and-netsh-commands"></a>Szenario 1: Beispiel für http-Timeout mit etw-Ablauf Verfolgung und Netsh-Befehlen

Mithilfe der etw-Ablauf Verfolgung kann der Datenfluss über die HTTP-Server-API-Komponente überprüft werden, um Probleme zu diagnostizieren. Beispielsweise können Benutzer einer Webanwendung Fehlermeldungen in Ihrem Browser sehen, die von einer Webseite nicht angezeigt werden können. Auf dem Server, auf dem die Webanwendung gehostet wird, sieht der IT-Experte auch einen Verbindungs Timeout Eintrag innerhalb des HTTP-Fehler Protokolls, wie in Abbildung 1 dargestellt. Das http-Fehlerprotokoll befindet sich im folgenden Verzeichnis:% windir% \\ system32 \\ Logfiles \\ Httperr \\ .

![Screenshot, der das Befehlsfenster "Netsh H t t p" anzeigt, das ein h t t p-Fehlerprotokoll für das Timeout anzeigt.](images/httperrorlog.png)

Abbildung 1: http-Fehlerprotokoll für Timeout

## <a name="generating-an-etw-trace-report"></a>Erstellen eines etw-Ablauf Verfolgungs Berichts

Um einen etw-Ablauf Verfolgungs Bericht für die HTTP-Server-API-Komponente zu generieren, führen Sie die folgenden Schritte an der Eingabeaufforderung aus. In diesem Beispiel wird die Ablauf Verfolgung auf dem Server ausgeführt, da die Webanwendung gehostet wird.

In den folgenden Schritten wird eine Ablauf Verfolgung mit dem Namen "Httptrace. ETL" generiert und dann die Ablauf Verfolgung in eine CSV-Datei mit dem Namen httptrace.csv Wie unten gezeigt, wird der ETW-Anbieter für die HTTP-Server-API als Microsoft-Windows-HttpService bezeichnet. Die Befehlszeilenoption 0xfff gibt an, dass alle ETW-Ereignisse für diesen Anbieter erfasst werden sollen.

**Generieren eines etw-Ablauf Verfolgungs Berichts**

1.  Etw-Ablauf Verfolgung für http-Server-API-Komponente starten: l **ogman.exe starten von Httptrace-p Microsoft-Windows-HttpService 0xFFFF-o Httptrace. ETL – ETS**
2.  Reproduzieren Sie das Problem, damit es in der Ablauf Verfolgung aufgezeichnet werden kann. In diesem Beispiel greifen Sie von einem Client Computer aus auf die Webanwendung zu, was dazu führt, dass die Meldung "die **Seite kann nicht angezeigt werden**" auf dem Client angezeigt wird.
3.  Nachdem das Problem reproduziert wurde, wird die Ablauf Verfolgung beendet: **logman.exe stopphttptrace – ETS**
4.  Konvertieren Sie den Bericht in das CSV **-Format:tracerpt.exe Httptrace. ETL-of CSV-o httptrace.csv**
5.  Anzeigen des Ablauf Verfolgungs Berichts. Unten in Tabelle 1 ist ein Auszug aus einer CSV-Ablauf Verfolgung aufgeführt.

## <a name="viewing-the-trace-and-diagnosing"></a>Anzeigen der Ablauf Verfolgung und Diagnose

Die resultierende CSV-Datei für Ablauf Verfolgungen kann in Excel oder einem beliebigen Tool angezeigt werden, das das CSV-Format unterstützt. Tabelle 1 unten zeigt Auszüge aus einer Beispieldatei für die Ablauf Verfolgung (httptrace.csv). Im Ablauf Verfolgungs Bericht wird in der Spalte "Ebene" ein Eintrag mit dem Wert "3" angezeigt, der einer Warnung in etw entspricht. Die HTTP-Server-API-Komponente befolgt die ETW-Ebenen, die im folgenden Artikel definiert sind: ( https://msdn2.microsoft.com/library/aa382793.aspx) . Die ETW-Ebenen umfassen Folgendes:



| Ebene | Bedeutung      |
|-------|--------------|
| 1     | Kritisch     |
| 2     | Fehler        |
| 3     | Warnung      |
| 4     | Infomational |
| 5     | Ausführlich      |



 

Mit dieser Warnung meldet der Ereignistyp (Typspalte) "" ". In den nachfolgenden Spalten für das Ereignis "Ereignis-Timeout" wird der Zeitgeber, der abgelaufen ist, als "Timer \_ connectionidle" gemeldet. Beachten Sie, dass die Spalte mit dem Eintrag "Timer \_ connectionidle" nicht in der Tabelle enthalten ist, um die Übersichtlichkeit zu vermeiden und um das Durchsuchen nicht zusammenhängender Spalten zu vermeiden.



| Ereignisname                    | type            | Ereignis-ID | Version | Channel | Ebene |
|-------------------------------|-----------------|----------|---------|---------|-------|
| EventTrace                    | Header          | 0        | 2       | 0       | 0     |
| Microsoft-Windows-HttpService | Chgurlgrpprop   | 28       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | Addurl          | 31       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | Chgreqqueueprop | 30       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | Chgurlgrpprop   | 28       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | Chgsrvsesprop   | 29       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | Chgsrvsesprop   | 29       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | Verbindung herstellen     | 21       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | "Config"     | 22       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | Recvreq         | 1        | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | Analysieren           | 2        | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | Logfilewrite    | 51       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | -Cleanup     | 24       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | "Verbindung"    | 53       | 0       | 16      | 3     |



 

Tabelle 1: Auszüge aus einem Beispiel Ablauf Verfolgungs Bericht für ein Zeit Geber Problem

In diesem Beispiel ist der Ablauf Zeitpunkt (Ereignis "Ereignis Ereignisse") des Header Zeit Gebers (Timer \_ connectionidle) der Grund, warum Endbenutzern angezeigt wird, dass die Meldung "die Seite kann nicht angezeigt werden" in ihren Webclients angezeigt wird. Ein möglicher Grund für das Timeout kann sein, dass Webclients aufgrund langsamer Verbindungen langsam senden. Um dieses Problem zu beheben, kann der Timeout Wert über Netsh-Befehle angepasst werden.

## <a name="adjusting-timeout-through-netsh-and-verifying-the-solution"></a>Anpassen des Timeouts über Netsh und Überprüfen der Lösung

Mit den Netsh-Befehlen für das unten aufgeführte http können IT-Experten Einstellungs Werte für die HTTP-Server-API-Komponente anzeigen und konfigurieren. Änderungen über Netsh HTTP-Befehle betreffen alle Server Anwendungen, die von der HTTP-Server-API-Komponente für diesen Computer gehostet werden. Diese Änderungen bleiben über Neustarts der Komponente und Neustarts des Computers erhalten. Die Netsh HTTP-Befehle sind in Windows Vista und Windows Server 2008 verfügbar und ersetzen das HttpCfg.exe Tool des Windows Server 2003 Resource Kits bei Ausführung unter Windows Vista und Windows Server 2008. In diesem Szenario wird ein Timeout Wert angepasst und die Lösung überprüft. Timer sind in der HTTP-Server-API-Komponente vorhanden, um die Verfügbarkeit zu gewährleisten und durch einen falsch konfigurierten oder böswilligen Benutzer vor übermäßigen Das Anpassen von Timern aus Standardwerten sollte sorgfältig anhand eines potenziellen DoS-Angriffs ausgewertet werden.

In diesem Beispiel befinden sich die Webclients hinter einer langsamen Netzwerkverbindung, sodass das ETW-Ereignis des Timers " \_ connectionidle" verursacht wird. Nach Berücksichtigung der Ursache der Timeouts und des Ausgleichs mit den Auswirkungen auf die Auslastung des Servers wird die Entscheidung getroffen, die Timeout Werte auf einen Wert von 240 Sekunden zu erhöhen. Sie können den Timer mit dem folgenden Verfahren anzeigen und konfigurieren.

**Konfigurieren des Timers für Leerlaufverbindungen (Timer \_ connectionidle) mit Netsh**

1.  Öffnen Sie auf dem-Server ein Befehlsfenster mit erhöhten Rechten, und führen Sie die folgenden Schritte aus, um den Timeout Wert anzuzeigen und zu konfigurieren. Ein Screenshot des Befehls netsh http ist in Abbildung 2 unten dargestellt.
2.  Aktuelle Timeout Werte anzeigen: **netsh http Show Timeout**
3.  Konfigurieren Sie den \_ Timeout Wert für Timer connectionidle. In diesem Beispiel wird der Wert in 240 Sekunden geändert: **netsh http Add Timeout timeouttype = idleconnectiontimeout Wert = 240**

![netsh http-Befehlsfenster](images/netshhttpcommand.png)

Abbildung 2: netsh http-Befehlsfenster

Nachdem Sie den Timeout Wert konfiguriert haben, führen Sie die ETW-Diagnose Schritte erneut aus. Wenn die Fehlerbedingung korrigiert wurde, sollte für die ETW-Ablauf Verfolgung kein Timeout mit einer etw-Ebene von "3" für den Timer für die Verbindung im Leerlauf mehr angezeigt werden.

 

 




