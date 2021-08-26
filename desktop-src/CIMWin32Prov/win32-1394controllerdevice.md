---
description: Die WMI-Zuordnungsklasse Win32 \_ 1394ControllerDevice verknüpft den High-Speed Serial Bus-Controller (IEEE 1394 Firewire) und die damit verbundene CIM \_ LogicalDevice-Instanz.
ms.assetid: 327fbced-4637-4402-a06f-6ac352da920c
ms.tgt_platform: multiple
title: Win32_1394ControllerDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_1394ControllerDevice
- Win32_1394ControllerDevice.NegotiatedDataWidth
- Win32_1394ControllerDevice.NegotiatedSpeed
- Win32_1394ControllerDevice.AccessState
- Win32_1394ControllerDevice.NumberOfHardResets
- Win32_1394ControllerDevice.NumberOfSoftResets
- Win32_1394ControllerDevice.Antecedent
- Win32_1394ControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4877c5e1088e2cf801987d2729d02f64075fc73d1d48daba1fc83b20041c1758
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918110"
---
# <a name="win32_1394controllerdevice-class"></a>Win32 \_ 1394ControllerDevice-Klasse

Die [WMI-Zuordnungsklasse](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ 1394ControllerDevice** verknüpft den Schnellgeschwindigkeits-Serial Bus-Controller (IEEE 1394 Firewire) und die damit verbundene CIM [**\_ LogicalDevice-Instanz.**](cim-logicaldevice.md) Dieser serielle Bus bietet erweiterte Konnektivität für eine Vielzahl von Geräten, einschließlich Audio- oder Videokomponenten von Consumern, Speicherperipheriegeräten, anderen Computern und portablen Geräten. IEEE 1394 wurde von der Consumer-Electronics-Branche übernommen und stellt eine Plug & Play-kompatible Erweiterungsschnittstelle bereit.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8835CFC9-BAEF-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class Win32_1394ControllerDevice : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  Win32_1394Controller REF Antecedent;
  CIM_LogicalDevice    REF Dependent;
};
```

## <a name="members"></a>Member

Die **Win32 \_ 1394ControllerDevice-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ 1394ControllerDevice-Klasse** verfügt über diese Eigenschaften.

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

Datentyp: **Win32 \_ 1394Controller**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ 1394Controller")
</dt> </dl>

Der Win32 1394Controller-Hinweis stellt den diesem Gerät zugeordneten \_ 1394-Controller dar.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LogicalDevice**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ LogicalDevice")
</dt> </dl>

Der \_ abhängige CIM-Verweis LogicalDevice stellt das CIM LogicalDevice dar, das mit dem \_ Controller 1394 verbunden ist.

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits")
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

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits pro Sekunde")
</dt> </dl>

Wenn mehrere Bus- oder Verbindungsgeschwindigkeiten möglich sind, definiert diese Eigenschaft die zwischen den Geräten verwendete Eigenschaft. Die Geschwindigkeit wird in Bits pro Sekunde angegeben. Wenn die Verbindungs- oder Busgeschwindigkeit nicht ausgehandelt wird oder wenn diese Informationen nicht verfügbar oder für die Geräteverwaltung wichtig sind, sollte die -Eigenschaft auf 0 (null) festgelegt werden.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

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

Die **Win32 \_ 1394ControllerDevice-Klasse** wird von [**CIM \_ ControlledBy abgeleitet.**](cim-controlledby.md)

## <a name="examples"></a>Beispiele

Im folgenden PowerShell-Codebeispiel werden 1394-Controllergeräteinformationen abgerufen.


```PowerShell
# Helper function to return AccessState

function get-WmiAccessState {
param ([uint16] $char)

# parse and return values

If ($char -le 2 -and $char -ge 0) {

switch ($char) {
0 {"00-Reserved"}
1 {"01-Reserved"}
2 {"02-Unknown"}
}
}

Else {
"$char - unknown value"
}
}

# Get 1394 Controller Device information from WMI
$1394Cont = Get-WMIObject Win32_1394ControllerDevice

# Display Details
"Win32_1394ControllerDevice WMI Information"
"=========================================="

foreach ($device in $1394Cont) {

"Device Characteristics - Device {0}" -f ++$i

"Access State : {0}" -f (Get-WmiAccessState($ch))
"Antecedent : {0}" -f $device.Antecedent
"Negotiated Data Width : {0}" -f $device.NegotiatedDataWidth
"Negotiated Speed : {0}" -f $device.NegotiatedSpeed
"Number of Hard Resets : {0}" -f $device.NumberofHardResets
"Number of Soft Resets : {0}" -f $device.NumberofSoftResets
} 
```



Im vorherigen Codebeispiel werden die folgenden Informationen zurückgegeben:

``` syntax
# Win32_1394ControllerDevice WMI Information

Device Characteristics -Device 1
Access State : 00-Reserved
Antecedent : \\UK0N055\root\CIMV2:Win32_1394Controller.DeviceID="PCI\\VEN_1217&DEV_00F7&SUBSYS_01CC1028
&REV_02\\4&2FE911E8&0&0CF0"
Negotiated Data Width :
Negotiated Speed :
Number of Hard Resets :
Number of Soft Resets :
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

[**CIM \_ ControlledBy**](cim-controlledby.md)
</dt> <dt>

[Hardwareklassen des Computersystems](computer-system-hardware-classes.md)
</dt> </dl>

 

