---
description: Die \_ WMI-Klasse für die Win32-Klasse "1394controllerdevice" verknüpft den Hochleistungs Controller (IEEE 1394 FireWire) und die Verbindung mit der CIM \_ LogicalDevice-Instanz.
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
ms.openlocfilehash: af3a54db81a388184da148cd411895ebb910de7d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861595"
---
# <a name="win32_1394controllerdevice-class"></a>Win32- \_ Klasse "1394controllerdevice"

Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) für die Win32-Klasse " **\_ 1394controllerdevice** " verknüpft den Hochleistungs Controller (IEEE 1394 FireWire) und die Verbindung mit der [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Instanz. Dieser serielle Bus bietet eine verbesserte Konnektivität für eine große Bandbreite von Geräten, einschließlich Consumer-Audiodaten oder Videokomponenten, Speicher Peripheriegeräte, andere Computer und tragbare Geräte. IEEE 1394 wurde von der Consumer Electronics Industry übernommen und bietet eine Plug & Play kompatible Erweiterungsschnittstelle.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

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

Die Win32-Klasse " **\_ 1394controllerdevice** " enthält diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse " **\_ 1394controllerdevice** " verfügt über diese Eigenschaften.

<dl> <dt>

**Accessstate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Controller aktiv auf das Gerät zugreift oder darauf zugreift. Diese Informationen sind erforderlich, wenn ein logisches Gerät durch mehrere Controller befohlen werden kann oder darauf zugegriffen werden kann.

Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.

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

Datentyp: **Win32 \_** -Wert Controller
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ 1394controller")
</dt> </dl>

Die Win32-Referenz für den " \_ 1394controller Vorgänger" stellt den 1394-Controller dar, der diesem Gerät zugeordnet ist.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LogicalDevice**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ LogicalDevice")
</dt> </dl>

Der \_ von CIM LogicalDevice abhängige Verweis stellt das CIM \_ LogicalDevice dar, das mit dem 1394-Controller verbunden ist.

</dd> <dt>

**Aushandateddatawidth**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits")
</dt> </dl>

Wenn mehrere Bus-oder Verbindungsdaten breiten möglich sind, definiert diese Eigenschaft die jeweils verwendete Eigenschaft zwischen den Geräten. Die Daten Breite wird in Bits angegeben. Wenn die Daten Breite nicht ausgehandelt wird oder diese Informationen für die Geräteverwaltung nicht verfügbar oder wichtig sind, sollte die-Eigenschaft auf 0 (null) festgelegt werden.

Diese Eigenschaft wird von CIM-Geräte [**\_ erviceconnetction**](cim-deviceconnection.md)geerbt.

</dd> <dt>

**Aushandatedspeed**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits pro Sekunde")
</dt> </dl>

Wenn mehrere Bus-oder Verbindungsgeschwindigkeiten möglich sind, definiert diese Eigenschaft die zwischen den Geräten verwendete. Die Geschwindigkeit wird in Bits pro Sekunde angegeben. Wenn Verbindungs-oder Busgeschwindigkeiten nicht ausgehandelt werden oder diese Informationen für die Geräteverwaltung nicht verfügbar oder wichtig sind, sollte die-Eigenschaft auf 0 (null) festgelegt werden.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Diese Eigenschaft wird von CIM-Geräte [**\_ erviceconnetction**](cim-deviceconnection.md)geerbt.

</dd> <dt>

**Anzahlersätze**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl von Festplatten, die vom Controller ausgegeben werden. Bei einer festen zurück setzung wird das Gerät wieder in den Initialisierungs-oder Startzustand versetzt. Alle internen Geräte Zustandsinformationen und Daten gehen verloren.

Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.

</dd> <dt>

**Anzahlermengen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der vom Controller ausgestellten Soft-zurück Stellungen. Eine weiche zurück Setzung löscht den aktuellen Gerätestatus und die Daten nicht vollständig. Die genaue Semantik ist abhängig vom Gerät und den Protokollen und Mechanismen, die für die Kommunikation mit dem Gerät verwendet werden.

Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Win32-Klasse " **\_ 1394controllerdevice** " ist von [**CIM \_ controlledby**](cim-controlledby.md)abgeleitet.

## <a name="examples"></a>Beispiele

Das folgende PowerShell-Codebeispiel ruft 1394 Controller-Geräteinformationen ab.


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
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ controlledby**](cim-controlledby.md)
</dt> <dt>

[Computer System-Hardware Klassen](computer-system-hardware-classes.md)
</dt> </dl>

 

