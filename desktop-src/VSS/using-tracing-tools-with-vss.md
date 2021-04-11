---
description: Zum Erfassen von Ablauf Verfolgungs Informationen für die VSS-Infrastruktur können Sie das vsstrace-Tool, das Logman-Tool oder das tracelog-Tool verwenden.
ms.assetid: afe2a0ed-1a8e-4f8b-be9e-241d55cd9ef6
title: Verwenden von Ablauf Verfolgungs Tools mit VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073a2ae9ba2ba2771abdc37ff0291764ed5e9efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214620"
---
# <a name="using-tracing-tools-with-vss"></a>Verwenden von Ablauf Verfolgungs Tools mit VSS

Zum Erfassen von Ablauf Verfolgungs Informationen für die VSS-Infrastruktur können Sie das vsstrace-Tool, das Logman-Tool oder das tracelog-Tool verwenden. Vsstrace ist im Microsoft Windows Software Development Kit (SDK) verfügbar und kann verwendet werden, um VSS-Anwendungen unter Windows 7 und höheren Versionen des Windows-Betriebssystems nachzuverfolgen. Logman ist ein Ablauf Verfolgungs Controller für Ablauf Verfolgungs Ereignisse und Leistungsindikatoren. Sie kann auch verwendet werden, um VSS-Anwendungen unter Windows 7 und höheren Versionen des Windows-Betriebssystems nachzuverfolgen. TraceLog ist im Windows-Treiberkit (WDK) enthalten.

Informationen zur Verwendung von Ablauf Verfolgungs Tools mit der [automatisierten System Wiederherstellung (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md)finden Sie unter [Verwenden von Ablauf Verfolgungs Tools mit ASR-Anwendungen](using-tracing-tools-with-vss-asr-applications.md)

> [!Note]  
> Vsstrace, logman und tracelog erfordern alle Administratorrechte.

 

Weitere Informationen zu den einzelnen Tools finden Sie in den folgenden Abschnitten:

-   [Verwenden von vsstrace](#using-vsstrace)
    -   [Optionen für vsstrace Command-Line](#vsstrace-command-line-options)
-   [Verwenden von logman](#using-logman)
-   [Verwenden von tracelog](#using-tracelog)

## <a name="using-vsstrace"></a>Verwenden von vsstrace

Verwenden Sie die folgende Syntax, um das vsstrace-Tool über die Befehlszeile auszuführen:

**vsstrace** *-Befehlszeilenoptionen*

Verwenden Sie die folgende Syntax, um eine präzise Befehlszeilen Hilfe für das vsstrace-Tool anzuzeigen:

**vsstrace-Hilfe**

Verwenden Sie die folgende Syntax, um eine ausführliche Befehlszeilen Hilfe für das vsstrace-Tool anzuzeigen:

**vsstrace-Hilfe**

### <a name="vsstrace-command-line-options"></a>Optionen für vsstrace Command-Line

Das vsstrace-Tool verwendet die folgenden Befehlszeilenoptionen:

<dl> <dt>

<span id="-f_Flags"></span><span id="-f_flags"></span><span id="-F_FLAGS"></span>**-f-** *Flags*
</dt> <dd>

Aktivieren Sie die Module, deren Flags von der *Flags* -Bitmaske angegeben werden. Jedes Flag entspricht einem VSS-Modul. Wenn *Flags* 0 (null) ist, werden keine Module aktiviert. Beachten Sie, dass die meisten Module standardmäßig aktiviert sind. Diese Option kann mit der **+** Option _Module_ kombiniert werden. Beispielsweise deaktiviert **vsstrace-f 0 + Writer + coord** die Ablauf Verfolgung aller Module, die standardmäßig aktiviert sind, und ermöglicht die Ablauf Verfolgung von VSS-Writern und des VSS-Diensts. Alternativ ermöglicht **vsstrace + f 0xFFFF-coord** die Ablauf Verfolgung aller Module mit Ausnahme des VSS-Diensts.

> [!Note]  
> Wenn Sie die Option **-f** in Verbindung mit der **+** Option _Module_ verwenden, muss die **-f** vor der **+** _Modul_ Option angezeigt werden.

 

In der folgenden Tabelle sind der Modulname und das Flag für die einzelnen verfügbaren Module aufgelistet.

| Modul | Flag       | Standardmäßig aktiviert | Verfolgte Elemente                                                                                                                                  |
|--------|------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| EXCEPT | 0x00000001 | Ja                | C++-Ausnahmebehandlung.                                                                                                                       |
| Koord  | 0x00000002 | Ja                | Der VSS-Dienst, der auch als VSS Coordinator bezeichnet wird.                                                                                    |
| Austausch Vorgänge  | 0x00000004 | Ja                | Der VSS-System Schatten Kopie-Anbieter Dienst.                                                                                                  |
| Bucomp | 0x00000008 | Ja                | Die VSS-Anforderer und die Verarbeitung der Sicherungs Metadaten.                                                                                             |
| WRITER | 0x00000010 | Ja                | VSS Writer Vorgänge und VSS-gehosteten Writer-Implementierungen, wie z. b. der Windows-Registrierungs Schreiber.                                             |
| Vssapi | 0x00000020 | Ja                | Verschiedene Funktionen der VSS-API, die von VSSAPI.DLL exportiert wurden.                                                                                |
| Hwdiag | 0x00000040 | Ja                | VSS-Hardware Anbieter Infrastruktur und-Vorgänge.                                                                                          |
| ADMIN  | 0x00000080 | Ja                | VSS-Befehlszeilen Dienstprogramme, z. b. VSSADMIN.EXE und DISKSHADOW.EXE.                                                                           |
| Vssui  | 0x00000100 | Ja                | Die Schattenkopien für freigegebene Ordner Konfigurations Benutzeroberfläche. Die Benutzeroberfläche ist nur unter Windows Server-Betriebssystemen verfügbar.         |
| TEST   | 0x00000200 | Ja                | Nicht zutreffend (Dieses Ablauf Verfolgungs Modul ist reserviert.)                                                                                            |
| IOCTL  | 0x00000400 | Ja                | Details zu FSCTL-und ioctl-Vorgängen, die der VSS-Dienst durch Aufrufen der [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) -Funktion initiiert hat. |
| Genen    | 0x00000800 | Ja                | Allgemeine VSS-Dienstprogramm Funktionen, z. b. Zuweisungen, Zeichen folgen Klassen sowie Registrierungs-und Volumevorgänge.                                        |
| Wrxml  | 0x00001000 | Nein                 | XML-Verarbeitung für Writer-Metadaten. Dieses Modul weist ein sehr hohes Maß an Rauschen auf.                                                               |
| Vssxml | 0x00002000 | Nein                 | Basisklassen für die XML-Verarbeitung. Dieses Modul weist ein sehr hohes Maß an Rauschen auf.                                                                      |



 

</dd> <dt>

<span id="_Module"></span><span id="_module"></span><span id="_MODULE"></span>**+**_Mond_
</dt> <dd>

Aktivieren Sie das Modul, das durch das *Modul* angegeben wird. Mehrere Module können gleichzeitig aktiviert werden. Um die verfügbaren Module aufzulisten, geben Sie **vsstrace – Help modules** an der Eingabeaufforderung ein.

</dd> <dt>

<span id="-Module"></span><span id="-module"></span><span id="-MODULE"></span>**-**_Mond_
</dt> <dd>

Deaktivieren Sie das Modul, das durch das *Modul* angegeben wird. Um die verfügbaren Module aufzulisten, geben Sie **vsstrace – Help modules** an der Eingabeaufforderung ein.

</dd> <dt>

<span id="_pid_ProcessId"></span><span id="_pid_processid"></span><span id="_PID_PROCESSID"></span>**+ PID** *-ProcessID*
</dt> <dd>

Aktivieren Sie den durch *ProcessID* angegebenen Prozess. Um alle Prozesse zu aktivieren, verwenden Sie " \* " für den Wert von *ProcessID*. Es kann jeweils mehr als eine **PID** -Option angegeben werden. Die Reihenfolge der Optionen bestimmt, welche Prozesse aktiviert oder deaktiviert werden. Um z. b. nur den Prozess zu aktivieren, dessen Prozess-ID 0xe8c ist, verwenden Sie **vsstrace-PID \* + PID 0xe8c**.

</dd> <dt>

<span id="-pid_ProcessId"></span><span id="-pid_processid"></span><span id="-PID_PROCESSID"></span>**-PID** *ProcessID*
</dt> <dd>

Deaktivieren Sie den durch *ProcessID* angegebenen Prozess. Um alle Prozesse zu deaktivieren, verwenden Sie " \* " für den Wert von *ProcessID*. Es kann jeweils mehr als eine **PID** -Option angegeben werden. Die Reihenfolge der Optionen bestimmt, welche Prozesse aktiviert oder deaktiviert werden. Um z. b. alle Prozesse außer dem Prozess zu deaktivieren, dessen Prozess-ID 0xe8c ist, verwenden Sie **vsstrace-PID \* + PID 0xe8c**.

</dd> <dt>

<span id="_tid_ThreadId"></span><span id="_tid_threadid"></span><span id="_TID_THREADID"></span>**+ TID** *ThreadId*
</dt> <dd>

Aktivieren Sie den von *ThreadId* angegebenen Thread. Um alle Threads zu aktivieren, verwenden Sie " \* " für den Wert von *ThreadId*. Es kann jeweils mehr als eine **TID** -Option angegeben werden. Die Reihenfolge der Optionen bestimmt, welche Threads aktiviert oder deaktiviert werden. Um z. b. nur den Thread zu aktivieren, dessen Prozess-ID 0x31a ist, verwenden Sie **vsstrace-TID \* + TID 0x31a**.

</dd> <dt>

<span id="-tid_ThreadId"></span><span id="-tid_threadid"></span><span id="-TID_THREADID"></span>**-TID** *ThreadId*
</dt> <dd>

Deaktivieren Sie den von *ThreadId* angegebenen Thread. Um alle Threads zu deaktivieren, verwenden Sie " \* " für den Wert von *ThreadId*. Es kann jeweils mehr als eine **TID** -Option angegeben werden. Die Reihenfolge der Optionen bestimmt, welche Threads aktiviert oder deaktiviert werden. Wenn Sie z. b. alle Threads außer dem Thread, dessen Prozess-ID 0x31a ist, deaktivieren möchten, verwenden Sie **vsstrace-TID \* + TID 0x31a**.

</dd> <dt>

<span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span>**-l-** *Ebene*
</dt> <dd>

Verwenden Sie die nach *Ebene* angegebene Ablauf Verfolgungs Ebene. Je höher die Ebene, desto ausführlicher wird die Ausgabe der Ablauf Verfolgung angezeigt. Jede Ebene enthält alle niedrigeren Ebenen. Der Standardwert ist 170. Die folgenden Ebenen sind verfügbar.



| Ebene | In der Ausgabe der Ablauf Verfolgung enthaltene Informationen |
|-------|------------------------------------------|
| 000   | Keine                                     |
| 020   | Schwerwiegende Fehler                             |
| 030   | Ausnahmefehler                     |
| 040   | Errors                                   |
| 050   | Assertionen                               |
| 060   | Warnungen                                 |
| 080   | Ausnahmebehandlung                       |
| 100   | Ereignisprotokoll Aktivität                       |
| 120   | Allgemeine Informationen                      |
| 140   | Codeflow                                |
| 160   | Funktion eingeben und beenden                  |
| 170   | Funktions Rückgabewerte                   |
| 180   | Funktionsparameter (Terse)              |
| 190   | Funktionsparameter (ausführlich)            |
| 200   | Ausführliche Informationsebene 1              |
| 210   | Ausführliche Informationsebene 2              |
| 220   | Ausführliche Informationen Ebene 3              |
| 230   | Schnelle Codeebene 1                        |
| 240   | Schnelle Codeebene 2                        |
| 250   | Schnelle Codeebene 3                        |
| 255   | Alle                                      |



 

</dd> <dt>

<span id="_indent"></span><span id="_INDENT"></span>**+ Einzug**
</dt> <dd>

Einzug der formatierten Ablauf Verfolgungs Ausgabe an jeder Funktions-und unter Funktions Grenze.

</dd> <dt>

<span id="-indent"></span><span id="-INDENT"></span>**Einzug**
</dt> <dd>

Die formatierte Ablauf Verfolgungs Ausgabe nicht einziehen.

</dd> <dt>

<span id="-etl_EtlFile"></span><span id="-etl_etlfile"></span><span id="-ETL_ETLFILE"></span>**-ETL** *etlfile*
</dt> <dd>

Konvertieren Sie die von *etlfile* angegebene logman-Ausgabedatei in ein lesbares Textformat.

</dd> <dt>

<span id="-o_OutputFile"></span><span id="-o_outputfile"></span><span id="-O_OUTPUTFILE"></span>**-o** *OutputFile*
</dt> <dd>

Speichern Sie die Ablauf Verfolgungs Informationen in der Ausgabedatei, die von *OutputFile* angegeben wird. Um die optimale Leistung zu erzielen, sollte sich die Ausgabedatei auf einem Volume befinden, das nicht Teil der Schatten Kopie ist.

</dd> <dt>

<span id="-help_HelpOption"></span><span id="-help_helpoption"></span><span id="-HELP_HELPOPTION"></span>**-Help** *helpop tion*
</dt> <dd>

Zeigt die Befehlszeilen Hilfe an, wie von *helpoption* angegeben. Gültige *helpoption* -Werte sind **Module**, **Levels** und **all**. Die Angabe von **Modulen** bewirkt, dass die Module aufgelistet werden. Das Angeben von **Ebenen** bewirkt, dass die verfügbaren Ebenen aufgelistet werden. Das Angeben von **all** bewirkt, dass ausführliche Hilfe angezeigt wird. Wenn keine Optionen verwendet werden, wird eine kurze Hilfe angezeigt.

</dd> </dl>

## <a name="using-logman"></a>Verwenden von logman

Im folgenden Verfahren wird beschrieben, wie Sie Logman mit der VSS-Anwendung verwenden.

**So verwenden Sie Logman mit der VSS-Anwendung**

1.  Verwenden Sie den folgenden Befehl zum Starten der Ablauf Verfolgung:

    **logman Start VSS-o** *x: \\ * * * VSS. ETL-ETS-p {9138500e-3648-4edb-aa4c-859e9f7b7c38} 0xfff 170**

    > [!Note]  
    > Ersetzen Sie "x: \\ " durch den Pfad zu dem Verzeichnis, in dem die Ablauf Verfolgungs Protokolldatei gespeichert werden soll.

     

2.  Verwenden Sie den folgenden Befehl, um die Ablauf Verfolgung anzuhalten:

    **logman stoppt VSS-ETS**

Die Ablauf Verfolgungs Protokolldatei ist *x \\ :* VSS. ETL.

Weitere Informationen zum Logman-Tool finden Sie unter [logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).

## <a name="using-tracelog"></a>Verwenden von tracelog

Im folgenden Verfahren wird die Verwendung von tracelog beschrieben.

**So verwenden Sie tracelog**

1.  Erstellen Sie eine Textdatei mit dem Namen "VSS. CTL", die nur den folgenden Text enthält:

    **9138500e-3648-4edb-aa4c-859e9f7b7c38 VSS**

2.  Verwenden Sie den folgenden Befehl zum Starten der Ablauf Verfolgung:

    **tracelog-Start VSS-f** *x: \\ * * * VSS. ETL-GUID VSS. CTL-Flag 0xFF-Level 0xaa**

    > [!Note]  
    > Ersetzen Sie "x: \\ " durch den Pfad zu dem Verzeichnis, in dem die Ablauf Verfolgungs Protokolldatei gespeichert werden soll.

     

3.  Verwenden Sie den folgenden Befehl, um die Ablauf Verfolgung anzuhalten:

    **tracelog-VSS Abbrechen**

Die Ablauf Verfolgungs Protokolldatei ist *x \\ :* VSS. ETL.

Weitere Informationen zum tracelog-Tool finden Sie unter [tracelog](https://msdn.microsoft.com/library/ms797927.aspx).

 

 
