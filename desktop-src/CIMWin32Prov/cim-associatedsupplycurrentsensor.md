---
description: Die CIM AssociatedSupplyCurrentSensor-Klasse ordnet eine Stromversorgung einem aktuellen Sensor (Amperage) zu, der \_ die Eingangsfrequenz überwacht.
ms.assetid: bed4714f-ecf4-4c53-b231-c8fac673371f
ms.tgt_platform: multiple
title: CIM_AssociatedSupplyCurrentSensor-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedSupplyCurrentSensor
- CIM_AssociatedSupplyCurrentSensor.Dependent
- CIM_AssociatedSupplyCurrentSensor.Antecedent
- CIM_AssociatedSupplyCurrentSensor.MonitoringRange
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1b20b519c0ec89243aefd9c87aba235548f11f93984a45702f7670a27bf073cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119080934"
---
# <a name="cim_associatedsupplycurrentsensor-class"></a>CIM \_ AssociatedSupplyCurrentSensor-Klasse

Die **CIM \_ AssociatedSupplyCurrentSensor-Klasse** ordnet eine Stromversorgung einem aktuellen Sensor (Amperage) zu, der die Eingangsfrequenz überwacht.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{29B273F2-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedSupplyCurrentSensor : CIM_AssociatedSensor
{
  CIM_PowerSupply   REF Dependent;
  CIM_CurrentSensor REF Antecedent;
  uint16                MonitoringRange;
};
```

## <a name="members"></a>Member

Die **CIM \_ AssociatedSupplyCurrentSensor-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ AssociatedSupplyCurrentSensor-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ CurrentSensor**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Ein [**CIM \_ CurrentSensor,**](cim-currentsensor.md) der den aktuellen Sensor beschreibt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ PowerSupply**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Abhängig")
</dt> </dl>

Ein [**\_ CIM-PowerSupply-Wert,**](cim-powersupply.md) der die dem aktuellen Sensor zugeordnete Stromversorgung beschreibt.

</dd> <dt>

**MonitoringRange**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Vom zugeordneten Sensor gemessenen Eingangsfrequenzbereich der Stromversorgung an.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>**Bereich 1** (2)


</dt> <dd></dd> <dt>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>**Bereich 2** (3)


</dt> <dd></dd> <dt>

<span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>

<span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>**Bereich 1 und 2** (4)


</dt> <dd>

Bereich 1 und 2

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **CIM \_ AssociatedSupplyCurrentSensor-Klasse** wird von [**CIM \_ AssociatedSensor abgeleitet.**](cim-associatedsensor.md)

WMI implementiert diese Klasse nicht.

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden. Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.

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

[**CIM \_ AssociatedSensor**](cim-associatedsensor.md)
</dt> </dl>

 

