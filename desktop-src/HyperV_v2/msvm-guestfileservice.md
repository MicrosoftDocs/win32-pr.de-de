---
description: MSVM \_ guestfileservice enthält eine Methode, die zum Kopieren einer Datei auf eine virtuelle Maschine vom Hyper-V-Host verwendet werden kann.
ms.assetid: 3599d5a8-415f-48f8-b887-00a93b7abb83
title: Msvm_GuestFileService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestFileService
- Msvm_GuestFileService.StartService
- Msvm_GuestFileService.StopService
- Msvm_GuestFileService.Caption
- Msvm_GuestFileService.CreationClassName
- Msvm_GuestFileService.Description
- Msvm_GuestFileService.InstallDate
- Msvm_GuestFileService.Name
- Msvm_GuestFileService.Started
- Msvm_GuestFileService.StartMode
- Msvm_GuestFileService.Status
- Msvm_GuestFileService.SystemCreationClassName
- Msvm_GuestFileService.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ee0f235d7549428ecf02e9c758c83bcea33efe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342829"
---
# <a name="msvm_guestfileservice-class"></a>MSVM \_ guestfileservice-Klasse

**MSVM \_ Guestfileservice** enthält eine Methode, die verwendet werden kann, um eine Datei auf einen virtuellen Computer vom Hyper-V-Host zu kopieren. Diese Klasse wird von [**MSVM \_ guestservice**](msvm-guestservice.md)abgeleitet.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestFileService : Msvm_GuestService
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  datetime InstallDate;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a>Member

Die **MSVM \_ guestfileservice** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MSVM \_ guestfileservice** -Klasse verfügt über diese Methoden.



| Methode                                                             | BESCHREIBUNG                                                                                                                                                                  |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Copyfilestoguest**](copyfilestoguest-msvm-guestfileservice.md) | Dateien werden vom Hyper-V-Host auf den virtuellen Computer kopiert.<br/> **Windows 8.1:** Diese Methode wird erst Windows 8.1 und Windows Server 2012 R2 unterstützt.<br/> |
| **Start Service**                                                   | Diese Methode wird nicht unterstützt.<br/>                                                                                                                                     |
| **Stop Service**                                                    | Diese Methode wird nicht unterstützt.<br/>                                                                                                                                     |



 

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ guestfileservice** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Kurze Textbeschreibung des-Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**"Name der Klassenname"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird. Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Textbeschreibung des Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Datum und Uhrzeit der Installation des-Objekts. Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eindeutiger Bezeichner für den Dienst, der auch eine Angabe der verwalteten Funktionalität bereitstellt. Weitere Informationen zu den Funktionen finden Sie in der **Description** -Eigenschaft des Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**Gestartet**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass der Dienst gestartet wurde.

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Dienst automatisch gestartet wird (z. b. durch ein Betriebssystem) oder nur nach Anforderung gestartet wird.

Folgende Werte sind gültig:

<dl><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span><dt>

**Schem**
</dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span><dt>

**Manual**
</dt> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Aktueller Status des Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

Folgende Werte sind gültig:

<dl><span id="OK"></span><span id="ok"></span><dt>

**Okay**
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

**Zeit**
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

**Zerstört**
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

**Unbekannter**
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

**"Pred Fail"**
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

**Fahren**
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

**Hindern**
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

**Leistungs**
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

**Gestresst**
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

**"Nicht wiederherstellen"**
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

**"Kein Kontakt"**
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

**"Verlorene comm"**
</dt> </dl>

</dd> <dt>

**Systemkreationclassname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Erstellungs Klasse des Bereichs Systems.

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Systems, das den Dienst hostet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM- \_ guestservice**](msvm-guestservice.md)
</dt> </dl>

 

