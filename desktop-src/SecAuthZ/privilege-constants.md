---
Description: Berechtigungen bestimmen den Typ der System Vorgänge, die ein Benutzerkonto ausführen kann. Ein Administrator weist Benutzer-und Gruppenkonten Berechtigungen zu. Jeder Benutzer verfügt über die Berechtigungen, die dem Benutzer und den Gruppen gewährt werden, zu denen der Benutzer gehört.
ms.assetid: 973796a6-bc2e-4e64-92db-5e17b9c25460
title: Berechtigungs Konstanten (WinNT. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 801eccb2f42ccf27b45bc5628a32cee3de994bfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370768"
---
# <a name="privilege-constants-authorization"></a>Berechtigungs Konstanten (Autorisierung)

Berechtigungen bestimmen den Typ der System Vorgänge, die ein Benutzerkonto ausführen kann. Ein Administrator weist Benutzer-und Gruppenkonten Berechtigungen zu. Zu den Berechtigungen des Benutzers gehören die Berechtigungen, die dem Benutzer gewährt wurden, sowie die Gruppen, zu denen der Benutzer gehört.

Die Funktionen, die die Berechtigungen in einem [*Zugriffs Token abrufen*](/windows/desktop/SecGloss/a-gly) und anpassen, verwenden den Typ der [*lokalen eindeutigen Kennung*](/windows/desktop/SecGloss/l-gly) (LUID) zum Identifizieren von Berechtigungen. Verwenden Sie die [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) -Funktion, um die [**LUID**](/windows/desktop/api/Winnt/ns-winnt-luid) auf dem lokalen System zu ermitteln, die einer Berechtigungs Konstante entspricht. Verwenden Sie die [**lookupprivilegilegename**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) -Funktion, um eine **LUID** in die entsprechende Zeichen folgen Konstante zu konvertieren.

Das Betriebssystem stellt eine Berechtigung mithilfe der Zeichenfolge dar, die in der Spalte Beschreibung der folgenden Tabelle auf "Benutzerrecht" folgt. Das Betriebssystem zeigt die Benutzerrechten Zeichen folgen in der Spalte **Richtlinie** des Knotens Zuweisen von **Benutzerrechten** im MMC-Snap-in (Microsoft Management Console) lokale Sicherheitseinstellungen an.

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
<td style="text-align: left;"><span id="SE_ASSIGNPRIMARYTOKEN_NAME"></span><span id="se_assignprimarytoken_name"></span><dl> <dt><strong>SE_ASSIGNPRIMARYTOKEN_NAME</strong></dt> <dt>Text ( &quot; seassignprimaryanmelkenprivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um das <a href="/windows/desktop/SecGloss/p-gly"><em>primäre Token</em></a> eines Prozesses zuzuweisen. <br/> Benutzerrecht: Ersetzen Sie ein Token auf Prozessebene.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_AUDIT_NAME"></span><span id="se_audit_name"></span><dl> <dt><strong>SE_AUDIT_NAME</strong></dt> <dt>Text (" &quot; abauditprivilege" &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um Überwachungs Protokolleinträge zu generieren. Stellen Sie diese Berechtigung sicheren Servern zur Verfügung. <br/> Benutzerrecht: Generieren von Sicherheits Überwachungen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_BACKUP_NAME"></span><span id="se_backup_name"></span><dl> <dt><strong>SE_BACKUP_NAME</strong></dt> <dt>Text ( &quot; &quot; </dt> "". </dl></td>
<td style="text-align: left;">Zum Ausführen von Sicherungs Vorgängen erforderlich. Diese Berechtigung bewirkt, dass das System allen Dateien alle Lese Zugriffs Steuerungen zuweist, unabhängig von der <a href="/windows/desktop/SecGloss/a-gly"><em>Zugriffs Steuerungs Liste</em></a> (ACL), die für die Datei angegeben wurde. Alle anderen Zugriffs Anforderungen als Read werden weiterhin mit der ACL ausgewertet. Diese Berechtigung ist für die Funktionen <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya"><strong>regsavekey</strong></a> und <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeyexa"><strong>regsavekeyex</strong></a>erforderlich. Wenn diese Berechtigung gewährt wird, werden die folgenden Zugriffsrechte erteilt:<br/>
<ul>
<li>READ_CONTROL</li>
<li>ACCESS_SYSTEM_SECURITY</li>
<li>FILE_GENERIC_READ</li>
<li>FILE_TRAVERSE</li>
</ul>
Benutzerrecht: Sichern Sie Dateien und Verzeichnisse.<br/>Wenn sich die Datei auf einem Wechsel Datenträger befindet und der "Wechsel Datenträger überwachen" aktiviert ist, ist für die SE_SECURITY_NAME ACCESS_SYSTEM_SECURITY erforderlich.</td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CHANGE_NOTIFY_NAME"></span><span id="se_change_notify_name"></span><dl> <dt><strong>SE_CHANGE_NOTIFY_NAME</strong></dt> <dt>Text (" &quot; abchangenotifyprivilege" &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um Benachrichtigungen über Änderungen an Dateien oder Verzeichnissen zu empfangen. Diese Berechtigung bewirkt auch, dass das System alle Überprüfungen des Durchlaufs überspringt. Sie ist standardmäßig für alle Benutzer aktiviert. <br/> Benutzerrecht: Umgehung der traversierungs Überprüfung.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_GLOBAL_NAME"></span><span id="se_create_global_name"></span><dl> <dt><strong>SE_CREATE_GLOBAL_NAME</strong></dt> <dt>Text ( &quot; SeCreateGlobalPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich zum Erstellen benannter Datei Zuordnung-Objekte im globalen Namespace während der Terminal Dienste-Sitzungen. Diese Berechtigung ist für Administratoren, Dienste und das lokale Systemkonto standardmäßig aktiviert.<br/> Benutzerrecht: Erstellen Sie globale Objekte.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CREATE_PAGEFILE_NAME"></span><span id="se_create_pagefile_name"></span><dl> <dt><strong>SE_CREATE_PAGEFILE_NAME</strong></dt> <dt>Text ( &quot; secreatepagefileprivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich zum Erstellen einer Auslagerungs Datei. <br/> Benutzerrecht: Erstellen Sie eine Pagefile-Datei.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_PERMANENT_NAME"></span><span id="se_create_permanent_name"></span><dl> <dt><strong>SE_CREATE_PERMANENT_NAME</strong></dt> <dt>Text ( &quot; SeCreatePermanentPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um ein dauerhaftes Objekt zu erstellen. <br/> Benutzerrecht: Erstellen Sie permanente freigegebene Objekte.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CREATE_SYMBOLIC_LINK_NAME"></span><span id="se_create_symbolic_link_name"></span><dl> <dt><strong>SE_CREATE_SYMBOLIC_LINK_NAME</strong></dt> <dt>Text ( &quot; secreatesymboliclinkprivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um eine symbolische Verknüpfung zu erstellen.<br/> Benutzerrecht: Erstellen Sie symbolische Verknüpfungen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_TOKEN_NAME"></span><span id="se_create_token_name"></span><dl> <dt><strong>SE_CREATE_TOKEN_NAME</strong></dt> <dt>Text ( &quot; secreateto kenprivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um ein primäres Token zu erstellen. <br/> Benutzerrecht: Erstellen Sie ein Tokenobjekt.<br/> Diese Berechtigung kann einem Benutzerkonto nicht mit der &quot; Richtlinie zum Erstellen eines Token-Objekts hinzugefügt werden &quot; . Außerdem ist es nicht möglich, diese Berechtigung mithilfe von Windows-APIs einem eigenen Prozess hinzuzufügen. <strong>Windows Server 2003 und Windows XP mit SP1 und früher:</strong> Windows-APIs können diese Berechtigung einem eigenen Prozess hinzufügen.<br/> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_DEBUG_NAME"></span><span id="se_debug_name"></span><dl> <dt><strong>SE_DEBUG_NAME</strong></dt> <dt>Text ("Einstellungs &quot; Berechtigung" &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um den Arbeitsspeicher eines Prozesses zu Debuggen und anzupassen, der im Besitz eines anderen Kontos ist <br/> Benutzerrecht: Debuggen von Programmen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME"></span><span id="se_delegate_session_user_impersonate_name"></span><dl> <dt><strong>SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME</strong></dt> <dt>Text ("c &quot; delegatesessionuseridentitäts ateprivilege" &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich zum Abrufen eines Identitätswechsel Tokens für einen anderen Benutzer in derselben Sitzung. <br/> Benutzerrecht: Identität anderer Benutzer annehmen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_ENABLE_DELEGATION_NAME"></span><span id="se_enable_delegation_name"></span><dl> <dt><strong>SE_ENABLE_DELEGATION_NAME</strong></dt> <dt>Text ( &quot; seenabledelegationprivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um Benutzer-und Computer Konten als vertrauenswürdig für die Delegierung zu markieren.<br/> Benutzerrecht: Aktivieren Sie Computer-und Benutzerkonten für die Delegierung als vertrauenswürdig.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_IMPERSONATE_NAME"></span><span id="se_impersonate_name"></span><dl> <dt><strong>SE_IMPERSONATE_NAME</strong></dt> <dt>Text ( &quot; SeImpersonatePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um einen Identitätswechsel auszuführen.<br/> Benutzerrecht: Identität eines Clients nach der Authentifizierung annehmen<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_INC_BASE_PRIORITY_NAME"></span><span id="se_inc_base_priority_name"></span><dl> <dt><strong>SE_INC_BASE_PRIORITY_NAME</strong></dt> <dt>Text ( &quot; seinkreasebasepriorityprivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um die Basis Priorität eines Prozesses zu erhöhen. <br/> Benutzerrecht: erhöhen Sie die Planungs Priorität.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_INCREASE_QUOTA_NAME"></span><span id="se_increase_quota_name"></span><dl> <dt><strong>SE_INCREASE_QUOTA_NAME</strong></dt> <dt>Text ( &quot; seinkreasequotaprivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um das einem Prozess zugewiesene Kontingent zu erhöhen. <br/> Benutzerrecht: passen Sie Arbeitsspeicher Kontingente für einen Prozess an.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_INC_WORKING_SET_NAME"></span><span id="se_inc_working_set_name"></span><dl> <dt><strong>SE_INC_WORKING_SET_NAME</strong></dt> <dt>Text ( &quot; seinkreaseworkingsetprivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um mehr Arbeitsspeicher für Anwendungen zuzuweisen, die im Kontext von Benutzern ausgeführt werden.<br/> Benutzerrecht: erhöhen Sie einen Prozess Arbeitssatz.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_LOAD_DRIVER_NAME"></span><span id="se_load_driver_name"></span><dl> <dt><strong>SE_LOAD_DRIVER_NAME</strong></dt> <dt>Text ( &quot; SeLoadDriverPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich zum Laden oder Entladen eines Gerätetreibers. <br/> Benutzerrecht: Gerätetreiber laden und entladen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_LOCK_MEMORY_NAME"></span><span id="se_lock_memory_name"></span><dl> <dt><strong>SE_LOCK_MEMORY_NAME</strong></dt> <dt>Text ( &quot; SeLockMemoryPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um physische Seiten im Arbeitsspeicher zu sperren. <br/> Benutzerrecht: Sperren von Seiten im Speicher.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_MACHINE_ACCOUNT_NAME"></span><span id="se_machine_account_name"></span><dl> <dt><strong>SE_MACHINE_ACCOUNT_NAME</strong></dt> <dt>Text (" &quot; \machineaccountprivilege" &quot; )</dt> </dl></td>
<td style="text-align: left;">Zum Erstellen eines Computer Kontos erforderlich. <br/> Benutzerrecht: Arbeitsstationen zur Domäne hinzufügen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_MANAGE_VOLUME_NAME"></span><span id="se_manage_volume_name"></span><dl> <dt><strong>SE_MANAGE_VOLUME_NAME</strong></dt> <dt>Text ( &quot; &quot; </dt> ". </dl></td>
<td style="text-align: left;">Erforderlich zum Aktivieren von Volumen Verwaltungs Berechtigungen. <br/> Benutzerrecht: Verwalten Sie die Dateien auf einem Volume.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_PROF_SINGLE_PROCESS_NAME"></span><span id="se_prof_single_process_name"></span><dl> <dt><strong>SE_PROF_SINGLE_PROCESS_NAME</strong></dt> <dt>Text ( &quot; &quot; </dt> "" ". </dl></td>
<td style="text-align: left;">Erforderlich, um Profil Erstellungs Informationen für einen einzelnen Prozess zu erfassen. <br/> Benutzerrecht: Profil für einen einzelnen Prozess.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_RELABEL_NAME"></span><span id="se_relabel_name"></span><dl> <dt><strong>SE_RELABEL_NAME</strong></dt> <dt>Text ( &quot; SeRelabelPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich zum Ändern der obligatorischen Integritäts Stufe eines Objekts.<br/> Benutzerrecht: Ändern Sie eine Objekt Bezeichnung.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_REMOTE_SHUTDOWN_NAME"></span><span id="se_remote_shutdown_name"></span><dl> <dt><strong>SE_REMOTE_SHUTDOWN_NAME</strong></dt> <dt>Text ( &quot; SeRemoteShutdownPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Ist erforderlich, um ein System mit einer Netzwerk Anforderung zu beenden. <br/> Benutzerrecht: Erzwingen des herunter Fahrens von einem Remote System aus.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_RESTORE_NAME"></span><span id="se_restore_name"></span><dl> <dt><strong>SE_RESTORE_NAME</strong></dt> <dt>Text ( &quot; SeRestorePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Zum Ausführen von Wiederherstellungs Vorgängen erforderlich. Diese Berechtigung bewirkt, dass das System alle Schreibzugriffs Berechtigungen allen Dateien erteilt, unabhängig von der für die Datei angegebenen ACL. Alle anderen Zugriffs Anforderungen als Write werden weiterhin mit der ACL ausgewertet. Außerdem können Sie mit dieser Berechtigung eine beliebige gültige Benutzer-oder Gruppen-SID als Besitzer einer Datei festlegen. Diese Berechtigung ist für die <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya"><strong>RegLoadKey</strong></a> -Funktion erforderlich. Wenn diese Berechtigung gewährt wird, werden die folgenden Zugriffsrechte erteilt:<br/>
<ul>
<li>WRITE_DAC</li>
<li>WRITE_OWNER</li>
<li>ACCESS_SYSTEM_SECURITY</li>
<li>FILE_GENERIC_WRITE</li>
<li>FILE_ADD_FILE</li>
<li>FILE_ADD_SUBDIRECTORY</li>
<li>Delete</li>
</ul>
Benutzerrecht: Stellen Sie Dateien und Verzeichnisse wieder her.<br/>Wenn sich die Datei auf einem Wechsel Datenträger befindet und der "Wechsel Datenträger überwachen" aktiviert ist, ist für die SE_SECURITY_NAME ACCESS_SYSTEM_SECURITY erforderlich.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SECURITY_NAME"></span><span id="se_security_name"></span><dl> <dt><strong>SE_SECURITY_NAME</strong></dt> <dt>Text ( &quot; SeSecurityPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Ist erforderlich, um eine Reihe von sicherheitsbezogenen Funktionen auszuführen, z. b. das Steuern und Anzeigen von Überwachungs Nachrichten. Dieses Privileg identifiziert seinen Inhaber als Sicherheits Operator. <br/> Benutzerrecht: Verwalten von Überwachungs-und Sicherheitsprotokollen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SHUTDOWN_NAME"></span><span id="se_shutdown_name"></span><dl> <dt><strong>SE_SHUTDOWN_NAME</strong></dt> <dt>Text ( &quot; SeShutdownPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Ist erforderlich, um ein lokales System herunterzufahren. <br/> Benutzerrecht: fahren Sie das System herunter.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SYNC_AGENT_NAME"></span><span id="se_sync_agent_name"></span><dl> <dt><strong>SE_SYNC_AGENT_NAME</strong></dt> <dt>Text ( &quot; sesyncagentprivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, damit ein Domänen Controller die Verzeichnis Synchronisierungs Dienste des <a href="/windows/desktop/SecGloss/l-gly"><em>Lightweight Directory Access-Protokolls</em></a> verwendet. Diese Berechtigung ermöglicht es dem Inhaber, alle Objekte und Eigenschaften im Verzeichnis zu lesen, unabhängig vom Schutz der Objekte und Eigenschaften. Standardmäßig wird Sie den Konten "Administrator" und "LocalSystem" auf Domänen Controllern zugewiesen. <br/> Benutzerrecht: Synchronisieren von Verzeichnisdienst Daten.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SYSTEM_ENVIRONMENT_NAME"></span><span id="se_system_environment_name"></span><dl> <dt><strong>SE_SYSTEM_ENVIRONMENT_NAME</strong></dt> <dt>Text ( &quot; sesystemumgebtungprivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um den nicht flüchtigen RAM von Systemen zu ändern, die diese Art von Arbeitsspeicher zum Speichern von Konfigurationsinformationen verwenden. <br/> Benutzerrecht: Ändern Sie die Werte der Firmware-Umgebung.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SYSTEM_PROFILE_NAME"></span><span id="se_system_profile_name"></span><dl> <dt><strong>SE_SYSTEM_PROFILE_NAME</strong></dt> <dt>Text ( &quot; sesystemprofileprivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um Profil Erstellungs Informationen für das gesamte System zu erfassen. <br/> Benutzerrecht: Profilsystem Leistung.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SYSTEMTIME_NAME"></span><span id="se_systemtime_name"></span><dl> <dt><strong>SE_SYSTEMTIME_NAME</strong></dt> <dt>Text ( &quot; SeSystemtimePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um die Systemzeit zu ändern. <br/> Benutzerrecht: Ändern Sie die Systemzeit.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_TAKE_OWNERSHIP_NAME"></span><span id="se_take_ownership_name"></span><dl> <dt><strong>SE_TAKE_OWNERSHIP_NAME</strong></dt> <dt>Text (" &quot; antakebesitzshipprivilege" &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um den Besitz eines Objekts zu übernehmen, ohne freigegebenen Zugriff zu erhalten. Diese Berechtigung ermöglicht es, dass der Besitzer Wert nur auf die Werte festgelegt wird, die der Inhaber rechtmäßig als Besitzer eines Objekts zuweisen kann. <br/> Benutzerrecht: übernehmen Sie den Besitz von Dateien oder anderen Objekten.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_TCB_NAME"></span><span id="se_tcb_name"></span><dl> <dt><strong>SE_TCB_NAME</strong></dt> <dt>Text ( &quot; SeTcbPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Dieses Privileg identifiziert seinen Inhaber als Teil der vertrauenswürdigen Computer Basis. Einigen vertrauenswürdigen geschützten Subsystemen wird dieses Privileg erteilt. <br/> Benutzerrecht: fungieren Sie als Teil des Betriebssystems.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_TIME_ZONE_NAME"></span><span id="se_time_zone_name"></span><dl> <dt><strong>SE_TIME_ZONE_NAME</strong></dt> <dt>Text (" &quot; \timezoneprivilege" &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich, um die Zeitzone anzupassen, die der internen Uhr des Computers zugeordnet ist.<br/> Benutzerrecht: Ändern Sie die Zeitzone.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_TRUSTED_CREDMAN_ACCESS_NAME"></span><span id="se_trusted_credman_access_name"></span><dl> <dt><strong>SE_TRUSTED_CREDMAN_ACCESS_NAME</strong></dt> <dt>Text ("Set- &quot; dkredmanaccessprivilege &quot; </dt> " </dl></td>
<td style="text-align: left;">Muss als vertrauenswürdiger Aufrufer auf Credential Manager zugreifen können.<br/> Benutzerrecht: greifen Sie als vertrauenswürdiger Aufrufer auf Credential Manager zu.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_UNDOCK_NAME"></span><span id="se_undock_name"></span><dl> <dt><strong>SE_UNDOCK_NAME</strong></dt> <dt>Text (" &quot; abdockprivilege" &quot; )</dt> </dl></td>
<td style="text-align: left;">Erforderlich zum Abdocken eines Laptops.<br/> Benutzerrecht: Entfernen Sie den Computer aus der Docking Station.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_UNSOLICITED_INPUT_NAME"></span><span id="se_unsolicited_input_name"></span><dl> <dt><strong>SE_UNSOLICITED_INPUT_NAME</strong></dt> <dt>Text ( &quot; &quot; </dt> "Einstellungs Element") </dl></td>
<td style="text-align: left;">Erforderlich zum Lesen von nicht angeforderten Eingaben von einem <a href="/windows/desktop/SecGloss/t-gly"><em>Terminal</em></a> Gerät.<br/> Benutzerrecht: nicht zutreffend.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Bemerkungen

Berechtigungs Konstanten werden als Zeichen folgen in "Winnt. h" definiert. Beispielsweise \_ ist die "SE Audit \_ Name Constant"-Konstante als "" "" "" ".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WinNT. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Berechtigungen](privileges.md)
</dt> </dl>

