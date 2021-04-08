---
description: Stellt eine Beziehung zwischen einem Controller und einem vom Controller verwalteten logischen Gerät dar.
ms.assetid: 5a938fa4-3b91-42ad-beee-12ed0ce6df9a
title: CIM_ControlledBy-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ControlledBy
- CIM_ControlledBy.Antecedent
- CIM_ControlledBy.Dependent
- CIM_ControlledBy.AccessState
- CIM_ControlledBy.TimeOfDeviceReset
- CIM_ControlledBy.NumberOfHardResets
- CIM_ControlledBy.NumberOfSoftResets
- CIM_ControlledBy.DeviceNumber
- CIM_ControlledBy.AccessMode
- CIM_ControlledBy.AccessPriority
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7b035a93c47f9c33d981614ba6fc46b35f916e7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863127"
---
# <a name="cim_controlledby-class-hyper-v-management"></a>CIM_ControlledBy-Klasse (Hyper-V-Verwaltung)

Stellt eine Beziehung zwischen einem Controller und einem vom Controller verwalteten logischen Gerät dar.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_ControlledBy : CIM_DeviceConnection
{
  CIM_Controller    REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint16                AccessState;
  datetime              TimeOfDeviceReset;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  string                DeviceNumber;
  uint16                AccessMode;
  uint16                AccessPriority;
};
```

## <a name="members"></a>Member

Die **CIM \_ controlledby** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ controlledby** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**AccessMode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft beschreibt den Zugriff auf das Gerät über den Controller.

<dt>

<span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>

**Lesen** (2)


</dt> <dd></dd> <dt>

<span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>

Schreib **geschützt (3** )


</dt> <dd></dd> <dt>

<span id="NoAccess"></span><span id="noaccess"></span><span id="NOACCESS"></span>

**NoAccess** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**Accesspriority**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Priorität für den Zugriff des Geräts über den Controller. Ein niedrigerer Wert weist auf eine höhere Priorität hin.

</dd> <dt>

**Accessstate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Controller das Gerät aktiv verwaltet.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

**Aktiv** (1)


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

**Inaktiv** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Controller**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")
</dt> </dl>

Der Controller.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LogicalDevice**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")
</dt> </dl>

Die logischen Geräte.

</dd> <dt>

**Devicengegen ber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Adresse des zugeordneten Geräts im Kontext des Controllers.

</dd> <dt>

**Anzahlersätze**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Counter**
</dt> </dl>

Die Anzahl von Festplatten, die vom Controller ausgegeben werden. Bei einer festen zurück setzung wird ein Gerät an den Initialisierungs-oder Startzustand zurückgegeben, in dem alle Informationen zum internen Gerätestatus und Daten verloren gehen.

</dd> <dt>

**Anzahlermengen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Counter**
</dt> </dl>

Die Anzahl der vom Controller ausgestellten Soft-zurück Stellungen. Eine weiche zurück Setzung löscht den Gerätezustand oder die Daten nicht.

</dd> <dt>

**Timeofdevicereset**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Zeitpunkt, zu dem das Downstream-Gerät zuletzt vom Controller zurückgesetzt wurde.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM-Geräte \_ Steuerung**](cim-deviceconnection.md)
</dt> </dl>

 

