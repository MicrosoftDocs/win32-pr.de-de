---
description: Stellt eine Zuordnung von metrikwertobjekten mit ihren metrikdefinitionen dar.
ms.assetid: 98ad9390-78b4-4c18-b068-d05efa2f1866
title: Msvm_MetricInstance-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricInstance
- Msvm_MetricInstance.Antecedent
- Msvm_MetricInstance.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab17dce339e866fb22654a0bd75c6f3945d320a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360525"
---
# <a name="msvm_metricinstance-class"></a>MSVM \_ metricinstance-Klasse

Stellt eine Zuordnung von metrikwertobjekten mit ihren metrikdefinitionen dar. Diese Zuordnung verknüpft eine Instanz von [**MSVM \_ basemetricvalue**](msvm-basemetricvalue.md) mit der [**MSVM \_ basemetricdefinition**](msvm-basemetricdefinition.md).

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricInstance : CIM_MetricInstance
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a>Member

Die **MSVM \_ metricinstance** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ metricinstance** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: * * * * CIM \_ managedelta * * * *
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Ein Verweis auf eine Instanz der [**MSVM \_ basemetricdefinition**](msvm-basemetricdefinition.md) -Klasse, die die metrikdefinitionen darstellt.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: * * * * CIM \_ managedelta * * * *
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Ein Verweis auf eine Instanz der [**MSVM \_ basemetricvalue**](msvm-basemetricvalue.md) -Klasse, die die Metriken darstellt, die vom **Vorgänger** abhängig sind.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




