---
description: Stellt den Instanzwert einer Metrik dar, die durch eine Instanz von CIM \_ aggregationmetricdefinition definiert wird.
ms.assetid: 663ef18a-0238-416f-9682-8809b271b4fc
title: CIM_AggregationMetricValue-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregationMetricValue
- CIM_AggregationMetricValue.AggregationTimeStamp
- CIM_AggregationMetricValue.AggregationDuration
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0af264b66838e7c039ef3f99a4f365ebab55c293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368248"
---
# <a name="cim_aggregationmetricvalue-class"></a>CIM \_ aggregationmetricvalue-Klasse

Stellt den Instanzwert einer Metrik dar, die durch eine Instanz von **CIM \_ aggregationmetricdefinition** definiert wird.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_AggregationMetricValue : CIM_BaseMetricValue
{
  datetime AggregationTimeStamp;
  datetime AggregationDuration;
};
```

## <a name="members"></a>Member

Die **CIM \_ aggregationmetricvalue** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ aggregationmetricvalue** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Aggregationduration**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ aggregationmetricvalue**".**Aggregationtimestamp**")
</dt> </dl>

Stellt die Zeitspanne dar, in der die Aggregation berechnet wurde. Der Start eines Überwachungs Intervalls, für das die Aggregations Funktion angewendet wird, wird durch Subtrahieren des **aggregationduration** -Werts vom **aggregationtimestamp** -Wert bestimmt.

</dd> <dt>

**Aggregationtimestamp**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ aggregationmetricvalue**".**Dauer**")
</dt> </dl>

Der Zeitpunkt, zu dem die Aggregations Funktion angewendet wurde, um den Wert der metrikinstanz zu bestimmen. Dies unterscheidet sich von der Zeit, zu der die Instanz erstellt wird. Der **aggregationtimestamp** -Wert ändert sich, wenn die Aggregations Funktion angewendet wird, um den Wert zu berechnen.

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

[**CIM \_ basemetricvalue**](cim-basemetricvalue.md)
</dt> </dl>

 

