---
description: Beschreibt die Anmeldesitzung oder -sitzungen, die einem Benutzer zugeordnet sind, der bei einem Computersystem angemeldet ist, auf dem Windows.
ms.assetid: d09a115b-95a3-47c7-a04d-c810d044ccc8
ms.tgt_platform: multiple
title: Win32_LogonSession-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogonSession
- Win32_LogonSession.Caption
- Win32_LogonSession.Description
- Win32_LogonSession.InstallDate
- Win32_LogonSession.Name
- Win32_LogonSession.Status
- Win32_LogonSession.StartTime
- Win32_LogonSession.AuthenticationPackage
- Win32_LogonSession.LogonId
- Win32_LogonSession.LogonType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 85cbc80050fafe887fa99974c41666c7189b2b12c21559aac0255870b2a697d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972982"
---
# <a name="win32_logonsession-class"></a>Win32 \_ LogonSession-Klasse

Die WMI-Klasse **Win32 \_ LogonSession** (siehe Abrufen einer [WMI-Klasse)](/windows/desktop/wmisdk/retrieving-a-class)beschreibt die Anmeldesitzung oder -sitzungen, die einem Benutzer zugeordnet sind, der bei einem Computersystem angemeldet ist, auf dem Windows.

Die folgende Syntax wird durch Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{9083C21E-7D58-4e0e-BC30-0BC8922AFB8B}"), AMENDMENT]
class Win32_LogonSession : Win32_Session
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime StartTime;
  string   AuthenticationPackage;
  string   LogonId;
  uint32   LogonType;
};
```

## <a name="members"></a>Member

Die **Win32 \_ LogonSession-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ LogonSession-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AuthenticationPackage**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Name des Subsystems, das zum Authentifizieren der Anmeldesitzung verwendet wird.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Eine kurze Textbeschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Eine Textbeschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Installation date")
</dt> </dl>

Gibt an, wann das Objekt installiert wurde. Das Fehlen eines Werts gibt nicht an, dass das Objekt nicht installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**LogonId**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

ID, die der Anmeldesitzung zugewiesen ist.

</dd> <dt>

**LogonType**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Numerischer Wert, der den Typ der Anmeldesitzung angibt.

<dt>

0
</dt> <dd>

Wird nur vom Systemkonto verwendet.

</dd> <dt>

<span id="Interactive"></span><span id="interactive"></span><span id="INTERACTIVE"></span>

<span id="Interactive"></span><span id="interactive"></span><span id="INTERACTIVE"></span>**Interaktiv** (2)


</dt> <dd>

Vorgesehen für Benutzer, die den Computer interaktiv verwenden, z. B. ein Benutzer, der von einem Terminalserver, einer Remoteshell oder einem ähnlichen Prozess angemeldet wird.

</dd> <dt>

<span id="Network"></span><span id="network"></span><span id="NETWORK"></span>

<span id="Network"></span><span id="network"></span><span id="NETWORK"></span>**Netzwerk** (3)


</dt> <dd>

Vorgesehen für Hochleistungsserver zum Authentifizieren von Klartextkennwörtern. LogonUser speichert anmeldeinformationen für diesen Anmeldetyp nicht zwischen.

</dd> <dt>

<span id="Batch"></span><span id="batch"></span><span id="BATCH"></span>

<span id="Batch"></span><span id="batch"></span><span id="BATCH"></span>**Batch** (4)


</dt> <dd>

Für Batchserver vorgesehen, bei denen Prozesse ohne direkten Eingriff im Auftrag eines Benutzers ausgeführt werden können. oder für Server mit höherer Leistung, die viele Klartextauthentifizierungsversuche gleichzeitig verarbeiten, z. B. E-Mail- oder Webserver. LogonUser speichert anmeldeinformationen für diesen Anmeldetyp nicht zwischen.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Dienst** (5)


</dt> <dd>

Gibt eine Diensttypanmeldung an. Für das bereitgestellte Konto muss die Dienstberechtigung aktiviert sein.

</dd> <dt>

<span id="Proxy"></span><span id="proxy"></span><span id="PROXY"></span>

<span id="Proxy"></span><span id="proxy"></span><span id="PROXY"></span>**Proxy** (6)


</dt> <dd>

Gibt eine Anmeldung vom Proxytyp an.

</dd> <dt>

<span id="Unlock"></span><span id="unlock"></span><span id="UNLOCK"></span>

<span id="Unlock"></span><span id="unlock"></span><span id="UNLOCK"></span>**Entsperren** (7)


</dt> <dd>

Dieser Anmeldetyp ist für die Protokollierung von GINA-DLLs für Benutzer vorgesehen, die den Computer interaktiv verwenden. Mit diesem Anmeldetyp kann ein eindeutiger Überwachungsdatensatz generiert werden, der zeigt, wann die Arbeitsstation entsperrt wurde.

</dd> <dt>

<span id="NetworkCleartext"></span><span id="networkcleartext"></span><span id="NETWORKCLEARTEXT"></span>

<span id="NetworkCleartext"></span><span id="networkcleartext"></span><span id="NETWORKCLEARTEXT"></span>**NetworkCleartext** (8)


</dt> <dd>

Behält den Namen und das Kennwort in den Authentifizierungspaketen bei, sodass der Server verbindungen mit anderen Netzwerkservern herstellen kann, während die Identität des Clients angenommen wird. Dadurch kann ein Server Klartextanmeldeinformationen von einem Client akzeptieren, LogonUser aufrufen, überprüfen, ob der Benutzer über das Netzwerk auf das System zugreifen und weiterhin mit anderen Servern kommunizieren kann.

</dd> <dt>

<span id="NewCredentials"></span><span id="newcredentials"></span><span id="NEWCREDENTIALS"></span>

<span id="NewCredentials"></span><span id="newcredentials"></span><span id="NEWCREDENTIALS"></span>**NewCredentials** (9)


</dt> <dd>

Ermöglicht dem Aufrufer, sein aktuelles Token zu klonen und neue Anmeldeinformationen für ausgehende Verbindungen anzugeben. Die neue Anmeldesitzung verfügt über die gleiche lokale Identifizierung, verwendet jedoch unterschiedliche Anmeldeinformationen für andere Netzwerkverbindungen.

</dd> <dt>

<span id="RemoteInteractive"></span><span id="remoteinteractive"></span><span id="REMOTEINTERACTIVE"></span>

<span id="RemoteInteractive"></span><span id="remoteinteractive"></span><span id="REMOTEINTERACTIVE"></span>**RemoteInteractive** (10)


</dt> <dd>

Terminaldienstesitzung, die sowohl remote als auch interaktiv ist.

</dd> <dt>

<span id="CachedInteractive"></span><span id="cachedinteractive"></span><span id="CACHEDINTERACTIVE"></span>

<span id="CachedInteractive"></span><span id="cachedinteractive"></span><span id="CACHEDINTERACTIVE"></span>**CachedInteractive** (11)


</dt> <dd>

Versuchen Sie, zwischengespeicherte Anmeldeinformationen ohne Zugriff auf das Netzwerk zu verwenden.

</dd> <dt>

<span id="CachedRemoteInteractive"></span><span id="cachedremoteinteractive"></span><span id="CACHEDREMOTEINTERACTIVE"></span>

<span id="CachedRemoteInteractive"></span><span id="cachedremoteinteractive"></span><span id="CACHEDREMOTEINTERACTIVE"></span>**CachedRemoteInteractive** (12)


</dt> <dd>

Identisch mit RemoteInteractive. Dies wird für die interne Überwachung verwendet.

</dd> <dt>

<span id="CachedUnlock"></span><span id="cachedunlock"></span><span id="CACHEDUNLOCK"></span>

<span id="CachedUnlock"></span><span id="cachedunlock"></span><span id="CACHEDUNLOCK"></span>**CachedUnlock** (13)


</dt> <dd>

Anmeldung auf der Arbeitsstation.

</dd> </dl>

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Bezeichnung, unter der das Objekt bekannt ist. Bei Unterklassen kann diese Eigenschaft überschrieben werden, um eine Schlüsseleigenschaft zu sein.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeitpunkt, zu dem die Sitzung gestartet wurde.

Diese Eigenschaft wird von [**Win32 \_ Session geerbt.**](win32-session.md)

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Eine Zeichenfolge, die den aktuellen Status des Objekts angibt. Betriebsstatus und nicht betriebsbereiter Status können definiert werden. Der Betriebsstatus kann "OK", "Heruntergestuft" und "Fehler vor dem Ausfall" enthalten. "Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. B. eine SMART-fähige Festplatte).

Nicht betriebsbereite Status können "Error", "Starting", "Stopping" und "Service" sein. "Dienst" kann während der Spiegelung des Datenträgers, beim erneuten Laden einer Benutzerberechtigungsliste oder bei anderen administrativen Aufgaben angewendet werden. Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

Folgende Werte sind gültig:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Fehler** ("Fehler")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Heruntergestuft** ("Heruntergestuft")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** ("Unbekannt")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred Fail** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Wird** gestartet ("Wird gestartet")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Wird beendet** ("Wird beendet")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Dienst** ("Dienst")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Striche** ("Strich")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Kein Kontakt** ("Kein Kontakt")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Lost Comm** ("Lost Comm")


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="examples"></a>Beispiele

Das [PowerShell-Beispiel](https://Gallery.TechNet.Microsoft.Com/scriptcenter/64cc7ab5-f1cd-460c-9d37-e6f989444de3) Zum Auflisten von Anmeldesitzungsinformationen gibt Informationen zu Anmeldesitzungen zurück, die dem aktuell bei einem Computer angemeldeten Benutzer zugeordnet sind.

Im folgenden PowerShell-Beispiel wird überprüft, ob die Remotesitzung für einen angegebenen Benutzer geöffnet ist.


```PowerShell
$user = "<user name>"
$servers = gci servers.txt 

     foreach ($server in $servers){
     $logons = gwmi win32_loggedonuser -computername $server

          foreach ($logon in $logons){
               if ($logon.antecedent -match $user){
               $logonid = $logon.dependent.split("=")[1] 
               $session =gwmi win32_logonsession |? {$_.logonid -match $logonid}
               if ($session.logontype -eq "10"){
               Write-host "You have an active Terminal Server session on server $($server)"
                }
          }
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32-Sitzung \_**](win32-session.md)
</dt> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

