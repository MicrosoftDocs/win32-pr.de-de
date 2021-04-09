---
description: Stellt den Instanzwert einer Metrik dar, die durch eine Instanz der MSVM \_ aggregationmetricdefinition-Klasse definiert wird.
ms.assetid: 6dfcb711-6137-492a-aff4-82facbd11949
title: Msvm_AggregationMetricValue-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AggregationMetricValue
- Msvm_AggregationMetricValue.InstanceID
- Msvm_AggregationMetricValue.Caption
- Msvm_AggregationMetricValue.Description
- Msvm_AggregationMetricValue.ElementName
- Msvm_AggregationMetricValue.MetricDefinitionId
- Msvm_AggregationMetricValue.MeasuredElementName
- Msvm_AggregationMetricValue.TimeStamp
- Msvm_AggregationMetricValue.Duration
- Msvm_AggregationMetricValue.MetricValue
- Msvm_AggregationMetricValue.BreakdownDimension
- Msvm_AggregationMetricValue.BreakdownValue
- Msvm_AggregationMetricValue.Volatile
- Msvm_AggregationMetricValue.AggregationTimeStamp
- Msvm_AggregationMetricValue.AggregationDuration
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6842e5a23fbbf7cf1d639862cf5b9737bc1ff96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042709"
---
# <a name="msvm_aggregationmetricvalue-class"></a>MSVM \_ aggregationmetricvalue-Klasse

Stellt den Instanzwert einer Metrik dar, die durch eine Instanz der [**MSVM \_ aggregationmetricdefinition**](msvm-aggregationmetricdefinition.md) -Klasse definiert wird. Die von [**MSVM \_ basemetricvalue**](msvm-basemetricvalue.md) geerbten Eigenschaften stellen den tatsächlichen Metrikwert bereit. Die Eigenschaften, die von dieser Klasse definiert werden, enthalten Informationen über das Intervall, für das die Aggregations Funktion angewendet wurde.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AggregationMetricValue : CIM_AggregationMetricValue
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  string   MetricDefinitionId;
  string   MeasuredElementName;
  datetime TimeStamp;
  datetime Duration;
  string   MetricValue;
  string   BreakdownDimension;
  string   BreakdownValue;
  boolean  Volatile;
  datetime AggregationTimeStamp;
  datetime AggregationDuration;
};
```

## <a name="members"></a>Member

Die **MSVM \_ aggregationmetricvalue** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ aggregationmetricvalue** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Aggregationduration**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt die Zeitspanne dar, in der die Aggregation berechnet wurde. Der Start eines Überwachungs Intervalls, für das die Aggregations Funktion angewendet wird, wird durch Subtrahieren der **aggregationduration** vom **aggregationtimestamp** bestimmt. Diese Eigenschaft wird von **CIM \_ aggregationmetricvalue** geerbt.

</dd> <dt>

**Aggregationtimestamp**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Zeit an, zu der die Aggregations Funktion angewendet wurde, um den Wert der metrikinstanz zu bestimmen. Dies entspricht nicht der Uhrzeit, zu der die Instanz erstellt wurde. Für eine bestimmte **CIM \_ aggregationmetricvalue** -Instanz ändert sich der **aggregationtimestamp** , wenn die Aggregations Funktion angewendet wird, um den Wert zu berechnen. Diese Eigenschaft wird von **CIM \_ aggregationmetricvalue** geerbt.

</dd> <dt>

**Breakdowndimension**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt eine zusammenteilungs Dimension aus dem **breakdowndimensions** -Array an, das in der zugeordneten [**MSVM \_ basemetricdefinition**](msvm-basemetricdefinition.md)definiert ist. Dies ist die Dimension, in der dieser Satz von Metrikwerten untergliedert ist. Diese Eigenschaft wird von [**CIM \_ basemetricdefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Breakdownwert**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Definiert einen Wert der **breakdowndimension** -Eigenschaft, die für diese metrikwertinstanz definiert ist. Wenn die **breakdowndimension** z. b. "transaktionname" lautet, könnte diese Eigenschaft die tatsächliche Transaktion benennen, für die dieser bestimmte Metrikwert gilt. Diese Eigenschaft wird von [**CIM \_ basemetricdefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Dauer**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Zeitspanne an, für die dieser Metrikwert gültig ist. Diese Eigenschaft darf nicht für Zeitstempel vorhanden sein, die nur auf einen bestimmten Zeitpunkt zutreffen, sondern sollte für Werte angegeben werden, die für einen bestimmten Zeitraum gültig sind (z. b. Stichproben). Wenn die **Duration** -Eigenschaft vorhanden ist und nicht **null** ist, gibt die **timestamp** -Eigenschaft das Ende des Intervalls an. Diese Eigenschaft wird von [**CIM \_ basemetricdefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeige Name für das-Objekt. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Eine Zeichenfolge, die eine Instanz dieser Klasse eindeutig identifiziert. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**"Messredelta Name"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein beschreibender Name für das Element, zu dem der Metrikwert gehört (das gemessene Element). Diese Eigenschaft wird von [**CIM \_ basemetricdefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**MetricDefinitionId**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Schlüssel der [**MSVM \_ basemetricdefinition**](msvm-basemetricdefinition.md) -Instanz für diesen Wert. Diese Eigenschaft wird von [**CIM \_ basemetricdefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Metricvalue**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Wert der Metrik, die als Zeichenfolge dargestellt wird. Diese Eigenschaft wird von [**CIM \_ basemetricdefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Zeitstempel**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Uhrzeit an, zu der der Metrikwert aufgezeichnet oder berechnet wurde. Beachten Sie, dass sich dies von dem Zeitpunkt der Erstellung der Instanz unterscheidet. Diese Eigenschaft wird von [**CIM \_ basemetricdefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Ständigem**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** , wenn der Wert für den nächsten Zeitpunkt die gleiche Klasseninstanz verwendet und nur die Eigenschaftswerte (z. b. der **Wert** oder der **Zeitstempel**) geändert werden. **True** gibt an, dass die-Instanz wieder verwendet wird. Wenn der Wert **false** ist, bleiben die vorhandenen Instanzen unverändert, und für den neuen Zeitpunkt wird eine neue Instanz erstellt. Diese Eigenschaft wird von [**CIM \_ basemetricdefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

