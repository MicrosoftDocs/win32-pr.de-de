---
description: Die \_ WMI-Klasse der Win32-IDEControllerDevice-Zuordnung verknüpft einen IDE-Controller (Integrated Drive Electronics) und das logische Gerät, das mit einem Datenträgerlaufwerk verbunden ist.
ms.assetid: 1b0a551c-d836-4147-91ed-a0a7d97f4a5b
ms.tgt_platform: multiple
title: Win32_IDEControllerDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_IDEControllerDevice
- Win32_IDEControllerDevice.NegotiatedDataWidth
- Win32_IDEControllerDevice.NegotiatedSpeed
- Win32_IDEControllerDevice.AccessState
- Win32_IDEControllerDevice.NumberOfHardResets
- Win32_IDEControllerDevice.NumberOfSoftResets
- Win32_IDEControllerDevice.Antecedent
- Win32_IDEControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d4cd05f3915e23b3fb03fec232e51596b435dddcd8d529c85343255125eee38a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828040"
---
# <a name="win32_idecontrollerdevice-class"></a>Win32 \_ IDEControllerDevice-Klasse

Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) der **Win32-IDEControllerDevice-Zuordnung \_** verknüpft einen IDE-Controller (Integrated Drive Electronics) und das logische Gerät, das mit einem Datenträgerlaufwerk verbunden ist.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{5BC42B62-C7A1-11d2-911D-0060081A46FD}"), AMENDMENT]
class Win32_IDEControllerDevice : CIM_ControlledBy
{
  uint32                  NegotiatedDataWidth;
  uint64                  NegotiatedSpeed;
  uint16                  AccessState;
  uint32                  NumberOfHardResets;
  uint32                  NumberOfSoftResets;
  Win32_IDEController REF Antecedent;
  CIM_LogicalDevice   REF Dependent;
};
```

## <a name="members"></a>Member

Die **\_ Win32-IDEControllerDevice-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ Win32-IDEControllerDevice-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Controller aktiv befehlet oder auf das Gerät zugreift. Diese Informationen sind erforderlich, wenn ein logisches Gerät von mehreren Controllern befehlsgesteuert oder über diese aufgerufen werden kann.

Diese Eigenschaft wird von [**CIM \_ ControlledBy**](cim-controlledby.md)geerbt.

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

Datentyp: **\_ Win32-IDEController**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| Win32 \_ IDEController")
</dt> </dl>

Ein [**\_ Win32-IDEController,**](win32-idecontroller.md) der den diesem Gerät zugeordneten IDE-Controller darstellt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LogicalDevice**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ LogicalDevice")
</dt> </dl>

Ein [**CIM \_ LogicalDevice,**](cim-logicaldevice.md) das das logische Gerät darstellt, das mit dem IDE-Controller verbunden ist.

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits")
</dt> </dl>

Wenn mehrere Bus- oder Verbindungsdatenbreiten möglich sind, definiert diese Eigenschaft den zwischen den Geräten verwendeten. Die Datenbreite wird in Bits angegeben. Wenn die Datenbreite nicht ausgehandelt wird oder diese Informationen für die Geräteverwaltung nicht verfügbar oder wichtig sind, sollte die -Eigenschaft auf 0 (null) festgelegt werden.

Diese Eigenschaft wird von [**CIM \_ DeviceConnection**](cim-deviceconnection.md)geerbt.

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits pro Sekunde")
</dt> </dl>

Wenn mehrere Bus- oder Verbindungsgeschwindigkeiten möglich sind, definiert diese Eigenschaft die zwischen den Geräten verwendete. Die Geschwindigkeit wird in Bits pro Sekunde angegeben. Wenn keine Verbindungs- oder Busgeschwindigkeiten ausgehandelt werden oder diese Informationen für die Geräteverwaltung nicht verfügbar oder wichtig sind, sollte die -Eigenschaft auf 0 (null) festgelegt werden.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

Diese Eigenschaft wird von [**CIM \_ DeviceConnection**](cim-deviceconnection.md)geerbt.

</dd> <dt>

**NumberOfHardResets**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl der vom Controller ausgegebenen hard resets. Durch eine harte Zurücksetzung wird das Gerät in den Initialisierungs- oder Startzustand zurückgesetzt. Alle informationen und Daten zum internen Gerätezustand gehen verloren.

Diese Eigenschaft wird von [**CIM \_ ControlledBy**](cim-controlledby.md)geerbt.

</dd> <dt>

**NumberOfSoftResets**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der vom Controller ausgestellten soft resets. Bei einem soft reset werden der aktuelle Gerätezustand und die Aktuellen Daten nicht vollständig gelöscht. Die genaue Semantik hängt vom Gerät sowie von den Protokollen und Mechanismen ab, die für die Kommunikation mit dem Gerät verwendet werden.

Diese Eigenschaft wird von [**CIM \_ ControlledBy**](cim-controlledby.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\_ Win32-IDEControllerDevice-Klasse** wird von [**CIM \_ ControlledBy**](cim-controlledby.md)abgeleitet.

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

[Computersystemhardwareklassen](computer-system-hardware-classes.md)
</dt> </dl>

 

