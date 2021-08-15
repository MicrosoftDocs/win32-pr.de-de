---
title: WER-Einstellungen
description: Einstellungen, um die Problemberichterstattung anzupassen. Alle diese Einstellungen können mit Gruppenrichtlinie festgelegt werden. Einige können auch im Action Center für Windows 7 und Windows 8 geändert werden. Verwenden Sie für Windows 10 die Suchfunktion in Einstellungen, um erweiterte Systemeinstellungen anzeigen zu suchen.
ms.assetid: 031c5591-31b0-42f1-9a98-ecf10a5d5571
keywords:
- Windows fehlerberichterstattung Windows-Fehlerberichterstattung , Einstellungen
ms.topic: article
ms.date: 03/12/2021
ms.openlocfilehash: 4586c4f282cbc5c4e2f683c0764eac048f6c05d22a1972cb0ceb84f9699c7925
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118442229"
---
# <a name="wer-settings"></a>WER-Einstellungen

Windows-Fehlerberichterstattung (WER) bietet viele Einstellungen zum Anpassen der Problemberichterstattung. Alle diese Einstellungen können mit Gruppenrichtlinie festgelegt werden. Einige können auch im **Action Center** für Windows 7 und Windows 8 geändert werden. Verwenden Sie für Windows 10 die Suchfunktion in Einstellungen, um **erweiterte Systemeinstellungen anzeigen** zu suchen. WER-Einstellungen befinden sich in einem der folgenden Registrierungsunterschlüssel:

-   **HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **Windows-Fehlerberichterstattung**
-   **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **Windows-Fehlerberichterstattung**

## <a name="windows-error-reporting-subkey"></a>Windows-Fehlerberichterstattung Unterschlüssel

<dl> <dt>

<span id="BypassDataThrottling"></span><span id="bypassdatathrottling"></span><span id="BYPASSDATATHROTTLING"></span>**BypassDataThrottling**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>

0: Deaktivieren Sie die Datenumgehungsdrosselung. Wenn die Umgehung deaktiviert oder nicht als Richtlinieneinstellung konfiguriert ist, drosselt WER die Daten standardmäßig. WER lädt nicht mehr als eine CAB-Datei für einen Bericht hoch, der Daten zu den gleichen Ereignistypen enthält.

</dd> <dd>

1: Aktivieren Sie die Datenumgehungsdrosselung. WER drosselt keine Daten. WER lädt zusätzliche CAB-Dateien hoch, die Daten zu den gleichen Ereignistypen enthalten können wie ein zuvor hochgeladener Bericht.

</dd> </dl>

Gibt an, ob die Umgehung der WER-Clientdatendrosselung aktiviert werden soll.

</dd> <dt>

<span id="ConfigureArchive"></span><span id="configurearchive"></span><span id="CONFIGUREARCHIVE"></span>**ConfigureArchive**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>1 – Nur Parameter (Standardeinstellung für Windows 7)</dd> <dd>2 – Alle Daten (Standardeinstellung für Windows Vista)</dd> </dl>

Ob nur Parameter oder alle Daten archiviert werden sollen

</dd> <dt>

<span id="Consent_DefaultConsent"></span><span id="consent_defaultconsent"></span><span id="CONSENT_DEFAULTCONSENT"></span>**Consent \\ DefaultConsent**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>1 – Immer fragen (Standard)</dd> <dd>2 – Nur Parameter</dd> <dd>3– Parameter und sichere Daten</dd> <dd>4 – Alle Daten</dd> </dl>

Standardmäßige Zustimmungsauswahl

</dd> <dt>

<span id="Consent_DefaultOverrideBehavior"></span><span id="consent_defaultoverridebehavior"></span><span id="CONSENT_DEFAULTOVERRIDEBEHAVIOR"></span>**Consent \\ DefaultOverrideBehavior**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>0 – Die vertikale Zustimmung überschreibt die Standardeinwilligung (Standard).</dd> <dd>1– Die Standardeinwilligung überschreibt die anwendungsspezifische Zustimmung.</dd> </dl>

Gibt an, ob die Standardmäßige Zustimmung die vertikale Zustimmung außer Kraft setzt.

</dd> <dt>

<span id="Consent__VerticalName_"></span><span id="consent__verticalname_"></span><span id="CONSENT__VERTICALNAME_"></span>**Consent \\ \[ VerticalName\]**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>1 – Immer fragen (Standard)</dd> <dd>2 – Nur Parameter</dd> <dd>3– Parameter und sichere Daten</dd> <dd>4 – Alle Daten</dd> </dl>

Zustimmungsauswahl für das WER-Plug-In

</dd> <dt>

<span id="CorporateWERDirectory"></span><span id="corporatewerdirectory"></span><span id="CORPORATEWERDIRECTORY"></span>**CorporateWERDirectory**
</dt> <dd>

**REG \_ SZ**

Der Verzeichnispfad

Zielverzeichnis auf dem Server

</dd> <dt>

<span id="CorporateWERPortNumber"></span><span id="corporatewerportnumber"></span><span id="CORPORATEWERPORTNUMBER"></span>**CorporateWERPortNumber**
</dt> <dd>

**REG \_ DWORD**

Die Portnummer

Portnummer, die mit dem Unternehmensserver verwendet werden soll

</dd> <dt>

<span id="CorporateWERServer"></span><span id="corporatewerserver"></span><span id="CORPORATEWERSERVER"></span>**CorporateWERServer**
</dt> <dd>

**REG \_ SZ**

Name des Servers

Name des Unternehmensservers

</dd> <dt>

<span id="CorporateWERUseAuthentication"></span><span id="corporateweruseauthentication"></span><span id="CORPORATEWERUSEAUTHENTICATION"></span>**CorporateWERUseAuthentication**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>0 – Nein (Standard)</dd> <dd>1 – Ja</dd> </dl>

Ob Windows integrierte Authentifizierung verwendet werden soll

</dd> <dt>

<span id="CorporateWERUseSSL"></span><span id="corporatewerusessl"></span><span id="CORPORATEWERUSESSL"></span>**CorporateWERUseSSL**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>0 – Nein (Standard)</dd> <dd>1 – Ja</dd> </dl>

Gibt an, ob SSL verwendet werden soll.

</dd> <dt>

<span id="DebugApplications__ExeName___replace___ExeName___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="debugapplications__exename___replace___exename___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="DEBUGAPPLICATIONS__EXENAME___REPLACE___EXENAME___WITH_AN_ACTUAL_NAME_OF_AN_.EXE_FILE__FOR_EXAMPLE___NOTEPAD.EXE__"></span>**DebugApplications \\ \[ ExeName \] (ersetzen Sie \[ "ExeName" \] durch einen tatsächlichen Namen einer .exe Datei, z.B. "notepad.exe").**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:

<dl> <dd>0 – Prozesse mit dem Namen eines ausführbaren Images mit dem Namen **\[ ExeName \]** erfordern nicht, dass der Benutzer **Debuggen** oder **Fortfahren** (Standard) auswählen muss.</dd> <dd>1– Für Prozesse mit dem Namen **\[ exeName \]** eines ausführbaren Images muss der Benutzer **Debuggen** oder **Fortfahren** auswählen.</dd> </dl> </dd> <dt>

<span id="DebugApplications________is_the_literal_value_name_"></span><span id="debugapplications________is_the_literal_value_name_"></span><span id="DEBUGAPPLICATIONS________IS_THE_LITERAL_VALUE_NAME_"></span>**DebugApplications \\ \* (" ist der \* Literalwertname)**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:

<dl> <dd>0 – Alle Prozesse mit Ausnahme der prozesse, die explizit in der Einstellung **DebugApplications \\ \[ \] ExeName** angegeben sind, erfordern nicht, dass der Benutzer **Debuggen** oder **Fortfahren** (Standard) auswählen muss.</dd> <dd>1 – Für alle Prozesse mit Ausnahme der prozesse, die explizit in  der Einstellung **\\ \[ \] DebuggenAnwendungsname angegeben** sind, muss der Benutzer **Debuggen** oder Fortfahren auswählen.</dd> </dl> </dd> <dt>

<span id="DisableArchive"></span><span id="disablearchive"></span><span id="DISABLEARCHIVE"></span>**DisableArchive**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>0–Aktiviert</dd> <dd>1 – Deaktiviert</dd> </dl>

Aktivieren oder Deaktivieren des Archivs

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>0 – Aktiviert (Standard)</dd> <dd>1 – Deaktiviert</dd> </dl>

Aktivieren oder Deaktivieren von WER

</dd> <dt>

<span id="DisableQueue"></span><span id="disablequeue"></span><span id="DISABLEQUEUE"></span>**DisableQueue**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>0–Aktiviert</dd> <dd>1 – Deaktiviert</dd> </dl>

Aktivieren oder Deaktivieren von Berichtswarteschlangen

</dd> <dt>

<span id="DontShowUI"></span><span id="dontshowui"></span><span id="DONTSHOWUI"></span>**DontShowUI**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>0 – Benutzeroberfläche (Standard)</dd> <dd>1 – Keine Benutzeroberfläche</dd> </dl>

Aktivieren oder Deaktivieren der WER-Benutzeroberfläche

</dd> <dt>

<span id="DontSendAdditionalData"></span><span id="dontsendadditionaldata"></span><span id="DONTSENDADDITIONALDATA"></span>**DontSendAdditionalData**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>0 – Senden (Standard)</dd> <dd>1 – Nicht senden</dd> </dl>

Gibt an, ob das Senden von Daten auf zweiter Ebene verhindert werden soll.

</dd> <dt>

<span id="ExcludedApplications__Application_Name_"></span><span id="excludedapplications__application_name_"></span><span id="EXCLUDEDAPPLICATIONS__APPLICATION_NAME_"></span>**\\ \[ ExcludedApplications-Anwendungsname\]**
</dt> <dd>

**REG \_ SZ**

Verwenden [ **von WerAddExcludedApplication**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication)

Liste der ausgeschlossenen Anwendungen

</dd> <dt>

<span id="ForceQueue"></span><span id="forcequeue"></span><span id="FORCEQUEUE"></span>**ForceQueue**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>0 – Nein (Standard)</dd> <dd>1 – Ja</dd> </dl>

Ob alle Berichte an die Warteschlange des Benutzers gesendet werden sollen

</dd> <dt>

<span id="LocalDumps_DumpFolder_or_LocalDumps__Application_Name__DumpFolder"></span><span id="localdumps_dumpfolder_or_localdumps__application_name__dumpfolder"></span><span id="LOCALDUMPS_DUMPFOLDER_OR_LOCALDUMPS__APPLICATION_NAME__DUMPFOLDER"></span>**LocalDumps \\ DumpFolder** oder **LocalDumps \\ \[ Application Name \] \\ DumpFolder**
</dt> <dd>

**REG \_ EXPAND \_ SZ**

Der Verzeichnispfad. Der Standardwert ist %LOCALAPPDATA% \\ CrashDumps. Wenn der Standardwert nicht verwendet wird, muss die Anwendung sicherstellen, dass der Ordner über eine ausreichende ACL verfügt.

**Windows Vista:** Die Registrierungswerte unter dem **LocalDumps-Schlüssel** werden nicht unterstützt. Beachten Sie, dass sich dieses Verhalten mit Windows Server 2008 und Windows Vista mit Service Pack 1 (SP1) geändert hat.

Der Pfad, in dem die Dumpdateien gespeichert werden sollen.

Beachten Sie, dass prozessspezifische Einstellungen alle vorhandenen globalen Einstellungen außer Kraft setzen. Weitere Informationen finden Sie unter [Sammeln von User-Mode Dumps.](collecting-user-mode-dumps.md)

Diese Einstellung wird in der **Registrierungsstruktur HKEY \_ CURRENT \_ USER** nicht unterstützt.

</dd> <dt>

<span id="LocalDumps_DumpCount_or_LocalDumps__Application_Name__DumpCount"></span><span id="localdumps_dumpcount_or_localdumps__application_name__dumpcount"></span><span id="LOCALDUMPS_DUMPCOUNT_OR_LOCALDUMPS__APPLICATION_NAME__DUMPCOUNT"></span>**LocalDumps \\ DumpCount** oder **LocalDumps \\ \[ Application Name \] \\ DumpCount**
</dt> <dd>

**REG \_ DWORD**

Die maximale Anzahl. Der Standardwert ist 10. Wenn der maximale Wert überschritten wird, wird die älteste Speicherabbilddatei im Ordner durch die neue Dumpdatei ersetzt.

**Windows Vista:** Die Registrierungswerte unter dem **LocalDumps-Schlüssel** werden nicht unterstützt. Beachten Sie, dass sich dieses Verhalten mit Windows Server 2008 und Windows Vista mit SP1 geändert hat.

Die maximale Anzahl von Sicherungsdateien im Ordner.

Diese Einstellung wird in der **Registrierungsstruktur HKEY \_ CURRENT \_ USER** nicht unterstützt.

</dd> <dt>

<span id="LocalDumps_DumpType_or_LocalDumps__Application_Name__DumpType"></span><span id="localdumps_dumptype_or_localdumps__application_name__dumptype"></span><span id="LOCALDUMPS_DUMPTYPE_OR_LOCALDUMPS__APPLICATION_NAME__DUMPTYPE"></span>**LocalDumps \\ DumpType** oder **LocalDumps \\ \[ Application Name \] \\ DumpType**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>0 – Benutzerdefiniertes Speicherabbild</dd> <dd>1 – Minidump (Standard)</dd> <dd>2– Vollständiges Speicherabbild</dd> </dl>

**Windows Vista:** Die Registrierungswerte unter dem **LocalDumps-Schlüssel** werden nicht unterstützt. Beachten Sie, dass sich dieses Verhalten mit Windows Server 2008 und Windows Vista mit SP1 geändert hat.

Der Dumptyp.

Diese Einstellung wird in der **Registrierungsstruktur HKEY \_ CURRENT \_ USER** nicht unterstützt.

</dd> <dt>

<span id="LocalDumps_CustomDumpFlags_or_LocalDumps__Application_Name__CustomDumpFlags"></span><span id="localdumps_customdumpflags_or_localdumps__application_name__customdumpflags"></span><span id="LOCALDUMPS_CUSTOMDUMPFLAGS_OR_LOCALDUMPS__APPLICATION_NAME__CUSTOMDUMPFLAGS"></span>**LocalDumps \\ CustomDumpFlags** oder **LocalDumps \\ \[ Anwendungsname \] \\ CustomDumpFlags**
</dt> <dd>

**REG \_ DWORD**

Mindestens ein Wert aus der [**MINIDUMP \_ TYPE-Enumeration.**](/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type) Der Standardwert ist {**MiniDumpWithDataSegs** \| **MiniDumpWithUnloadedModules** \| **MiniDumpWithProcessThreadData**}.

**Windows Vista:** Die Registrierungswerte unter dem **LocalDumps-Schlüssel** werden nicht unterstützt. Beachten Sie, dass sich dieses Verhalten mit Windows Server 2008 und Windows Vista mit SP1 geändert hat.

Die zu verwendenden benutzerdefinierten Speicherabbildoptionen. Dieser Wert wird nur verwendet, wenn **DumpType** auf 0 festgelegt ist.

Diese Einstellung wird in der **Registrierungsstruktur HKEY \_ CURRENT \_ USER** nicht unterstützt.

</dd> <dt>

<span id="LoggingDisabled"></span><span id="loggingdisabled"></span><span id="LOGGINGDISABLED"></span>**LoggingDisabled**
</dt> <dd>

**REG \_ DWORD**

Mögliche Werte:<dl> <dd>0 –Aktiviert (Standard)</dd> <dd>1– Deaktiviert</dd> </dl>

Aktivieren oder Deaktivieren der Protokollierung

</dd> <dt>

<span id="MaxArchiveCount"></span><span id="maxarchivecount"></span><span id="MAXARCHIVECOUNT"></span>**MaxArchiveCount**
</dt> <dd>

**REG \_ DWORD**

Bereich der möglichen Werte: 1 bis 5000. Der Standardwert lautet 1000.

Maximale Größe des Archivs in Dateien

</dd> <dt>

<span id="MaxQueueCount"></span><span id="maxqueuecount"></span><span id="MAXQUEUECOUNT"></span>**MaxQueueCount**
</dt> <dd>

**REG \_ DWORD**

Bereich der möglichen Werte: 1 bis 500. Der Standardwert ist 50.

Maximale Größe der Warteschlange

</dd> <dt>

<span id="QueuePesterInterval"></span><span id="queuepesterinterval"></span><span id="QUEUEPESTERINTERVAL"></span>**QueuePesterInterval**
</dt> <dd>

**REG \_ DWORD**

Anzahl von Tagen

Interval between reminders to the user to check for solutions, in days (Intervall zwischen Erinnerungen an den Benutzer, um nach Lösungen zu suchen) in Tagen

</dd> <dt>

<span id="RuntimeExceptionHelperModules___pwszOutOfProcessCallbackDll_name_including_path_"></span><span id="runtimeexceptionhelpermodules___pwszoutofprocesscallbackdll_name_including_path_"></span><span id="RUNTIMEEXCEPTIONHELPERMODULES___PWSZOUTOFPROCESSCALLBACKDLL_NAME_INCLUDING_PATH_"></span>**RuntimeExceptionHelperModules! \[ pwszOutOfProcessCallbackDll-Name einschließlich Pfad\]**
</dt> <dd>

**REG \_ DWORD**

Der Inhalt des Werts wird ignoriert.

Der Name des Werts wird verwendet, um den pwszOutOfProcessCallbackDll-Wert abzurufen.

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Registrierungswert wird nicht unterstützt.

</dd> </dl>

## <a name="wer-live-kernel-reports-settings"></a>WER Live Kernel Reports Einstellungen

Die Live Kernel Reports-Einstellungen von WER, die als Nächstes beschrieben werden, befinden sich beide unter dem folgenden Registrierungsunterschlüssel:

-   **HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Control** \\ **CrashControl**

## <a name="fulllivekernelreports-subkey"></a>FullLiveKernelReports-Unterschlüssel

<dl> <dt>

<span id="ComponentThrottleThreshold"></span><span id="componentthrottlethreshold"></span><span id="COMPONENTTHROTTLETHRESHOLD"></span>**ComponentThrottleThreshold**
</dt> <dd>

**REG \_ DWORD**

Der Schwellenwert (in Stunden), mit dem festgelegt wird, wie oft eine einzelne Komponente ein vollständiges Livedump erstellen kann. Dieser Wert muss größer oder gleich **SystemThrottleThreshold** sein. Wenn beide auf 0 (null) festgelegt werden, wird die gesamte zeitbasierte Drosselung deaktiviert. Der Standardwert ist 168 (7 Tage).

</dd> <dt>

<span id="FullLiveReportsMax"></span><span id="fulllivereportsmax"></span><span id="FULLLIVEREPORTSMAX"></span>**FullLiveReportsMax**
</dt> <dd>

**REG \_ DWORD**

Die maximale Anzahl von vollständigen Livedumps, die zu einem bestimmten Zeitpunkt auf dem Datenträger vorhanden sein können. Der Standardwert ist 1. Wenn Sie diesen Wert auf 0 (null) festlegen, wird das Livedumpfeature deaktiviert.

</dd> <dt>

<span id="LastFullLiveReport"></span><span id="lastfulllivereport"></span><span id="LASTFULLLIVEREPORT"></span>**LastFullLiveReport**
</dt> <dd>

**REG \_ QWORD**

Ein [SystemTime-Wert,](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) der die uhrzeit des letzten vollständigen Liveberichts für das System oder einen bestimmten ReportType angibt. Dies wird verwendet, um zu berechnen, ob ein Richtlinienschwellenwert erfüllt wurde.

</dd> <dt>

<span id="SystemThrottleThreshold"></span><span id="systemthrottlethreshold"></span><span id="SYSTEMTHROTTLETHRESHOLD"></span>**SystemThrottleThreshold**
</dt> <dd>

**REG \_ DWORD**

Der Schwellenwert (in Stunden), mit dem jede Komponente im System ein vollständiges Livedump erstellen kann. Der Standardwert ist 120 (5 Tage).

</dd> </dl>

## <a name="livekernelreports-subkey"></a>LiveKernelReports-Unterschlüssel

<dl> <dt>

<span id="LiveKernelReportsPath"></span><span id="livekernelreportspath"></span><span id="LIVEKERNELREPORTSPATH"></span>**LiveKernelReportsPath**
</dt> <dd>

**REG \_ SZ**


Der umgeleitete Speicherort von Live-Kernelberichten. Der Standardspeicherort ist %systemroot%\LiveKernelReports. Dieser Wert muss ein gültiger Pfad sein. Der Pfad muss im NT-Pfadformat vorliegen. Beispiel: \? ?\C:\LiveDumpsFolder.  Weitere Informationen zu Pfadformaten finden Sie unter [Dateipfadformate auf Windows Systemen.](/dotnet/standard/io/file-path-formats)

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WER-Referenz](wer-reference.md)
</dt> </dl>

 

 
