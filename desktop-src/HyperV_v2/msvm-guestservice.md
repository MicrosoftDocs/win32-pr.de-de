---
description: MSVM \_ guestservice ist die abstrakte Basisklasse für Dienste im Gast, auf die vom Host zugegriffen werden kann.
ms.assetid: F9E6FFE6-B8C5-4F06-BF22-A4BDB20F813A
title: Msvm_GuestService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService
- Msvm_GuestService.Caption
- Msvm_GuestService.CreationClassName
- Msvm_GuestService.Description
- Msvm_GuestService.InstallDate
- Msvm_GuestService.Name
- Msvm_GuestService.Started
- Msvm_GuestService.StartMode
- Msvm_GuestService.Status
- Msvm_GuestService.SystemCreationClassName
- Msvm_GuestService.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 99d1936a2678fc2d8357974f9c11a250a1d9bce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393430"
---
# <a name="msvm_guestservice-class"></a>MSVM \_ guestservice-Klasse

**MSVM \_ Guestservice** ist die abstrakte Basisklasse für Dienste im Gast, auf die vom Host zugegriffen werden kann. Diese Klasse wird von der [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service) Klasse abgeleitet.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, AMENDMENT]
class Msvm_GuestService : CIM_Service
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

Die **MSVM \_ guestservice** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MSVM \_ guestservice** -Klasse verfügt über diese Methoden.



| Methode                                                             | BESCHREIBUNG                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**RequestStateChange**](requeststatechange-msvm-guestservice.md) | Fordert an, dass der Zustand des Gast Diensts auf den angegebenen Wert geändert wird.<br/> |
| [**Start Service**](startservice-msvm-guestservice.md)             | Versetzt den Gast Dienst in den Zustand "gestartet". <br/>                                     |
| [**Stop Service**](stopservice-msvm-guestservice.md)               | Beendet den Gast Dienst. <br/>                                                       |



 

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ guestservice** -Klasse verfügt über diese Eigenschaften.

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

[**CIM- \_ Dienst**](cim-service.md)
</dt> <dt>

[**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)
</dt> </dl>

 

