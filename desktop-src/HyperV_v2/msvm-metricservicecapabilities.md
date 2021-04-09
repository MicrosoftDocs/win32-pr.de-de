---
description: Beschreibt die Funktionen der zugeordneten MSVM- \_ metricservice-Instanz.
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
ms.openlocfilehash: 635e153d3184e74ea581a045e3d6d54a5fea199f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868500"
---
# <a name="msvm_metricservicecapabilities-class"></a>MSVM \_ metricservicecapabili-Klasse

Beschreibt die Funktionen der zugeordneten [**MSVM- \_ metricservice**](msvm-metricservice.md) -Instanz.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

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

Die **MSVM-Klasse " \_ metricservicecapabili"** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM- \_ metricservicecapabili-** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Hyper-V Metric Service-Funktionen" festgelegt.

</dd> <dt>

**Controllablemanagedelements**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **arrayType** ("indiziert")
</dt> </dl>

Identifiziert die Instanzen von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) , die von der zugeordneten **CIM \_ metricservice** -Instanz gesteuert werden können. Wenn diese Eigenschaft den Wert **null** hat, können alle Elemente gesteuert werden. Diese Eigenschaft wird von **CIM \_ metricservicecapabiligeerbt**.

</dd> <dt>

**Controllablemetrics**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **arrayType** ("indiziert")
</dt> </dl>

Identifiziert die Instanzen von **CIM \_ basemetricdefinition** , die von der zugeordneten **CIM \_ metricservice** -Instanz gesteuert werden können. Wenn diese Eigenschaft den Wert **null** hat, können alle Metriken gesteuert werden. Diese Eigenschaft wird von **CIM \_ metricservicecapabiligeerbt**.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "definiert Hyper-V Metric Service-Funktionen" festgelegt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeige Name für das-Objekt. Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Hyper-V Metric Service-Funktionen" festgelegt.

</dd> <dt>

**Elementnameeditsupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **ElementName** -Eigenschaft geändert werden kann. Diese Eigenschaft wird von **CIM \_ enabledlogicalelementfunktionalitäten** geerbt.

</dd> <dt>

**Elementnamemask**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Einschränkungen für **ElementName** an, ausgedrückt als regulärer Ausdruck. Diese Eigenschaft wird von **CIM \_ enabledlogicalelementfunktionalitäten** geerbt.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Managedelta Type Controller Types**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **arrayType** ("indiziert")
</dt> </dl>

Gibt den Typ des Steuer Elements an, der von der zugeordneten **CIM- \_ metricservice** -Instanz für das [**CIM- \_ managedelements**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) -Objekt unterstützt wird, das durch den Wert am selben Array Index in der Eigenschaft " **controllablemanagedelements** " Wenn diese Eigenschaft **null** ist, werden alle Steuerelement Typen unterstützt. Diese Eigenschaft wird von **CIM \_ metricservicecapabiligeerbt**.



| Wert                                                                                   | Bedeutung                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl>            | Unbekannt<br/>         |
| <dl> <dt>2</dt> </dl>            | Discrete<br/>        |
| <dl> <dt>3</dt> </dl>            | Massenvorgang<br/>            |
| <dl> <dt>4</dt> </dl>            | Both<br/>            |
| <dl> <dt>5.. 32767</dt> </dl>     | DMTF reserviert<br/>   |
| <dl> <dt>32768.. 65535</dt> </dl> | Hersteller spezifisch<br/> |



 

</dd> <dt>

**Maxelementnamelen**
</dt> <dd> <dl> <dt>

Datentyp: **unit16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxValue** (256)
</dt> </dl>

Gibt die maximal unterstützte Länge der **ElementName** -Eigenschaft an. Diese Eigenschaft wird von **CIM \_ enabledlogicalelementfunktionalitäten** geerbt.

</dd> <dt>

**Metricscontroltypes**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **arrayType** ("indiziert")
</dt> </dl>

Gibt den Typ des Steuer Elements an, der von der zugeordneten **CIM- \_ metricservice** -Instanz für die **CIM- \_ basemetricdefinition** unterstützt wird, die durch den Wert am selben Array Index in der **controllablemetrics** -Eigenschaft identifiziert wird Wenn diese Eigenschaft **null** ist, werden alle Steuerelement Typen unterstützt. Diese Eigenschaft wird von **CIM \_ metricservicecapabiligeerbt**.



| Wert                                                                                   | Bedeutung                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl>            | Unbekannt<br/>         |
| <dl> <dt>2</dt> </dl>            | Discrete<br/>        |
| <dl> <dt>3</dt> </dl>            | Massenvorgang<br/>            |
| <dl> <dt>4</dt> </dl>            | Both<br/>            |
| <dl> <dt>5.. 32767</dt> </dl>     | DMTF reserviert<br/>   |
| <dl> <dt>32768.. 65535</dt> </dl> | Hersteller spezifisch<br/> |



 

</dd> <dt>

**Requestedstaatunter stützt**
</dt> <dd> <dl> <dt>

Datentyp: **unit16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die möglichen Zustände an, die bei Verwendung der **requestStateChange** -Methode für das aktivierte logische Element angefordert werden können. Diese Eigenschaft wird von **CIM \_ enabledlogicalelementfunktionalitäten** geerbt.



| Wert                                                                         | Bedeutung              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <dt>2</dt> </dl>  | Aktiviert<br/>   |
| <dl> <dt>3</dt> </dl>  | Deaktiviert<br/>  |
| <dl> <dt>4</dt> </dl>  | Herunterfahren<br/> |
| <dl> <dt>6</dt> </dl>  | Offline<br/>   |
| <dl> <dt>7</dt> </dl>  | Test<br/>      |
| <dl> <dt>8</dt> </dl>  | Wickeln<br/>     |
| <dl> <dt>9</dt> </dl>  | Stilllegen<br/>   |
| <dl> <dt>10</dt> </dl> | Reboot<br/>    |
| <dl> <dt>11</dt> </dl> | Reset<br/>     |



 

</dd> <dt>

**SupportedMethods**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Methoden an, die vom metrikdienst unterstützt werden. Diese Eigenschaft wird von **CIM \_ metricservicecapabiligeerbt**.



| Wert                                                                                   | Bedeutung                                                                                         |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>2</dt> </dl>            | Die [**controlmetrics**](controlmetrics-msvm-metricservice.md) -Methode wird unterstützt.<br/> |
| <dl> <dt>3</dt> </dl>            | Die **controlmetricsbyclass** -Methode wird unterstützt.<br/>                                   |
| <dl> <dt>4</dt> </dl>            | Die **showmetrics** -Methode wird unterstützt.<br/>                                             |
| <dl> <dt>5</dt> </dl>            | Die **showmetricsbyclass** -Methode wird unterstützt.<br/>                                      |
| <dl> <dt>6</dt> </dl>            | Die **getmetricvalues** -Methode wird unterstützt.<br/>                                         |
| <dl> <dt>7</dt> </dl>            | Die **controlsampletimes** -Methode wird unterstützt.<br/>                                      |
| <dl> <dt>8.. 32767</dt> </dl>     | DMTF reserviert<br/>                                                                        |
| <dl> <dt>32768.. 65535</dt> </dl> | Hersteller spezifisch<br/>                                                                      |



 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ metricservicecapabilitäten**](cim-metricservicecapabilities.md)
</dt> <dt>

[**MSVM \_ metricservice**](msvm-metricservice.md)
</dt> </dl>

 

