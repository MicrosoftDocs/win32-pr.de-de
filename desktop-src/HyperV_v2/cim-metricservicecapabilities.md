---
description: Beschreibt die Funktionen eines CIM \_ metricservice-Objekts.
ms.assetid: 3b4da02f-5298-46d4-876c-404baca38c03
title: CIM_MetricServiceCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricServiceCapabilities
- CIM_MetricServiceCapabilities.ControllableMetrics
- CIM_MetricServiceCapabilities.MetricsControlTypes
- CIM_MetricServiceCapabilities.ControllableManagedElements
- CIM_MetricServiceCapabilities.ManagedElementControlTypes
- CIM_MetricServiceCapabilities.SupportedMethods
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f878cb0e616cb710a33d350df866160fc0eebb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363529"
---
# <a name="cim_metricservicecapabilities-class"></a>CIM \_ metricservicecapabili-Klasse

Beschreibt die Funktionen eines [**CIM \_ metricservice**](cim-metricservice.md) -Objekts.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetrics"), AMENDMENT]
class CIM_MetricServiceCapabilities : CIM_EnabledLogicalElementCapabilities
{
  string ControllableMetrics[];
  uint16 MetricsControlTypes[];
  string ControllableManagedElements[];
  uint16 ManagedElementControlTypes[];
  uint16 SupportedMethods[];
};
```

## <a name="members"></a>Member

Die **CIM \_ metricservicecapabili-** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ metricservicecapabili-** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Controllablemanagedelements**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ metricservicecapabili.****Managedelta Message Controller Types**")
</dt> </dl>

Ein Array, das Bezeichner der [**CIM- \_ managedelta**](cim-managedelement.md) -Instanzen enthält, die vom metrikdienst gesteuert werden. Die Bezeichner müssen als Web-Based Enterprise Management (WBEM)-URIs formatiert sein. Um diese Eigenschaft verwenden zu können, muss der metrikdienst das Aktivieren oder Deaktivieren von mindestens einer Metrik unterstützen, die für die **CIM- \_ managedelements** -Instanz definiert ist.

</dd> <dt>

**Controllablemetrics**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ metricservicecapabili.****Metriccontroltypes**")
</dt> </dl>

Ein Array, das Bezeichner der [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) enthält, die die vom metrikdienst verwalteten Metriken definiert. Die Bezeichner müssen als Web-Based Enterprise Management (WBEM)-URIs formatiert sein.

Um diese Eigenschaft zu verwenden, muss eine [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) -Instanz über die [**CIM \_ serviceaffectselements**](cim-serviceaffectselement.md) -Klasse einer [**CIM- \_ metricservice**](cim-metricservice.md) -Instanz zugeordnet werden. Außerdem muss der metrikdienst das Aktivieren oder Deaktivieren von mindestens einer Metrik unterstützen, die von der **CIM \_ basemetricdefinition** -Instanz definiert wird.

</dd> <dt>

**Managedelta Type Controller Types**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ metricservicecapabili.****Controllablemanagedelements**")
</dt> </dl>

Ein Array, das die Steuerelement Typen angibt, die vom metrikdienst für die verwalteten Elemente im **Steuerelement "controllablemanagedelements** " unterstützt werden. Dieses Array entspricht dem **controllablemanagedelements** -Array. Die Steuerelement Typen in diesem Array sind über das Steuerelement " **controllablemanagedelements** " mit Metriken verknüpft.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Discrete"></span><span id="discrete"></span><span id="DISCRETE"></span>

**Diskret** (2)


</dt> <dd></dd> <dt>

<span id="Bulk"></span><span id="bulk"></span><span id="BULK"></span>

**Massen** Vorgang (3)


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

**Beides** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**Hersteller spezifisch** (32768.65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Metricscontroltypes**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ metricservicecapabili.****Controllablemetrics**")
</dt> </dl>

Ein Array, das die Steuerelement Typen angibt, die vom metrikdienst unterstützt werden. Dieses Array entspricht dem **controllablemetrics** -Array. Die Steuerelement Typen in diesem Array werden Metriken über das **controllablemetrics** -Array zugeordnet.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Discrete"></span><span id="discrete"></span><span id="DISCRETE"></span>

**Diskret** (2)


</dt> <dd></dd> <dt>

<span id="Bulk"></span><span id="bulk"></span><span id="BULK"></span>

**Massen** Vorgang (3)


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

**Beides** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**Hersteller spezifisch** (32768.65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**SupportedMethods**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array, das die Namen der Methoden enthält, die vom metrikdienst unterstützt werden.

<dt>

<span id="ControlMetrics"></span><span id="controlmetrics"></span><span id="CONTROLMETRICS"></span>

**Controlmetrics** (2)


</dt> <dd></dd> <dt>

<span id="ControlMetricsByClass"></span><span id="controlmetricsbyclass"></span><span id="CONTROLMETRICSBYCLASS"></span>

**Controlmetricsbyclass** (3)


</dt> <dd></dd> <dt>

<span id="ShowMetrics"></span><span id="showmetrics"></span><span id="SHOWMETRICS"></span>

**Showmetrics** (4)


</dt> <dd></dd> <dt>

<span id="ShowMetricsByClass"></span><span id="showmetricsbyclass"></span><span id="SHOWMETRICSBYCLASS"></span>

**Showmetricsbyclass** (5)


</dt> <dd></dd> <dt>

<span id="GetMetricValues"></span><span id="getmetricvalues"></span><span id="GETMETRICVALUES"></span>

**Getmetricvalues** (6)


</dt> <dd></dd> <dt>

<span id="ControlSampleTimes"></span><span id="controlsampletimes"></span><span id="CONTROLSAMPLETIMES"></span>

**Controlsampletimes** (7)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**Hersteller spezifisch** (0X8000..)


</dt> <dd></dd> </dl>

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

[**CIM \_ enabledlogicalelementfunktionalitäten**](cim-enabledlogicalelementcapabilities.md)
</dt> </dl>

 

