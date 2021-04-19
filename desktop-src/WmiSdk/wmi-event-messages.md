---
description: In der folgenden Liste sind Ereignisse aufgelistet, die von WMI-Protokollen in Windows Vista und neueren Betriebssystemen unterstützt werden.
ms.assetid: ad8891cc-0b76-404d-81fc-961bcdbfae32
ms.tgt_platform: multiple
title: WMI-Ereignismeldungen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 543e7131ac0c73a9f1e0f111dafe90197989a33d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348301"
---
# <a name="wmi-event-messages"></a>WMI-Ereignismeldungen

In der folgenden Liste sind Ereignisse aufgelistet, die von WMI-Protokollen in Windows Vista und neueren Betriebssystemen unterstützt werden.

> [!Note]  
> Die folgende Dokumentation ist für Entwickler und IT-Administratoren konzipiert. Wenn Sie versuchen, eine WMI-Fehlermeldung auf Ihrem Heimsystem aufzulösen, finden Sie weitere Informationen auf der [Microsoft-Support](https://support.microsoft.com/) -Website.

 

<dl> <dt>

<span id="WBEM_MC_REPOSITORY_INCONSISTENT"></span><span id="wbem_mc_repository_inconsistent"></span>**WBEM \_ MC- \_ Repository \_ inkonsistent**
</dt> <dd> <dl> <dt>

1073747424 (0x400015e0)
</dt> <dt>



Der Windows-Verwaltungsinstrumentation Dienst hat eine Inkonsistenz mit dem WMI-Repository im Verzeichnis *% windir% \\ system32 \\ WBEM \\ Repository* festgestellt und konnte es nicht wiederherstellen. Das WMI-Repository wird nun gelöscht. basierend auf dem Mechanismus für die automatische Wiederherstellung wird ein neues Repository erstellt.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_PROVIDER_SUBSYSTEM_LOCALSYSTEM_PROVIDER_LOAD"></span><span id="wbem_mc_provider_subsystem_localsystem_provider_load"></span>**Last des \_ \_ \_ \_ LocalSystem- \_ Anbieters \_ des WBEM MC-Anbieters**
</dt> <dd> <dl> <dt>

2147483711 (0x8000003f)
</dt> <dt>



Der Anbieter "%1" wurde im Windows-Verwaltungsinstrumentation Namespace "%2" registriert, um das Konto "LocalSystem" zu verwenden. Dieses Konto ist privilegiert, und der Anbieter kann zu einer Sicherheitsverletzung führen, wenn die Identität von Benutzer Anforderungen nicht ordnungsgemäß angenommen wird.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_MOF_NOT_LOADED_AT_RECOVERY"></span><span id="wbem_mc_mof_not_loaded_at_recovery"></span>**WBEM \_ MC \_ MOF \_ wurde \_ \_ bei der \_ Wiederherstellung nicht geladen.**
</dt> <dd> <dl> <dt>

3221225476 (0xc0000004)
</dt> <dt>



Fehler "%1" beim Versuch, MOF "%2" bei der Wiederherstellung zu laden. MOF-Datei, die mit AutoRecover gekennzeichnet ist.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_CANNOT_ACTIVATE_FILTER"></span><span id="wbem_mc_cannot_activate_filter"></span>**WBEM \_ MC \_ kann \_ Filter nicht aktivieren \_**
</dt> <dd> <dl> <dt>

3221225482 (0xc000000a)
</dt> <dt>



Der Ereignis Filter mit der Abfrage "%2" konnte aufgrund von Fehler "%3" im Namespace "%1" nicht erneut aktiviert werden. Ereignisse können erst über diesen Filter übermittelt werden, wenn das Problem behoben wurde.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_INVALID_EVENT_PROVIDER_QUERY"></span><span id="wbem_mc_invalid_event_provider_query"></span>**WBEM \_ MC- \_ Abfrage mit ungültigem \_ Ereignis \_ Anbieter \_**
</dt> <dd> <dl> <dt>

3221225493 (0xc0000015)
</dt> <dt>



Der Ereignis Anbieter %1 hat versucht, eine syntaktisch ungültige Abfrage "%2" zu registrieren. Die Abfrage wird ignoriert. Die Abfrage kann korrigiert werden, indem das WMI-Repository mit CIM Studio untersucht und die permanenten Abonnements für den aufgelisteten Anbieter und die Abfrage aktualisiert werden. Wenn das permanente Abonnement mit einer MOF-Datei erstellt wird, die mit einem installierten Produkt stammt, muss der Hersteller der Anwendung kontaktiert werden, um die fehlerhafte Registrierung zu korrigieren.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_INVALID_EVENT_PROVIDER_INTRINSIC_QUERY"></span><span id="wbem_mc_invalid_event_provider_intrinsic_query"></span>**systeminterne Abfrage für WBEM \_ MC- \_ \_ Ereignis \_ Anbieter \_ \_**
</dt> <dd> <dl> <dt>

3221225494 (0xc0000016)
</dt> <dt>



Der Ereignis Anbieter %1 hat versucht, eine intrinsische Ereignis Abfrage "%2" im Namespace "%3" zu registrieren, für den der Satz von Zielobjekt Klassen nicht bestimmt werden konnte. Die Abfrage wird ignoriert.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_TOO_BROAD"></span><span id="wbem_mc_event_provider_query_too_broad"></span>**WBEM \_ MC- \_ Ereignis \_ Anbieter \_ Abfrage \_ zu \_ breit**
</dt> <dd> <dl> <dt>

3221225495 (0xc0000017)
</dt> <dt>



Der Ereignis Anbieter %1 hat versucht, die Abfrage "%2" im Namespace "%3" zu registrieren, der zu breit ist. Ereignis Anbieter können keine Ereignisse bereitstellen, die vom System bereitgestellt werden. Die Abfrage wird ignoriert. Wenden Sie sich an den Anwendungshersteller.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_FOUND"></span><span id="wbem_mc_event_provider_query_not_found"></span>**die WBEM \_ MC- \_ Ereignis \_ Anbieter \_ Abfrage wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

3221225496 (0xc0000018)
</dt> <dt>



Der Ereignis Anbieter %1 hat versucht, die Abfrage "%2" zu registrieren, deren Zielklasse "%3" im %4-Namespace nicht vorhanden ist. Die Abfrage wird ignoriert.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_EVENT"></span><span id="wbem_mc_event_provider_query_not_event"></span>**WBEM \_ MC- \_ Ereignis \_ Anbieter \_ Abfrage \_ nicht \_ Ereignis**
</dt> <dd> <dl> <dt>

3221225497 (0xc0000019)
</dt> <dt>



Der Ereignis Anbieter %1 hat versucht, die Abfrage %2 zu registrieren, &quot; &quot; deren Zielklasse &quot; %3 &quot; keine Ereignisklasse ist. Die Abfrage wird ignoriert. Wenden Sie sich an den Anwendungshersteller.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_CORE_FAILURE"></span><span id="wbem_mc_wbem_core_failure"></span>**WBEM \_ MC \_ WBEM \_ Core- \_ Fehler**
</dt> <dd> <dl> <dt>

3221225500 (0xc000001c)
</dt> <dt>



Fehler beim Initialisieren des WMI-Core-oder Anbieter Subsystems oder des-Ereignis Subsystems mit der Fehlernummer %1. Dies kann auf eine fehlerhafte Version von WMI, eine fehlerhafte WMI-Repository-Aktualisierung, unzureichenden Speicherplatz oder unzureichenden Arbeitsspeicher zurückzuführen sein.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_CONNECTION_FAILURE"></span><span id="wbem_mc_adap_connection_failure"></span>**Fehler beim \_ \_ ADAP- \_ Verbindungs \_ Fehler in WBEM MC.**
</dt> <dd> <dl> <dt>

3221225515 (0xc000002b)
</dt> <dt>



Fehler beim Herstellen einer Verbindung mit dem Namespace "%1" Windows-Verwaltungsinstrumentation ADAP mit dem folgenden Fehler: %2.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_PERFLIB_PUTCLASS_FAILURE"></span><span id="wbem_mc_adap_perflib_putclass_failure"></span>**WBEM \_ MC \_ ADAP \_ Perflib \_ putclass- \_ Fehler**
</dt> <dd> <dl> <dt>

3221225520 (0xc0000030)
</dt> <dt>



Windows-Verwaltungsinstrumentation ADAP konnte das Objekt "%1" im Namespace "%2" aufgrund des folgenden Fehlers nicht speichern: %3.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERF"></span><span id="wbem_mc_adap_unable_to_add_win32perf"></span>**WBEM \_ MC \_ ADAP \_ kann \_ \_ WIN32PERF nicht hinzufügen \_**
</dt> <dd> <dl> <dt>

3221225530 (0xc000003a)
</dt> <dt>



Windows-Verwaltungsinstrumentation ADAP konnte die Win32 \_ perf-Basisklasse in "%1" nicht erstellen: Ergebnis = %2.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERFRAWDATA"></span><span id="wbem_mc_adap_unable_to_add_win32perfrawdata"></span>**WBEM \_ MC \_ ADAP \_ kann \_ \_ WIN32PERFRAWDATA nicht hinzufügen \_**
</dt> <dd> <dl> <dt>

3221225531 (0xc000003b)
</dt> <dt>



Windows-Verwaltungsinstrumentation ADAP konnte die Win32 \_ perfrawdata-Basisklasse "%1" nicht erstellen.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_REPOSITORY_FAILED_TO_START"></span><span id="wbem_mc_repository_failed_to_start"></span>**WBEM \_ MC \_ - \_ Repository \_ konnte nicht \_ gestartet werden**
</dt> <dd> <dl> <dt>

3221231073 (0xc00015e1)
</dt> <dt>



Der Windows-Verwaltungsinstrumentation-Dienst konnte die Repository-Dateien nicht in das Verzeichnis *% windir% \\ system32 \\ WBEM \\ Repository* laden. Dies kann durch eine Beschädigung der Repository-Dateien, Sicherheitseinstellungen für dieses Verzeichnis, unzureichenden Speicherplatz oder andere Systemressourcen Probleme, wie z. b. unzureichenden Arbeitsspeicher, verursacht werden. Tritt dieser Fehler immer dann auf, wenn der Computer neu gestartet wird, muss der Administrator auf diesem Computer ggf. den WMI-Dienst unterbinden, die Sicherheitseinstellungen für diesen Ordner und die Dateien in diesem Ordner überprüfen und WMIDiag ausführen, um den Zustand der Windows-Verwaltungsinstrumentation zu überprüfen.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_denied"></span>**WBEM \_ MC \_ WBEM \_ erfordert \_ Verschlüsselung \_ verweigert**
</dt> <dd> <dl> <dt>

3221231077 (0xc00015e5)
</dt> <dt>



Der Zugriff auf den %1-Namespace wurde verweigert, da der Namespace mit "Requirements" gekennzeichnet ist, das Skript oder die Anwendung jedoch versucht hat, eine Verbindung mit diesem Namespace mit einer Authentifizierungs Ebene unterhalb des **Pkt- \_ Datenschutzes** herzustellen. Ändern Sie die Authentifizierungs Ebene in **Pkt \_ Privacy** , und führen Sie das Skript oder die Anwendung erneut aus.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_ASYNC_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_async_denied"></span>**WBEM \_ MC \_ WBEM \_ erfordert \_ Verschlüsselung \_ Async \_ verweigert**
</dt> <dd> <dl> <dt>

3221231078 (0xc00015e6)
</dt> <dt>



Windows-Verwaltungsinstrumentation Dienst konnte die Ergebnisse für den %1-Namespace nicht asynchron bereitzustellen. Der Namespace ist mit "Requirements sencryption" gekennzeichnet, aber WinMgmt konnte keine sichere Verbindung mit dem Client Computer herstellen. Stellen Sie sicher, dass zwischen den Client-und Server Computern eine Vertrauensstellung besteht, sodass der Client das Server Computer Konto erkennt.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_HOST_KILLED"></span><span id="wbem_mc_wbem_host_killed"></span>**WBEM \_ MC \_ WBEM- \_ Host \_ wurde abgebrochen.**
</dt> <dd> <dl> <dt>

3221231084 (0xc00015ec)
</dt> <dt>



Windows-Verwaltungsinstrumentation wurde WMIPRVSE.EXE beendet, weil ein Kontingent einen Warnungs Wert erreicht hat. Kontingent: %1, Wert: %2, Maximalwert: %3, wmiprvse-PID: %4.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REPFILESNOTFOUND"></span><span id="wbem_mc_wbem_repfilesnotfound"></span>**WBEM \_ MC \_ WBEM \_ repfilesnotfound**
</dt> <dd> <dl> <dt>

3221231086 (0xc00015ee)
</dt> <dt>



Während des Dienst Starts konnte der Windows-Verwaltungsinstrumentation-Dienst die Repository-Dateien nicht finden. Basierend auf dem Mechanismus für die automatische Wiederherstellung wird ein neues Repository erstellt.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_STARTED_SUCESSFULLY"></span><span id="wbem_mc_wbem_started_sucessfully"></span>**WBEM \_ MC \_ WBEM wurde erfolgreich \_ gestartet \_ .**
</dt> <dd> <dl> <dt>

3221231087 (0xc00015ef)
</dt> <dt>



Windows-Verwaltungsinstrumentation Dienst wurde erfolgreich gestartet.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_CORE_PSS_ESS_INITIALIZED"></span><span id="wbem_mc_wbem_core_pss_ess_initialized"></span>**WBEM \_ MC \_ WBEM \_ Core \_ PSS \_ ESS \_ Initialisiert**
</dt> <dd> <dl> <dt>

3221231089 (0xc00015, f 1)
</dt> <dt>



Windows-Verwaltungsinstrumentation Dienst Subsysteme wurden erfolgreich initialisiert.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_SERVICE_INIT_FAILURE"></span><span id="wbem_mc_wbem_service_init_failure"></span>**Fehler beim Initialisierungs Dienst von WBEM \_ MC \_ WBEM. \_ \_ \_**
</dt> <dd> <dl> <dt>

3221225501 (0xc000001d)
</dt> <dt>



Fehlernummer %1 wurde bei dem Versuch zurückgegeben, Windows-Verwaltungsinstrumentation Dienst zu initialisieren. Dies kann auf eine fehlerhafte Version von WMI, eine fehlerhafte WMI-Repository-Aktualisierung, unzureichenden Speicherplatz oder unzureichenden Arbeitsspeicher zurückzuführen sein.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REPOSITORY_RECREATED"></span><span id="wbem_mc_wbem_repository_recreated"></span>**WBEM \_ MC \_ WBEM- \_ Repository \_ neu erstellt**
</dt> <dd> <dl> <dt>

3221231088 (0xc00015, f 0)
</dt> <dt>



Windows-Verwaltungsinstrumentation Repository wurde mit dem AutoRecovery-Mechanismus erfolgreich neu erstellt.


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

[WMI-Problembehandlung](wmi-troubleshooting.md)
</dt> </dl>

 

 




