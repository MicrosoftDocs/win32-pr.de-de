---
description: In der folgenden Liste sind ereignisse aufgeführt, die von WMI-Protokollen in Windows Vista- und späteren Betriebssystemen unterstützt werden.
ms.assetid: ad8891cc-0b76-404d-81fc-961bcdbfae32
ms.tgt_platform: multiple
title: WMI-Ereignismeldungen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7bb2b0a732d79c8b8c11e8bd14a217ef1ee81eb29bead4a885003ea98f82898
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120710"
---
# <a name="wmi-event-messages"></a>WMI-Ereignismeldungen

In der folgenden Liste sind ereignisse aufgeführt, die von WMI-Protokollen in Windows Vista- und späteren Betriebssystemen unterstützt werden.

> [!Note]  
> Die folgende Dokumentation richtet sich an Entwickler und IT-Administratoren. Wenn Sie versuchen, eine WMI-Fehlermeldung auf Ihrem Basissystem [](https://support.microsoft.com/) zu beheben, finden Sie weitere Informationen auf der Microsoft-Support-Website.

 

<dl> <dt>

<span id="WBEM_MC_REPOSITORY_INCONSISTENT"></span><span id="wbem_mc_repository_inconsistent"></span>**WBEM \_ \_ MC-REPOSITORY \_ INKONSISTENT**
</dt> <dd> <dl> <dt>

1073747424 (0x400015E0)
</dt> <dt>



Der Windows Management Instrumentation Service hat eine Inkonsistenz mit dem WMI-Repository im Verzeichnis *%windir% \\ system32 \\ wbem-Repository \\* erkannt und konnte es nicht wiederherstellen. Das WMI-Repository wird nun gelöscht. Basierend auf dem Mechanismus für die automatische Wiederherstellung wird ein neues Repository erstellt.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_PROVIDER_SUBSYSTEM_LOCALSYSTEM_PROVIDER_LOAD"></span><span id="wbem_mc_provider_subsystem_localsystem_provider_load"></span>**WBEM \_ MC \_ PROVIDER \_ SUBSYSTEM \_ LOCALSYSTEM \_ PROVIDER \_ LOAD**
</dt> <dd> <dl> <dt>

2147483711 (0x8000003F)
</dt> <dt>



Der Anbieter %1 wurde im Windows Management Instrumentation-Namespace %2 registriert, um das LocalSystem-Konto zu verwenden. Dieses Konto ist privilegiert, und der Anbieter kann eine Sicherheitsverletzung verursachen, wenn es die Identität von Benutzeranforderungen nicht ordnungsgemäß angibt.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_MOF_NOT_LOADED_AT_RECOVERY"></span><span id="wbem_mc_mof_not_loaded_at_recovery"></span>**WBEM \_ MC MOF BEI DER \_ \_ \_ \_ \_ WIEDERHERSTELLUNG NICHT GELADEN**
</dt> <dd> <dl> <dt>

3221225476 (0xC0000004)
</dt> <dt>



Fehler %1 beim Versuch, MOF %2 beim Wiederherstellen von zu laden. MOF-Datei, die mit autorecover markiert ist.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_CANNOT_ACTIVATE_FILTER"></span><span id="wbem_mc_cannot_activate_filter"></span>**WBEM \_ MC KANN FILTER \_ NICHT \_ AKTIVIEREN \_**
</dt> <dd> <dl> <dt>

3221225482 (0xC000000A)
</dt> <dt>



Der Ereignisfilter mit der Abfrage "%2" konnte im Namespace "%1" aufgrund des Fehlers %3 nicht reaktiviert werden. Ereignisse können erst über diesen Filter übermittelt werden, wenn das Problem behoben wurde.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_INVALID_EVENT_PROVIDER_QUERY"></span><span id="wbem_mc_invalid_event_provider_query"></span>**WBEM \_ MC \_ INVALID \_ EVENT \_ PROVIDER \_ QUERY**
</dt> <dd> <dl> <dt>

3221225493 (0xC0000015)
</dt> <dt>



Der Ereignisanbieter %1 hat versucht, eine syntaktisch ungültige Abfrage "%2" zu registrieren. Die Abfrage wird ignoriert. Die Abfrage kann korrigiert werden, indem das WMI-Repository mit CIM Studio untersucht und die permanenten Abonnements für den aufgelisteten Anbieter und die Abfrage aktualisiert werden. Wenn das permanente Abonnement mit einer MOF-Datei erstellt wird, die ein installiertes Produkt enthält, muss der Anwendungsanbieter kontaktiert werden, um die fehlerhafte Registrierung zu korrigieren.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_INVALID_EVENT_PROVIDER_INTRINSIC_QUERY"></span><span id="wbem_mc_invalid_event_provider_intrinsic_query"></span>**SYSTEMINTERNE ABFRAGE DES WBEM \_ MC \_ \_ INVALID-EREIGNISANBIETERS \_ \_ \_**
</dt> <dd> <dl> <dt>

3221225494 (0xC0000016)
</dt> <dt>



Der Ereignisanbieter %1 hat versucht, eine systeminterne Ereignisabfrage "%2" im %3-Namespace zu registrieren, für die der Satz von Zielobjektklassen nicht bestimmt werden konnte. Die Abfrage wird ignoriert.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_TOO_BROAD"></span><span id="wbem_mc_event_provider_query_too_broad"></span>**WBEM \_ \_ \_ MC-EREIGNISANBIETERABFRAGE \_ \_ ZU \_ UMFANGREICH**
</dt> <dd> <dl> <dt>

3221225495 (0xC0000017)
</dt> <dt>



Der Ereignisanbieter %1 hat versucht, die Abfrage "%2" im %3-Namespace zu registrieren, der zu breit ist. Ereignisanbieter können keine Vom System bereitgestellten Ereignisse bereitstellen. Die Abfrage wird ignoriert. Wenden Sie sich an den Anwendungsanbieter.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_FOUND"></span><span id="wbem_mc_event_provider_query_not_found"></span>**WBEM \_ \_ MC-EREIGNISANBIETERABFRAGE \_ \_ NICHT \_ \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

3221225496 (0xC0000018)
</dt> <dt>



Der Ereignisanbieter %1 hat versucht, die Abfrage "%2" zu registrieren, deren Zielklasse "%3" im %4-Namespace nicht vorhanden ist. Die Abfrage wird ignoriert.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_EVENT"></span><span id="wbem_mc_event_provider_query_not_event"></span>**WBEM \_ MC \_ EVENT \_ PROVIDER \_ QUERY \_ NOT \_ EVENT**
</dt> <dd> <dl> <dt>

3221225497 (0xC0000019)
</dt> <dt>



Der Ereignisanbieter %1 hat versucht, die Abfrage &quot; %2 zu &quot; registrieren, deren Zielklasse &quot; %3 &quot; keine Ereignisklasse ist. Die Abfrage wird ignoriert. Wenden Sie sich an den Anwendungsanbieter.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_CORE_FAILURE"></span><span id="wbem_mc_wbem_core_failure"></span>**WBEM \_ MC \_ WBEM \_ CORE \_ FAILURE**
</dt> <dd> <dl> <dt>

3221225500 (0xC000001C)
</dt> <dt>



Fehler beim Initialisieren von WMI Core oder Provider SubSystem oder Event SubSystem mit der Fehlernummer %1. Dies kann auf eine schlecht installierte Version von WMI, einen Fehler beim WMI-Repositoryupgrade, unzureichenden Speicherplatz oder unzureichenden Arbeitsspeicher zurückzuführen sein.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_CONNECTION_FAILURE"></span><span id="wbem_mc_adap_connection_failure"></span>**WBEM \_ MC \_ \_ ADAP-VERBINDUNGSFEHLER \_**
</dt> <dd> <dl> <dt>

3221225515 (0xC000002B)
</dt> <dt>



Windows Adap der Verwaltungsinstrumentation konnte keine Verbindung mit namespace %1 herstellen. Der folgende Fehler ist %2.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_PERFLIB_PUTCLASS_FAILURE"></span><span id="wbem_mc_adap_perflib_putclass_failure"></span>**FEHLER BEI WBEM \_ MC \_ ADAP \_ PERFLIB \_ PUTCLASS \_**
</dt> <dd> <dl> <dt>

3221225520 (0xC0000030)
</dt> <dt>



Windows Adap für die Verwaltungsinstrumentation konnte das Objekt %1 im Namespace %2 aufgrund des folgenden Fehlers %3 nicht speichern.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERF"></span><span id="wbem_mc_adap_unable_to_add_win32perf"></span>**WBEM \_ MC \_ ADAP KANN \_ \_ \_ \_ WIN32PERF NICHT HINZUFÜGEN**
</dt> <dd> <dl> <dt>

3221225530 (0xC000003A)
</dt> <dt>



Windows Adap für die Verwaltungsinstrumentation konnte die Win32 \_ Perf-Basisklasse in %1:Result=%2 nicht erstellen.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERFRAWDATA"></span><span id="wbem_mc_adap_unable_to_add_win32perfrawdata"></span>**WBEM \_ MC \_ ADAP KANN \_ \_ \_ \_ WIN32PERFRAWDATA NICHT HINZUFÜGEN**
</dt> <dd> <dl> <dt>

3221225531 (0xC000003B)
</dt> <dt>



Windows Adap für die Verwaltungsinstrumentation konnte die Win32 \_ PerfRawData-Basisklasse %1 nicht erstellen.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_REPOSITORY_FAILED_TO_START"></span><span id="wbem_mc_repository_failed_to_start"></span>**FEHLER BEIM STARTEN DES WBEM \_ \_ MC-REPOSITORYS \_ \_ \_**
</dt> <dd> <dl> <dt>

3221231073 (0xC00015E1)
</dt> <dt>



Der Windows Management Instrumentation Service konnte die Repositorydateien nicht im Verzeichnis *%windir% \\ system32 \\ wbem \\ repository* laden. Dies kann durch eine Beschädigung der Repositorydateien, Sicherheitseinstellungen in diesem Verzeichnis, fehlenden Speicherplatz oder andere Probleme mit systembedingten Ressourcen wie unzureichendem Arbeitsspeicher verursacht werden. Wenn dieser Fehler bei jedem Neustart des Computers auftritt, muss der Administrator auf diesem Computer möglicherweise den WMI-Dienst beenden, die Sicherheitseinstellung für diesen Ordner und die Dateien unter diesem Ordner überprüfen und WMIDiag ausführen, um die Integrität Windows Verwaltungsinstrumentation zu überprüfen.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_denied"></span>**WBEM \_ MC \_ WBEM \_ ERFORDERT VERSCHLÜSSELUNG \_ \_ VERWEIGERT**
</dt> <dd> <dl> <dt>

3221231077 (0xC00015E5)
</dt> <dt>



Der Zugriff auf den %1-Namespace wurde verweigert, da der Namespace mit RequiresEncryption markiert ist, das Skript oder die Anwendung jedoch versucht hat, eine Verbindung mit diesem Namespace mit einer Authentifizierungsebene unterhalb von **Pkt \_ Privacy** herzustellen. Ändern Sie die Authentifizierungsebene in **Pkt \_ Privacy,** und führen Sie das Skript oder die Anwendung erneut aus.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_ASYNC_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_async_denied"></span>**WBEM \_ MC \_ WBEM \_ ERFORDERT ENCRYPTION \_ \_ ASYNC \_ DENIED**
</dt> <dd> <dl> <dt>

3221231078 (0xC00015E6)
</dt> <dt>



Windows Der Verwaltungsinstrumentationsdienst konnte keine Ergebnisse asynchron für den %1-Namespace übermitteln. Der Namespace ist mit RequiresEncryption markiert, winMgmt konnte jedoch keine sichere Verbindung mit dem Clientcomputer herstellen. Stellen Sie sicher, dass zwischen dem Client und den Servercomputern eine Vertrauensstellung besteht, damit der Client das Servercomputerkonto erkennt.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_HOST_KILLED"></span><span id="wbem_mc_wbem_host_killed"></span>**WBEM \_ MC \_ WBEM \_ HOST \_ KILLED**
</dt> <dd> <dl> <dt>

3221231084 (0xC00015EC)
</dt> <dt>



Windows Die Verwaltungsinstrumentation wurde WMIPRVSE.EXE beendet, da ein Kontingent einen Warnungswert erreicht hat. Kontingent: %1 Wert: %2 Maximalwert: %3 WMIPRVSE PID: %4.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REPFILESNOTFOUND"></span><span id="wbem_mc_wbem_repfilesnotfound"></span>**WBEM \_ MC \_ WBEM \_ REPFILESNOTFOUND**
</dt> <dd> <dl> <dt>

3221231086 (0xC00015EE)
</dt> <dt>



Während des Dienststarts konnte der Windows-Verwaltungsinstrumentationsdienst die Repositorydateien nicht finden. Basierend auf dem Mechanismus für die automatische Wiederherstellung wird ein neues Repository erstellt.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_STARTED_SUCESSFULLY"></span><span id="wbem_mc_wbem_started_sucessfully"></span>**WBEM \_ MC \_ WBEM \_ WURDE ERFOLGREICH GESTARTET \_**
</dt> <dd> <dl> <dt>

3221231087 (0xC00015EF)
</dt> <dt>



Windows Der Verwaltungsinstrumentationsdienst wurde erfolgreich gestartet.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_CORE_PSS_ESS_INITIALIZED"></span><span id="wbem_mc_wbem_core_pss_ess_initialized"></span>**WBEM \_ MC \_ WBEM \_ CORE \_ PSS \_ ESS \_ INITIALISIERT**
</dt> <dd> <dl> <dt>

3221231089 (0xC00015F1)
</dt> <dt>



Windows Subsysteme des Verwaltungsinstrumentationsdiensts wurden erfolgreich initialisiert.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_SERVICE_INIT_FAILURE"></span><span id="wbem_mc_wbem_service_init_failure"></span>**WBEM \_ MC \_ WBEM \_ SERVICE \_ INIT \_ FAILURE**
</dt> <dd> <dl> <dt>

3221225501 (0xC000001D)
</dt> <dt>



Fehlernummer %1 wurde beim Versuch zurückgegeben, Windows Management Instrumentation Service zu initialisieren. Dies kann auf eine schlecht installierte Version von WMI, einen Fehler beim WMI-Repositoryupgrade, unzureichenden Speicherplatz oder unzureichenden Arbeitsspeicher zurückzuführen sein.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REPOSITORY_RECREATED"></span><span id="wbem_mc_wbem_repository_recreated"></span>**WBEM \_ MC \_ WBEM-REPOSITORY \_ NEU \_ ERSTELLT**
</dt> <dd> <dl> <dt>

3221231088 (0xC00015F0)
</dt> <dt>



Windows Das Repository für die Verwaltungsinstrumentation wurde mithilfe des Autorecovery-Mechanismus erfolgreich neu erstellt.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WMI-Ereignisse](wmi-events.md)
</dt> <dt>

[Problembehandlung bei WMI](wmi-troubleshooting.md)
</dt> </dl>

 

 




