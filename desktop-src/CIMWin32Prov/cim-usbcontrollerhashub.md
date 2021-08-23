---
description: Die \_ CIM-Klasse USBControllerHasHub definiert die Hubs, die dem USB-Controller nachgeschaltet sind.
ms.assetid: 38bc0342-3ff0-42c8-9c1e-ea5a5822e1d3
ms.tgt_platform: multiple
title: CIM_USBControllerHasHub-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBControllerHasHub
- CIM_USBControllerHasHub.NegotiatedDataWidth
- CIM_USBControllerHasHub.NegotiatedSpeed
- CIM_USBControllerHasHub.AccessState
- CIM_USBControllerHasHub.NumberOfHardResets
- CIM_USBControllerHasHub.NumberOfSoftResets
- CIM_USBControllerHasHub.Dependent
- CIM_USBControllerHasHub.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f218fa125470793a680251fe9ae5b3d0be4a211626915d2214358c351b8f0cd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547750"
---
# <a name="cim_usbcontrollerhashub-class"></a>CIM \_ USBControllerHasHub-Klasse

Die **\_ CIM-Klasse USBControllerHasHub** definiert die Hubs, die dem USB-Controller nachgeschaltet sind.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[AMENDMENT]
class CIM_USBControllerHasHub : CIM_ControlledBy
{
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
  uint16                AccessState;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  CIM_USBHub        REF Dependent;
  CIM_USBController REF Antecedent;
};
```

## <a name="members"></a>Member

Die **\_ CIM-Klasse USBControllerHasHub** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ CIM-Klasse USBControllerHasHub** verfügt über diese Eigenschaften.

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

Datentyp: **CIM \_ USBController**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ein [**\_ CIM-USBController,**](cim-usbcontroller.md) der den USBController beschreibt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ USBHub**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ein [**\_ CIM-USBHub,**](cim-usbhub.md) der den USBHub beschreibt, der dem Controller zugeordnet ist.

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

Die **CIM \_ USBControllerHasHub-Klasse** wird von [**CIM \_ ControlledBy abgeleitet.**](cim-controlledby.md)

WMI implementiert diese Klasse nicht. Informationen zu WMI-Klassen, die von **CIM \_ USBControllerHasHub abgeleitet werden,** finden Sie unter [Win32-Klassen](win32-provider.md).

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden. Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.

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
</dt> </dl>

 

