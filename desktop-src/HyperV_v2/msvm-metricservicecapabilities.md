---
description: Beschreibt die Funktionen der zugeordneten Msvm \_ MetricService-Instanz.
ms.assetid: 4E24D675-8265-4B5E-9551-550510B138FE
title: Msvm_MetricServiceCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricServiceCapabilities
- Msvm_MetricServiceCapabilities.InstanceID
- Msvm_MetricServiceCapabilities.Caption
- Msvm_MetricServiceCapabilities.Description
- Msvm_MetricServiceCapabilities.ElementName
- Msvm_MetricServiceCapabilities.ElementNameEditSupported
- Msvm_MetricServiceCapabilities.MaxElementNameLen
- Msvm_MetricServiceCapabilities.RequestedStatesSupported
- Msvm_MetricServiceCapabilities.ElementNameMask
- Msvm_MetricServiceCapabilities.ControllableMetrics
- Msvm_MetricServiceCapabilities.MetricsControlTypes
- Msvm_MetricServiceCapabilities.ControllableManagedElements
- Msvm_MetricServiceCapabilities.ManagedElementControlTypes
- Msvm_MetricServiceCapabilities.SupportedMethods
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 37fed3fead642ecfc5370d55c9f8b954477406b4b276cac392d9776a0cefb338
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521330"
---
# <a name="msvm_metricservicecapabilities-class"></a>Msvm \_ MetricServiceCapabilities-Klasse

Beschreibt die Funktionen der zugeordneten [**Msvm \_ MetricService-Instanz.**](msvm-metricservice.md)

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricServiceCapabilities : CIM_MetricServiceCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Metric Service Capabilities";
  string  Description = "Defines Hyper-V Metric Service Capabilities";
  string  ElementName = "Hyper-V Metric Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  ControllableMetrics[];
  uint16  MetricsControlTypes[];
  string  ControllableManagedElements[];
  uint16  ManagedElementControlTypes[];
  uint16  SupportedMethods[];
};
```

## <a name="members"></a>Member

Die **Msvm \_ MetricServiceCapabilities-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ MetricServiceCapabilities-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und immer auf "Hyper-V Metric Service Capabilities" festgelegt.

</dd> <dt>

**ControllableManagedElements**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **ArrayType** ("Indiziert")
</dt> </dl>

Identifiziert die Instanzen von [**CIM \_ ManagedElement,**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) die von der zugeordneten **CIM \_ MetricService-Instanz** gesteuert werden können. Wenn diese Eigenschaft **NULL** ist, können alle Elemente gesteuert werden. Diese Eigenschaft wird von **CIM \_ MetricServiceCapabilities** geerbt.

</dd> <dt>

**ControllableMetrics**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **ArrayType** ("Indiziert")
</dt> </dl>

Identifiziert die Instanzen von **CIM \_ BaseMetricDefinition,** die von der zugeordneten **CIM \_ MetricService-Instanz** gesteuert werden können. Wenn diese Eigenschaft **NULL** ist, können alle Metriken gesteuert werden. Diese Eigenschaft wird von **CIM \_ MetricServiceCapabilities** geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und immer auf "Definiert Hyper-V-Metrikdienstfunktionen" festgelegt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeigename für das Objekt. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und immer auf "Hyper-V Metric Service Capabilities" festgelegt.

</dd> <dt>

**ElementNameEditSupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **ElementName-Eigenschaft** geändert werden kann. Diese Eigenschaft wird von **CIM \_ EnabledLogicalElementCapabilities** geerbt.

</dd> <dt>

**ElementNameMask**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Einschränkungen für **ElementName** an, ausgedrückt als regulärer Ausdruck. Diese Eigenschaft wird von **CIM \_ EnabledLogicalElementCapabilities** geerbt.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**ManagedElementControlTypes**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **ArrayType** ("Indiziert")
</dt> </dl>

Identifiziert den Typ des Steuerelements, das von der zugeordneten **CIM \_ MetricService-Instanz** für das [**CIM \_ ManagedElement-Objekt**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) unterstützt wird, das durch den Wert am gleichen Arrayindex in der **ControllableManagedElements-Eigenschaft** identifiziert wird. Wenn diese Eigenschaft **NULL** ist, werden alle Steuerelementtypen unterstützt. Diese Eigenschaft wird von **CIM \_ MetricServiceCapabilities** geerbt.



| Wert                                                                                   | Bedeutung                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl>            | Unbekannt<br/>         |
| <dl> <dt>2</dt> </dl>            | Discrete<br/>        |
| <dl> <dt>3</dt> </dl>            | Massenvorgang<br/>            |
| <dl> <dt>4</dt> </dl>            | Beide<br/>            |
| <dl> <dt>5..32767</dt> </dl>     | DMTF reserviert<br/>   |
| <dl> <dt>32768..65535</dt> </dl> | Anbieterspezifisch<br/> |



 

</dd> <dt>

**MaxElementNameLen**
</dt> <dd> <dl> <dt>

Datentyp: **unit16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxValue** (256)
</dt> </dl>

Gibt die maximal unterstützte Länge der **ElementName-Eigenschaft** an. Diese Eigenschaft wird von **CIM \_ EnabledLogicalElementCapabilities** geerbt.

</dd> <dt>

**MetricsControlTypes**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **ArrayType** ("Indiziert")
</dt> </dl>

Identifiziert den Typ des Steuerelements, das von der zugeordneten **CIM \_ MetricService-Instanz** für CIM **\_ BaseMetricDefinition** unterstützt wird, die durch den Wert am gleichen Arrayindex in der **ControllableMetrics-Eigenschaft** identifiziert wird. Wenn diese Eigenschaft **NULL** ist, werden alle Steuerelementtypen unterstützt. Diese Eigenschaft wird von **CIM \_ MetricServiceCapabilities** geerbt.



| Wert                                                                                   | Bedeutung                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl>            | Unbekannt<br/>         |
| <dl> <dt>2</dt> </dl>            | Discrete<br/>        |
| <dl> <dt>3</dt> </dl>            | Massenvorgang<br/>            |
| <dl> <dt>4</dt> </dl>            | Beide<br/>            |
| <dl> <dt>5..32767</dt> </dl>     | DMTF reserviert<br/>   |
| <dl> <dt>32768..65535</dt> </dl> | Anbieterspezifisch<br/> |



 

</dd> <dt>

**RequestedStatesSupported**
</dt> <dd> <dl> <dt>

Datentyp: **unit16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die möglichen Zustände an, die angefordert werden können, wenn die **RequestStateChange-Methode** für das aktivierte logische Element verwendet wird. Diese Eigenschaft wird von **CIM \_ EnabledLogicalElementCapabilities** geerbt.



| Wert                                                                         | Bedeutung              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <dt>2</dt> </dl>  | Aktiviert<br/>   |
| <dl> <dt>3</dt> </dl>  | Deaktiviert<br/>  |
| <dl> <dt>4</dt> </dl>  | Herunterfahren<br/> |
| <dl> <dt>6</dt> </dl>  | Offline<br/>   |
| <dl> <dt>7</dt> </dl>  | Test<br/>      |
| <dl> <dt>8</dt> </dl>  | Verschieben<br/>     |
| <dl> <dt>9</dt> </dl>  | Stilllegen<br/>   |
| <dl> <dt>10</dt> </dl> | Neustart<br/>    |
| <dl> <dt>11</dt> </dl> | Reset<br/>     |



 

</dd> <dt>

**SupportedMethods**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die vom Metrikdienst unterstützten Methoden an. Diese Eigenschaft wird von **CIM \_ MetricServiceCapabilities** geerbt.



| Wert                                                                                   | Bedeutung                                                                                         |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>2</dt> </dl>            | Die [**ControlMetrics-Methode**](controlmetrics-msvm-metricservice.md) wird unterstützt.<br/> |
| <dl> <dt>3</dt> </dl>            | Die **ControlMetricsByClass-Methode** wird unterstützt.<br/>                                   |
| <dl> <dt>4</dt> </dl>            | Die **ShowMetrics-Methode** wird unterstützt.<br/>                                             |
| <dl> <dt>5</dt> </dl>            | Die **ShowMetricsByClass-Methode** wird unterstützt.<br/>                                      |
| <dl> <dt>6</dt> </dl>            | Die **GetMetricValues-Methode** wird unterstützt.<br/>                                         |
| <dl> <dt>7</dt> </dl>            | Die **ControlSampleTimes-Methode** wird unterstützt.<br/>                                      |
| <dl> <dt>8..32767</dt> </dl>     | DMTF reserviert<br/>                                                                        |
| <dl> <dt>32768..65535</dt> </dl> | Anbieterspezifisch<br/>                                                                      |



 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ MetricServiceCapabilities**](cim-metricservicecapabilities.md)
</dt> <dt>

[**Msvm \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

