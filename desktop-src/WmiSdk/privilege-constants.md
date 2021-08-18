---
description: Der strPrivilege-Parameter der SWbemPrivilegeSet.AddAsString-Methode und der iPrivilege-Parameter für SWbemPrivilegeSet.Add erfordern Berechtigungszeichenfolgen aus WbemPrivilegeEnum.
ms.assetid: f9400597-81bb-44a8-80dc-aba0160aea26
ms.tgt_platform: multiple
title: Berechtigungskonstanten (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- wbemPrivilegeCreateToken
- wbemPrivilegePrimaryToken
- wbemPrivilegeLockMemory
- wbemPrivilegeIncreaseQuota
- wbemPrivilegeMachineAccount
- wbemPrivilegeTcb
- wbemPrivilegeSecurity
- wbemPrivilegeTakeOwnership
- wbemPrivilegeLoadDriver
- wbemPrivilegeSystemProfile
- wbemPrivilegeSystemtime
- wbemPrivilegeProfileSingleProcess
- wbemPrivilegeIncreaseBasePriority
- wbemPrivilegeCreatePagefile
- wbemPrivilegeCreatePermanent
- wbemPrivilegeBackup
- wbemPrivilegeRestore
- wbemPrivilegeShutdown
- wbemPrivilegeDebug
- wbemPrivilegeAudit
- wbemPrivilegeSystemEnvironment
- wbemPrivilegeChangeNotify
- wbemPrivilegeRemoteShutdown
- wbemPrivilegeUndock
- wbemPrivilegeSyncAgent
- wbemPrivilegeEnableDelegation
- wbemPrivilegeManageVolume
api_type:
- HeaderDef
api_location:
- Wbemdisp.h
ms.openlocfilehash: 38d104c99885d4328ce8b12413e91607655ab1e260a61b511e3ea4a600b80b4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131022"
---
# <a name="privilege-constants"></a>Berechtigungskonstanten

Der *strPrivilege-Parameter* der [**SWbemPrivilegeSet.AddAsString-Methode**](swbemprivilegeset-addasstring.md) und der *iPrivilege-Parameter* für [**SWbemPrivilegeSet.Add**](swbemprivilegeset-add.md) erfordern Berechtigungszeichenfolgen aus [WbemPrivilegeEnum.](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) Weitere Informationen zur Verwendung von Berechtigungskonstanten finden Sie unter [Ausführen privilegierter Vorgänge.](executing-privileged-operations.md)

Die folgenden Konstanten sind in [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)definiert. Die folgende Liste enthält die entsprechenden Konstanten für C++ und Zeichenfolgen für die Skripterstellung. Um den Kurznamen der Skripterstellung zu bilden, entfernen Sie "Se" und "Privilege" aus dem C++-Konstantennamen.

Das folgende VBScript-Codebeispiel zeigt, wie Sie die RemoteShutdown-Berechtigung in einem Skript aktivieren.


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (RemoteShutdown)}")
```



Viele WMI-Methoden erfordern, dass mindestens eine Berechtigung aktiviert ist. Wenn einem Konto keine Berechtigung erteilt wurde, kann es nicht für den Methodenaufruf aktiviert werden.

<dl> <dt>

<span id="wbemPrivilegeCreateToken"></span><span id="wbemprivilegecreatetoken"></span><span id="WBEMPRIVILEGECREATETOKEN"></span>**wbemPrivilegeCreateToken**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



C++-Konstante: **SE \_ CREATE TOKEN \_ \_ NAME-Zeichenfolge:** **SeCreateTokenPrivilege**

Kurzname der Skripterstellung: **CreateToken**

Erforderlich, um ein primäres Tokenobjekt zu erstellen.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegePrimaryToken"></span><span id="wbemprivilegeprimarytoken"></span><span id="WBEMPRIVILEGEPRIMARYTOKEN"></span>**wbemPrivilegePrimaryToken**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



C++-Konstante: **SeAssignPrimaryTokenPrivilege** string: **SeAssignPrimaryTokenPrivilege**

Kurzname der Skripterstellung: **AssignPrimaryToken**

Erforderlich, um ein Token auf Prozessebene zu ersetzen.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeLockMemory"></span><span id="wbemprivilegelockmemory"></span><span id="WBEMPRIVILEGELOCKMEMORY"></span>**wbemPrivilegeLockMemory**
</dt> <dd> <dl> <dt>

3 (0x3)
</dt> <dt>



C++-Konstante: **SE \_ LOCK MEMORY \_ \_ NAME-Zeichenfolge:** **SeLockMemoryPrivilege**

Kurzname der Skripterstellung: **LockMemory**

Erforderlich, um Seiten im Arbeitsspeicher zu sperren.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeIncreaseQuota"></span><span id="wbemprivilegeincreasequota"></span><span id="WBEMPRIVILEGEINCREASEQUOTA"></span>**wbemPrivilegeIncreaseQuota**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



C++-Konstante: **SE \_ INCREASE QUOTA \_ \_ NAME-Zeichenfolge:** **SeIncreaseQuotaPrivilege**

Kurzname der Skripterstellung: **IncreaseQuotaPrivilege**

Erforderlich, um Speicherkontingente für einen Prozess anzupassen.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeMachineAccount"></span><span id="wbemprivilegemachineaccount"></span><span id="WBEMPRIVILEGEMACHINEACCOUNT"></span>**wbemPrivilegeMachineAccount**
</dt> <dd> <dl> <dt>

5 (0x5)
</dt> <dt>



C++-Konstante: **SE \_ MACINE ACCOUNT \_ \_ NAME-Zeichenfolge:** **SeMachineAccountPrivilege**

Kurzname der Skripterstellung: **MachineAccount**

Erforderlich zum Hinzufügen von Arbeitsstationen zu einer Domäne.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeTcb"></span><span id="wbemprivilegetcb"></span><span id="WBEMPRIVILEGETCB"></span>**wbemPrivilegeTcb**
</dt> <dd> <dl> <dt>

6 (0x6)
</dt> <dt>



C++-Konstante: **SE \_ TCB \_ NAME-Zeichenfolge:** **SeTcbPrivilege**

Kurzname der Skripterstellung: **Tcb**

Erforderlich, um als Teil des Betriebssystems zu fungieren. Der Besitzer ist Teil der vertrauenswürdigen Computerbasis.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSecurity"></span><span id="wbemprivilegesecurity"></span><span id="WBEMPRIVILEGESECURITY"></span>**wbemPrivilegeSecurity**
</dt> <dd> <dl> <dt>

7 (0x7)
</dt> <dt>



C++-Konstante: **SE \_ SECURITY \_ NAME-Zeichenfolge:** **SeSecurityPrivilege**

Kurzname der Skripterstellung: **Sicherheit**

Erforderlich zum Verwalten der Überwachung und des NT-Sicherheitsprotokolls.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeTakeOwnership"></span><span id="wbemprivilegetakeownership"></span><span id="WBEMPRIVILEGETAKEOWNERSHIP"></span>**wbemPrivilegeTakeOwnership**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



C++-Konstante: **SE \_ TAKE OWNERSHIP \_ \_ NAME-Zeichenfolge:** **SeTakeOwnershipPrivilege**

Kurzname der Skripterstellung: **TakeOwnership**

Erforderlich, um den Besitz von Dateien oder anderen Objekten zu übernehmen, ohne dass ein [*Access Control Entry*](/windows/desktop/SecGloss/a-gly) (ACE) in der *DACL (Discretionary Access Control List)* vorhanden ist.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeLoadDriver"></span><span id="wbemprivilegeloaddriver"></span><span id="WBEMPRIVILEGELOADDRIVER"></span>**wbemPrivilegeLoadDriver**
</dt> <dd> <dl> <dt>

9 (0x9)
</dt> <dt>



C++-Konstante: **SE \_ LOAD \_ DRIVER-Zeichenfolge:** **SeLoadDriverPrivilege**

Kurzname der Skripterstellung: **LoadDriver**

Erforderlich zum Laden oder Entladen eines Gerätetreibers.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemProfile"></span><span id="wbemprivilegesystemprofile"></span><span id="WBEMPRIVILEGESYSTEMPROFILE"></span>**wbemPrivilegeSystemProfile**
</dt> <dd> <dl> <dt>

10 (0xA)
</dt> <dt>



C++-Konstante: **SE \_ ZEICHENFOLGE SYSTEM PROFILE \_ \_ NAME:** **SeSystemProfilePrivilege**

Kurzname der Skripterstellung: **SystemProfile**

Erforderlich, um Profilinformationen zur Systemleistung zu sammeln.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemtime"></span><span id="wbemprivilegesystemtime"></span><span id="WBEMPRIVILEGESYSTEMTIME"></span>**wbemPrivilegeSystemtime**
</dt> <dd> <dl> <dt>

11 (0xB)
</dt> <dt>



C++-Konstante: **SE \_ SYSTEMTIME** \_ NAME-Zeichenfolge: **SeSystemtimePrivilege**

Kurzname der Skripterstellung: **Systemtime**

Erforderlich, um die Systemzeit zu ändern.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeProfileSingleProcess"></span><span id="wbemprivilegeprofilesingleprocess"></span><span id="WBEMPRIVILEGEPROFILESINGLEPROCESS"></span>**wbemPrivilegeProfileSingleProcess**
</dt> <dd> <dl> <dt>

12 (0xC)
</dt> <dt>



C++-Konstante: **SE \_ PROF SINGLE PROCESS \_ \_ \_ NAME-Zeichenfolge:** **SeProfileSingleProcessPrivilege**

Kurzname der Skripterstellung: **ProfileSingleProcess**

Erforderlich, um Profilinformationen für einen einzelnen Prozess zu sammeln.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeIncreaseBasePriority"></span><span id="wbemprivilegeincreasebasepriority"></span><span id="WBEMPRIVILEGEINCREASEBASEPRIORITY"></span>**wbemPrivilegeIncreaseBasePriority**
</dt> <dd> <dl> <dt>

13 (0xD)
</dt> <dt>



C++-Konstante: **SE INC BASE PRIORITY \_ \_ \_ \_ NAME-Zeichenfolge:** **SeIncreaseBasePriorityPrivilege**

Kurzname der Skripterstellung: **IncreaseBasePriority**

Erforderlich, um die Planungspriorität zu erhöhen.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeCreatePagefile"></span><span id="wbemprivilegecreatepagefile"></span><span id="WBEMPRIVILEGECREATEPAGEFILE"></span>**wbemPrivilegeCreatePagefile**
</dt> <dd> <dl> <dt>

14 (0xE)
</dt> <dt>



C++-Konstante: **SE \_ CREATE \_ PAGEFILE \_ NAME-Zeichenfolge:** **SeCreatePagefilePrivilege**

Kurzname der Skripterstellung: **CreatePagefile**

Erforderlich, um eine Auslagerungsdatei zu erstellen.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeCreatePermanent"></span><span id="wbemprivilegecreatepermanent"></span><span id="WBEMPRIVILEGECREATEPERMANENT"></span>**wbemPrivilegeCreatePermanent**
</dt> <dd> <dl> <dt>

15 (0xF)
</dt> <dt>



C++-Konstante: **SE \_ CREATE PERMANENT \_ \_ NAME-Zeichenfolge:** **SeCreatePermanentPrivilege**

Kurzname der Skripterstellung: **CreatePermanent**

Erforderlich, um permanente freigegebene Objekte zu erstellen.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeBackup"></span><span id="wbemprivilegebackup"></span><span id="WBEMPRIVILEGEBACKUP"></span>**wbemPrivilegeBackup**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



C++-Konstante: **SE \_ BACKUP \_ NAME-Zeichenfolge:** **SeBackupPrivilege**

Kurzname der Skripterstellung: **Sicherung**

Erforderlich zum Sichern von Dateien und Verzeichnissen, unabhängig von der für die Datei angegebenen ACL.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeRestore"></span><span id="wbemprivilegerestore"></span><span id="WBEMPRIVILEGERESTORE"></span>**wbemPrivilegeRestore**
</dt> <dd> <dl> <dt>

17 (0x11)
</dt> <dt>



C++-Konstante: **SE \_ RESTORE \_ NAME-Zeichenfolge:** **SeRestorePrivilege**

Kurzname der Skripterstellung: **Wiederherstellen**

Erforderlich zum Wiederherstellen von Dateien und Verzeichnissen, unabhängig von der für die Datei angegebenen ACL.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeShutdown"></span><span id="wbemprivilegeshutdown"></span><span id="WBEMPRIVILEGESHUTDOWN"></span>**wbemPrivilegeShutdown**
</dt> <dd> <dl> <dt>

18 (0x12)
</dt> <dt>



C++-Konstante: **SE \_ SHUTDOWN \_ NAME-Zeichenfolge:** **SeShutdownPrivilege**

Kurzname der Skripterstellung: **Herunterfahren**

Erforderlich, um das lokale System herunterzufahren.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeDebug"></span><span id="wbemprivilegedebug"></span><span id="WBEMPRIVILEGEDEBUG"></span>**wbemPrivilegeDebug**
</dt> <dd> <dl> <dt>

19 (0x13)
</dt> <dt>



C++-Konstante: **SE \_ DEBUG \_ NAME-Zeichenfolge:** **SeDebugPrivilege**

Kurzname der Skripterstellung: **Debuggen**

Erforderlich zum Debuggen und Anpassen des Arbeitsspeichers eines Prozesses, der sich im Besitz eines anderen Kontos befindet.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeAudit"></span><span id="wbemprivilegeaudit"></span><span id="WBEMPRIVILEGEAUDIT"></span>**wbemPrivilegeAudit**
</dt> <dd> <dl> <dt>

20 (0x14)
</dt> <dt>



C++-Konstante: **SE \_ AUDIT \_ NAME-Zeichenfolge:** **SeAuditPrivilege**

Kurzname der Skripterstellung: **Überwachung**

Erforderlich, um Überwachungseinträge im NT-Sicherheitsprotokoll zu generieren. Nur sichere Server sollten über diese Berechtigung verfügen.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemEnvironment"></span><span id="wbemprivilegesystemenvironment"></span><span id="WBEMPRIVILEGESYSTEMENVIRONMENT"></span>**wbemPrivilegeSystemEnvironment**
</dt> <dd> <dl> <dt>

21 (0x15)
</dt> <dt>



C++-Konstante: **SE \_ SYSTEM ENVIRONMENT \_ \_ NAME-Zeichenfolge:** **SeSystemEnvironmentPrivilege**

Kurzname der Skripterstellung: **SystemUmgebung**

Erforderlich, um den nicht flüchtigen RAM von Systemen zu ändern, die diesen Speichertyp zum Speichern von Konfigurationsdaten verwenden.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeChangeNotify"></span><span id="wbemprivilegechangenotify"></span><span id="WBEMPRIVILEGECHANGENOTIFY"></span>**wbemPrivilegeChangeNotify**
</dt> <dd> <dl> <dt>

22 (0x16)
</dt> <dt>



C++-Konstante: **SE \_ CHANGE NOTIFY \_ \_ NAME** Zeichenfolge: **SeChangeNotifyPrivilege**

Kurzname der Skripterstellung: **ChangeNotify**

Erforderlich, um Benachrichtigungen über Änderungen an Dateien oder Verzeichnissen zu empfangen und Überprüfungen des Durchlaufzugriffs zu umgehen. Diese Berechtigung ist standardmäßig für alle Benutzer aktiviert.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeRemoteShutdown"></span><span id="wbemprivilegeremoteshutdown"></span><span id="WBEMPRIVILEGEREMOTESHUTDOWN"></span>**wbemPrivilegeRemoteShutdown**
</dt> <dd> <dl> <dt>

23 (0x17)
</dt> <dt>



C++-Konstante: **SE ZEICHENFOLGE REMOTE SHUTDOWN \_ \_ \_ NAME:** **SeRemoteShutdownPrivilege**

Kurzname der Skripterstellung: **RemoteShutdown**

Erforderlich, um einen Remotecomputer herunterzufahren.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeUndock"></span><span id="wbemprivilegeundock"></span><span id="WBEMPRIVILEGEUNDOCK"></span>**wbemPrivilegeUndock**
</dt> <dd> <dl> <dt>

24 (0x18)
</dt> <dt>



C++-Konstante: **SE \_ UNDOCK \_ NAME-Zeichenfolge:** **SeUndockPrivilege**

Kurzname der Skripterstellung: **Abdocken**

Erforderlich, um einen Laptop von einer Dockingstation zu entfernen.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSyncAgent"></span><span id="wbemprivilegesyncagent"></span><span id="WBEMPRIVILEGESYNCAGENT"></span>**wbemPrivilegeSyncAgent**
</dt> <dd> <dl> <dt>

25 (0x19)
</dt> <dt>



C++-Konstante: **SE \_ SYNC AGENT \_ \_ NAME-Zeichenfolge:** **SeSyncAgentPrivilege**

Kurzname der Skripterstellung: **SyncAgent**

Erforderlich zum Synchronisieren von Verzeichnisdienstdaten.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeEnableDelegation"></span><span id="wbemprivilegeenabledelegation"></span><span id="WBEMPRIVILEGEENABLEDELEGATION"></span>**wbemPrivilegeEnableDelegation**
</dt> <dd> <dl> <dt>

26 (0x1A)
</dt> <dt>



C++-Konstante: **SE \_ ENABLE DELEGATION \_ \_ NAME** Zeichenfolge: **SeEnableDelegationPrivilege**

Kurzname der Skripterstellung: **EnableDelegation**

Erforderlich, damit Computer- und Benutzerkonten für die Delegierung als vertrauenswürdig eingestuft werden können.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeManageVolume"></span><span id="wbemprivilegemanagevolume"></span><span id="WBEMPRIVILEGEMANAGEVOLUME"></span>**wbemPrivilegeManageVolume**
</dt> <dd> <dl> <dt>

27 (0x1B)
</dt> <dt>



C++-Konstante: **SE \_ MANAGE VOLUME \_ \_ NAME-Zeichenfolge:** **SeManageVolumePrivilege**

Kurzname der Skripterstellung: **ManageVolume**

Erforderlich zum Ausführen von Volumewartungsaufgaben.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wbemdisp.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Skripterstellungs-API-Konstanten](scripting-api-constants.md)
</dt> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[Ausführen privilegierter Vorgänge](executing-privileged-operations.md)
</dt> <dt>

[Ausführen privilegierter Vorgänge mit VBScript](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

