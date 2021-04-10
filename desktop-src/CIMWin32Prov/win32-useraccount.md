---
description: Das Win32- \_ Benutzerkonto&\# 32; Die WMI-Klasse enthält Informationen zu einem Benutzerkonto auf einem Computersystem, auf dem Windows ausgeführt wird.
ms.assetid: 747b2ce2-ae38-47de-bf3a-97058df56a7a
ms.tgt_platform: multiple
title: Win32_UserAccount-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserAccount
- Win32_UserAccount.AccountType
- Win32_UserAccount.Caption
- Win32_UserAccount.Description
- Win32_UserAccount.Disabled
- Win32_UserAccount.Domain
- Win32_UserAccount.FullName
- Win32_UserAccount.InstallDate
- Win32_UserAccount.LocalAccount
- Win32_UserAccount.Lockout
- Win32_UserAccount.Name
- Win32_UserAccount.PasswordChangeable
- Win32_UserAccount.PasswordExpires
- Win32_UserAccount.PasswordRequired
- Win32_UserAccount.SID
- Win32_UserAccount.SIDType
- Win32_UserAccount.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5af83f7a52e9f3db9dbaa4a959bfe01ae740746
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041373"
---
# <a name="win32_useraccount-class"></a>Win32 \_ User Account-Klasse

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) für das **Win32- \_ Benutzerkonto** enthält Informationen zu einem Benutzerkonto auf einem Computersystem, auf dem Windows ausgeführt wird.

> [!Note]  
> Da sowohl der **Name** als auch die **Domäne** Schlüsseleigenschaften sind, kann das Auflisten von **Win32 \_ Useraccount** in einem großen Netzwerk die Leistung beeinträchtigen. Das Aufrufen von **GetObject** oder Abfragen für eine bestimmte Instanz hat weniger Auswirkungen.

 

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_UserAccount : Win32_Account
{
  uint32   AccountType;
  string   Caption;
  string   Description;
  boolean  Disabled;
  string   Domain;
  string   FullName;
  datetime InstallDate;
  boolean  LocalAccount;
  boolean  Lockout;
  string   Name;
  boolean  PasswordChangeable;
  boolean  PasswordExpires;
  boolean  PasswordRequired;
  string   SID;
  uint8    SIDType;
  string   Status;
};
```

## <a name="members"></a>Member

Die **Win32 \_ User Account** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ User Account** -Klasse verfügt über diese Methoden.



| Methode                                                     | BESCHREIBUNG                                             |
|:-----------------------------------------------------------|:--------------------------------------------------------|
| [**Benen**](rename-method-in-class-win32-useraccount.md) | Ermöglicht das Umbenennen des Benutzerkontos.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ User Account** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**AccountType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| usri2 \_ Flags")
</dt> </dl>

Flags, die die Merkmale eines Windows-Benutzerkontos beschreiben.

<dt>

<span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>

<span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>**Temporäres doppeltes Konto** (256)


</dt> <dd>

**\_Konto für Temp Temp- \_ Duplizierung \_**

Lokales Benutzerkonto für Benutzer, die über ein primäres Konto in einer anderen Domäne verfügen. Dieses Konto ermöglicht nur den Benutzer Zugriff auf diese Domäne – nicht auf eine Domäne, die dieser Domäne vertraut.

</dd> <dt>

<span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>

<span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>**Normales Konto** (512)


</dt> <dd>

**\_normales \_ Konto**

Der Standard Kontotyp, der einen typischen Benutzer darstellt.

</dd> <dt>

<span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>

<span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>**Domänen Vertrauensstellungs Konto** (2048)


</dt> <dd>

**Konto für die Vertrauensstellung der \_ Verbindungs Domäne \_ \_**

Konto für eine System Domäne, die anderen Domänen vertraut.

</dd> <dt>

<span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>

<span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>Arbeitsstations- **Vertrauensstellungs Konto** (4096)


</dt> <dd>

**Konto der Vertrauensstellung der \_ \_ Vertrauensstellung \_**

Computer Konto für ein Computersystem, auf dem Windows ausgeführt wird, das Mitglied dieser Domäne ist.

</dd> <dt>

<span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>

<span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>**Server Vertrauensstellungs Konto** (8192)


</dt> <dd>

**\_ \_ \_ Konto Vertrauens Konto für den Server**

Konto für einen Domänen Controller der Systemsicherung, der Mitglied dieser Domäne ist.

</dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Domäne und Benutzername des Kontos.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Die Beschreibung des Kontos.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Deaktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| Benutzer \_ Info \| UF \_ accountdeaktivieren")
</dt> </dl>

Das Windows-Benutzerkonto ist deaktiviert.

</dd> <dt>

**Domäne**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("Domäne"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Functions \| Domain Name")
</dt> </dl>

Der Name der Windows-Domäne, zu der ein Benutzerkonto gehört, z. b.: "na-Sales".

</dd> <dt>

**FullName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **usri2 \_ Full \_ Name**")
</dt> </dl>

Der vollständige Name eines lokalen Benutzers, z. b.: "Dan Wilson".

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")
</dt> </dl>

Das Datum, an dem das Objekt installiert ist. Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**LocalAccount**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **korrigiert**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

**True** gibt an, dass das Konto auf dem lokalen Computer definiert ist.

Diese Eigenschaft wird vom [**Win32- \_ Konto**](win32-account.md)geerbt.

</dd> <dt>

**Sperrung**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **UF \_ Lockout**")
</dt> </dl>

**True** gibt an, dass das Benutzerkonto aus dem Windows-Betriebssystem gesperrt ist.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("Name"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| Name")
</dt> </dl>

Der Name des Windows-Benutzerkontos in der Domäne, die von der **Domänen** Eigenschaft dieser Klasse angegeben wird.

Beispiel: "danwilson".

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Passwordänderbar**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **UF \_ passwd \_ cant \_ Change**")
</dt> </dl>

**True** gibt an, dass das Kennwort für dieses Benutzerkonto geändert werden kann.

</dd> <dt>

**PasswordExpires**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **UF \_ 't \_ expire \_ passwd**")
</dt> </dl>

**True** gibt an, dass das Kennwort für dieses Benutzerkonto abläuft.

</dd> <dt>

**PasswordRequired**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **UF \_ passwd \_ notreqd**")
</dt> </dl>

**True** gibt an, dass ein Kennwort für ein Windows-Benutzerkonto erforderlich ist. **False** gibt an, dass für dieses Konto kein Kennwort erforderlich ist.

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Security IDs (SIDs)")
</dt> </dl>

Sicherheits-ID (SID) für dieses Konto. Eine SID ist ein Zeichen folgen Wert variabler Länge, der zum Identifizieren eines Vertrauens nehmers verwendet wird. Jedes Konto verfügt über eine eindeutige SID, die eine Zertifizierungsstelle, z. b. eine Windows-Domäne, ausgibt. Die SID wird in der Sicherheitsdatenbank gespeichert. Wenn sich ein Benutzer anmeldet, ruft das System die Benutzer-SID aus der Datenbank ab, platziert die SID im Benutzer Zugriffs Token und verwendet dann die SID im Benutzer Zugriffs Token, um den Benutzer bei allen nachfolgenden Interaktionen mit der Windows-Sicherheit zu identifizieren. Jede sid ist ein eindeutiger Bezeichner für einen Benutzer oder eine Gruppe, und ein anderer Benutzer oder eine andere Gruppe kann nicht dieselbe SID haben.

Diese Eigenschaft wird vom [**Win32- \_ Konto**](win32-account.md)geerbt.

</dd> <dt>

**SIDType**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Access Control Enumerationstypen- \| [**sid- \_ Name \_ verwenden**](/windows/win32/api/winnt/ne-winnt-sid_name_use)")
</dt> </dl>

Enumerationswert, der den Typ der SID angibt.

Diese Eigenschaft wird vom [**Win32- \_ Konto**](win32-account.md)geerbt.

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

**SidTypeUser** (1)


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

**SidTypeGroup** (2)


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

**SidTypeDomain** (3)


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

**Sidtypealias** (4)


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

**Sidtypewellknowngroup** (5)


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

**SidTypeDeletedAccount** (6)


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

**Sidtypeingabe valid** (7)


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

**SidTypeUnknown** (8)


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

**Sidtypecomputer** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Aktueller Status eines Objekts. Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden. Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail". dabei handelt es sich um ein Element, z. b. ein intelligent-fähiges Festplattenlaufwerk, das möglicherweise ordnungsgemäß funktioniert, aber in naher Zukunft einen Fehler vorhersagt. Nicht operative Status sind: "Error", "Starting", "Stop" und "Service". Diese können während der Spiegelung von Spiegelung eines Datenträgers, erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.

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

## <a name="remarks"></a>Bemerkungen

Die **Win32 \_ User Account** -Klasse wird vom [**Win32- \_ Konto**](win32-account.md)abgeleitet.

> [!Note]  
> Bei dem Versuch, in eine schreibgeschützte Eigenschaft zu schreiben, wird kein Fehler zurückgegeben, und der Wert der Eigenschaft bleibt unverändert.

 

## <a name="examples"></a>Beispiele

In der [Liste lokale Benutzerkonten mit WMI](https://Gallery.TechNet.Microsoft.Com/827623f5-eb55-4035-8f57-25c4afb444cd) VBScript in der TechNet Gallery auflisten werden die Informationen zu den lokalen Benutzerkonten, die auf einem Computer gefunden werden, mithilfe des Win32-Benutzer **\_ Kontos** zurückgegeben.

[Die Übersetzung der SID in das Benutzerkonto und das Benutzerkonto in sid](https://Gallery.TechNet.Microsoft.Com/f1c83aed-fe60-48d5-90ab-22388fcbd54f) PowerShell-Codebeispiel in der TechNet Gallery verwendet **Win32 \_ Useraccount** , um eine SID in ein Benutzerkonto und/oder ein Benutzerkonto in sid zu übersetzen.

Im folgenden VBScript-Codebeispiel wird gezeigt, wie Sie den vollständigen Namen eines Benutzers auf einem lokalen Computer erhalten. Der vollständige Name ist der Name der menschlichen Sprache, z. b., wenn eine Person den Benutzernamen "kensanchez" hat und der vollständige Name "Ken Sanchez" ist, geben Sie den tatsächlichen Domänen Namen und den Benutzernamen für "MyDomainName" und "MyUserName" ein. Für eine effiziente Abfrage müssen Sie die Eigenschaften "Domäne" und "Benutzername" angeben.

Wenn Sie als Administrator auf einem Remote Computer angemeldet sind, können Sie den Namen des Remote Computers für den Cluster (anstelle von ".") zuweisen und dann mithilfe des folgenden Skript Typs den vollständigen Namen eines Benutzerkontos auf einem lokalen Computer – von einem Remote Computer aus erhalten.


```VB
On Error Resume Next
strComputer = "."

Set objUserAccount = GetObject("winmgmts{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2:Win32_UserAccount.Domain='MyDomainName',Name='MyUserName' ")

If Err = 0 Then
    WScript.Echo objUserAccount.FullName
Else
    WScript.Echo "No object found" & Err.Number
End If
```




```CSharp
using System.Management;

{
     ManagementScope mgmtScope = new ManagementScope("\\\\.\\Root\\CIMv2");
     ObjectQuery oQuery = new ObjectQuery("SELECT * FROM Win32_UserAccount Where Name=\"myUserName\"");
     ManagementObjectSearcher mgmtSearch = new ManagementObjectSearcher(mgmtScope, oQuery);
     ManagementObjectCollection objCollection = mgmtSearch.Get();
     foreach (ManagementObject mgmtObject in objCollection)
     {
          Console.WriteLine("Full Name : {0}", mgmtObject["FullName"]);
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

[**Win32- \_ Konto**](win32-account.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> </dl>

 

 
