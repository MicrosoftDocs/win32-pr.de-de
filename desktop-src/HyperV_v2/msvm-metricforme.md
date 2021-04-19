---
description: Diese Zuordnung verknüpft ein verwaltetes Element mit den Metrikwerten, die für das Element beibehalten werden.
ms.assetid: 89b43736-90ae-49e0-a0ed-7918ddec8558
title: Msvm_MetricForME-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricForME
- Msvm_MetricForME.Antecedent
- Msvm_MetricForME.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 554f77390737b336b8660d09f737049be193b448
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353960"
---
# <a name="msvm_metricforme-class"></a>MSVM- \_ metricforme-Klasse

Diese Zuordnung verknüpft ein verwaltetes Element mit den Metrikwerten, die für das Element beibehalten werden.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricForME : CIM_MetricForME
{
  CIM_ManagedElement  REF Antecedent;
  CIM_BaseMetricValue REF Dependent;
};
```

## <a name="members"></a>Member

Die **MSVM- \_ metricforme** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM- \_ metricforme** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Verweis auf eine Instanz der [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) -Klasse, die das verwaltete Element darstellt, dessen Metriken durch **abhängige** beibehalten definiert wurden. Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)geerbt.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: * * * * CIM \_ basemetricvalue * * * *
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Verweis auf eine Instanz der **CIM \_ basemetricvalue** -Klasse, die die Metrik darstellt, die der **Vorgänger** für Sie erfasst hat. Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)geerbt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

