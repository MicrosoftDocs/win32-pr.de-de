---
description: Ab Windows Vista verwendet der WMI-Dienst nicht die WMI-Protokolldateien. Stattdessen wird die Ereignis Ablauf Verfolgung für Windows (ETW) verwendet, und Ereignisse sind über Ereignisanzeige oder das Befehlszeilen Tool wevtutil verfügbar.
ms.assetid: bb6401e8-caf7-4f39-ab64-b7532723ce9a
ms.tgt_platform: multiple
title: WMI-Ablauf Verfolgung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14371a4f18b81019073cd2b428500b12385719e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758005"
---
# <a name="tracing-wmi-activity"></a>WMI-Ablauf Verfolgung

Ab Windows Vista verwendet der WMI-Dienst nicht die [WMI-Protokolldateien](wmi-log-files.md). Stattdessen wird die [Ereignis Ablauf Verfolgung für Windows (ETW)](/windows/desktop/ETW/event-tracing-portal) verwendet, und Ereignisse sind über **Ereignisanzeige** oder das Befehlszeilen Tool wevtutil verfügbar.

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Abrufen von WMI-Ereignissen durch Ereignisanzeige](#obtaining-wmi-events-through-event-viewer)
-   [Aktivieren der WMI-Ablauf Verfolgung an der Eingabeaufforderung](#enabling-wmi-tracing-at-command-prompt)
-   [Verwenden der WPP-basierten WMI-Ablauf Verfolgung](#using-wpp-based-wmi-tracing)
-   [Zugehörige Themen](#related-topics)

## <a name="obtaining-wmi-events-through-event-viewer"></a>Abrufen von WMI-Ereignissen durch Ereignisanzeige

Die Datei "wmitracing. log" enthält die Ereignisse, die von WMI verfolgt werden. Dabei handelt es sich jedoch um eine Binärdatei. Um diese Ereignisse in einem Format anzuzeigen, das von Menschen lesbar ist, verwenden Sie die **Ereignisanzeige**.

Standardmäßig werden keine WMI-Ereignisse verfolgt. In diesem Verfahren wird beschrieben, wie Sie mit **Ereignisanzeige** die WMI-Ereignis Ablauf Verfolgung aktivieren und WMI-Ereignisse suchen. Sie können die gleichen Vorgänge auch über das Befehlszeilen Tool wevtutil ausführen.

**So zeigen Sie WMI-Ereignisse in Ereignisanzeige an**

1.  Öffnen Sie die **Ereignisanzeige**. Klicken Sie im Menü **Ansicht** auf **Analytische und Debugprotokolle einblenden**. Suchen Sie  unter Anwendungs-und Dienst Protokolle \| Microsoft \| Windows \| WMI-Aktivität nach dem Ablauf Verfolgungs Kanal Protokoll für WMI.
2.  Klicken Sie mit der rechten Maustaste auf das Ablauf **Verfolgungs** Protokoll, und wählen Sie **Log** Aktivieren Sie das Kontrollkästchen **Protokollierung aktivieren** , um die WMI-Ereignis Ablauf Verfolgung zu starten. Weitere Informationen zu Kanälen finden Sie unter [Ereignisprotokolle und Kanäle im Windows-Ereignisprotokoll](/previous-versions//aa385225(v=vs.85)).
3.  WMI-Ereignisse werden im Ereignisfenster für **WMI-Activity** angezeigt. Doppelklicken Sie auf ein Ereignis in der Liste, um die detaillierten Informationen anzuzeigen. Sie können ein Ereignis in der **XML-Ansicht** oder im **Anzeige Format anzeigen** .

Das Feld **Ereignis-ID** zeigt einen Wert an, der die folgenden Informationen enthält.

<dl> <dt>

<span id="Event_1"></span><span id="event_1"></span><span id="EVENT_1"></span>Ereignis 1
</dt> <dd>

Beginn der Ereignis Sequenz für einen bestimmten Vorgang. Ein Vorkommen für jede Sequenz.

Die Ereignis Felder für ein Ereignis 1 lauten wie folgt:

-   **Groupoperationid** ist ein eindeutiger Bezeichner, der für alle Ereignisse verwendet wird, die für einen bestimmten Client gemeldet werden.
-   **OperationId** gibt die Vorgangs Sequenz an.
-   Der **Vorgang** gibt die Verbindung oder die WMI-Anforderung an.
-   Der **Benutzer** gibt das Konto an, das eine WMI-Anforderung durch Ausführen eines Skripts oder mithilfe von CIM Studio sendet.
-   **Namespace** zeigt den WMI-Namespace an, mit dem die Verbindung hergestellt wird.

Beispielsweise kann ein Skript alle Instanzen einer WMI-Klasse, z. b. den [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service), anfordern. Der erste Vorgang ist möglicherweise eine Verbindung mit WMI.

</dd> <dt>

<span id="Event_2"></span><span id="event_2"></span><span id="EVENT_2"></span>Ereignis 2
</dt> <dd>

Ereignisse, die den Vorgang ausmachen. Ein oder mehrere Vorkommen in der Sequenz.

Die Ereignis Felder für ein Ereignis 2 lauten wie folgt:

-   **Groupoperationid** gibt die Reihenfolge an, in der das Ereignis auftritt.
-   **Groupoperationid** gibt die Reihenfolge an, in der das Ereignis auftritt.
-   **ProviderName** gibt den Namen des Anbieters an, der die Daten bereitstellt.
-   **Path** ist der WMI-Pfad zum Objekt.

Der Vorgang kann beispielsweise eine Enumeration des Win32- [**\_ Dienstanbieter**](/windows/desktop/CIMWin32Prov/win32-service)sein.

</dd> <dt>

<span id="Event_3"></span><span id="event_3"></span><span id="EVENT_3"></span>Ereignis 3
</dt> <dd>

Ende der Ereignis Sequenz für einen bestimmten Vorgang. Ein Vorkommen für jede Sequenz.

Nur **groupoperationid** wird angezeigt.

</dd> </dl>

## <a name="enabling-wmi-tracing-at-command-prompt"></a>Aktivieren der WMI-Ablauf Verfolgung an der Eingabeaufforderung

Sie können die WMI-Ereignis Ablauf Verfolgung auch über das Befehlszeilen Tool "wevtutil" aktivieren. Verwenden Sie den folgenden Befehl: **Wevtutil.exe SL Microsoft-Windows-WMI-Activity/Trace/e: true**. Die WMI-Ereignis Quelle lautet Microsoft-Windows-WMI. Weitere Informationen zu Wevtutil.exe finden Sie unter Informationen [zum Windows-Ereignisprotokoll](/previous-versions//aa382610(v=vs.85)).

## <a name="using-wpp-based-wmi-tracing"></a>Verwenden der WPP-basierten WMI-Ablauf Verfolgung

In Windows-Betriebssystemen ab Windows Vista erstellt WMI während des Startvorgangs einen aktiven Ablauf Verfolgungs Kanal. Der Name des Kanals lautet WMI-Ablauf \_ Verfolgungs \_ Sitzung. Nur Fehler werden im Kanal protokolliert.

Der Windows-Ablaufverfolgungs-Präprozessor (WPP) zeichnet Informationen in einer Binärdatei auf. Um die Datei zu lesen, müssen Sie Sie zuerst in ein lesbares Textformat übersetzen. Verwenden Sie zum Durchführen der Übersetzung ein Tool namens tracefmt.exe aus dem [Windows-Treiberkit (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) . Das Tool erfordert Informationen, die in einigen zugeordneten Dateien gespeichert sind. Die Dateien befinden sich im Verzeichnis "% SystemRoot% \\ system32 \\ WBEM \\ TMF" und haben die Dateinamenerweiterung ". TMF". Das Tool erfordert tatsächlich eine einzelne TMF-Datei. Sie erstellen diese einzelne Datei, indem Sie alle TMF-Dateien in einer anderen TMF-Datei verketten. Weitere Informationen zu TMF-Dateien finden Sie unter [Format Datei der Ablauf Verfolgungs Meldung](/windows-hardware/drivers/devtest/trace-message-format-file).

Nachdem Sie das [Windows-Treiberkit (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) zum Abrufen der tracelog.exe und tracefmt.exe Befehlszeilen Tools installiert haben, führen Sie die folgenden Schritte aus, um eine WPP-basierte WMI-Ablauf Verfolgung zu erfassen.

**So zeigen Sie eine WPP-basierte WMI-Ablauf Verfolgung an**

1.  Öffnen Sie zum Erstellen der einzelnen TMF-Datei ein Eingabe Aufforderungs Fenster mit erhöhten Rechten, und navigieren Sie zum Verzeichnis% systemroot% \\ system32 \\ WBEM \\ TMF.

2.  Geben Sie **Copy/y% systemroot% \\ system32 \\ WBEM \\ TMF \\ \* . TMF% systemroot% \\ system32 \\ WBEM \\ TMF \\ WMI. TMF** ein. Dadurch wird eine Datei mit dem Namen "WMI. TMF" erstellt, die den Inhalt aller anderen TMF-Dateien enthält.

3.  Geben Sie **tracelog-WMI-Ablauf \_ Verfolgungs \_ Sitzung** ein. Dadurch werden die WPP-Puffer auf den Datenträger geleert.
4.  Typsatz-Ablauf **Verfolgungs \_ Format \_ -Präfix = \[ %9! d! \] %8! 04x!. %3! 04x!. %3! 04x!:: %4! s! \[ %1! s! \] (%! Compname!:%! Func!: %2! s!)**. Das Tool tracefmt fügt jeder Ablauf Verfolgungs Meldung einige Standardinformationen hinzu. Sie können konfigurieren, welche Informationen eingeschlossen werden, indem Sie die \_ Umgebungsvariable "Trace Format Prefix" festlegen \_ . Informationen zur verwendeten Syntax finden Sie unter [Präfix der Ablauf Verfolgungs Meldung](https://msdn.microsoft.com/library/aa139695.aspx).
5.  Geben Sie **tracefmt-TMF% systemroot% \\ system32 \\ WBEM \\ TMF \\ WMI. TMF-o OUTPUT.TXT% systemroot% \\ system32 \\ WBEM \\ Logs \\ wmitracing. log** ein. Dadurch wird die Übersetzung vom Binärformat in das lesbare Textformat durchführt.
6.  Geben Sie **Editor% systemroot% \\ system32 \\ WBEM \\ TMF \\OUTPUT.TXT** ein. Dadurch wird die Ablauf Verfolgungs Datei in Notepad geöffnet.

Im folgenden finden Sie einige weitere WPP-bezogene Aufgaben, die Sie möglicherweise ausführen müssen.

**So verhindern Sie die WPP-basierte WMI-Ablauf Verfolgung**

-   Geben Sie **tracelog-WMI-Ablauf \_ Verfolgungs \_ Sitzung Abbrechen** ein.

**So starten Sie die WPP-basierte WMI-Ablauf Verfolgung**

-   Geben Sie **tracelog-Start WMI \_ Trace \_ Session-GUID \# 1ff6b227-2ca7-40F9-9a66-980eadaa602e-RT-Level 5-Flag 0x7-f mytrace ein. BIN**

**Windows Vista:** Standardmäßig ist die WPP-basierte WMI-Ablauf Verfolgung auf Ebene 2 festgelegt, die nur Fehlermeldungen enthält. Legen Sie die Ebene auf 4 fest, um auch Informationsmeldungen einzuschließen. Alle Bereiche von WMI werden standardmäßig verfolgt. Es gibt drei verschiedene Bereiche, die verfolgt werden können: Core (Flag = 0x1), ESS (Flag = 0x2) und PROV (Flag = 0x4). Im obigen Startbefehl bewirkt **Flag 0x7** , dass alle drei Bereiche nachverfolgt werden.

**Windows 7:** Standardmäßig ist die WPP-basierte WMI-Ablauf Verfolgung deaktiviert und auf Ebene 0 festgelegt. Um die WPP-basierte WMI-Ablauf Verfolgung verwenden zu können, muss diese Funktion aktiviert und auf Ebene 2 für Fehlermeldungen oder Ebene 4 für Fehler-und Informationsmeldungen festgelegt werden.

**So Listen Sie alle WPP-Ablauf Verfolgungs Sitzungen auf**

-   Geben Sie **tracelog-l** ein.

**So Listen Sie Informationen über die WPP-Ablauf Verfolgungs Sitzung auf**

-   Geben Sie **tracelog-l \| findstr/i "WMI \_ Trace"** ein.

**So zeigen Sie die Parameter für die WPP-Ablauf Verfolgungs Sitzung an**

-   Geben Sie **tracelog-q WMI-Ablauf \_ Verfolgungs \_ Sitzung** ein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Problembehandlung](wmi-troubleshooting.md)
</dt> <dt>

[WMI-Protokolldateien](wmi-log-files.md)
</dt> </dl>

 

 
