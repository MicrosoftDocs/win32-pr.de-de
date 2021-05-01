---
Description: Berechtigungen bestimmen den Typ der Systemvorgänge, die ein Benutzerkonto ausführen kann. Ein Administrator weist Benutzer- und Gruppenkonten Berechtigungen zu. Zu den Einzelnen Benutzerberechtigungen gehören die Berechtigungen, die dem Benutzer und den Gruppen gewährt werden, denen der Benutzer angehört.
ms.assetid: 973796a6-bc2e-4e64-92db-5e17b9c25460
title: Berechtigungskonstanten (Winnt.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: cd33cf947f6425d717b4d41524fe7cf0fed14cef
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327155"
---
# <a name="privilege-constants-authorization"></a>Berechtigungskonstanten (Autorisierung)

Berechtigungen bestimmen den Typ der Systemvorgänge, die ein Benutzerkonto ausführen kann. Ein Administrator weist Benutzer- und Gruppenkonten Berechtigungen zu. Zu den Berechtigungen jedes Benutzers gehören die berechtigungen, die dem Benutzer und den Gruppen gewährt werden, denen der Benutzer angehört.

Die Funktionen, die die Berechtigungen in einem [*Zugriffstoken*](/windows/desktop/SecGloss/a-gly) abrufen und anpassen, verwenden den Lokal [*eindeutigen Bezeichnertyp*](/windows/desktop/SecGloss/l-gly) (LUID), um Berechtigungen zu identifizieren. Verwenden Sie die [**LookupPrivilegeValue-Funktion,**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) um die [**LUID**](/windows/desktop/api/Winnt/ns-winnt-luid) auf dem lokalen System zu bestimmen, die einer Berechtigungskonstante entspricht. Verwenden Sie die [**LookupPrivilegeName-Funktion,**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) um eine **LUID** in die entsprechende Zeichenfolgenkonstante zu konvertieren.

Das Betriebssystem stellt eine Berechtigung dar, indem die Zeichenfolge verwendet wird, die in der Spalte Beschreibung der folgenden Tabelle auf "Benutzerrecht" folgt. Das Betriebssystem zeigt die Zeichenfolgen der Benutzerrechte in der Spalte **Richtlinie** des Knotens Zuweisen von **Benutzerrechten** des MMC-Snap-Ins (Local Security Settings Microsoft Management Console) an.

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
Beispiel aus [klassischen Windows-Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/ManagementInfrastructure/cpp/Process/Provider/WindowsProcess.c) auf GitHub.

## <a name="constants"></a>Konstanten


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstante/Wert</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="SE_ASSIGNPRIMARYTOKEN_NAME"></span><span id="se_assignprimarytoken_name"></span><dl> <dt><strong>SE_ASSIGNPRIMARYTOKEN_NAME</strong></dt> <dt>TEXT( &quot; SeAssignPrimaryTokenPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um das <a href="/windows/desktop/SecGloss/p-gly"><em>primäre Token</em></a> eines Prozesses zuzuweisen. <br/> Benutzerrecht: Ersetzen Sie ein Token auf Prozessebene.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_AUDIT_NAME"></span><span id="se_audit_name"></span><dl> <dt><strong>SE_AUDIT_NAME</strong></dt> <dt>TEXT( &quot; SeAuditPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um Überwachungsprotokolleinträge zu generieren. Erteilen Sie diese Berechtigung für sichere Server. <br/> Benutzerrecht: Generiert Sicherheitsüberprüfungen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_BACKUP_NAME"></span><span id="se_backup_name"></span><dl> <dt><strong>SE_BACKUP_NAME</strong></dt> <dt>TEXT( &quot; SeBackupPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um Sicherungsvorgänge durchzuführen. Diese Berechtigung bewirkt, dass das System allen Dateien lesezugriffssteuerung gewährt, unabhängig von der für die Datei angegebenen Zugriffssteuerungsliste (Access <a href="/windows/desktop/SecGloss/a-gly"><em>Control List,</em></a> ACL). Jede andere Zugriffsanforderung als "Read" wird weiterhin mit der ACL ausgewertet. Diese Berechtigung ist für die <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya"><strong>Funktionen RegSaveKey</strong></a> und <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeyexa"><strong>RegSaveKeyEx</strong></a>erforderlich. Die folgenden Zugriffsrechte werden gewährt, wenn diese Berechtigung erteilt wird:<br/>
<ul>
<li>READ_CONTROL</li>
<li>ACCESS_SYSTEM_SECURITY</li>
<li>FILE_GENERIC_READ</li>
<li>FILE_TRAVERSE</li>
</ul>
Benutzerrecht: Sichern Sie Dateien und Verzeichnisse.<br/>Wenn sich die Datei auf einem Wechseldatenträger befindet und "Wechseldatenträger überwachen" aktiviert ist, muss die SE_SECURITY_NAME-Datei ACCESS_SYSTEM_SECURITY.</td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CHANGE_NOTIFY_NAME"></span><span id="se_change_notify_name"></span><dl> <dt><strong>SE_CHANGE_NOTIFY_NAME</strong></dt> <dt>TEXT( &quot; SeChangeNotifyPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um Benachrichtigungen über Änderungen an Dateien oder Verzeichnissen zu erhalten. Diese Berechtigung bewirkt auch, dass das System alle Traversalzugriffsüberprüfungen überspringt. Sie ist standardmäßig für alle Benutzer aktiviert. <br/> Benutzerrecht: Durchquerungsüberprüfung umgehen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_GLOBAL_NAME"></span><span id="se_create_global_name"></span><dl> <dt><strong>SE_CREATE_GLOBAL_NAME</strong></dt> <dt>TEXT( &quot; SeCreateGlobalPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um benannte Dateizuordnungsobjekte im globalen Namespace während Terminaldienstesitzungen zu erstellen. Diese Berechtigung ist standardmäßig für Administratoren, Dienste und das lokale Systemkonto aktiviert.<br/> Benutzerrecht: Erstellen Sie globale Objekte.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CREATE_PAGEFILE_NAME"></span><span id="se_create_pagefile_name"></span><dl> <dt><strong>SE_CREATE_PAGEFILE_NAME</strong></dt> <dt>TEXT( &quot; SeCreatePagefilePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um eine Auslagerungsdatei zu erstellen. <br/> Benutzerrecht: Erstellen Sie eine Auslagerungsdatei.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_PERMANENT_NAME"></span><span id="se_create_permanent_name"></span><dl> <dt><strong>SE_CREATE_PERMANENT_NAME</strong></dt> <dt>TEXT( &quot; SeCreatePermanentPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um ein permanentes -Objekt zu erstellen. <br/> Benutzerrecht: Erstellen Sie permanente freigegebene Objekte.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CREATE_SYMBOLIC_LINK_NAME"></span><span id="se_create_symbolic_link_name"></span><dl> <dt><strong>SE_CREATE_SYMBOLIC_LINK_NAME</strong></dt> <dt>TEXT( &quot; SeCreateSymbolicLinkPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um eine symbolische Verknüpfung zu erstellen.<br/> Benutzerrecht: Erstellen Sie symbolische Verknüpfungen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_TOKEN_NAME"></span><span id="se_create_token_name"></span><dl> <dt><strong>SE_CREATE_TOKEN_NAME</strong></dt> <dt>TEXT( &quot; SeCreateTokenPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um ein primäres Token zu erstellen. <br/> Benutzerrecht: Erstellen Sie ein Tokenobjekt.<br/> Sie können diese Berechtigung nicht einem Benutzerkonto mit der &quot; Richtlinie Tokenobjekt erstellen &quot; hinzufügen. Darüber hinaus können Sie diese Berechtigung nicht mithilfe von Windows-APIs einem eigenen Prozess hinzufügen. <strong>Windows Server 2003 und Windows XP mit SP1 und früher:</strong> Windows-APIs können diese Berechtigung einem eigenen Prozess hinzufügen.<br/> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_DEBUG_NAME"></span><span id="se_debug_name"></span><dl> <dt><strong>SE_DEBUG_NAME</strong></dt> <dt>TEXT( &quot; SeDebugPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich zum Debuggen und Anpassen des Arbeitsspeichers eines Prozesses, der sich im Besitz eines anderen Kontos befindet. <br/> Benutzerrecht: Debugprogramme.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME"></span><span id="se_delegate_session_user_impersonate_name"></span><dl> <dt><strong>SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME</strong></dt> <dt>TEXT( &quot; SeDelegateSessionUserImpersonatePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um ein Identitätswechseltoken für einen anderen Benutzer in derselben Sitzung abzurufen. <br/> Benutzerrecht: Identität anderer Benutzer annehmen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_ENABLE_DELEGATION_NAME"></span><span id="se_enable_delegation_name"></span><dl> <dt><strong>SE_ENABLE_DELEGATION_NAME</strong></dt> <dt>TEXT( &quot; SeEnableDelegationPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um Benutzer- und Computerkonten für die Delegierung als vertrauenswürdig zu kennzeichnen.<br/> Benutzerrecht: Aktivieren Sie, dass Computer- und Benutzerkonten für die Delegierung als vertrauenswürdig eingestuft werden.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_IMPERSONATE_NAME"></span><span id="se_impersonate_name"></span><dl> <dt><strong>SE_IMPERSONATE_NAME</strong></dt> <dt>TEXT( &quot; SeImpersonatePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich für den Identitätswechsel.<br/> Benutzerrecht: Angenommen, ein Client wird nach der Authentifizierung angenommen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_INC_BASE_PRIORITY_NAME"></span><span id="se_inc_base_priority_name"></span><dl> <dt><strong>SE_INC_BASE_PRIORITY_NAME</strong></dt> <dt>TEXT( &quot; SeIncreaseBasePriorityPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um die Basispriorität eines Prozesses zu erhöhen. <br/> Benutzerrecht: Erhöhen Sie die Planungspriorität.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_INCREASE_QUOTA_NAME"></span><span id="se_increase_quota_name"></span><dl> <dt><strong>SE_INCREASE_QUOTA_NAME</strong></dt> <dt>TEXT( &quot; SeIncreaseQuotaPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um das einem Prozess zugewiesene Kontingent zu erhöhen. <br/> Benutzerrecht: Passen Sie die Speicherkontingente für einen Prozess an.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_INC_WORKING_SET_NAME"></span><span id="se_inc_working_set_name"></span><dl> <dt><strong>SE_INC_WORKING_SET_NAME</strong></dt> <dt>TEXT( &quot; SeIncreaseWorkingSetPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um mehr Arbeitsspeicher für Anwendungen zu reservieren, die im Kontext von Benutzern ausgeführt werden.<br/> Benutzerrecht: Erhöhen Sie einen Prozessarbeitssatz.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_LOAD_DRIVER_NAME"></span><span id="se_load_driver_name"></span><dl> <dt><strong>SE_LOAD_DRIVER_NAME</strong></dt> <dt>TEXT( &quot; SeLoadDriverPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich zum Laden oder Entladen eines Gerätetreibers. <br/> Benutzerrecht: Laden und Entladen von Gerätetreibern.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_LOCK_MEMORY_NAME"></span><span id="se_lock_memory_name"></span><dl> <dt><strong>SE_LOCK_MEMORY_NAME</strong></dt> <dt>TEXT( &quot; SeLockMemoryPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um physische Seiten im Arbeitsspeicher zu sperren. <br/> Benutzerrecht: Sperren von Seiten im Arbeitsspeicher.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_MACHINE_ACCOUNT_NAME"></span><span id="se_machine_account_name"></span><dl> <dt><strong>SE_MACHINE_ACCOUNT_NAME</strong></dt> <dt>TEXT( &quot; SeMachineAccountPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um ein Computerkonto zu erstellen. <br/> Benutzerrecht: Fügen Sie Arbeitsstationen zur Domäne hinzu.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_MANAGE_VOLUME_NAME"></span><span id="se_manage_volume_name"></span><dl> <dt><strong>SE_MANAGE_VOLUME_NAME</strong></dt> <dt>TEXT( &quot; SeManageVolumePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um Volumeverwaltungsberechtigungen zu aktivieren. <br/> Benutzerrecht: Verwalten Sie die Dateien auf einem Volume.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_PROF_SINGLE_PROCESS_NAME"></span><span id="se_prof_single_process_name"></span><dl> <dt><strong>SE_PROF_SINGLE_PROCESS_NAME</strong></dt> <dt>TEXT( &quot; SeProfileSingleProcessPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um Profilerstellungsinformationen für einen einzelnen Prozess zu sammeln. <br/> Benutzerrecht: Profil für einen einzelnen Prozess.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_RELABEL_NAME"></span><span id="se_relabel_name"></span><dl> <dt><strong>SE_RELABEL_NAME</strong></dt> <dt>TEXT( &quot; SeRelabelPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um die erforderliche Integritätsebene eines Objekts zu ändern.<br/> Benutzerrecht: Ändern sie eine Objektbezeichnung.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_REMOTE_SHUTDOWN_NAME"></span><span id="se_remote_shutdown_name"></span><dl> <dt><strong>SE_REMOTE_SHUTDOWN_NAME</strong></dt> <dt>TEXT( &quot; SeRemoteShutdownPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um ein System mithilfe einer Netzwerkanforderung herunterzufahren. <br/> Benutzerrecht: Erzwingen des Herunterfahrens von einem Remotesystem.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_RESTORE_NAME"></span><span id="se_restore_name"></span><dl> <dt><strong>SE_RESTORE_NAME</strong></dt> <dt>TEXT( &quot; SeRestorePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich zum Ausführen von Wiederherstellungsvorgängen. Diese Berechtigung bewirkt, dass das System jede Schreibzugriffssteuerung für jede Datei gewährt, unabhängig von der für die Datei angegebenen Zugriffssteuerungsliste. Jede andere Zugriffsanforderung als write wird weiterhin mit der Zugriffssteuerungsliste ausgewertet. Darüber hinaus können Sie mit dieser Berechtigung eine gültige Benutzer- oder Gruppen-SID als Besitzer einer Datei festlegen. Diese Berechtigung ist für die <a href="/windows/desktop/api/winreg/nf-winreg-regloadkeya"><strong>RegLoadKey-Funktion</strong></a> erforderlich. Die folgenden Zugriffsrechte werden gewährt, wenn diese Berechtigung erteilt wird:<br/>
<ul>
<li>WRITE_DAC</li>
<li>WRITE_OWNER</li>
<li>ACCESS_SYSTEM_SECURITY</li>
<li>FILE_GENERIC_WRITE</li>
<li>FILE_ADD_FILE</li>
<li>FILE_ADD_SUBDIRECTORY</li>
<li>DELETE</li>
</ul>
Benutzerrecht: Dateien und Verzeichnisse wiederherstellen.<br/>Wenn sich die Datei auf einem Wechseldatenträger befindet und "Wechseldatenträger überwachen" aktiviert ist, muss die SE_SECURITY_NAME-Datei ACCESS_SYSTEM_SECURITY.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SECURITY_NAME"></span><span id="se_security_name"></span><dl> <dt><strong>SE_SECURITY_NAME</strong></dt> <dt>TEXT( &quot; SeSecurityPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um eine Reihe von sicherheitsbezogenen Funktionen auszuführen, z. B. Steuern und Anzeigen von Überwachungsmeldungen. Diese Berechtigung identifiziert den Besitzer als Sicherheitsoperator. <br/> Benutzerrecht: Verwalten der Überwachung und des Sicherheitsprotokolls.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SHUTDOWN_NAME"></span><span id="se_shutdown_name"></span><dl> <dt><strong>SE_SHUTDOWN_NAME</strong></dt> <dt>TEXT( &quot; SeShutdownPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um ein lokales System herunterfahren zu können. <br/> Benutzerrecht: Fahren Sie das System herunter.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SYNC_AGENT_NAME"></span><span id="se_sync_agent_name"></span><dl> <dt><strong>SE_SYNC_AGENT_NAME</strong></dt> <dt>TEXT( &quot; SeSyncAgentPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, damit ein Domänencontroller die <a href="/windows/desktop/SecGloss/l-gly"><em>Verzeichnissynchronisierungsdienste des Lightweight Directory Access Protocol</em></a> verwenden kann. Mit dieser Berechtigung kann der Besitzer alle Objekte und Eigenschaften im Verzeichnis lesen, unabhängig vom Schutz der Objekte und Eigenschaften. Standardmäßig wird sie den Administrator- und LocalSystem-Konten auf Domänencontrollern zugewiesen. <br/> Benutzerrecht: Synchronisieren von Verzeichnisdienstdaten.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SYSTEM_ENVIRONMENT_NAME"></span><span id="se_system_environment_name"></span><dl> <dt><strong>SE_SYSTEM_ENVIRONMENT_NAME</strong></dt> <dt>TEXT( &quot; SeSystemEnvironmentPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um den nicht flüchtigen RAM von Systemen zu ändern, die diesen Speichertyp zum Speichern von Konfigurationsinformationen verwenden. <br/> Benutzerrecht: Ändern Sie die Werte der Firmwareumgebung.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SYSTEM_PROFILE_NAME"></span><span id="se_system_profile_name"></span><dl> <dt><strong>SE_SYSTEM_PROFILE_NAME</strong></dt> <dt>TEXT( &quot; SeSystemProfilePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um Profilerstellungsinformationen für das gesamte System zu sammeln. <br/> Benutzerrecht: Profilsystemleistung.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SYSTEMTIME_NAME"></span><span id="se_systemtime_name"></span><dl> <dt><strong>SE_SYSTEMTIME_NAME</strong></dt> <dt>TEXT( &quot; SeSystemtimePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um die Systemzeit zu ändern. <br/> Benutzerrecht: Ändern Sie die Systemzeit.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_TAKE_OWNERSHIP_NAME"></span><span id="se_take_ownership_name"></span><dl> <dt><strong>SE_TAKE_OWNERSHIP_NAME</strong></dt> <dt>TEXT( &quot; SeTakeOwnershipPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um den Besitz eines Objekts zu übernehmen, ohne dass ein diskreter Zugriff gewährt wird. Mit dieser Berechtigung kann der Besitzerwert nur auf die Werte festgelegt werden, die der Besitzer berechtigterweise als Besitzer eines Objekts zuweisen kann. <br/> Benutzerrecht: Übernehmen Sie den Besitz von Dateien oder anderen Objekten.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_TCB_NAME"></span><span id="se_tcb_name"></span><dl> <dt><strong>SE_TCB_NAME</strong></dt> <dt>TEXT( &quot; SeTcbPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Mit dieser Berechtigung wird der Besitzer als Teil der vertrauenswürdigen Computerbasis identifiziert. Einigen vertrauenswürdigen geschützten Subsystemen wird diese Berechtigung gewährt. <br/> Benutzerrecht: Fungiert als Teil des Betriebssystems.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_TIME_ZONE_NAME"></span><span id="se_time_zone_name"></span><dl> <dt><strong>SE_TIME_ZONE_NAME</strong></dt> <dt>TEXT( &quot; SeTimeZonePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um die Zeitzone anzupassen, die der internen Uhr des Computers zugeordnet ist.<br/> Benutzerrecht: Ändern Sie die Zeitzone.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_TRUSTED_CREDMAN_ACCESS_NAME"></span><span id="se_trusted_credman_access_name"></span><dl> <dt><strong>SE_TRUSTED_CREDMAN_ACCESS_NAME</strong></dt> <dt>TEXT( &quot; SeTrustedCredManAccessPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um Anmeldeinformationsverwaltung als vertrauenswürdiger Aufrufer zu erhalten.<br/> Benutzerrecht: Zugriff Anmeldeinformationsverwaltung als vertrauenswürdiger Aufrufer.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_UNDOCK_NAME"></span><span id="se_undock_name"></span><dl> <dt><strong>SE_UNDOCK_NAME</strong></dt> <dt>TEXT( &quot; SeUndockPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich zum Abdocken eines Laptops.<br/> Benutzerrecht: Entfernen Sie den Computer aus der Andockstation.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_UNSOLICITED_INPUT_NAME"></span><span id="se_unsolicited_input_name"></span><dl> <dt><strong>SE_UNSOLICITED_INPUT_NAME</strong></dt> <dt>TEXT( &quot; SeUnsolicitedInputPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um nicht angeforderte Eingaben von einem <a href="/windows/desktop/SecGloss/t-gly"><em>Terminalgerät zu</em></a> lesen.<br/> Benutzerrecht: Nicht zutreffend.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Hinweise

Berechtigungskonst constants werden in Winnt.h als Zeichenfolgen definiert. Die SE \_ AUDIT \_ NAME-Konstante ist beispielsweise als "SeAuditPrivilege" definiert.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Winnt.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Berechtigungen](privileges.md)
</dt> </dl>

