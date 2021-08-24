---
description: Stellt ein Ressourcenpoolelement der Microsoft Windows Hyper-V-Plattform dar.
ms.assetid: DF48E8A6-240F-44E9-9DA3-1E6694396F10
title: Msvm_ResourcePoolComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolComponent
- Msvm_ResourcePoolComponent.CLSID
- Msvm_ResourcePoolComponent.Context
- Msvm_ResourcePoolComponent.Enabled
- Msvm_ResourcePoolComponent.Name
- Msvm_ResourcePoolComponent.AllocationCapabilitiesClassName
- Msvm_ResourcePoolComponent.ResourcePoolClassName
- Msvm_ResourcePoolComponent.ResourcePoolSettingDataClassName
- Msvm_ResourcePoolComponent.PhysicalDeviceClassName
- Msvm_ResourcePoolComponent.WmiFactoryCLSID
- Msvm_ResourcePoolComponent.MaxParentPools
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 470317d3afd961ad74eb788ebdb70e67617749446fa4a432f40f00f43214cd92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535610"
---
# <a name="msvm_resourcepoolcomponent-class"></a>Msvm \_ ResourcePoolComponent-Klasse

Stellt ein Ressourcenpoolelement der Microsoft Windows Hyper-V-Plattform dar.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
class Msvm_ResourcePoolComponent : Msvm_VirtualizationComponent
{
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  Name;
  string  AllocationCapabilitiesClassName;
  string  ResourcePoolClassName;
  string  ResourcePoolSettingDataClassName = "Msvm_ResourcePoolSettingData";
  string  PhysicalDeviceClassName;
  string  WmiFactoryCLSID;
  uint8   MaxParentPools = 0;
};
```

## <a name="members"></a>Member

Die **Msvm \_ ResourcePoolComponent-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ ResourcePoolComponent-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AllocationCapabilitiesClassName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der von [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities) abgeleiteten Klasse, die die Zuordnungsfunktionen dieses Ressourcenpools beschreibt.

</dd> <dt>

**Clsid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine **GUID,** die den Klassenbezeichner des COM-Objekts des Diensts darstellt. Diese Eigenschaft wird von [**Msvm \_ VirtualizationComponent geerbt.**](msvm-virtualizationcomponent.md)

</dd> <dt>

**Context**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Kontext, in dem das neu erstellte Objekt ausgeführt wird. Dieser Wert wird im *dwClsContext-Parameter* an **CoCreateInstance übergeben.** Diese Eigenschaft wird von [**Msvm \_ VirtualizationComponent geerbt**](msvm-virtualizationcomponent.md)und immer auf 1 festgelegt.

</dd> <dt>

**Aktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True,** wenn diese Instanz aktiviert ist und zum Abschließen von Clientanforderungen verwendet werden kann. andernfalls **False.** Diese Eigenschaft wird von [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)geerbt und immer auf **True festgelegt.**

</dd> <dt>

**MaxParentPools**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Anzahl von übergeordneten Ressourcenpools, die ein untergeordneter Pool unterstützt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Eine sprachneutrale Zeichenfolge, die das Element eindeutig identifiziert. Das folgende Format wird empfohlen, um Namenskonflikte zu vermeiden: \| \| "Herstellerkomponentenversion". Dieser Name stellt beispielsweise Version 1.0 der Microsoft Emulated Network Port Component dar: "Microsoft \| EmulatedNetworkPortComponent \| V1.0". Diese Eigenschaft wird von [**Msvm \_ VirtualizationComponent geerbt.**](msvm-virtualizationcomponent.md)

</dd> <dt>

**PhysicalDeviceClassName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) abgeleiteten Klasse, die das physische Gerät implementiert, von dem dieser Pool Ressourcen zuteilen. Diese Eigenschaft kann NULL **sein,** wenn die aus diesem Pool zugeordnete virtuelle Geräteklasse mit der physischen Geräteklasse identisch ist.

</dd> <dt>

**ResourcePoolClassName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Klasse, die von [**CIM \_ ResourcePool abgeleitet wurde,**](/previous-versions//cc136903(v=vs.85)) die den Ressourcenpool implementiert.

</dd> <dt>

**ResourcePoolSettingDataClassName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) abgeleiteten Klasse, die die nicht zuordnungsbezogenen Einstellungen des Ressourcenpools beschreibt.

</dd> <dt>

**WmiFactoryCLSID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine **GUID,** die den Klassenbezeichner der WMI-Objekt factory der Komponente darstellt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ ResourcePoolComponent-Klasse** kann durch UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Ende des Supports (Client)<br/>    | Windows 8.1<br/>                                                                                  |
| Ende des Supports (Server)<br/>    | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ VirtualizationComponent**](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)
</dt> </dl>

 

