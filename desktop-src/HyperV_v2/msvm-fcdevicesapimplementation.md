---
description: Stellt eine Zuordnung zwischen einem Dienst Zugriffspunkt und dem logischen Gerät dar, von dem es implementiert wird.
ms.assetid: 5510c179-09e6-4762-b9b3-68ed49eafd66
title: Msvm_FcDeviceSAPImplementation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcDeviceSAPImplementation
- Msvm_FcDeviceSAPImplementation.Antecedent
- Msvm_FcDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bc40f25e3b288155e713415aa512d629b538d1cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355504"
---
# <a name="msvm_fcdevicesapimplementation-class"></a>MSVM \_ fcdevicesapimplementation-Klasse

Stellt eine Zuordnung zwischen einem Dienst Zugriffspunkt und dem logischen Gerät dar, von dem es implementiert wird. Die Kardinalität dieser Zuordnung ist m:n. Ein Dienst Zugriffspunkt (SAP) kann von mehreren logischen Geräten bereitgestellt werden, die zusammenarbeiten. Jedes Gerät kann mehr als ein SAP bereitstellen. Wenn viele logische Geräte einem einzelnen SAP zugeordnet sind, wird davon ausgegangen, dass diese Elemente zusammenarbeiten, um den Zugriffspunkt bereitzustellen. Wenn verschiedene Implementierungen eines SAP vorhanden sind, führt jede dieser Implementierungen zu einzelnen Instanziierungen des SAP-Objekts. Diese einzelnen Instanziierungen haben dann Zuordnungen zu den eindeutigen Implementierungen.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_FCPort      REF Antecedent;
  Msvm_FcEndpoint REF Dependent;
};
```

## <a name="members"></a>Member

Die **MSVM \_ fcdevicesapimplementation** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ fcdevicesapimplementation** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ fcport**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")
</dt> </dl>

Ein Verweis auf eine von **CIM \_ fcport** abgeleitete Klasse, die das logische Gerät darstellt.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **MSVM \_ fcendpoint**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")
</dt> </dl>

Ein Verweis auf eine Instanz der [**MSVM \_ fcendpoint**](msvm-fcendpoint.md) -Klasse, die den SAP darstellt, der den **Vorgänger** verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

