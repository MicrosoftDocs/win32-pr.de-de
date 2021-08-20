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
ms.openlocfilehash: 107dc3721ee32ca7f51efd563cdd6af14af483a69a5990e0b107a153b79b9351
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014698"
---
# <a name="cim_basemetricvalue-class"></a>CIM \_ BaseMetricValue-Klasse

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

Die **CIM \_ BaseMetricValue-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ BaseMetricValue-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**BreakdownDimension**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Dimension, für die dieser Satz von Metrikwerten basierend auf der **BreakdownDimensions-Eigenschaft** des zugeordneten [**CIM \_ BaseMetricDefinition-Objekts**](cim-basemetricdefinition.md) unterteilt wird.

</dd> <dt>

**BreakdownValue**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Wert der **BreakdownDimension-Eigenschaft,** die für diesen Instanzwert definiert ist. Wenn **BreakdownDimension** beispielsweise "TransactionName" enthält, kann diese Eigenschaft die tatsächliche Transaktion benennen, für die dieser metrikspezifischen Wert gilt.

</dd> <dt>

**Dauer**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**", "**CIM \_ BaseMetricValue**.**TimeStamp**")
</dt> </dl>

Die Zeitspanne, für die dieser Metrikwert gültig ist. Diese Eigenschaft sollte nicht für Zeitstempel vorhanden sein, die nur für einen bestimmten Zeitpunkt gelten. Sie sollte jedoch für Werte definiert werden, die für einen bestimmten Zeitraum gültig sind (z. B. Sampling). Wenn die **Duration-Eigenschaft** vorhanden ist und ungleich NULL ist, sollte der **TimeStamp-Wert** das Ende des Intervalls sein.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")
</dt> </dl>

Identifiziert eine Instanz dieser Klasse innerhalb des Bereichs des enthaltenden Namespace eindeutig.

> [!IMPORTANT]
>
> Um die Eindeutigkeit innerhalb des Namespace sicherzustellen, sollte der Wert der **InstanceID-Eigenschaft** im folgenden Muster erstellt werden: *OrgID*:*LocalID*
>
> *OrgID* muss einen urheberrechtlich geschützten, markengeschützten oder anderweitig eindeutigen Namen enthalten, der sich im Besitz der Geschäftsentität befindet, die die **Instanz-ID** definiert, oder es muss sich um eine registrierte ID handeln, die von einer anerkannten globalen Autorität zugewiesen wird. Dieses Muster ähnelt der Struktur von Schemaklassennamen. Darüber hinaus muss der erste Doppelpunkt in **InstanceID** zwischen *orgID* und *LocalID* stehen, um eindeutig zu sein. Daher darf die *OrgID* keinen Doppelpunkt (":") enthalten.
>
> *LocalID* wird von der Geschäftsentität ausgewählt und sollte nicht erneut verwendet werden, um verschiedene zugrunde liegende reale Elemente zu identifizieren.
>
> Wenn das obige Muster nicht verwendet wird, muss die definierende Entität sicherstellen, dass der resultierende **InstanceID-Wert** nicht für alle **InstanceID-Eigenschaften** wiederverwendet wird, die von diesem Anbieter oder anderen Anbietern für diesen Namespace erstellt werden.
>
> Für definierte DMTF-Instanzen (Distributed Management Task Force) muss das Muster mit der *OrgID* verwendet werden, die auf CIM festgelegt ist.

 

</dd> <dt>

**MeasuredElementName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein beschreibender Name für das Element, das durch die Metrik gemessen wird.

Diese Eigenschaft ist erforderlich, wenn die Metrikdefinition keinem [**CIM \_ ManagedElement-Objekt**](cim-managedelement.md) zugeordnet ist und in anderen Fällen verwendet werden kann, um zusätzliche Informationen bereitzustellen. Dadurch können Metriken unabhängig von einem **CIM \_ ManagedElement-Objekt** erfasst werden.

Wenn dem Metrikwert mehrere [**CIM \_ ManagedElement-Objekte**](cim-managedelement.md) zugeordnet sind, können Sie eines der verwalteten Elemente auswählen, um die zusätzlichen Informationen für die Metrik zu erstellen. Die -Eigenschaft ist nicht für die Verwendung als Fremdschlüssel zum Abfragen des gemessenen Elements vorgesehen. Stattdessen sollte die Zuordnung zum **CIM \_ ManagedElement** verwendet werden.

</dd> <dt>

**MetricDefinitionId**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Erforderlich,**](/windows/desktop/WmiSdk/standard-qualifiers) [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**ID**")
</dt> </dl>

Der Schlüssel der [**CIM \_ BaseMetricDefinition-Instanz,**](cim-basemetricdefinition.md) die diesem Instanzwert zugeordnet ist.

</dd> <dt>

**MetricValue**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Eine Zeichenfolgendarstellung des Metrikwerts. Der ursprüngliche Datentyp des Metrikwerts wird im zugeordneten [**CIM \_ BaseMetricDefinition-Objekt**](cim-basemetricdefinition.md) angegeben.

</dd> <dt>

**Timestamp**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**", "**CIM \_ BaseMetricValue**.**Dauer**")
</dt> </dl>

Der Zeitpunkt, zu dem der Wert einer Metrikinstanz berechnet wird. Dies unterscheidet sich von dem Zeitpunkt, zu dem die Instanz erstellt wird. Wenn die **Volatile-Eigenschaft** true ist, ändert sich dieser Wert, sobald eine neue Momentaufnahme der Messung erstellt wird.

Eine Verwaltungsanwendung kann eine Zeitreihe von Metrikdaten erstellen, indem sie die Instanzen von **CIM \_ BaseMetricValue** abruft und sie nach ihrem **TimeStamp-Wert** sortiert.

</dd> <dt>

**Volatil**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True, wenn sich der **TimeStamp-Wert** ändert, wenn sich der Wert der Metrikinstanz ändert. False, wenn dieses Objekt unverändert bleiben muss und ein neues -Objekt für den neuen **TimeStamp-Wert** erstellt werden muss.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ ManagedElement**](cim-managedelement.md)
</dt> </dl>

 

