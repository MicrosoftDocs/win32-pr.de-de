---
title: WER-Einstellungen
description: Einstellungen zum Anpassen der Problembericht Erstellungs Umgebung. Alle diese Einstellungen können mit Gruppenrichtlinie festgelegt werden. Einige können auch im Aktions Center für Windows 7 und Windows 8 geändert werden. Verwenden Sie für Windows 10 die Suchfunktion in den Einstellungen, um Erweiterte Systemeinstellungen anzuzeigen.
ms.assetid: 031c5591-31b0-42f1-9a98-ecf10a5d5571
keywords:
- Windows-Fehlerberichterstattung für die Windows-Fehlerberichterstattung, Einstellungen
ms.topic: article
ms.date: 03/12/2021
ms.openlocfilehash: 28b6abbda7d851daddb75ec534b8128d1a831b3f
ms.sourcegitcommit: 434d5437d4c31c47358598ea5275177c2698f557
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/13/2021
ms.locfileid: "106366613"
---
# <a name="wer-settings"></a>WER-Einstellungen

Windows-Fehlerberichterstattung (wer) bietet viele Einstellungen zum Anpassen der Problembericht Erstellungs Umgebung. Alle diese Einstellungen können mit Gruppenrichtlinie festgelegt werden. Einige können auch im **Aktions Center** für Windows 7 und Windows 8 geändert werden. Verwenden Sie für Windows 10 die Suchfunktion in den Einstellungen, um **Erweiterte Systemeinstellungen anzuzeigen**. Die wer-Einstellungen befinden sich in einem der folgenden Registrierungs Unterschlüssel:

-   **HKEY \_ Aktuelle \_ Benutzer** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **Windows-Fehlerberichterstattung**
-   **HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **Windows** \\ **Windows-Fehlerberichterstattung**

## <a name="windows-error-reporting-subkey"></a>Windows-Fehlerberichterstattung Unterschlüssel

<dl> <dt>

<span id="BypassDataThrottling"></span><span id="bypassdatathrottling"></span><span id="BYPASSDATATHROTTLING"></span>**Bypassdatathrottndes**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>

0-Drosselung der Daten Umgehung deaktivieren. Wenn die Umgehung deaktiviert oder nicht als Richtlinien Einstellung konfiguriert ist, werden die Daten von wer standardmäßig gedrosselt. Wer lädt nicht mehr als eine CAB-Datei für einen Bericht hoch, der Daten zu denselben Ereignis Typen enthält.

</dd> <dd>

1: Aktivieren Sie die Drosselung der Daten Umgehung. Wer führt keine Drosselung von Daten aus. Wer lädt zusätzliche CAB-Dateien hoch, die Daten zu denselben Ereignis Typen wie ein früherer hochgeladener Bericht enthalten können.

</dd> </dl>

Gibt an, ob die Umgehung der wer-Client Daten Drosselung aktiviert werden soll.

</dd> <dt>

<span id="ConfigureArchive"></span><span id="configurearchive"></span><span id="CONFIGUREARCHIVE"></span>**Konfigurieren von rearchive**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>1-nur Parameter (Standard unter Windows 7)</dd> <dd>2-alle Daten (Standard unter Windows Vista)</dd> </dl>

Ob nur Parameter oder alle Daten archiviert werden sollen

</dd> <dt>

<span id="Consent_DefaultConsent"></span><span id="consent_defaultconsent"></span><span id="CONSENT_DEFAULTCONSENT"></span>**Zustimmung \\ defaultconsent**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>1-immer Fragen (Standard)</dd> <dd>2: nur Parameter</dd> <dd>3-Parameter und sichere Daten</dd> <dd>4-alle Daten</dd> </dl>

Standardmäßige Zustimmungs Auswahl

</dd> <dt>

<span id="Consent_DefaultOverrideBehavior"></span><span id="consent_defaultoverridebehavior"></span><span id="CONSENT_DEFAULTOVERRIDEBEHAVIOR"></span>**Zustimmung von \\ defauldeverridebehavior**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>0-die vertikale Zustimmung überschreibt die Standard Zustimmung (Standard).</dd> <dd>1: die Standard Zustimmung wird die anwendungsspezifische Zustimmung überschreiben.</dd> </dl>

Gibt an, ob die Standard Zustimmung die vertikale Zustimmung überschreibt

</dd> <dt>

<span id="Consent__VerticalName_"></span><span id="consent__verticalname_"></span><span id="CONSENT__VERTICALNAME_"></span>**\\ \[ Verticalname der Zustimmung\]**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>1-immer Fragen (Standard)</dd> <dd>2: nur Parameter</dd> <dd>3-Parameter und sichere Daten</dd> <dd>4-alle Daten</dd> </dl>

Zustimmungs Auswahl für das wer-Plug-in

</dd> <dt>

<span id="CorporateWERDirectory"></span><span id="corporatewerdirectory"></span><span id="CORPORATEWERDIRECTORY"></span>**Corporatewerdirectory**
</dt> <dd>

**REG- \_ SZ**

Der Verzeichnispfad

Zielverzeichnis auf dem Server

</dd> <dt>

<span id="CorporateWERPortNumber"></span><span id="corporatewerportnumber"></span><span id="CORPORATEWERPORTNUMBER"></span>**Corporatewerportnumber**
</dt> <dd>

**REG \_ DWORD**

Die Portnummer

Port Nummer, die mit dem Unternehmensserver verwendet werden soll

</dd> <dt>

<span id="CorporateWERServer"></span><span id="corporatewerserver"></span><span id="CORPORATEWERSERVER"></span>**Corporatewerserver**
</dt> <dd>

**REG- \_ SZ**

Name des Servers

Name des Unternehmens Servers

</dd> <dt>

<span id="CorporateWERUseAuthentication"></span><span id="corporateweruseauthentication"></span><span id="CORPORATEWERUSEAUTHENTICATION"></span>**Corporateweruseauthentication**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>0-Nein (Standard)</dd> <dd>1 – Ja</dd> </dl>

Ob die integrierte Windows-Authentifizierung verwendet werden soll

</dd> <dt>

<span id="CorporateWERUseSSL"></span><span id="corporatewerusessl"></span><span id="CORPORATEWERUSESSL"></span>**Corporatewerus Essl**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>0-Nein (Standard)</dd> <dd>1 – Ja</dd> </dl>

Ob SSL verwendet werden soll

</dd> <dt>

<span id="DebugApplications__ExeName___replace___ExeName___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="debugapplications__exename___replace___exename___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="DEBUGAPPLICATIONS__EXENAME___REPLACE___EXENAME___WITH_AN_ACTUAL_NAME_OF_AN_.EXE_FILE__FOR_EXAMPLE___NOTEPAD.EXE__"></span>**Debugapplications \\ \[ EXEName \] (ersetzen Sie " \[ EXEName \] " durch den tatsächlichen Namen einer exe-Datei, z. b. "notepad.exe")**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:

<dl> <dd>0-für Prozesse mit dem ausführbaren Image Namen **\[ EXEName \]** ist es nicht erforderlich, dass der Benutzer **Debuggen** oder **fortfahren** auswählt (Standard).</dd> <dd>1: für Prozesse mit dem Namen des ausführbaren Images von **\[ EXEName \]** muss der Benutzer **Debuggen** oder **fortfahren** auswählen.</dd> </dl> </dd> <dt>

<span id="DebugApplications________is_the_literal_value_name_"></span><span id="debugapplications________is_the_literal_value_name_"></span><span id="DEBUGAPPLICATIONS________IS_THE_LITERAL_VALUE_NAME_"></span>**Debug Applications \\ \* (" \* " ist der literalwertname)**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:

<dl> <dd>0-alle Prozesse, ausgenommen der explizit in der Einstellung **debugapplications \\ \[ EXEName \]** angegebenen Prozesse, erfordern nicht, dass der Benutzer **Debuggen** oder **fortfahren** auswählt (Standard).</dd> <dd>1: alle Prozesse außer den explizit in der Einstellung **debugapplications \\ \[ EXEName \]** angegebenen Prozessen erfordern, dass der **Benutzer Debuggen oder** **fortfahren** auswählt.</dd> </dl> </dd> <dt>

<span id="DisableArchive"></span><span id="disablearchive"></span><span id="DISABLEARCHIVE"></span>**Disablearchive**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>0–Aktiviert</dd> <dd>1 – Deaktiviert</dd> </dl>

Aktivieren oder Deaktivieren des Archivs

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>0-aktiviert (Standard)</dd> <dd>1 – Deaktiviert</dd> </dl>

Aktivieren oder Deaktivieren von wer

</dd> <dt>

<span id="DisableQueue"></span><span id="disablequeue"></span><span id="DISABLEQUEUE"></span>**Disablequeue**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>0–Aktiviert</dd> <dd>1 – Deaktiviert</dd> </dl>

Aktivieren oder Deaktivieren von Berichts Warteschlangen

</dd> <dt>

<span id="DontShowUI"></span><span id="dontshowui"></span><span id="DONTSHOWUI"></span>**DontShowUI**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>0-UI (Standard)</dd> <dd>1-keine Benutzeroberfläche</dd> </dl>

Aktivieren oder Deaktivieren der Wer-Benutzeroberfläche

</dd> <dt>

<span id="DontSendAdditionalData"></span><span id="dontsendadditionaldata"></span><span id="DONTSENDADDITIONALDATA"></span>**Dontsendadditionaldata**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>0-senden (Standard)</dd> <dd>1-nicht senden</dd> </dl>

Ob das Senden von Daten der zweiten Ebene verhindert werden soll

</dd> <dt>

<span id="ExcludedApplications__Application_Name_"></span><span id="excludedapplications__application_name_"></span><span id="EXCLUDEDAPPLICATIONS__APPLICATION_NAME_"></span>**Ausschluss \\ \[ Anwendungs Name\]**
</dt> <dd>

**REG- \_ SZ**

Verwenden von [ **weraddexcludebug**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication)

Liste ausgeschlossener Anwendungen

</dd> <dt>

<span id="ForceQueue"></span><span id="forcequeue"></span><span id="FORCEQUEUE"></span>**Forcequeue**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>0-Nein (Standard)</dd> <dd>1 – Ja</dd> </dl>

Ob alle Berichte an die Warteschlange des Benutzers gesendet werden sollen

</dd> <dt>

<span id="LocalDumps_DumpFolder_or_LocalDumps__Application_Name__DumpFolder"></span><span id="localdumps_dumpfolder_or_localdumps__application_name__dumpfolder"></span><span id="LOCALDUMPS_DUMPFOLDER_OR_LOCALDUMPS__APPLICATION_NAME__DUMPFOLDER"></span>**Localdumps \\ Dumpfolder** oder **localdumps \\ \[ Anwendungs Name \] \\ dumpfolder**
</dt> <dd>

**REG \_ Expand \_ SZ**

Der Verzeichnispfad. Der Standardwert ist% LocalAppData% \\ CrashDumps. Wenn der Standardwert nicht verwendet wird, muss die Anwendung sicherstellen, dass der Ordner über eine ausreichende ACL verfügt.

**Windows Vista:** Die Registrierungs Werte unter dem **localdumps** -Schlüssel werden nicht unterstützt. Beachten Sie, dass sich dieses Verhalten mit Windows Server 2008 und Windows Vista mit Service Pack 1 (SP1) geändert hat.

Der Pfad, in dem die Dumpdateien gespeichert werden sollen.

Beachten Sie, dass prozessspezifische Einstellungen sämtliche globalen Einstellungen überschreiben, die für weitere Informationen vorhanden sind. Weitere Informationen finden Sie unter [Erfassen von User-Mode Dumps](collecting-user-mode-dumps.md).

Diese Einstellung wird in der Registrierungs Struktur des **aktuellen HKEY- \_ \_ Benutzers** nicht unterstützt.

</dd> <dt>

<span id="LocalDumps_DumpCount_or_LocalDumps__Application_Name__DumpCount"></span><span id="localdumps_dumpcount_or_localdumps__application_name__dumpcount"></span><span id="LOCALDUMPS_DUMPCOUNT_OR_LOCALDUMPS__APPLICATION_NAME__DUMPCOUNT"></span>**Localdumps \\ Dumpcount** oder **localdumps \\ \[ Anwendungs Name \] \\ dumpcount**
</dt> <dd>

**REG \_ DWORD**

Die maximale Anzahl. Der Standardwert ist 10. Wenn der Höchstwert überschritten wird, wird die älteste Dumpdatei im Ordner durch die neue Dumpdatei ersetzt.

**Windows Vista:** Die Registrierungs Werte unter dem **localdumps** -Schlüssel werden nicht unterstützt. Beachten Sie, dass sich dieses Verhalten in Windows Server 2008 und Windows Vista mit SP1 geändert hat.

Die maximale Anzahl von Dumpdateien im Ordner.

Diese Einstellung wird in der Registrierungs Struktur des **aktuellen HKEY- \_ \_ Benutzers** nicht unterstützt.

</dd> <dt>

<span id="LocalDumps_DumpType_or_LocalDumps__Application_Name__DumpType"></span><span id="localdumps_dumptype_or_localdumps__application_name__dumptype"></span><span id="LOCALDUMPS_DUMPTYPE_OR_LOCALDUMPS__APPLICATION_NAME__DUMPTYPE"></span>**Localdumps \\ Dumptype** oder **localdumps \\ \[ Anwendungs Name \] \\ dumptype**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>0-benutzerdefiniertes Dump</dd> <dd>1-Minidump (Standard)</dd> <dd>2: vollständiges Dump</dd> </dl>

**Windows Vista:** Die Registrierungs Werte unter dem **localdumps** -Schlüssel werden nicht unterstützt. Beachten Sie, dass sich dieses Verhalten in Windows Server 2008 und Windows Vista mit SP1 geändert hat.

Der dumptyp.

Diese Einstellung wird in der Registrierungs Struktur des **aktuellen HKEY- \_ \_ Benutzers** nicht unterstützt.

</dd> <dt>

<span id="LocalDumps_CustomDumpFlags_or_LocalDumps__Application_Name__CustomDumpFlags"></span><span id="localdumps_customdumpflags_or_localdumps__application_name__customdumpflags"></span><span id="LOCALDUMPS_CUSTOMDUMPFLAGS_OR_LOCALDUMPS__APPLICATION_NAME__CUSTOMDUMPFLAGS"></span>**Localdumps \\ Customdumpflags** oder **localdumps \\ \[ Anwendungs Name \] \\ customdumpflags**
</dt> <dd>

**REG \_ DWORD**

Mindestens ein Wert aus der [**Minidump- \_ Typenumeration**](/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type) . Der Standardwert ist {**minidumpwithdatasegs** \| **minidumpwithunloadedmodules** \| **minidumpwithprocessthreaddata**}.

**Windows Vista:** Die Registrierungs Werte unter dem **localdumps** -Schlüssel werden nicht unterstützt. Beachten Sie, dass sich dieses Verhalten in Windows Server 2008 und Windows Vista mit SP1 geändert hat.

Die benutzerdefinierten dumpoptionen, die verwendet werden sollen. Dieser Wert wird nur verwendet, wenn **dumptype** auf 0 festgelegt ist.

Diese Einstellung wird in der Registrierungs Struktur des **aktuellen HKEY- \_ \_ Benutzers** nicht unterstützt.

</dd> <dt>

<span id="LoggingDisabled"></span><span id="loggingdisabled"></span><span id="LOGGINGDISABLED"></span>**Loggingdeaktiviert**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>0 – aktiviert (Standard)</dd> <dd>1 – deaktiviert</dd> </dl>

Aktivieren oder Deaktivieren der Protokollierung

</dd> <dt>

<span id="MaxArchiveCount"></span><span id="maxarchivecount"></span><span id="MAXARCHIVECOUNT"></span>**Maxarchivecount**
</dt> <dd>

**REG \_ DWORD**

Bereich möglicher Werte: 1 – 5.000. Der Standardwert lautet 1000.

Maximale Größe des Archivs in Dateien

</dd> <dt>

<span id="MaxQueueCount"></span><span id="maxqueuecount"></span><span id="MAXQUEUECOUNT"></span>**Maxqueuecount**
</dt> <dd>

**REG \_ DWORD**

Bereich möglicher Werte: 1 – 500. Der Standardwert ist 50.

Maximale Größe der Warteschlange

</dd> <dt>

<span id="QueuePesterInterval"></span><span id="queuepesterinterval"></span><span id="QUEUEPESTERINTERVAL"></span>**Queuepeer Interval**
</dt> <dd>

**REG \_ DWORD**

Anzahl von Tagen

Intervall zwischen Erinnerungen an den Benutzer für die Überprüfung auf Lösungen in Tagen

</dd> <dt>

<span id="RuntimeExceptionHelperModules___pwszOutOfProcessCallbackDll_name_including_path_"></span><span id="runtimeexceptionhelpermodules___pwszoutofprocesscallbackdll_name_including_path_"></span><span id="RUNTIMEEXCEPTIONHELPERMODULES___PWSZOUTOFPROCESSCALLBACKDLL_NAME_INCLUDING_PATH_"></span>**Runtimeexceptionhelpermodules! \[ pwszouybprocesscallbackdll-Name einschließlich Pfad\]**
</dt> <dd>

**REG \_ DWORD**

Der Inhalt des Werts wird ignoriert.

Der Name des Werts wird zum Abrufen des pwszouesfprocesscallbackdll-Werts verwendet.

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Registrierungs Wert wird nicht unterstützt.

</dd> </dl>

## <a name="wer-live-kernel-reports-settings"></a>Einstellungen für wer Live Kernel Berichte

Die im nächsten beschriebenen Live Kernel Berichte-Einstellungen befinden sich beide unter dem folgenden Registrierungs Unterschlüssel:

-   **HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **CrashControl**

## <a name="fulllivekernelreports-subkey"></a>Fulllivekernelreports-Unterschlüssel

<dl> <dt>

<span id="ComponentThrottleThreshold"></span><span id="componentthrottlethreshold"></span><span id="COMPONENTTHROTTLETHRESHOLD"></span>**Componentthrottlethreshold**
</dt> <dd>

**REG \_ DWORD**

Der Schwellenwert (in Stunden), wie oft eine einzelne Komponente ein vollständiges livedump erstellen kann. Dieser Wert muss größer oder gleich **systemthrottlethreshold** sein. Wenn beide Werte auf 0 (null) festgelegt werden, wird die zeitbasierte Drosselung deaktiviert. Der Standardwert ist 168 (7 Tage).

</dd> <dt>

<span id="FullLiveReportsMax"></span><span id="fulllivereportsmax"></span><span id="FULLLIVEREPORTSMAX"></span>**Fulllivereportsmax**
</dt> <dd>

**REG \_ DWORD**

Die maximale Anzahl vollständiger Live Abbilder, die zu einem beliebigen Zeitpunkt auf dem Datenträger gespeichert werden können. Der Standardwert ist 1. Wenn dieser Wert auf NULL (0) festgelegt wird, wird die Live Dump-Funktion deaktiviert.

</dd> <dt>

<span id="LastFullLiveReport"></span><span id="lastfulllivereport"></span><span id="LASTFULLLIVEREPORT"></span>**Lastfulllivereport**
</dt> <dd>

**REG \_ QWORD**

Ein [SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Wert, der den Zeitpunkt des letzten vollständigen Live Berichts für das System oder einen bestimmten reportType angibt. Hiermit wird berechnet, ob ein Richtlinien Schwellenwert erfüllt wurde.

</dd> <dt>

<span id="SystemThrottleThreshold"></span><span id="systemthrottlethreshold"></span><span id="SYSTEMTHROTTLETHRESHOLD"></span>**Systemdrossellethreshold**
</dt> <dd>

**REG \_ DWORD**

Der Schwellenwert (in Stunden), wie oft eine beliebige Komponente im System ein vollständiges livedump erstellen kann. Der Standardwert ist 120 (5 Tage).

</dd> </dl>

## <a name="livekernelreports-subkey"></a>Livekernelreports-Unterschlüssel

<dl> <dt>

<span id="LiveKernelReportsPath"></span><span id="livekernelreportspath"></span><span id="LIVEKERNELREPORTSPATH"></span>**Livekernelreportspath**
</dt> <dd>

**REG- \_ SZ**


Der umgeleitete Speicherort von Live-Kernel-Berichten. Der Standard Speicherort ist%SystemRoot%\livekernelreports. Dieser Wert muss ein gültiger Pfad sein. Der Pfad muss im NT-Pfad Format vorliegen. Beispiel \? :? \c: \livedumpsfolder.  Weitere Informationen zu Pfad Formaten finden Sie unter  [Datei Pfad Formate auf Windows-Systemen](/dotnet/standard/io/file-path-formats).

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Wer-Verweis](wer-reference.md)
</dt> </dl>

 

 
