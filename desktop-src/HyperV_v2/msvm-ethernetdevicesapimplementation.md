---
description: 'Msvm_EthernetDeviceSAPImplementation -Klasse: Stellt eine Zuordnung zwischen einem Dienstzugriffspunkt und dem logischen Gerät dar, das ihn implementiert.'
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
ms.openlocfilehash: 0cabf80b7e55513fc5fc31b744db8cbc973ccd15bcda170804c754850d65dbfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119524980"
---
# <a name="msvm_ethernetdevicesapimplementation-class"></a>Msvm \_ EthernetDeviceSAPImplementation-Klasse

Stellt eine Zuordnung zwischen einem Dienstzugriffspunkt und dem logischen Gerät dar, das ihn implementiert. Die Kardinalität dieser Zuordnung ist m:n. Ein Dienstzugriffspunkt (SAP) kann von mehreren logischen Geräten bereitgestellt werden, die zusammen betrieben werden. Jedes Gerät kann mehrere SAP-Geräte bereitstellen. Wenn viele logische Geräte einem einzelnen SAP zugeordnet sind, wird davon ausgegangen, dass diese Elemente zusammen ausgeführt werden, um den Zugriffspunkt bereitzustellen. Wenn unterschiedliche Implementierungen eines SAP vorhanden sind, würde jede dieser Implementierungen zu einzelnen Instanziierungen des SAP-Objekts führen. Diese einzelnen Instanziierungen verfügen dann über Zuordnungen zu den eindeutigen Implementierungen.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

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

Die **Msvm \_ EthernetDeviceSAPImplementation-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ EthernetDeviceSAPImplementation-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")
</dt> </dl>

Ein Verweis auf eine von [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) abgeleitete Klasse, die das logische Gerät darstellt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **[ **Msvm \_ LANEndpoint**](msvm-lanendpoint.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Abhängig")
</dt> </dl>

Ein Verweis auf eine Instanz der [**Msvm \_ LANEndpoint-Klasse,**](msvm-lanendpoint.md) die den SAP darstellt, der den **Vorgänger** verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

