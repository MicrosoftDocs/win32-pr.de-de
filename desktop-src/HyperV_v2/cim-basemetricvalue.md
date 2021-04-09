---
description: Stellt den Instanzwert einer Metrik dar.
ms.assetid: 6b272ae8-7684-45bb-bff8-6559680cc8b6
title: CIM_BaseMetricValue-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BaseMetricValue
- CIM_BaseMetricValue.InstanceID
- CIM_BaseMetricValue.MetricDefinitionId
- CIM_BaseMetricValue.MeasuredElementName
- CIM_BaseMetricValue.TimeStamp
- CIM_BaseMetricValue.Duration
- CIM_BaseMetricValue.MetricValue
- CIM_BaseMetricValue.BreakdownDimension
- CIM_BaseMetricValue.BreakdownValue
- CIM_BaseMetricValue.Volatile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ca6c90a4b6b3ef3e690c13612f69480ec5f008be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960357"
---
# <a name="cim_basemetricvalue-class"></a>CIM \_ basemetricvalue-Klasse

Stellt den Instanzwert einer Metrik dar.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_BaseMetricValue : CIM_ManagedElement
{
  string   InstanceID;
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

Die **CIM \_ basemetricvalue** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ basemetricvalue** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Breakdowndimension**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Dimension, für die dieser Satz von Metrikwerten basierend auf der **breakdowndimensions** -Eigenschaft des zugeordneten [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) -Objekts aufgeteilt wird.

</dd> <dt>

**Breakdownwert**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Wert der **breakdowndimension** -Eigenschaft, die für diesen Instanzwert definiert ist. Wenn **breakdowndimension** z. b. "transaktionname" enthält, könnte diese Eigenschaft die tatsächliche Transaktion benennen, für die dieser bestimmte Metrikwert gilt.

</dd> <dt>

**Dauer**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md)".**Timescope**","**CIM \_ basemetricvalue**.**Zeitstempel**")
</dt> </dl>

Die Zeitspanne, für die dieser Metrikwert gültig ist. Diese Eigenschaft darf nicht für Zeitstempel vorhanden sein, die nur auf einen bestimmten Zeitpunkt zutreffen, sondern sollte für Werte definiert werden, die für einen bestimmten Zeitraum gültig sind (z. Sampling). Wenn die **Duration** -Eigenschaft vorhanden ist und nicht NULL ist, sollte der **Zeitstempel** Wert das Ende des Intervalls sein.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig innerhalb des Gültigkeits Bereichs des enthaltenden Namespace.

> [!IMPORTANT]
>
> Um die Eindeutigkeit innerhalb des Namespaces sicherzustellen, sollte der Wert der **InstanceId-** Eigenschaft im folgenden Muster erstellt werden: *OrgId*:*localId*
>
> *OrgId* muss einen urheberrechtlich geschützten oder anderweitig eindeutigen Namen enthalten, der der Geschäfts Entität gehört, die die **InstanceId** definiert, oder eine registrierte ID ist, die von einer anerkannten globalen Autorität zugewiesen wird. Dieses Muster ähnelt der Struktur von Schema Klassennamen. Um die Eindeutigkeit sicherzustellen, muss der erste Doppelpunkt in **InstanceId** zwischen der *OrgId* und der *Lok-* ID liegen. Daher darf die *OrgId* keinen Doppelpunkt (': ') enthalten.
>
> *LocalId* wird von der Geschäfts Entität ausgewählt und sollte nicht erneut verwendet werden, um verschiedene zugrunde liegende reale Elemente zu identifizieren.
>
> Wenn das obige Muster nicht verwendet wird, muss die definierende Entität sicherstellen, dass der resultierende **InstanceId** -Wert nicht für **InstanceId** -Eigenschaften wieder verwendet wird, die von diesem Anbieter oder von anderen Anbietern für diesen Namespace erstellt werden.
>
> Für von DMTF (verteilte Management Task Force) definierte Instanzen muss das Muster verwendet werden, wenn die *OrgId* auf CIM festgelegt ist.

 

</dd> <dt>

**"Messredelta Name"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein beschreibender Name für das Element, das von der Metrik gemessen wird.

Diese Eigenschaft ist erforderlich, wenn die metrikdefinition keinem [**CIM \_ managedelta**](cim-managedelement.md) -Objekt zugeordnet ist und in anderen Fällen zum Bereitstellen zusätzlicher Informationen verwendet werden kann. Dadurch können Metriken unabhängig von einem CIM- **\_ managedelta** -Objekt erfasst werden.

Wenn dem Metrikwert mehrere [**CIM \_ managedelements**](cim-managedelement.md) -Objekte zugeordnet sind, können Sie eines der verwalteten Elemente auswählen, um die ergänzenden Informationen für die Metrik zu erstellen. Die-Eigenschaft ist nicht für die Verwendung als Fremdschlüssel zum Abfragen des gemessenen Elements vorgesehen. Stattdessen sollte die Zuordnung zum **CIM- \_ managedelta** verwendet werden.

</dd> <dt>

**MetricDefinitionId**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md)".**ID**")
</dt> </dl>

Der Schlüssel der [**CIM- \_ basemetricdefinition**](cim-basemetricdefinition.md) -Instanz, die diesem Instanzwert zugeordnet ist.

</dd> <dt>

**Metricvalue**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Eine Zeichen folgen Darstellung des metrikwerts. Der ursprüngliche Datentyp des metrikwerts wird im zugehörigen [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) -Objekt angegeben.

</dd> <dt>

**Zeitstempel**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md)".**Timescope**","**CIM \_ basemetricvalue**.**Dauer**")
</dt> </dl>

Der Zeitpunkt, zu dem der Wert einer metrikinstanz berechnet wird. Dies unterscheidet sich von der Zeit, zu der die Instanz erstellt wird. Wenn die **volatile** -Eigenschaft den Wert true hat, ändert sich dieser Wert immer, wenn eine neue Mess Momentaufnahme erstellt wird.

Eine Verwaltungs Anwendung kann eine Zeitreihe von Metrikdaten erstellen, indem Sie die Instanzen von **CIM \_ basemetricvalue** abruft und Sie entsprechend Ihres **Zeitstempel** Werts sortiert.

</dd> <dt>

**Ständigem**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True, wenn sich der **Zeitstempel** Wert ändert, wenn sich der Wert der metrikinstanz ändert. False, wenn dieses Objekt unverändert bleiben muss und ein neues-Objekt für den neuen **Zeitstempel** Wert erstellt wurde.

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

[**CIM- \_ managedelta**](cim-managedelement.md)
</dt> </dl>

 

