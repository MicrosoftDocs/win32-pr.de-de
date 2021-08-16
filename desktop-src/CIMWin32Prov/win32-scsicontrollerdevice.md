---
description: Die WMI-Klasse für die \_ Win32-SCSIControllerDevice-Zuordnung verknüpft einen kleinen SCSI-Controller (Computer System Interface) und das damit verbundene logische Gerät (Laufwerk).
ms.assetid: 0334829c-3625-4acf-8ef3-da934c51e9bf
ms.tgt_platform: multiple
title: Win32_SCSIControllerDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SCSIControllerDevice
- Win32_SCSIControllerDevice.NegotiatedDataWidth
- Win32_SCSIControllerDevice.NegotiatedSpeed
- Win32_SCSIControllerDevice.AccessState
- Win32_SCSIControllerDevice.NumberOfHardResets
- Win32_SCSIControllerDevice.NumberOfSoftResets
- Win32_SCSIControllerDevice.Antecedent
- Win32_SCSIControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1f703d5a290245b1596801f78c005c565faa45296c3582e4feaad5dc4011787b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117834171"
---
# <a name="win32_scsicontrollerdevice-class"></a>Win32 \_ SCSIControllerDevice-Klasse

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) für die **\_ Win32-SCSIControllerDevice-Zuordnung** verknüpft einen kleinen SCSI-Controller (Computer System Interface) und das damit verbundene logische Gerät (Laufwerk).

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{CC0F48D2-C847-11d2-911E-0060081A46FD}"), AMENDMENT]
class Win32_SCSIControllerDevice : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  Win32_SCSIController REF Antecedent;
  CIM_LogicalDevice    REF Dependent;
};
```

## <a name="members"></a>Member

Die **Win32 \_ SCSIControllerDevice-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ Win32-Klasse SCSIControllerDevice verfügt** über diese Eigenschaften.

<dl> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Controller aktiv befehlet oder auf das Gerät zutritt. Diese Informationen sind erforderlich, wenn ein logisches Gerät von mehreren Controllern befehlet oder über diese aufgerufen werden kann.

Diese Eigenschaft wird von [**CIM \_ ControlledBy geerbt.**](cim-controlledby.md)

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

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ SCSIController**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| Win32 \_ SCSIController")
</dt> </dl>

Der [**Win32 \_ SCSIController-Hinweis**](win32-scsicontroller.md) stellt den diesem Gerät zugeordneten SCSI-Controller dar.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LogicalDevice**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")
</dt> </dl>

Der [**\_ abhängige CIM-Verweis LogicalDevice**](cim-logicaldevice.md) stellt das logische Gerät dar, das mit dem SCSI-Controller verbunden ist.

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bits")
</dt> </dl>

Wenn mehrere Bus- oder Verbindungsdatenbreiten möglich sind, definiert diese Eigenschaft die zwischen den Geräten verwendete Eigenschaft. Die Datenbreite wird in Bits angegeben. Wenn die Datenbreite nicht ausgehandelt wird oder diese Informationen für die Geräteverwaltung nicht verfügbar oder wichtig sind, sollte die -Eigenschaft auf 0 (null) festgelegt werden.

Diese Eigenschaft wird von [**CIM \_ DeviceConnection geerbt.**](cim-deviceconnection.md)

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bits pro Sekunde")
</dt> </dl>

Wenn mehrere Bus- oder Verbindungsgeschwindigkeiten möglich sind, definiert diese Eigenschaft die zwischen den Geräten verwendete Eigenschaft. Die Geschwindigkeit wird in Bits pro Sekunde angegeben. Wenn die Verbindungs- oder Busgeschwindigkeit nicht ausgehandelt wird oder wenn diese Informationen nicht verfügbar oder für die Geräteverwaltung wichtig sind, sollte die -Eigenschaft auf 0 (null) festgelegt werden.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](../wmisdk/creating-a-wmi-script.md)

Diese Eigenschaft wird von [**CIM \_ DeviceConnection geerbt.**](cim-deviceconnection.md)

</dd> <dt>

**NumberOfHardResets**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der vom Controller ausgegebenen zurückgesetzten Festplatten. Durch eine harte Zurücksetzung wird das Gerät in den Initialisierungs- oder Startzustand zurückgesetzt. Alle internen Gerätestatusinformationen und -daten gehen verloren.

Diese Eigenschaft wird von [**CIM \_ ControlledBy geerbt.**](cim-controlledby.md)

</dd> <dt>

**NumberOfSoftResets**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der vom Controller ausgegebenen zurückgesetzten Daten. Bei einer zurückgesetzten Zurücksetzung werden der aktuelle Gerätestatus und die aktuellen Daten nicht vollständig entschlossen. Die genaue Semantik hängt vom Gerät sowie von den Protokollen und Mechanismen ab, die für die Kommunikation verwendet werden.

Diese Eigenschaft wird von [**CIM \_ ControlledBy geerbt.**](cim-controlledby.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ SCSIControllerDevice-Klasse** wird von [**CIM \_ ControlledBy abgeleitet.**](cim-controlledby.md)

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

[**CIM \_ ControlledBy**](cim-controlledby.md)
</dt> <dt>

[Hardwareklassen des Computersystems](computer-system-hardware-classes.md)
</dt> </dl>

 

 
