---
description: 'Msvm_WiFiDeviceSAPImplementation Klasse: Eine Zuordnung zwischen einem Dienstzugriffspunkt (SAP) und seiner Implementierung.'
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
ms.openlocfilehash: 31200fc05e87a15b00463903a21a4e1822df50d9f286162ee75e7bbe4da0daa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980420"
---
# <a name="msvm_wifidevicesapimplementation-class"></a>Msvm \_ WiFiDeviceSAPImplementation-Klasse

Eine Zuordnung zwischen einem Dienstzugriffspunkt (SAP) und seiner Implementierung. Die Kardinalität dieser Zuordnung ist n:n. Ein SAP kann von mehr als einem logischen Gerät bereitgestellt werden, das in Verbindung ausgeführt wird. Jedes Gerät kann mehrere SAP-Daten bereitstellen. Wenn viele logische Geräte einem einzelnen SAP zugeordnet sind, wird davon ausgegangen, dass diese Elemente zusammen zum Bereitstellen des Zugriffspunkts verwendet werden. Wenn verschiedene Implementierungen eines SAP vorhanden sind, würde jede dieser Implementierungen zu einzelnen Instanziierungen des SAP-Objekts führen. Diese einzelnen Instanziierungen würden dann Zuordnungen zu den eindeutigen Implementierungen haben.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

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

Die **Msvm \_ WiFiDeviceSAPImplementation-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ WiFiDeviceSAPImplementation-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **[ **Msvm \_ WiFiPort**](msvm-wifiport.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorerst")
</dt> </dl>

Eine Instanz der [**Msvm \_ WiFiPort-Klasse,**](msvm-wifiport.md) die das logische Gerät darstellt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **[ **Msvm \_ WiFiEndpoint**](msvm-wifiendpoint.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("Abhängig")
</dt> </dl>

Eine Instanz der [**Msvm \_ WiFiEndpoint-Klasse,**](msvm-wifiendpoint.md) die den dienstzugriffspunkt darstellt, der mit dem logischen Gerät implementiert wurde.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

