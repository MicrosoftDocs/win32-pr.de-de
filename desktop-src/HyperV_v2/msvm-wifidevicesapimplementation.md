---
description: Eine Zuordnung zwischen einem Dienst Zugriffspunkt (SAP) und seiner Implementierung.
ms.assetid: d1d99299-f2d9-4025-a48d-cf8180f2f7af
title: Msvm_WiFiDeviceSAPImplementation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiDeviceSAPImplementation
- Msvm_WiFiDeviceSAPImplementation.Antecedent
- Msvm_WiFiDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8debec96efb93e60ec18d75b62ffa0d13b0e0a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862463"
---
# <a name="msvm_wifidevicesapimplementation-class"></a>MSVM- \_ wifidevicesapimplementation-Klasse

Eine Zuordnung zwischen einem Dienst Zugriffspunkt (SAP) und seiner Implementierung. Die Kardinalität dieser Zuordnung ist m:n. Ein SAP kann von mehreren logischen Geräten bereitgestellt werden, die zusammenarbeiten. Jedes Gerät kann mehr als ein SAP bereitstellen. Wenn viele logische Geräte einem einzelnen SAP zugeordnet sind, wird davon ausgegangen, dass diese Elemente zusammenarbeiten, um den Zugriffspunkt bereitzustellen. Wenn verschiedene Implementierungen eines SAP vorhanden sind, führt jede dieser Implementierungen zu einzelnen Instanziierungen des SAP-Objekts. Diese einzelnen Instanziierungen haben dann Zuordnungen zu den eindeutigen Implementierungen.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  Msvm_WiFiPort     REF Antecedent;
  Msvm_WiFiEndpoint REF Dependent;
};
```

## <a name="members"></a>Member

Die **MSVM \_ wifidevicesapimplementation** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ wifidevicesapimplementation** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM- \_ wifiport**](msvm-wifiport.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")
</dt> </dl>

Eine Instanz der [**MSVM- \_ wifiport**](msvm-wifiport.md) -Klasse, die das logische Gerät darstellt.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM \_ wifiendpoint**](msvm-wifiendpoint.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")
</dt> </dl>

Eine Instanz der [**MSVM \_ wifiendpoint**](msvm-wifiendpoint.md) -Klasse, die den mithilfe des logischen Geräts implementierten Dienst Zugriffspunkt darstellt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

