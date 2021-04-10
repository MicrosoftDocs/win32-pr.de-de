---
description: Enthält Informationen zu Benutzerkonten und Gruppenkonten, die dem Computersystem bekannt sind, auf dem Windows ausgeführt wird.
ms.assetid: c0916f20-05be-4282-9642-28cec606bfd7
ms.tgt_platform: multiple
title: Win32_Account-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Account
- Win32_Account.Caption
- Win32_Account.Description
- Win32_Account.Domain
- Win32_Account.InstallDate
- Win32_Account.LocalAccount
- Win32_Account.Name
- Win32_Account.SID
- Win32_Account.SIDType
- Win32_Account.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2af601799095192d7af4ffedce0c8e0cd28bff21
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127493"
---
# <a name="win32_account-class"></a>Win32- \_ Konto Klasse

Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) für das **Win32- \_ Konto** enthält Informationen zu Benutzerkonten und Gruppenkonten, die dem Computersystem bekannt sind, auf dem Windows ausgeführt wird. Benutzer-oder Gruppennamen, die von einer Windows-Domäne erkannt werden, sind Nachfolger (oder Member) dieser Klasse.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{8502C4C9-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Account : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  string   Domain;
  datetime InstallDate;
  boolean  LocalAccount;
  string   Name;
  string   SID;
  uint8    SIDType;
  string   Status;
};
```

## <a name="members"></a>Member

Die **Win32- \_ Konto** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32- \_ Konto** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Kurze Beschreibung des Objekts.

Diese Eigenschaft wird von der [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) -Klasse geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Eine Beschreibung des Objekts.

Diese Eigenschaft wird von der [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) -Klasse geerbt.

</dd> <dt>

**Domäne**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Functions \| Domain")
</dt> </dl>

Der Name der Windows-Domäne, zu der eine Gruppe oder ein Benutzer gehört.

Beispiel: "na-Sales"

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")
</dt> </dl>

Datum und Uhrzeit der Installation des-Objekts. Diese Eigenschaft erfordert keinen Wert, um anzugeben, dass das-Objekt installiert ist.

Diese Eigenschaft wird von der [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) -Klasse geerbt.

</dd> <dt>

**LocalAccount**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

**True** gibt an, dass das Konto auf dem lokalen Computer definiert ist. Um nur Konten abzurufen, die auf dem lokalen Computer definiert sind, entwerfen Sie eine Abfrage, die die Bedingung "LocalAccount =**true**" enthält.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| Name")
</dt> </dl>

Der Name des Windows-System Kontos in der Domäne, die durch die **Domänen** Eigenschaft dieser Klasse angegeben wird. Diese Eigenschaft überschreibt die **Name** -Eigenschaft, die von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt wurde.

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Security IDs (SIDs)")
</dt> </dl>

Sicherheits-ID (SID) für dieses Konto. Eine SID ist ein Zeichen folgen Wert mit variabler Länge, der zum Identifizieren eines Vertrauens nehmers verwendet wird. Jedes Konto verfügt über eine eindeutige SID, die von einer Zertifizierungsstelle (z. b. einer Windows-Domäne) ausgestellt wurde und in einer Sicherheitsdatenbank gespeichert ist. Wenn ein Benutzer sich anmeldet, ruft das System die SID des Benutzers aus der Datenbank ab und legt Sie im Zugriffs Token des Benutzers ab. Das System verwendet die SID im Zugriffs Token des Benutzers, um den Benutzer bei allen nachfolgenden Interaktionen mit der Windows-Sicherheit zu identifizieren. Wenn eine SID als eindeutiger Bezeichner für einen Benutzer oder eine Gruppe verwendet wurde, kann Sie nicht erneut verwendet werden, um einen anderen Benutzer oder eine andere Gruppe zu identifizieren.

</dd> <dt>

**SIDType**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Access Control Enumerationstypen- \| sid- \_ Name \_ verwenden")
</dt> </dl>

Enumerationswerte, die den Typ der Sicherheits-ID (SID) angeben.

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

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Aktueller Status des Objekts. Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden. Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein intelligent-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber prognostiziert in naher Zukunft einen Fehler.) Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service". Der letztere Dienst kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden. Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

Diese Eigenschaft wird von der [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) -Klasse geerbt.

Die Werte sind:

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

Die **Win32- \_ Konto** Klasse wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.

## <a name="examples"></a>Beispiele

Mit dem folgenden PowerShell-Code werden die lokalen Konten abgerufen.


```PowerShell
Get-WmiObject Win32_Account -Filter "Domain='$Env:ComputerName'"
```



Mit dem folgenden PowerShell-Code werden die Domänen Konten abgerufen.


```PowerShell
 Get-WmiObject Win32_Account -Filter "Domain='$Env:UserDomain'" 
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

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

