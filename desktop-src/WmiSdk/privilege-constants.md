---
description: Der strprivilege-Parameter der Methode "slibemprivilegeset. addasstring" und der Parameter "iprivilege" für "slibemprivilegeset. Add" erfordern Berechtigungs Zeichenfolgen aus "wbemprivilegeenum".
ms.assetid: f9400597-81bb-44a8-80dc-aba0160aea26
ms.tgt_platform: multiple
title: Berechtigungs Konstanten (wbemdisp. h)
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
ms.openlocfilehash: 73fb9167af63f40f3a6e1c00470d871f749d228a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759768"
---
# <a name="privilege-constants"></a>Berechtigungs Konstanten

Der *strprivilege* -Parameter der Methode " [**slibemprivilegeset. addasstring**](swbemprivilegeset-addasstring.md) " und der Parameter " *iprivilege* " für " [**slibemprivilegeset. Add**](swbemprivilegeset-add.md) " erfordern Berechtigungs Zeichenfolgen aus " [wbemprivilegeenum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)". Weitere Informationen zum Verwenden von Berechtigungs Konstanten finden Sie unter [Ausführen privilegierter Vorgänge](executing-privileged-operations.md).

Die folgenden Konstanten sind in [**wbemprivilegeenumeration**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)definiert. Die folgende Liste enthält die äquivalenten Konstanten für C++ und Zeichen folgen für die Skripterstellung. Um den Namen der Skripterstellung zu bilden, entfernen Sie "SE" und "Privilege" aus dem C++-Konstantennamen.

Im folgenden VBScript-Codebeispiel wird gezeigt, wie die RemoteShutdown-Berechtigung in einem Skript aktiviert wird.


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (RemoteShutdown)}")
```



Viele WMI-Methoden erfordern, dass mindestens eine Berechtigung aktiviert ist. Wenn einem Konto keine Berechtigung erteilt wurde, kann es für den Methoden Aufrufvorgang nicht aktiviert werden.

<dl> <dt>

<span id="wbemPrivilegeCreateToken"></span><span id="wbemprivilegecreatetoken"></span><span id="WBEMPRIVILEGECREATETOKEN"></span>**wbemprivilegekreatetoken**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



C++ Constant: **SE \_ Create \_ Token \_ Name** String: **secreatetokenprivilege**

Name der Skripterstellung **: "** ".

Erforderlich, um ein primäres Tokenobjekt zu erstellen.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegePrimaryToken"></span><span id="wbemprivilegeprimarytoken"></span><span id="WBEMPRIVILEGEPRIMARYTOKEN"></span>**wbemprivilegeprimarytoken**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



C++-Konstante: **seassignprimaryaufkenprivilege** -Zeichenfolge: **seassignprimaryanmelkenprivilege**

Name der Skripterstellung: **zugriffprimarytoken**

Ist erforderlich, um ein Token auf Prozessebene zu ersetzen.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeLockMemory"></span><span id="wbemprivilegelockmemory"></span><span id="WBEMPRIVILEGELOCKMEMORY"></span>**wbemprivilegelockmemory**
</dt> <dd> <dl> <dt>

3 (0x3)
</dt> <dt>



C++-Konstante: Zeichenfolge für den **\_ \_ Speicher \_ Namen der SE-Sperre** : **SeLockMemoryPrivilege**

Kurzname für Skripterstellung: **lockmemory**

Zum Sperren von Seiten im Arbeitsspeicher erforderlich.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeIncreaseQuota"></span><span id="wbemprivilegeincreasequota"></span><span id="WBEMPRIVILEGEINCREASEQUOTA"></span>**wbemprivilegilegeingekreasequota**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



C++-Konstante: **SE \_ Erhöhung des \_ Kontingent \_ namens** String: **seinkreasequotaprivilege**

Kurzname für Skripterstellung: Erstellungs **Berechtigung**

Erforderlich zum Anpassen von Speicher Kontingenten für einen Prozess.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeMachineAccount"></span><span id="wbemprivilegemachineaccount"></span><span id="WBEMPRIVILEGEMACHINEACCOUNT"></span>**wbemprivilegemachineaccount**
</dt> <dd> <dl> <dt>

5 (0x5)
</dt> <dt>



C++-Konstante: **SE \_ Macine \_ Account \_ Name** String: **tarmachineaccountprivilege**

Kurzname für Skripterstellung: **MachineAccount**

Erforderlich zum Hinzufügen von Arbeitsstationen zu einer Domäne.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeTcb"></span><span id="wbemprivilegetcb"></span><span id="WBEMPRIVILEGETCB"></span>**wbemprivilegetcb**
</dt> <dd> <dl> <dt>

6 (0x6)
</dt> <dt>



C++-Konstante: **SE \_ TCB \_ Name** String: **SeTcbPrivilege**

Kurzname für Skripterstellung: **TCB**

Erforderlich, um als Teil des Betriebssystems zu agieren. Der Inhaber ist Teil der vertrauenswürdigen Computer Basis.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSecurity"></span><span id="wbemprivilegesecurity"></span><span id="WBEMPRIVILEGESECURITY"></span>**wbemprivilegeseatur**
</dt> <dd> <dl> <dt>

7 (0x7)
</dt> <dt>



C++-Konstante: **SE- \_ Sicherheits \_ Namen** Zeichenfolge: **SeSecurityPrivilege**

Skript Kurzname: **Sicherheit**

Erforderlich zum Verwalten der Überwachung und des NT-Sicherheitsprotokolls.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeTakeOwnership"></span><span id="wbemprivilegetakeownership"></span><span id="WBEMPRIVILEGETAKEOWNERSHIP"></span>**wbemprivilegetakeownership**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



C++-Konstante **: \_ SE \_ Besitz \_ Name** Zeichenfolge **: "** "

Kurzname der Skripterstellung: **Take Ownership**

Erforderlich, um den Besitz von Dateien oder anderen Objekten ohne einen [*Access Control Eintrag*](/windows/desktop/SecGloss/a-gly) (ACE) in der *Zugriffs Steuerungs Liste* (DACL) zu übernehmen.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeLoadDriver"></span><span id="wbemprivilegeloaddriver"></span><span id="WBEMPRIVILEGELOADDRIVER"></span>**wbemprivilegeloaddriver**
</dt> <dd> <dl> <dt>

9 (0x9)
</dt> <dt>



C++-Konstante **: \_ \_ Treiber** Zeichenfolge für "SE laden": **SeLoadDriverPrivilege**

Kurzname für Skripterstellung: **LoadDriver**

Erforderlich zum Laden oder Entladen eines Gerätetreibers.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemProfile"></span><span id="wbemprivilegesystemprofile"></span><span id="WBEMPRIVILEGESYSTEMPROFILE"></span>**wbemprivilegesystemprofile**
</dt> <dd> <dl> <dt>

10 (0xa)
</dt> <dt>



C++-Konstante: Name der namens Zeichenfolge für das **\_ System \_ Profil \_** : **sesystemprofileprivilege**

Kurzname für Skripterstellung: **Systemprofile**

Erforderlich, um Profilinformationen zur Systemleistung zu erfassen.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemtime"></span><span id="wbemprivilegesystemtime"></span><span id="WBEMPRIVILEGESYSTEMTIME"></span>**wbemprivilegesystemtime**
</dt> <dd> <dl> <dt>

11 (0xB)
</dt> <dt>



C++-Konstante: **SE \_ SYSTEMTIME**- \_ namens Zeichenfolge: **SeSystemtimePrivilege**

Kurzname für Skripterstellung: **SYSTEMTIME**

Erforderlich, um die Systemzeit zu ändern.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeProfileSingleProcess"></span><span id="wbemprivilegeprofilesingleprocess"></span><span id="WBEMPRIVILEGEPROFILESINGLEPROCESS"></span>**wbemprivilegeprofilesingleprocess**
</dt> <dd> <dl> <dt>

12 (0xc)
</dt> <dt>



C++-Konstante: **SE \_ Prof \_ Single \_ Process \_ Name** String: **sprofilesingleprocessprivilege**

Skript Kurzname: **profilesingleprocess**

Erforderlich, um Profilinformationen für einen einzelnen Prozess zu erfassen.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeIncreaseBasePriority"></span><span id="wbemprivilegeincreasebasepriority"></span><span id="WBEMPRIVILEGEINCREASEBASEPRIORITY"></span>**wbemprivilegilegeingekreasebasepriority**
</dt> <dd> <dl> <dt>

13 (0xD)
</dt> <dt>



C++ Constant: **SE \_ Inc \_ \_ \_ Name der Basis Priorität** Zeichenfolge: **seinkreasebasepriorityprivilege**

Name der Skripterstellung: **erstellebasepriority**

Erforderlich, um die Planungs Priorität zu erhöhen.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeCreatePagefile"></span><span id="wbemprivilegecreatepagefile"></span><span id="WBEMPRIVILEGECREATEPAGEFILE"></span>**wbemprivilegekreatepagefile**
</dt> <dd> <dl> <dt>

14 (0xe)
</dt> <dt>



C++-Konstante: **SE \_ Create \_ Pagefile \_ Name** String: **secreatepagefileprivilege**

Kurzname für Skript **Erstellung: "** ".

Erforderlich zum Erstellen einer Pagefile-Datei.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeCreatePermanent"></span><span id="wbemprivilegecreatepermanent"></span><span id="WBEMPRIVILEGECREATEPERMANENT"></span>**wbemprivilegekreatepermanent**
</dt> <dd> <dl> <dt>

15 (0xF)
</dt> <dt>



C++-Konstante: **SE \_ Create \_ permanent \_ Name** String: **SeCreatePermanentPrivilege**

Kurzname für Skripterstellung: " **kreatepermanent** "

Erforderlich, um permanente freigegebene Objekte zu erstellen.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeBackup"></span><span id="wbemprivilegebackup"></span><span id="WBEMPRIVILEGEBACKUP"></span>**wbemprivilegebackup**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



C++-Konstante: **SE \_ Backup \_ Name** String: " **sbackupprivilege** "

Kurzname für Skripterstellung: **Sicherung**

Zum Sichern von Dateien und Verzeichnissen erforderlich, unabhängig von der für die Datei angegebenen ACL.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeRestore"></span><span id="wbemprivilegerestore"></span><span id="WBEMPRIVILEGERESTORE"></span>**wbemprivilegerestore**
</dt> <dd> <dl> <dt>

17 (0x11)
</dt> <dt>



C++ Constant: **SE \_ Restore \_ Name** String: **SeRestorePrivilege**

Skript Kurzname: **Restore**

Ist erforderlich, um Dateien und Verzeichnisse unabhängig von der für die Datei angegebenen ACL wiederherzustellen.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeShutdown"></span><span id="wbemprivilegeshutdown"></span><span id="WBEMPRIVILEGESHUTDOWN"></span>**wbemprivilegeshutdown**
</dt> <dd> <dl> <dt>

18 (0x12)
</dt> <dt>



C++-Konstante: **SE \_ Shutdown \_ Name** String: **SeShutdownPrivilege**

Kurzname für Skripterstellung: **herunter** fahren

Erforderlich, um das lokale System herunterzufahren.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeDebug"></span><span id="wbemprivilegedebug"></span><span id="WBEMPRIVILEGEDEBUG"></span>**wbemprivilegedebug**
</dt> <dd> <dl> <dt>

19 (0x13)
</dt> <dt>



C++-Konstante: **SE \_ Debug \_ Name** String: " **sdebugprivilege** "

Kurzname für Skripterstellung: **Debug**

Erforderlich, um den Arbeitsspeicher eines Prozesses zu Debuggen und anzupassen, der im Besitz eines anderen Kontos ist


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeAudit"></span><span id="wbemprivilegeaudit"></span><span id="WBEMPRIVILEGEAUDIT"></span>**wbemprivilegeaudit**
</dt> <dd> <dl> <dt>

20 (0x14)
</dt> <dt>



C++-Konstante: SE-Überwachungs **\_ \_ Name** Zeichen **Folge: "** ".

Kurzname für Skripterstellung: **Audit**

Erforderlich, um Überwachungs Einträge im NT-Sicherheitsprotokoll zu generieren. Nur sichere Server sollten über dieses Privileg verfügen.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemEnvironment"></span><span id="wbemprivilegesystemenvironment"></span><span id="WBEMPRIVILEGESYSTEMENVIRONMENT"></span>**wbemprivilegesystemenvironment**
</dt> <dd> <dl> <dt>

21 (0x15)
</dt> <dt>



C++-Konstante: namens Zeichenfolge für die **SE- \_ System Umgebung: \_ \_** **sesystemenvironment Privilege**

Kurzname für Skripterstellung: **systemenvironment**

Erforderlich, um das nicht flüchtige RAM von Systemen zu ändern, die diese Art von Arbeitsspeicher zum Speichern von Konfigurationsdaten verwenden.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeChangeNotify"></span><span id="wbemprivilegechangenotify"></span><span id="WBEMPRIVILEGECHANGENOTIFY"></span>**wbemprivilegechangenotifizieren**
</dt> <dd> <dl> <dt>

22 (0x16)
</dt> <dt>



C++-Konstante: **SE- \_ Änderungs \_ \_ Name** Zeichenfolge: " **abchangenotifyprivilege** "

Kurzname für Skripterstellung: **changenotifizieren**

Ist erforderlich, um Benachrichtigungen über Änderungen an Dateien oder Verzeichnissen zu empfangen und durchgängige Zugriffs Überprüfungen zu umgehen. Dieses Privileg ist standardmäßig für alle Benutzer aktiviert.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeRemoteShutdown"></span><span id="wbemprivilegeremoteshutdown"></span><span id="WBEMPRIVILEGEREMOTESHUTDOWN"></span>**wbemprivilegeremuteshutdown**
</dt> <dd> <dl> <dt>

23 (0x17)
</dt> <dt>



C++-Konstante: **SE \_ Remote \_ Shutdown \_ Name** String: **SeRemoteShutdownPrivilege**

Kurzname für Skripterstellung: **RemoteShutdown**

Zum Herunterfahren eines Remote Computers erforderlich.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeUndock"></span><span id="wbemprivilegeundock"></span><span id="WBEMPRIVILEGEUNDOCK"></span>**wbemprivilegeundock**
</dt> <dd> <dl> <dt>

24 (0x18)
</dt> <dt>



C++-Konstante: **SE \_ Undock- \_ namens** Zeichenfolge: " **sundockprivilege** "

Skript Kurzname: **Abdocken**

Ist erforderlich, um einen Laptop von einer Docking Station zu entfernen.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSyncAgent"></span><span id="wbemprivilegesyncagent"></span><span id="WBEMPRIVILEGESYNCAGENT"></span>**wbemprivilegesyncagent**
</dt> <dd> <dl> <dt>

25 (0x19)
</dt> <dt>



C++-Konstante: Name Zeichenfolge für den **SE \_ Sync- \_ Agent \_** : **sesyncagentprivilege**

Kurzname für Skripterstellung: **SyncAgent**

Erforderlich zum Synchronisieren von Verzeichnisdienst Daten.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeEnableDelegation"></span><span id="wbemprivilegeenabledelegation"></span><span id="WBEMPRIVILEGEENABLEDELEGATION"></span>**wbemprivilegeenabledelegation**
</dt> <dd> <dl> <dt>

26 (0x1A)
</dt> <dt>



C++-Konstante: **SE \_ Aktivieren der \_ Delegierungs \_ namens** Zeichenfolge: **seenabledelegationprivilege**

Skript Kurzname: **enabledelegation**

Erforderlich, damit Computer-und Benutzerkonten für die Delegierung vertrauenswürdig sind.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeManageVolume"></span><span id="wbemprivilegemanagevolume"></span><span id="WBEMPRIVILEGEMANAGEVOLUME"></span>**wbemprivilegemanagevolume**
</dt> <dd> <dl> <dt>

27 (0x1B)
</dt> <dt>



C++-Konstante: **SE \_ Manage \_ Volume \_ Name** String: " **smanagevolumeprivilege** "

Skript Kurzname: **managevolume**

Erforderlich zum Ausführen von Volumewartungsaufgaben.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wbemdisp. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Skript-API-Konstanten](scripting-api-constants.md)
</dt> <dt>

[**Austausch Sicherheit**](swbemsecurity.md)
</dt> <dt>

[**Wbemprivilegeumum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[Ausführen privilegierter Vorgänge](executing-privileged-operations.md)
</dt> <dt>

[Ausführen privilegierter Vorgänge mit VBScript](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

