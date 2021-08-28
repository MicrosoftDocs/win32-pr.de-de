---
Description: Berechtigungen bestimmen den Typ der Systemvorgänge, die ein Benutzerkonto ausführen kann. Ein Administrator weist Benutzer- und Gruppenkonten Berechtigungen zu. Zu den Einzelnen Benutzerberechtigungen gehören die Berechtigungen, die dem Benutzer und den Gruppen gewährt werden, denen der Benutzer angehört.
ms.assetid: 973796a6-bc2e-4e64-92db-5e17b9c25460
title: Berechtigungskonstanten (Winnt.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 5da0a0e6f9ad3b0559fdf2d8e375e6d25e7d2fdf
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475742"
---
# <a name="privilege-constants-authorization"></a>Berechtigungskonstanten (Autorisierung)

Berechtigungen bestimmen den Typ der Systemvorgänge, die ein Benutzerkonto ausführen kann. Ein Administrator weist Benutzer- und Gruppenkonten Berechtigungen zu. Zu den Berechtigungen jedes Benutzers gehören die Berechtigungen, die dem Benutzer und den Gruppen gewährt werden, denen der Benutzer angehört.

Die Funktionen, die die Berechtigungen in einem [*Zugriffstoken*](/windows/desktop/SecGloss/a-gly) abrufen und anpassen, verwenden den Lokal [*eindeutigen Bezeichnertyp*](/windows/desktop/SecGloss/l-gly) (LUID), um Berechtigungen zu identifizieren. Verwenden Sie die [**LookupPrivilegeValue-Funktion,**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) um die [**LUID**](/windows/desktop/api/Winnt/ns-winnt-luid) auf dem lokalen System zu bestimmen, die einer Berechtigungskonstante entspricht. Verwenden Sie die [**LookupPrivilegeName-Funktion,**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) um eine **LUID** in die entsprechende Zeichenfolgenkonstante zu konvertieren.

Das Betriebssystem stellt eine Berechtigung dar, indem die Zeichenfolge verwendet wird, die in der Spalte Beschreibung der folgenden Tabelle auf "Benutzerrecht" folgt. Das Betriebssystem zeigt die Zeichenfolgen der Benutzerrechte in der Spalte **Richtlinie** des Knotens Zuweisen von **Benutzerrechten** des MMC-Snap-Ins (Local Security Einstellungen Microsoft Management Console) an.

## <a name="example"></a>Beispiel

```cpp
BOOL EnablePrivilege()
{
    LUID PrivilegeRequired ;
    BOOL bRes = FALSE;
  
    bRes = LookupPrivilegeValue(NULL, SE_DEBUG_NAME, &PrivilegeRequired);

    // ...

    return bRes;
}
```
Beispiel aus [Windows klassischen Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/ManagementInfrastructure/cpp/Process/Provider/WindowsProcess.c) auf GitHub.

## <a name="constants"></a>Konstanten



| Konstante/Wert | BESCHREIBUNG | 
|----------------|-------------|
| <span id="SE_ASSIGNPRIMARYTOKEN_NAME"></span><span id="se_assignprimarytoken_name"></span><dl><dt><strong>SE_ASSIGNPRIMARYTOKEN_NAME</strong></dt><dt>TEXT("SeAssignPrimaryTokenPrivilege")</dt></dl> | Erforderlich, um das <a href="/windows/desktop/SecGloss/p-gly"><em>primäre Token</em></a> eines Prozesses zuzuweisen. <br /> Benutzerrecht: Ersetzen Sie ein Token auf Prozessebene.<br /> | 
| <span id="SE_AUDIT_NAME"></span><span id="se_audit_name"></span><dl><dt><strong>SE_AUDIT_NAME</strong></dt><dt>TEXT("SeAuditPrivilege")</dt></dl> | Erforderlich, um Überwachungsprotokolleinträge zu generieren. Erteilen Sie diese Berechtigung für sichere Server. <br /> Benutzerrecht: Generieren sie Sicherheitsüberwachungen.<br /> | 
| <span id="SE_BACKUP_NAME"></span><span id="se_backup_name"></span><dl><dt><strong>SE_BACKUP_NAME</strong></dt><dt>TEXT("SeBackupPrivilege")</dt></dl> | Erforderlich zum Ausführen von Sicherungsvorgängen. Diese Berechtigung bewirkt, dass das System jeder Datei alle Lesezugriffssteuerung gewährt, unabhängig von der für die Datei angegebenen <a href="/windows/desktop/SecGloss/a-gly"><em>Zugriffssteuerungsliste (Access Control List,</em></a> ACL). Jede andere Zugriffsanforderung als read wird weiterhin mit der Zugriffssteuerungsliste ausgewertet. Diese Berechtigung ist für die <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya"><strong>Funktionen RegSaveKey</strong></a> und <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeyexa"><strong>RegSaveKeyEx</strong></a>erforderlich. Die folgenden Zugriffsrechte werden gewährt, wenn diese Berechtigung besteht:<br /><ul><li>READ_CONTROL</li><li>ACCESS_SYSTEM_SECURITY</li><li>FILE_GENERIC_READ</li><li>FILE_TRAVERSE</li></ul>Benutzerrecht: Sichern Sie Dateien und Verzeichnisse.<br />Wenn sich die Datei auf einem Wechseldatenträger befindet und die Option "Wechselbares Storage überwachen" aktiviert ist, muss die SE_SECURITY_NAME über ACCESS_SYSTEM_SECURITY verfügen. | 
| <span id="SE_CHANGE_NOTIFY_NAME"></span><span id="se_change_notify_name"></span><dl><dt><strong>SE_CHANGE_NOTIFY_NAME</strong></dt><dt>TEXT("SeChangeNotifyPrivilege")</dt></dl> | Erforderlich, um Benachrichtigungen über Änderungen an Dateien oder Verzeichnissen zu erhalten. Diese Berechtigung bewirkt auch, dass das System alle Überprüfungen des Durchlaufzugriffs überspringt. Sie ist standardmäßig für alle Benutzer aktiviert. <br /> Benutzerrecht: Umgehen Sie die Traversierungsüberprüfung.<br /> | 
| <span id="SE_CREATE_GLOBAL_NAME"></span><span id="se_create_global_name"></span><dl><dt><strong>SE_CREATE_GLOBAL_NAME</strong></dt><dt>TEXT("SeCreateGlobalPrivilege")</dt></dl> | Erforderlich, um benannte Dateizuordnungsobjekte im globalen Namespace während Terminaldienstesitzungen zu erstellen. Diese Berechtigung ist standardmäßig für Administratoren, Dienste und das lokale Systemkonto aktiviert.<br /> Benutzerrecht: Erstellen sie globale Objekte.<br /> | 
| <span id="SE_CREATE_PAGEFILE_NAME"></span><span id="se_create_pagefile_name"></span><dl><dt><strong>SE_CREATE_PAGEFILE_NAME</strong></dt><dt>TEXT("SeCreatePagefilePrivilege")</dt></dl> | Erforderlich, um eine Auslagerungsdatei zu erstellen. <br /> Benutzerrecht: Erstellen Sie eine Auslagerungsdatei.<br /> | 
| <span id="SE_CREATE_PERMANENT_NAME"></span><span id="se_create_permanent_name"></span><dl><dt><strong>SE_CREATE_PERMANENT_NAME</strong></dt><dt>TEXT("SeCreatePermanentPrivilege")</dt></dl> | Erforderlich, um ein permanentes -Objekt zu erstellen. <br /> Benutzerrecht: Erstellen Sie permanente freigegebene Objekte.<br /> | 
| <span id="SE_CREATE_SYMBOLIC_LINK_NAME"></span><span id="se_create_symbolic_link_name"></span><dl><dt><strong>SE_CREATE_SYMBOLIC_LINK_NAME</strong></dt><dt>TEXT("SeCreateSymbolicLinkPrivilege")</dt></dl> | Erforderlich, um eine symbolische Verknüpfung zu erstellen.<br /> Benutzerrecht: Erstellen Sie symbolische Verknüpfungen.<br /> | 
| <span id="SE_CREATE_TOKEN_NAME"></span><span id="se_create_token_name"></span><dl><dt><strong>SE_CREATE_TOKEN_NAME</strong></dt><dt>TEXT("SeCreateTokenPrivilege")</dt></dl> | Erforderlich, um ein primäres Token zu erstellen. <br /> Benutzerrecht: Erstellen Sie ein Tokenobjekt.<br /> Sie können diese Berechtigung nicht einem Benutzerkonto mit der Richtlinie "Tokenobjekt erstellen" hinzufügen. Darüber hinaus können Sie diese Berechtigung nicht mithilfe von Windows-APIs einem eigenen Prozess hinzufügen. <strong>Windows Server 2003 und Windows XP mit SP1 und früher:</strong> Windows-APIs können diese Berechtigung einem eigenen Prozess hinzufügen.<br /><br /> | 
| <span id="SE_DEBUG_NAME"></span><span id="se_debug_name"></span><dl><dt><strong>SE_DEBUG_NAME</strong></dt><dt>TEXT("SeDebugPrivilege")</dt></dl> | Erforderlich zum Debuggen und Anpassen des Arbeitsspeichers eines Prozesses, der sich im Besitz eines anderen Kontos befindet. <br /> Benutzerrecht: Debugprogramme.<br /> | 
| <span id="SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME"></span><span id="se_delegate_session_user_impersonate_name"></span><dl><dt><strong>SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME</strong></dt><dt>TEXT("SeDelegateSessionUserImpersonatePrivilege")</dt></dl> | Erforderlich, um ein Identitätswechseltoken für einen anderen Benutzer in derselben Sitzung abzurufen. <br /> Benutzerrecht: Identität anderer Benutzer annehmen.<br /> | 
| <span id="SE_ENABLE_DELEGATION_NAME"></span><span id="se_enable_delegation_name"></span><dl><dt><strong>SE_ENABLE_DELEGATION_NAME</strong></dt><dt>TEXT("SeEnableDelegationPrivilege")</dt></dl> | Erforderlich, um Benutzer- und Computerkonten als vertrauenswürdig für die Delegierung zu kennzeichnen.<br /> Benutzerrecht: Aktivieren Sie Computer- und Benutzerkonten, damit sie für die Delegierung als vertrauenswürdig eingestuft werden.<br /> | 
| <span id="SE_IMPERSONATE_NAME"></span><span id="se_impersonate_name"></span><dl><dt><strong>SE_IMPERSONATE_NAME</strong></dt><dt>TEXT("SeImpersonatePrivilege")</dt></dl> | Erforderlich, um die Identität zu annehmen.<br /> Benutzerrecht: Annehmen der Identität eines Clients nach der Authentifizierung.<br /> | 
| <span id="SE_INC_BASE_PRIORITY_NAME"></span><span id="se_inc_base_priority_name"></span><dl><dt><strong>SE_INC_BASE_PRIORITY_NAME</strong></dt><dt>TEXT("SeIncreaseBasePriorityPrivilege")</dt></dl> | Erforderlich, um die Basispriorität eines Prozesses zu erhöhen. <br /> Benutzerrecht: Erhöhen Sie die Planungspriorität.<br /> | 
| <span id="SE_INCREASE_QUOTA_NAME"></span><span id="se_increase_quota_name"></span><dl><dt><strong>SE_INCREASE_QUOTA_NAME</strong></dt><dt>TEXT("SeIncreaseQuotaPrivilege")</dt></dl> | Erforderlich, um das einem Prozess zugewiesene Kontingent zu erhöhen. <br /> Benutzerrecht: Passen Sie Speicherkontingente für einen Prozess an.<br /> | 
| <span id="SE_INC_WORKING_SET_NAME"></span><span id="se_inc_working_set_name"></span><dl><dt><strong>SE_INC_WORKING_SET_NAME</strong></dt><dt>TEXT("SeIncreaseWorkingSetPrivilege")</dt></dl> | Erforderlich, um mehr Arbeitsspeicher für Anwendungen zuzuweisen, die im Kontext von Benutzern ausgeführt werden.<br /> Benutzerrecht: Erhöhen Sie ein Prozessarbeitssatz.<br /> | 
| <span id="SE_LOAD_DRIVER_NAME"></span><span id="se_load_driver_name"></span><dl><dt><strong>SE_LOAD_DRIVER_NAME</strong></dt><dt>TEXT("SeLoadDriverPrivilege")</dt></dl> | Erforderlich zum Laden oder Entladen eines Gerätetreibers. <br /> Benutzerrecht: Laden und Entladen von Gerätetreibern.<br /> | 
| <span id="SE_LOCK_MEMORY_NAME"></span><span id="se_lock_memory_name"></span><dl><dt><strong>SE_LOCK_MEMORY_NAME</strong></dt><dt>TEXT("SeLockMemoryPrivilege")</dt></dl> | Erforderlich, um physische Seiten im Arbeitsspeicher zu sperren. <br /> Benutzerrecht: Sperren von Seiten im Arbeitsspeicher.<br /> | 
| <span id="SE_MACHINE_ACCOUNT_NAME"></span><span id="se_machine_account_name"></span><dl><dt><strong>SE_MACHINE_ACCOUNT_NAME</strong></dt><dt>TEXT("SeMachineAccountPrivilege")</dt></dl> | Erforderlich, um ein Computerkonto zu erstellen. <br /> Benutzerrecht: Fügen Sie Arbeitsstationen zur Domäne hinzu.<br /> | 
| <span id="SE_MANAGE_VOLUME_NAME"></span><span id="se_manage_volume_name"></span><dl><dt><strong>SE_MANAGE_VOLUME_NAME</strong></dt><dt>TEXT("SeManageVolumePrivilege")</dt></dl> | Erforderlich, um Volumeverwaltungsberechtigungen zu aktivieren. <br /> Benutzerrecht: Verwalten Sie die Dateien auf einem Volume.<br /> | 
| <span id="SE_PROF_SINGLE_PROCESS_NAME"></span><span id="se_prof_single_process_name"></span><dl><dt><strong>SE_PROF_SINGLE_PROCESS_NAME</strong></dt><dt>TEXT("SeProfileSingleProcessPrivilege")</dt></dl> | Erforderlich, um Profilerstellungsinformationen für einen einzelnen Prozess zu sammeln. <br /> Benutzerrecht: Profil für einen einzelnen Prozess.<br /> | 
| <span id="SE_RELABEL_NAME"></span><span id="se_relabel_name"></span><dl><dt><strong>SE_RELABEL_NAME</strong></dt><dt>TEXT("SeRelabelPrivilege")</dt></dl> | Erforderlich, um die erforderliche Integritätsebene eines Objekts zu ändern.<br /> Benutzerrecht: Ändern sie eine Objektbezeichnung.<br /> | 
| <span id="SE_REMOTE_SHUTDOWN_NAME"></span><span id="se_remote_shutdown_name"></span><dl><dt><strong>SE_REMOTE_SHUTDOWN_NAME</strong></dt><dt>TEXT("SeRemoteShutdownPrivilege")</dt></dl> | Erforderlich, um ein System mithilfe einer Netzwerkanforderung herunterzufahren. <br /> Benutzerrecht: Erzwingen des Herunterfahrens von einem Remotesystem.<br /> | 
| <span id="SE_RESTORE_NAME"></span><span id="se_restore_name"></span><dl><dt><strong>SE_RESTORE_NAME</strong></dt><dt>TEXT("SeRestorePrivilege")</dt></dl> | Erforderlich zum Ausführen von Wiederherstellungsvorgängen. Diese Berechtigung bewirkt, dass das System jede Schreibzugriffssteuerung für jede Datei gewährt, unabhängig von der für die Datei angegebenen Zugriffssteuerungsliste. Jede andere Zugriffsanforderung als "write" wird weiterhin mit der Zugriffssteuerungsliste ausgewertet. Darüber hinaus können Sie mit dieser Berechtigung alle gültigen Benutzer- oder Gruppen-SID als Besitzer einer Datei festlegen. Diese Berechtigung ist für die <a href="/windows/desktop/api/winreg/nf-winreg-regloadkeya"><strong>RegLoadKey-Funktion</strong></a> erforderlich. Die folgenden Zugriffsrechte werden gewährt, wenn diese Berechtigung gewährt wird:<br /><ul><li>WRITE_DAC</li><li>WRITE_OWNER</li><li>ACCESS_SYSTEM_SECURITY</li><li>FILE_GENERIC_WRITE</li><li>FILE_ADD_FILE</li><li>FILE_ADD_SUBDIRECTORY</li><li>Delete</li></ul>Benutzerrecht: Wiederherstellen von Dateien und Verzeichnissen.<br />Wenn sich die Datei auf einem Wechseldatenträger befindet und die Option "Wechselbares Storage überwachen" aktiviert ist, muss die SE_SECURITY_NAME über ACCESS_SYSTEM_SECURITY verfügen.<br /> | 
| <span id="SE_SECURITY_NAME"></span><span id="se_security_name"></span><dl><dt><strong>SE_SECURITY_NAME</strong></dt><dt>TEXT("SeSecurityPrivilege")</dt></dl> | Erforderlich, um eine Reihe von sicherheitsbezogenen Funktionen auszuführen, z. B. das Steuern und Anzeigen von Überwachungsmeldungen. Diese Berechtigung identifiziert seinen Besitzer als Sicherheitsoperator. <br /> Benutzerrecht: Verwalten sie die Überwachung und das Sicherheitsprotokoll.<br /> | 
| <span id="SE_SHUTDOWN_NAME"></span><span id="se_shutdown_name"></span><dl><dt><strong>SE_SHUTDOWN_NAME</strong></dt><dt>TEXT("SeShutdownPrivilege")</dt></dl> | Erforderlich, um ein lokales System herunterzufahren. <br /> Benutzerrecht: Fahren Sie das System herunter.<br /> | 
| <span id="SE_SYNC_AGENT_NAME"></span><span id="se_sync_agent_name"></span><dl><dt><strong>SE_SYNC_AGENT_NAME</strong></dt><dt>TEXT("SeSyncAgentPrivilege")</dt></dl> | Erforderlich, damit ein Domänencontroller die Verzeichnissynchronisierungsdienste des <a href="/windows/desktop/SecGloss/l-gly"><em>Lightweight-Verzeichniszugriffsprotokolls</em></a> verwenden kann. Mit dieser Berechtigung kann der Besitzer alle Objekte und Eigenschaften im Verzeichnis lesen, unabhängig vom Schutz der Objekte und Eigenschaften. Standardmäßig wird sie den Administrator- und LocalSystem-Konten auf Domänencontrollern zugewiesen. <br /> Benutzerrecht: Synchronisieren von Verzeichnisdienstdaten.<br /> | 
| <span id="SE_SYSTEM_ENVIRONMENT_NAME"></span><span id="se_system_environment_name"></span><dl><dt><strong>SE_SYSTEM_ENVIRONMENT_NAME</strong></dt><dt>TEXT("SeSystemEnvironmentPrivilege")</dt></dl> | Erforderlich, um den nicht flüchtigen RAM von Systemen zu ändern, die diesen Speichertyp zum Speichern von Konfigurationsinformationen verwenden. <br /> Benutzerrecht: Ändern Sie die Werte der Firmwareumgebung.<br /> | 
| <span id="SE_SYSTEM_PROFILE_NAME"></span><span id="se_system_profile_name"></span><dl><dt><strong>SE_SYSTEM_PROFILE_NAME</strong></dt><dt>TEXT("SeSystemProfilePrivilege")</dt></dl> | Erforderlich, um Profilerstellungsinformationen für das gesamte System zu sammeln. <br /> Benutzerrecht: Profilsystemleistung.<br /> | 
| <span id="SE_SYSTEMTIME_NAME"></span><span id="se_systemtime_name"></span><dl><dt><strong>SE_SYSTEMTIME_NAME</strong></dt><dt>TEXT("SeSystemtimePrivilege")</dt></dl> | Erforderlich, um die Systemzeit zu ändern. <br /> Benutzerrecht: Ändern Sie die Systemzeit.<br /> | 
| <span id="SE_TAKE_OWNERSHIP_NAME"></span><span id="se_take_ownership_name"></span><dl><dt><strong>SE_TAKE_OWNERSHIP_NAME</strong></dt><dt>TEXT("SeTakeOwnershipPrivilege")</dt></dl> | Erforderlich, um den Besitz eines Objekts zu übernehmen, ohne dass ein diskreter Zugriff gewährt wird. Mit dieser Berechtigung kann der Besitzerwert nur auf die Werte festgelegt werden, die der Besitzer berechtigterweise als Besitzer eines Objekts zuweisen kann. <br /> Benutzerrecht: Übernehmen Sie den Besitz von Dateien oder anderen Objekten.<br /> | 
| <span id="SE_TCB_NAME"></span><span id="se_tcb_name"></span><dl><dt><strong>SE_TCB_NAME</strong></dt><dt>TEXT("SeTcbPrivilege")</dt></dl> | Mit dieser Berechtigung wird der Besitzer als Teil der vertrauenswürdigen Computerbasis identifiziert. Einigen vertrauenswürdigen geschützten Subsystemen wird diese Berechtigung gewährt. <br /> Benutzerrecht: Fungiert als Teil des Betriebssystems.<br /> | 
| <span id="SE_TIME_ZONE_NAME"></span><span id="se_time_zone_name"></span><dl><dt><strong>SE_TIME_ZONE_NAME</strong></dt><dt>TEXT("SeTimeZonePrivilege")</dt></dl> | Erforderlich, um die Zeitzone anzupassen, die der internen Uhr des Computers zugeordnet ist.<br /> Benutzerrecht: Ändern Sie die Zeitzone.<br /> | 
| <span id="SE_TRUSTED_CREDMAN_ACCESS_NAME"></span><span id="se_trusted_credman_access_name"></span><dl><dt><strong>SE_TRUSTED_CREDMAN_ACCESS_NAME</strong></dt><dt>TEXT("SeTrustedCredManAccessPrivilege")</dt></dl> | Erforderlich, um als vertrauenswürdiger Aufrufer auf Anmeldeinformationsverwaltung zuzugreifen.<br /> Benutzerrecht: Zugriff Anmeldeinformationsverwaltung als vertrauenswürdiger Aufrufer.<br /> | 
| <span id="SE_UNDOCK_NAME"></span><span id="se_undock_name"></span><dl><dt><strong>SE_UNDOCK_NAME</strong></dt><dt>TEXT("SeUndockPrivilege")</dt></dl> | Erforderlich, um einen Laptop abzudocken.<br /> Benutzerrecht: Entfernen Sie den Computer aus der Dockingstation.<br /> | 
| <span id="SE_UNSOLICITED_INPUT_NAME"></span><span id="se_unsolicited_input_name"></span><dl><dt><strong>SE_UNSOLICITED_INPUT_NAME</strong></dt><dt>TEXT("SeUnsoli citInputPrivilege")</dt></dl> | Erforderlich, um nicht angeforderte Eingaben von einem <a href="/windows/desktop/SecGloss/t-gly"><em>Terminalgerät</em></a> zu lesen.<br /> Benutzerrecht: Nicht zutreffend.<br /> | 




## <a name="remarks"></a>Hinweise

Berechtigungskonstanten werden in Winnt.h als Zeichenfolgen definiert. Beispielsweise wird die SE \_ AUDIT \_ NAME-Konstante als "SeAuditPrivilege" definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Winnt.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Berechtigungen](privileges.md)
</dt> </dl>

