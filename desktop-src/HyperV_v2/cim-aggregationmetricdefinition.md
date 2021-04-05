---
description: Stellt die Definition einer Metrik dar, die von einem anderen Metrikwert abgeleitet ist. Ein CIM \_ aggregationmetricdefinition-Objekt muss den CIM \_ managedelta-Objekten zugeordnet werden, auf die es angewendet wird.
ms.assetid: 0059bfd6-ecf3-41f0-be6b-0ce46dfbbb18
title: CIM_AggregationMetricDefinition-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregationMetricDefinition
- CIM_AggregationMetricDefinition.ChangeType
- CIM_AggregationMetricDefinition.SimpleFunction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9a84eed5a725ebff3b39ca92bab530ef90cfca58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755448"
---
# <a name="cim_aggregationmetricdefinition-class"></a>CIM \_ aggregationmetricdefinition-Klasse

Stellt die Definition einer Metrik dar, die von einem anderen Metrikwert abgeleitet ist. Ein **CIM \_ aggregationmetricdefinition** -Objekt muss den **CIM \_ managedelta** -Objekten zugeordnet werden, auf die es angewendet wird.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_AggregationMetricDefinition : CIM_BaseMetricDefinition
{
  uint16 ChangeType = 5;
  uint16 SimpleFunction;
};
```

## <a name="members"></a>Member

Die **CIM \_ aggregationmetricdefinition** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ aggregationmetricdefinition** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**ChangeType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("ChangeType"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ aggregationmetricdefinition**".**Iscontinuous**")
</dt> </dl>

Gibt an, wie sich der Metrikwert mithilfe allgemeiner Attribute ändert, wie z. b. Richtungsänderung, Mindest-und Höchstwerte und Wrapping Semantik.

<dt>

<span id="Simple_Function"></span><span id="simple_function"></span><span id="SIMPLE_FUNCTION"></span>

**Einfache Funktion** (5)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Anbieter reserviert** (32768.65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Simplefunction**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die grundlegende Berechnung für eine zugrunde liegende Metrik, die auf den Wert dieser abgeleiteten Metrik ankommt. Diese Eigenschaft ist **null** , wenn die **ChangeType** -Eigenschaft einen anderen Wert als "5" (einfache Funktion) aufweist.

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)


</dt> <dd></dd> <dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimal** (2)


</dt> <dd>

Die Metrik meldet den niedrigsten für die zugeordneten überwachten Entität erkannten Wert. Dies wird auch als niedrige Grenze bezeichnet.

</dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (3)


</dt> <dd>

Die Metrik meldet den maximal für die zugeordneten überwachten Entität erkannten Wert. Dies wird auch als hohes Wasserzeichen bezeichnet.

</dd> <dt>

<span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>

<span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>**Durchschnitt** (4)


</dt> <dd>

Die Metrik meldet den durchschnittlichen Wert der zugrunde liegenden Metrikwerte.

</dd> <dt>

<span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>

<span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>**Median** (5)


</dt> <dd>

Die Metrik meldet den Medianwert der zugrunde liegenden Metrikwerte.

</dd> <dt>

<span id="Mode"></span><span id="mode"></span><span id="MODE"></span>

<span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Modus** (6)


</dt> <dd>

die Metrik meldet den modalen Wert der zugrunde liegenden Metrikwerte.

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (32768.65535)


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

[**CIM- \_ basemetricdefinition**](cim-basemetricdefinition.md)
</dt> </dl>

 

