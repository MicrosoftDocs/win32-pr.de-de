---
description: Stellt eine CIM \_ controlledby-Beziehung dar, die angibt, auf welche Geräte über einen SCSI-Controller und die Zugriffs Eigenschaften zugegriffen wird.
ms.assetid: a036dbf9-f9ce-4c85-9184-fefcbe4583ba
ms.tgt_platform: multiple
title: CIM_SCSIInterface-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SCSIInterface
- CIM_SCSIInterface.NegotiatedDataWidth
- CIM_SCSIInterface.NegotiatedSpeed
- CIM_SCSIInterface.AccessState
- CIM_SCSIInterface.NumberOfHardResets
- CIM_SCSIInterface.NumberOfSoftResets
- CIM_SCSIInterface.Dependent
- CIM_SCSIInterface.Antecedent
- CIM_SCSIInterface.SCSIRetries
- CIM_SCSIInterface.SCSITimeouts
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1211b142681f15aa8b4d5e61c1d2165a59f5a62c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748593"
---
# <a name="cim_scsiinterface-class"></a>CIM \_ scsiinterface-Klasse

Die **CIM- \_ scsiinterface** -Klasse stellt eine [**CIM- \_ controlledby**](cim-controlledby.md) -Beziehung dar, die angibt, auf welche Geräte über einen SCSI-Controller und die Zugriffs Eigenschaften zugegriffen wird.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{7CE7448E-E3D4-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_SCSIInterface : CIM_ControlledBy
{
  uint32                 NegotiatedDataWidth;
  uint64                 NegotiatedSpeed;
  uint16                 AccessState;
  uint32                 NumberOfHardResets;
  uint32                 NumberOfSoftResets;
  CIM_LogicalDevice  REF Dependent;
  CIM_SCSIController REF Antecedent;
  uint32                 SCSIRetries;
  uint32                 SCSITimeouts;
};
```

## <a name="members"></a>Member

Die **CIM \_ scsiinterface** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ scsiinterface** -Klasse verfügt über diese Eigenschaften.

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

Datentyp: **CIM \_ SCSIController**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")
</dt> </dl>

Ein [**CIM- \_ SCSIController**](cim-scsicontroller.md) , der den SCSI-Controller beschreibt.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LogicalDevice**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")
</dt> </dl>

Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das das logische Gerät beschreibt.

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

</dd> <dt>

**Scsiretries**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der SCSI-Wiederholungen, die seit dem letzten hart oder vorläufig Zurücksetzen des kontrollierten Geräts aufgetreten sind. Die Zeit der letzten zurück setzung wird in der **timeofdevicereset** -Eigenschaft angegeben, die von der [**CIM \_ controlledby**](cim-controlledby.md) -Zuordnung geerbt wurde.

</dd> <dt>

**Scsitimeouts**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der SCSI-Timeouts, die seit der letzten fest-oder Soft-zurück setzung auf das kontrollierte Gerät aufgetreten sind. Die Zeit der letzten zurück setzung wird in der **timeofdevicereset** -Eigenschaft angegeben, die von der [**CIM \_ controlledby**](cim-controlledby.md) -Zuordnung geerbt wurde.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **CIM- \_ scsiinterface** -Klasse wird von [**CIM \_ controlledby**](cim-controlledby.md)abgeleitet.

Diese Klasse wird von WMI nicht implementiert.

Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet. Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.

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
</dt> </dl>

 

