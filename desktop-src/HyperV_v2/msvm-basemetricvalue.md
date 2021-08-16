---
description: Stellt einen Metrikwert dar, der von einer Instanz der Msvm \_ BaseMetricDefinition-Klasse definiert wird.
ms.assetid: bd872f21-ab71-4ab7-88d3-b26dd2fbdbe5
title: Msvm_BaseMetricValue-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BaseMetricValue
- Msvm_BaseMetricValue.InstanceID
- Msvm_BaseMetricValue.Caption
- Msvm_BaseMetricValue.Description
- Msvm_BaseMetricValue.ElementName
- Msvm_BaseMetricValue.MetricDefinitionId
- Msvm_BaseMetricValue.MeasuredElementName
- Msvm_BaseMetricValue.TimeStamp
- Msvm_BaseMetricValue.Duration
- Msvm_BaseMetricValue.MetricValue
- Msvm_BaseMetricValue.BreakdownDimension
- Msvm_BaseMetricValue.BreakdownValue
- Msvm_BaseMetricValue.Volatile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 24d61f6068cffc83f8556637bba30de57308b6a5bcefe5b015bc185ab7811108
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790220"
---
# <a name="msvm_basemetricvalue-class"></a>Msvm \_ BaseMetricValue-Klasse

Stellt einen Metrikwert dar, der von einer Instanz der [**Msvm \_ BaseMetricDefinition-Klasse**](msvm-basemetricdefinition.md) definiert wird.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BaseMetricValue : CIM_BaseMetricValue
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
};
```

## <a name="members"></a>Member

Die **Msvm \_ BaseMetricValue-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ BaseMetricValue-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**BreakdownDimension**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt eine Aufschlüsselungsdimension aus dem **BreakdownDimensions-Array** an, das in der zugeordneten [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md)definiert ist. Dies ist die Dimension, in der dieser Satz von Metrikwerten unterteilt wird. Diese Eigenschaft wird von [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**BreakdownValue**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Definiert einen Wert der **BreakdownDimension-Eigenschaft,** die für diese Metrikwertinstanz definiert ist. Wenn **breakdownDimension** z. B. "TransactionName" ist, kann diese Eigenschaft die tatsächliche Transaktion benennen, für die dieser bestimmte Metrikwert gilt. Diese Eigenschaft wird von [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Dauer**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Zeitdauer an, für die dieser Metrikwert gültig ist. Diese Eigenschaft sollte nicht für Zeitstempel vorhanden sein, die nur für einen bestimmten Zeitpunkt gelten. Sie sollte jedoch für Werte angegeben werden, die für einen bestimmten Zeitraum (z. B. Stichprobenentnahme) gültig sind. Wenn die **Duration-Eigenschaft** vorhanden ist und nicht **NULL** ist, gibt die **TimeStamp-Eigenschaft** das Ende des Intervalls an. Diese Eigenschaft wird von [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeigename für das Objekt. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Eine Zeichenfolge, die eine Instanz dieser Klasse eindeutig identifiziert. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**MeasuredElementName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein beschreibender Name für das Element, zu dem der Metrikwert gehört (das gemessene Element). Diese Eigenschaft wird von [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**MetricDefinitionId**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Schlüssel der [**Msvm \_ BaseMetricDefinition-Instanz**](msvm-basemetricdefinition.md) für diesen Wert. Diese Eigenschaft wird von [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**MetricValue**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Wert der Metrik, die als Zeichenfolge dargestellt wird. Diese Eigenschaft wird von [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Timestamp**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Zeitpunkt an, zu dem der Metrikwert erfasst oder berechnet wurde. Beachten Sie, dass sich dies von dem Zeitpunkt unterscheidet, zu dem die Instanz erstellt wurde. Diese Eigenschaft wird von [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Volatil**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**TRUE,** wenn der Wert für den nächsten Zeitpunkt dieselbe Klasseninstanz verwendet und nur die Eigenschaftswerte ändert (z. B. **Value** oder **TimeStamp).** **True** gibt an, dass die Instanz wiederverwendet wird. **False** gibt an, dass die vorhandenen Instanzen unverändert bleiben und für den neuen Zeitpunkt eine neue Instanz erstellt wird. Diese Eigenschaft wird von [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

