---
description: Stellt eine Zuordnung zwischen einem Dienst Zugriffspunkt und dem logischen Gerät dar, von dem es implementiert wird.
ms.assetid: C0DDB199-AD97-4DD7-8056-BD6BD0CECFA8
title: Msvm_EthernetDeviceSAPImplementation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetDeviceSAPImplementation
- Msvm_EthernetDeviceSAPImplementation.Antecedent
- Msvm_EthernetDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 96290eb0d572f4848fbf3805a44ce0ae173892c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345788"
---
# <a name="msvm_ethernetdevicesapimplementation-class"></a>MSVM- \_ Klasse "ethernetdevicesapimplementation"

Stellt eine Zuordnung zwischen einem Dienst Zugriffspunkt und dem logischen Gerät dar, von dem es implementiert wird. Die Kardinalität dieser Zuordnung ist m:n. Ein Dienst Zugriffspunkt (SAP) kann von mehreren logischen Geräten bereitgestellt werden, die zusammenarbeiten. Jedes Gerät kann mehr als ein SAP bereitstellen. Wenn viele logische Geräte einem einzelnen SAP zugeordnet sind, wird davon ausgegangen, dass diese Elemente zusammenarbeiten, um den Zugriffspunkt bereitzustellen. Wenn verschiedene Implementierungen eines SAP vorhanden sind, führt jede dieser Implementierungen zu einzelnen Instanziierungen des SAP-Objekts. Diese einzelnen Instanziierungen haben dann Zuordnungen zu den eindeutigen Implementierungen.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_EthernetPort REF Antecedent;
  Msvm_LANEndpoint REF Dependent;
};
```

## <a name="members"></a>Member

Die **MSVM-Klasse " \_ ethernetdevicesapimplementation** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM-Klasse " \_ ethernetdevicesapimplementation** " verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")
</dt> </dl>

Ein Verweis auf eine vom CIM- [**\_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) abgeleitete Klasse, die das logische Gerät darstellt.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM \_ lanendpoint**](msvm-lanendpoint.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")
</dt> </dl>

Ein Verweis auf eine Instanz der [**MSVM \_ lanendpoint**](msvm-lanendpoint.md) -Klasse, die den SAP darstellt, der den **Vorgänger** verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

