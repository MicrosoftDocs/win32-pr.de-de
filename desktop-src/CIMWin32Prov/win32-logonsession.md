---
description: Beschreibt die Anmelde Sitzung oder Sitzungen, die einem Benutzer zugeordnet sind, der bei einem Computersystem mit Windows angemeldet ist.
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
ms.openlocfilehash: 78e14bbd41c2fd8bb0c10a7bfeeda0dc9d426b0f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747984"
---
# <a name="win32_logonsession-class"></a>Win32 \_ logonsession-Klasse

Die WMI-Klasse der **Win32- \_ logonsession** (siehe [Abrufen einer WMI-Klasse](/windows/desktop/wmisdk/retrieving-a-class)) beschreibt die Anmelde Sitzung oder die Sitzungen, die einem Benutzer zugeordnet sind, der bei einem Computersystem mit Windows angemeldet ist.

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

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

Die **Win32 \_ logonsession** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ logonsession** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**AuthenticationPackage**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Subsystems, das zum Authentifizieren der Anmelde Sitzung verwendet wird.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Eine kurze Textbeschreibung des-Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Eine Textbeschreibung des-Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")
</dt> </dl>

Gibt an, wann das Objekt installiert wurde. Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Anmelde-ID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Die der Anmelde Sitzung zugewiesene ID.

</dd> <dt>

**LogonType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Numerischer Wert, der den Typ der Anmelde Sitzung angibt.

<dt>

0
</dt> <dd>

Wird nur vom System Konto verwendet.

</dd> <dt>

<span id="Interactive"></span><span id="interactive"></span><span id="INTERACTIVE"></span>

<span id="Interactive"></span><span id="interactive"></span><span id="INTERACTIVE"></span>**Interaktiv** (2)


</dt> <dd>

Gedacht für Benutzer, die den Computer interaktiv verwenden, z. b. ein Benutzer, der von einem Terminal Server, einer Remoteshell oder einem ähnlichen Prozess angemeldet ist.

</dd> <dt>

<span id="Network"></span><span id="network"></span><span id="NETWORK"></span>

<span id="Network"></span><span id="network"></span><span id="NETWORK"></span>**Netzwerk** (3)


</dt> <dd>

Ist für Hochleistungsserver zum Authentifizieren von Klartext-Kenn Wörtern vorgesehen. LogonUser speichert die Anmelde Informationen für diesen Anmeldetyp nicht zwischen.

</dd> <dt>

<span id="Batch"></span><span id="batch"></span><span id="BATCH"></span>

<span id="Batch"></span><span id="batch"></span><span id="BATCH"></span>**Batch** (4)


</dt> <dd>

Gedacht für Batch Server, bei denen Prozesse im Auftrag eines Benutzers ohne direkten Eingriff ausgeführt werden können. oder für Server mit höherer Leistung, die viele Clear-Text-Authentifizierungs Versuche gleichzeitig verarbeiten, z. b. e-Mail-oder Webserver. LogonUser speichert die Anmelde Informationen für diesen Anmeldetyp nicht zwischen.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Dienst** (5)


</dt> <dd>

Gibt die Anmeldung eines Dienst Typs an. Für das angegebene Konto muss die Dienst Berechtigung aktiviert sein.

</dd> <dt>

<span id="Proxy"></span><span id="proxy"></span><span id="PROXY"></span>

<span id="Proxy"></span><span id="proxy"></span><span id="PROXY"></span>**Proxy** (6)


</dt> <dd>

Gibt eine Proxy-Typ-Anmeldung an.

</dd> <dt>

<span id="Unlock"></span><span id="unlock"></span><span id="UNLOCK"></span>

<span id="Unlock"></span><span id="unlock"></span><span id="UNLOCK"></span>**Entsperren** (7)


</dt> <dd>

Dieser Anmeldetyp ist für die Gina-DLLs-Protokollierung bei Benutzern vorgesehen, die den Computer interaktiv verwenden. Dieser Anmeldetyp ermöglicht das Generieren eines eindeutigen Überwachungsdaten Satzes, der anzeigt, wann die Arbeitsstation entsperrt wurde.

</dd> <dt>

<span id="NetworkCleartext"></span><span id="networkcleartext"></span><span id="NETWORKCLEARTEXT"></span>

<span id="NetworkCleartext"></span><span id="networkcleartext"></span><span id="NETWORKCLEARTEXT"></span>**Network cleartext** (8)


</dt> <dd>

Behält den Namen und das Kennwort in den Authentifizierungs Paketen bei und ermöglicht dem Server das Herstellen von Verbindungen mit anderen Netzwerkservern, während die Identität des Clients angenommen wird. Dadurch kann ein Server Klartext-Anmelde Informationen von einem Client akzeptieren, LogonUser aufrufen, überprüfen, ob der Benutzer über das Netzwerk auf das System zugreifen kann und trotzdem mit anderen Servern kommunizieren kann.

</dd> <dt>

<span id="NewCredentials"></span><span id="newcredentials"></span><span id="NEWCREDENTIALS"></span>

<span id="NewCredentials"></span><span id="newcredentials"></span><span id="NEWCREDENTIALS"></span>**Neuanmelde** Informationen (9)


</dt> <dd>

Ermöglicht dem Aufrufer das Klonen seines aktuellen Tokens und das Angeben neuer Anmelde Informationen für ausgehende Verbindungen. Die neue Anmelde Sitzung hat dieselbe lokale Identifizierung, verwendet jedoch andere Anmelde Informationen für andere Netzwerkverbindungen.

</dd> <dt>

<span id="RemoteInteractive"></span><span id="remoteinteractive"></span><span id="REMOTEINTERACTIVE"></span>

<span id="RemoteInteractive"></span><span id="remoteinteractive"></span><span id="REMOTEINTERACTIVE"></span>**Remoteinteractive** (10)


</dt> <dd>

Terminal Dienste-Sitzung, die sowohl Remote als auch interaktiv ist.

</dd> <dt>

<span id="CachedInteractive"></span><span id="cachedinteractive"></span><span id="CACHEDINTERACTIVE"></span>

<span id="CachedInteractive"></span><span id="cachedinteractive"></span><span id="CACHEDINTERACTIVE"></span>**Cachedinteractive** (11)


</dt> <dd>

Versuchen Sie zwischengespeicherte Anmelde Informationen ohne Zugriff auf das Netzwerk.

</dd> <dt>

<span id="CachedRemoteInteractive"></span><span id="cachedremoteinteractive"></span><span id="CACHEDREMOTEINTERACTIVE"></span>

<span id="CachedRemoteInteractive"></span><span id="cachedremoteinteractive"></span><span id="CACHEDREMOTEINTERACTIVE"></span>**Cachedremuteinteractive** (12)


</dt> <dd>

Identisch mit remoteinteractive. Diese wird für die interne Überwachung verwendet.

</dd> <dt>

<span id="CachedUnlock"></span><span id="cachedunlock"></span><span id="CACHEDUNLOCK"></span>

<span id="CachedUnlock"></span><span id="cachedunlock"></span><span id="CACHEDUNLOCK"></span>**Cachedunlock** (13)


</dt> <dd>

Arbeitsstations Anmeldung.

</dd> </dl>

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Die Bezeichnung, nach der das-Objekt bekannt ist. Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Zeitpunkt, zu dem die Sitzung gestartet wurde.

Diese Eigenschaft wird von der [**Win32- \_ Sitzung**](win32-session.md)geerbt.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Eine Zeichenfolge, die den aktuellen Status des Objekts angibt. Der Betriebsstatus und der nicht betriebliche Status können definiert werden. Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten. "Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).

Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten. "Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird. Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

Folgende Werte sind gültig:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Fehler** ("Fehler")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

Herunter **gestuft ("** heruntergestuft")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** ("unbekannt")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred-** Fehler ("pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

Wird **gestartet** ("wird gestartet")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

Wird **beendet ("wird angehalten** ")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Dienst** ("Dienst")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Betont** ("gestresst")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Nicht wiederherstellen** ("nicht wiederherstellen")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Kein Kontakt** ("kein Kontakt")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Verlorene** Kommunikations ("verlorene Kommunikations-")


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="examples"></a>Beispiele

Das PowerShell-Beispiel " [Auflisten von Anmelde Informationen](https://Gallery.TechNet.Microsoft.Com/scriptcenter/64cc7ab5-f1cd-460c-9d37-e6f989444de3) " gibt Informationen zu Anmelde Sitzungen zurück, die dem aktuell auf einem Computer angemeldeten Benutzer zugeordnet sind.

Das folgende PowerShell-Beispiel prüft, ob eine Remote Sitzung für einen angegebenen Benutzer geöffnet ist.


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
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ Sitzung**](win32-session.md)
</dt> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

