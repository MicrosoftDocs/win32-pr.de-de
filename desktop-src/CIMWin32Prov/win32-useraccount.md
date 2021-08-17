---
description: Win32 \_ UserAccount&\# 32; Die WMI-Klasse enthält Informationen zu einem Benutzerkonto auf einem Computersystem, auf dem Windows.
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
ms.openlocfilehash: df907b1686677db8ea895d8788055567e24dc7be7ffe758bcfa82801591a0dfb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922750"
---
# <a name="win32_useraccount-class"></a>Win32 \_ UserAccount-Klasse

Die **WMI-Klasse \_ Win32 UserAccount** enthält Informationen zu einem Benutzerkonto auf einem Computersystem, auf dem Windows. [](../wmisdk/retrieving-a-class.md)

> [!Note]  
> Da sowohl Name **als** auch **Domäne** wichtige Eigenschaften sind, kann sich das Aufzählen von **Win32 \_ UserAccount** in einem großen Netzwerk negativ auf die Leistung auswirken. Das **Aufrufen von GetObject** oder das Abfragen einer bestimmten Instanz hat weniger Auswirkungen.

 

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge.

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

Die **Win32 \_ UserAccount-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ UserAccount-Klasse** verfügt über diese Methoden.



| Methode                                                     | BESCHREIBUNG                                             |
|:-----------------------------------------------------------|:--------------------------------------------------------|
| [**Umbenennen**](rename-method-in-class-win32-useraccount.md) | Ermöglicht das Umbenennen des Benutzerkontos.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ UserAccount-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AccountType**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| usri2 \_ flags")
</dt> </dl>

Flags, die die Merkmale eines Windows beschreiben.

<dt>

<span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>

<span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>**Temporäres doppeltes** Konto (256)


</dt> <dd>

**TEMPORÄRES \_ DOPPELTES \_ UF-KONTO \_**

Lokales Benutzerkonto für Benutzer, die über ein primäres Konto in einer anderen Domäne verfügen. Dieses Konto bietet nur Benutzerzugriff auf diese Domäne – nicht auf eine Domäne, die dieser Domäne vertraut.

</dd> <dt>

<span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>

<span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>**Normales** Konto (512)


</dt> <dd>

**NORMALES \_ \_ UF-KONTO**

Standardkontotyp, der einen typischen Benutzer darstellt.

</dd> <dt>

<span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>

<span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>**Domänenübergreifendes Vertrauensstellungskonto** (2048)


</dt> <dd>

**UF \_ INTERDOMAIN \_ TRUST \_ ACCOUNT**

Konto für eine Systemdomäne, die anderen Domänen vertraut.

</dd> <dt>

<span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>

<span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>**Arbeitsstations-Vertrauensstellungskonto** (4096)


</dt> <dd>

**UF \_ WORKSTATION \_ TRUST \_ ACCOUNT**

Computerkonto für ein Computersystem, auf dem Windows, das Mitglied dieser Domäne ist.

</dd> <dt>

<span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>

<span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>**Server-Vertrauensstellungskonto** (8192)


</dt> <dd>

**UF \_ SERVER \_ TRUST \_ ACCOUNT**

Konto für einen Domänencontroller für die Systemsicherung, der Mitglied dieser Domäne ist.

</dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Domäne und Benutzername des Kontos.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Beschreibung des Kontos.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**Disabled** (Deaktiviert)
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| \_ \| UF \_ ACCOUNTDISABLE")
</dt> </dl>

Windows Benutzerkonto ist deaktiviert.

</dd> <dt>

**Domain**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](../wmisdk/standard-qualifiers.md) ("Domäne"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Domänenname der Win32API-Netzwerkverwaltungsfunktionen") \| \|
</dt> </dl>

Name der Windows Domäne, zu der ein Benutzerkonto gehört, z. B. "NA-SALES".

</dd> <dt>

**FullName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **usri2 \_ full \_ name**")
</dt> </dl>

Vollständiger Name eines lokalen Benutzers, z.B. "Dan Soll".

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Installationsdatum")
</dt> </dl>

Datum, an dem das Objekt installiert wurde. Diese Eigenschaft benötigt keinen Wert, um anzugeben, dass das Objekt installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**LocalAccount**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Behoben**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

True **gibt an,** dass das Konto auf dem lokalen Computer definiert ist.

Diese Eigenschaft wird vom [**Win32-Konto \_ geerbt.**](win32-account.md)

</dd> <dt>

**Sperrung**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **UF \_ LOCKOUT**")
</dt> </dl>

True **gibt an,** dass das Benutzerkonto aus dem Windows gesperrt ist.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Name der Win32API-Netzwerkverwaltungsstrukturen") \| \|
</dt> </dl>

Der Name des Windows Benutzerkontos in der Domäne, die von der **Domain-Eigenschaft** dieser Klasse angegeben wird.

Beispiel: "danwilson".

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**PasswordChangeable**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **UF \_ PASSWD \_ CANT \_ CHANGE**")
</dt> </dl>

True **gibt an,** dass das Kennwort für dieses Benutzerkonto geändert werden kann.

</dd> <dt>

**PasswordExpires**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Netzwerkverwaltungsstrukturen \| USER INFO \| [**\_ \_ 2 UF**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **\_ DONT \_ EXPIRE \_ PASSWD**")
</dt> </dl>

True gibt an, dass das Kennwort für dieses Benutzerkonto abläuft.

</dd> <dt>

**PasswordRequired**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Netzwerkverwaltungsstrukturen \| USER INFO \| [**\_ \_ 2 UF**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **\_ PASSWD \_ NOTREQD**")
</dt> </dl>

True gibt an, dass ein Kennwort für ein Windows Benutzerkonto erforderlich ist. False gibt an, dass für dieses Konto kein Kennwort erforderlich ist.

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Behoben:**](../wmisdk/standard-wmi-qualifiers.md) [**, MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Sicherheitsbezeichner \| (SIDs)")
</dt> </dl>

Sicherheits-ID (SID) für dieses Konto. Eine SID ist ein Zeichenfolgenwert variabler Länge, der zum Identifizieren eines Vertrauensnehmers verwendet wird. Jedes Konto verfügt über eine eindeutige SID, die von einer Autorität, z. B. einer Windows Domäne, ausgibt. Die SID wird in der Sicherheitsdatenbank gespeichert. Wenn sich ein Benutzer anmeldet, ruft das System die Benutzer-SID aus der Datenbank ab, platziert die SID im Benutzerzugriffstoken und verwendet dann die SID im Benutzerzugriffstoken, um den Benutzer in allen nachfolgenden Interaktionen mit Windows Sicherheit zu identifizieren. Jede SID ist ein eindeutiger Bezeichner für einen Benutzer oder eine Gruppe, und ein anderer Benutzer oder eine andere Gruppe kann nicht dieselbe SID aufweisen.

Diese Eigenschaft wird vom [**\_ Win32-Konto**](win32-account.md)geerbt.

</dd> <dt>

**SIDType**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Behoben:**](../wmisdk/standard-wmi-qualifiers.md) [**, MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Access Control Enumerationstypen \| [**SID NAME \_ \_ USE**](/windows/win32/api/winnt/ne-winnt-sid_name_use)")
</dt> </dl>

Aufzählungswert, der den Typ der SID angibt.

Diese Eigenschaft wird vom [**\_ Win32-Konto**](win32-account.md)geerbt.

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

**SidTypeAlias** (4)


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

**SidTypeWellKnownGroup** (5)


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

**SidTypeDeletedAccount** (6)


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

**SidTypeInvalid** (7)


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

**SidTypeUnknown** (8)


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

**SidTypeComputer** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Aktueller Status eines Objekts. Es können verschiedene Betriebs- und Nichtoperationsstatus definiert werden. Betriebsstatus: "OK", "Heruntergestuft" und "Pred Fail". Dabei handelt es sich um ein Element wie ein SMART-fähiges Festplattenlaufwerk, das möglicherweise ordnungsgemäß funktioniert, aber einen Fehler in naher Zukunft vorhersagt. Nichtoperationale Status: "Error", "Starting", "Stopping" und "Service", die während des Spiegelresilverings eines Datenträgers, beim erneuten Laden einer Benutzerberechtigungsliste oder bei anderen administrativen Arbeiten angewendet werden können.

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

**Heruntergestuft** ("Heruntergestuft")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** ("Unbekannt")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred Fail** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Wird gestartet** ("Wird gestartet")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Beenden** ("Wird beendet")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Dienst** ("Dienst")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Mannslast** ("1000")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Kein Kontakt** ("Kein Kontakt")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Verlorenes Komma** ("Verlorenes Komma")


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ UserAccount-Klasse** wird von [**Win32-Konto \_**](win32-account.md)abgeleitet.

> [!Note]  
> Beim Versuch, in eine schreibgeschützte Eigenschaft zu schreiben, wird kein Fehler zurückgegeben, und der Wert der Eigenschaft bleibt unverändert.

 

## <a name="examples"></a>Beispiele

Das Codebeispiel List Local User Accounts Using WMI VBScript [(Lokale Benutzerkonten mit WMI](https://Gallery.TechNet.Microsoft.Com/827623f5-eb55-4035-8f57-25c4afb444cd) VBScript auflisten) im TechNet-Katalog verwendet **Win32 \_ UserAccount,** um Informationen zu den auf einem Computer gefundenen lokalen Benutzerkonten zurückgibt.

Übersetzen der [SID in das Benutzerkonto und des Benutzerkontos in die SID](https://Gallery.TechNet.Microsoft.Com/f1c83aed-fe60-48d5-90ab-22388fcbd54f) Das PowerShell-Codebeispiel im TechNet-Katalog verwendet **Win32 \_ UserAccount,** um eine SID in ein Benutzerkonto und/oder ein Benutzerkonto in SID zu übersetzen.

Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie Sie den vollständigen Namen eines Benutzers auf einem lokalen Computer abrufen. Der vollständige Name ist der Name der menschlichen Sprache, z. B. kann eine Person den Benutzernamen "kensaali" und den vollständigen Namen "Ken Saoa" haben, sodass Sie den tatsächlichen Domänennamen und Benutzernamen durch "MyDomainName" und "MyUserName" ersetzen. Für eine effiziente Abfrage müssen Sie sowohl die Domänen- als auch die Benutzernameneigenschaften angeben.

Wenn Sie Administrator auf einem Remotecomputer sind, können Sie den Namen des Remotecomputers für strComputer (anstelle von ".") zuweisen und dann den folgenden Skripttyp verwenden, um den vollständigen Namen eines Benutzerkontos auf einem lokalen Computer abzurufen – von einem Remotecomputer.


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
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_Win32-Konto**](win32-account.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> </dl>

 

 
