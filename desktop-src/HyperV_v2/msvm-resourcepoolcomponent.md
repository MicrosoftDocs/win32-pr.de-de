---
description: Stellt ein Ressourcenpool Element der Microsoft Windows Hyper-V-Plattform dar.
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
ms.openlocfilehash: a0cf64a9e01d904aa4e6c6ec263fdeec92eb7c94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350295"
---
# <a name="msvm_resourcepoolcomponent-class"></a>MSVM \_ resourcepoolcomponent-Klasse

Stellt ein Ressourcenpool Element der Microsoft Windows Hyper-V-Plattform dar.

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

Die **MSVM \_ resourcepoolcomponent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ resourcepoolcomponent** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Zuordnung von "Zuweisung Name"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der von [**CIM \_ allocationfunktionalitäten**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities) abgeleiteten Klasse, die die Zuordnungs Funktionen dieses Ressourcenpools beschreibt.

</dd> <dt>

**CLSID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine **GUID** , die den Klassen Bezeichner des COM-Objekts des dienstanders darstellt. Diese Eigenschaft wird von [**MSVM \_ virtualizationcomponent**](msvm-virtualizationcomponent.md)geerbt.

</dd> <dt>

**Context**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Kontext, in dem das neu erstellte-Objekt ausgeführt wird. Dieser Wert wird im *dwClsContext* -Parameter an **cokreateingestance** übergeben. Diese Eigenschaft wird von [**MSVM \_ virtualizationcomponent**](msvm-virtualizationcomponent.md)geerbt und ist immer auf 1 festgelegt.

</dd> <dt>

**Aktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** , wenn diese Instanz aktiviert ist und verwendet werden kann, um Client Anforderungen abzuschließen. andernfalls **false**. Diese Eigenschaft wird von [**MSVM \_ virtualizationcomponent**](msvm-virtualizationcomponent.md)geerbt und ist immer auf " **true**" festgelegt.

</dd> <dt>

**Maxparser-Pools**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Anzahl von übergeordneten Ressourcenpools, die von einem untergeordneten Pool unterstützt werden.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Eine sprachneutrale Zeichenfolge, die das Element eindeutig identifiziert. Das folgende Format wird vorgeschlagen, um Namenskonflikte zu vermeiden: "Hersteller \| Komponenten \| Version". Dieser Name repräsentiert beispielsweise Version 1,0 der Microsoft emulierten Netzwerk Port Komponente: "Microsoft \| emulatednetworkportcomponent \| v 1.0". Diese Eigenschaft wird von [**MSVM \_ virtualizationcomponent**](msvm-virtualizationcomponent.md)geerbt.

</dd> <dt>

**Physicalenviceclassname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) abgeleiteten Klasse, die das physische Gerät implementiert, von dem dieser Pool Ressourcen freigibt. Diese Eigenschaft kann **null** sein, wenn die von diesem Pool zugewiesene virtuelle Geräteklasse mit der Klasse des physischen Geräts identisch ist.

</dd> <dt>

**Resourcepoolclassname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Klasse, die von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85)) abgeleitet wird und den Ressourcenpool implementiert.

</dd> <dt>

**Resourcepoolsettingdataclassname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) abgeleiteten Klasse, die die nicht Zuordnungs bezogenen Einstellungen des Ressourcenpools beschreibt.

</dd> <dt>

**Wmifactoriyclsid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine **GUID** , die den Klassen Bezeichner der WMI-Objektfactory der Komponente darstellt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM \_ resourcepoolcomponent** -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Ende des Supports (Client)<br/>    | Windows 8.1<br/>                                                                                  |
| Ende des Supports (Server)<br/>    | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ virtualizationcomponent**](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[**MSVM \_ virtualizationcomponent**](msvm-virtualizationcomponent.md)
</dt> </dl>

 

