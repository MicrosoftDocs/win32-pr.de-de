---
description: Stellt einen Dienst für virtuelle Geräte der Microsoft Windows Hyper-V-Plattform dar.
ms.assetid: 865D83E1-0FC6-4F96-94BB-AA5116890127
title: Msvm_VirtualSystemResourceComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemResourceComponent
- Msvm_VirtualSystemResourceComponent.Name
- Msvm_VirtualSystemResourceComponent.CLSID
- Msvm_VirtualSystemResourceComponent.Context
- Msvm_VirtualSystemResourceComponent.Enabled
- Msvm_VirtualSystemResourceComponent.AdditionalClassNames
- Msvm_VirtualSystemResourceComponent.Type
- Msvm_VirtualSystemResourceComponent.HotAdd
- Msvm_VirtualSystemResourceComponent.HotRemove
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0758858e9e45066cdfaddf36616c7861bbae914b12e3698665f8650c6c57d67c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119340170"
---
# <a name="msvm_virtualsystemresourcecomponent-class"></a>Msvm \_ VirtualSystemResourceComponent-Klasse

Stellt einen Dienst für virtuelle Geräte der Microsoft Windows Hyper-V-Plattform dar.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
class Msvm_VirtualSystemResourceComponent : Msvm_VirtualizationComponent
{
  string  Name;
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  AdditionalClassNames[];
  uint16  Type = 1;
  boolean HotAdd = False;
  boolean HotRemove = False;
};
```

## <a name="members"></a>Member

Die **Msvm \_ VirtualSystemResourceComponent-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ VirtualSystemResourceComponent-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AdditionalClassNames**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von Zeichenfolgen, die zusätzliche Klassen enthalten, die keine Zuordnungen sind, die von dieser **Msvm \_ VirtualSystemResourceComponent-Instanz zur Hand gestellt** werden. Diese Klassen dürfen weder von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) noch [**von CIM \_ ResourceAllocationSettingData ableiten.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**Clsid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine GUID, die den Klassenbezeichner des COM-Objekts des Diensts darstellt. Diese Eigenschaft wird von [**Msvm \_ VirtualizationComponent geerbt.**](msvm-virtualizationcomponent.md)

</dd> <dt>

**Context**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Kontext, in dem das neu erstellte Objekt ausgeführt wird. Dieser Wert wird im *dwClsContext-Parameter* an [**CoCreateInstance übergeben.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) Diese Eigenschaft wird von [**Msvm \_ VirtualizationComponent geerbt**](msvm-virtualizationcomponent.md)und immer auf 1 festgelegt.

</dd> <dt>

**Aktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True,** wenn diese Instanz aktiviert ist und zum Abschließen von Clientanforderungen verwendet werden kann. andernfalls **False.** Diese Eigenschaft wird von [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)geerbt und immer auf **True festgelegt.**

</dd> <dt>

**HotAdd**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True,** wenn diese Instanz einem virtuellen Computer hinzugefügt werden kann. andernfalls **False.** Der Standardwert ist **False**.

</dd> <dt>

**HotRemove**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**TRUE,** wenn diese Instanz von einem virtuellen Computer entfernt werden kann. andernfalls **False.** Der Standardwert ist **False**.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Eine sprachneutrale Zeichenfolge, die den Dienst eindeutig identifiziert. Das folgende Format wird empfohlen, um Namenskonflikte zu vermeiden: \| \| "Herstellerkomponentenversion". Dieser Name stellt beispielsweise Version 1.0 der Microsoft Emulated Network Port Component dar: "Microsoft \| EmulatedNetworkPortComponent \| V1.0". Diese Eigenschaft wird von [**Msvm \_ VirtualizationComponent geerbt.**](msvm-virtualizationcomponent.md)

</dd> <dt>

**Typ**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Beziehung des WMI-Objekts, das hier mit dem virtuellen Gerät beschrieben wird.



| Wert                                                                                                                                                                                                                                                           | Bedeutung                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_Not_Changeable_"></span><span id="_not_changeable_"></span><span id="_NOT_CHANGEABLE_"></span><dl> <dt>**"Not Changeable"**</dt> <dt>0</dt> </dl> |                                                                                                                                                                                                                |
| <span id="_Singleton_"></span><span id="_singleton_"></span><span id="_SINGLETON_"></span><dl> <dt>**"Singleton"**</dt> <dt>1</dt> </dl>                     | Singleton ist ein WMI-Objekt der obersten Ebene, das 1:1 an ein virtuelles Gerät gebunden ist und nur einmal pro virtuellem Computer vorhanden sein kann. Dies ist der Standardwert.<br/>                                                  |
| <span id="_MultiInstance_"></span><span id="_multiinstance_"></span><span id="_MULTIINSTANCE_"></span><dl> <dt>**"MultiInstance"**</dt> <dt>2</dt> </dl>     | MultiInstance ist ein WMI-Objekt der obersten Ebene, das mehrmals pro virtuellem Computer vorhanden sein kann und 1:1 an ein virtuelles Gerät gebunden ist.<br/>                                                                    |
| <span id="_Subdevice_"></span><span id="_subdevice_"></span><span id="_SUBDEVICE_"></span><dl> <dt>**"Subdevice"**</dt> <dt>3</dt> </dl>                     | Subdevice ist ein WMI-Objekt, das über keinen übergeordneten Verweis verfügt, aber nur von einem virtuellen Gerät gesteuert wird, das nur einmal pro virtuellem Computer vorhanden sein kann. Das WMI-Objekt kann jedoch mehrfach vorhanden sein.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ VirtualSystemResourceComponent-Klasse** kann durch UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

 

