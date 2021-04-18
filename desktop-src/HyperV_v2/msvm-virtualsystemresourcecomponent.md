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
ms.openlocfilehash: 81c2d31a6497325ac77003ded266333518de890a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344255"
---
# <a name="msvm_virtualsystemresourcecomponent-class"></a>MSVM \_ virtualsystemresourcecomponent-Klasse

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

Die **MSVM \_ virtualsystemresourcecomponent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ virtualsystemresourcecomponent** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Additionalclassnames**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von Zeichen folgen, das zusätzliche nicht Zuordnungs Klassen enthält, die von dieser **MSVM \_ virtualsystemresourcecomponent** -Instanz bereitgestellt werden. Diese Klassen müssen von weder [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) noch [**CIM \_ resourcezucationsettingdata abgeleitet werden**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**CLSID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine GUID, die den Klassen Bezeichner des COM-Objekts des dienstanders darstellt. Diese Eigenschaft wird von [**MSVM \_ virtualizationcomponent**](msvm-virtualizationcomponent.md)geerbt.

</dd> <dt>

**Context**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Kontext, in dem das neu erstellte-Objekt ausgeführt wird. Dieser Wert wird im *dwClsContext* -Parameter an [**cokreateingestance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)übergeben. Diese Eigenschaft wird von [**MSVM \_ virtualizationcomponent**](msvm-virtualizationcomponent.md)geerbt und ist immer auf 1 festgelegt.

</dd> <dt>

**Aktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** , wenn diese Instanz aktiviert ist und verwendet werden kann, um Client Anforderungen abzuschließen. andernfalls **false**. Diese Eigenschaft wird von [**MSVM \_ virtualizationcomponent**](msvm-virtualizationcomponent.md)geerbt und ist immer auf " **true**" festgelegt.

</dd> <dt>

**Hotadd**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** , wenn diese Instanz einem virtuellen Computer hinzugefügt werden kann. andernfalls **false**. Der Standardwert ist **False**.

</dd> <dt>

**Baum verschieben**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** , wenn diese Instanz von einem virtuellen Computer entfernt werden kann. andernfalls **false**. Der Standardwert ist **False**.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Eine sprachneutrale Zeichenfolge, die den Dienst eindeutig identifiziert. Das folgende Format wird vorgeschlagen, um Namenskonflikte zu vermeiden: "Hersteller \| Komponenten \| Version". Dieser Name repräsentiert beispielsweise Version 1,0 der Microsoft emulierten Netzwerk Port Komponente: "Microsoft \| emulatednetworkportcomponent \| v 1.0". Diese Eigenschaft wird von [**MSVM \_ virtualizationcomponent**](msvm-virtualizationcomponent.md)geerbt.

</dd> <dt>

**Type**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Beziehung des WMI-Objekts, das hier mit dem virtuellen Gerät beschrieben wird.



| Wert                                                                                                                                                                                                                                                           | Bedeutung                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_Not_Changeable_"></span><span id="_not_changeable_"></span><span id="_NOT_CHANGEABLE_"></span><dl> <dt>**"Nicht änderbar"**</dt> <dt>0</dt> </dl> |                                                                                                                                                                                                                |
| <span id="_Singleton_"></span><span id="_singleton_"></span><span id="_SINGLETON_"></span><dl> <dt>**"Singleton"**</dt> <dt>1</dt> </dl>                     | Singleton ist ein WMI-Objekt der obersten Ebene, das 1:1 an ein virtuelles Gerät gebunden ist und nur einmal pro virtuellem Computer vorhanden sein kann. Dies ist der Standardwert.<br/>                                                  |
| <span id="_MultiInstance_"></span><span id="_multiinstance_"></span><span id="_MULTIINSTANCE_"></span><dl> <dt>**"MultiInstance"**</dt> <dt>2</dt> </dl>     | MultiInstance ist ein WMI-Objekt der obersten Ebene, das mehrmals pro virtuellem Computer vorhanden sein kann und 1:1 an ein virtuelles Gerät gebunden ist.<br/>                                                                    |
| <span id="_Subdevice_"></span><span id="_subdevice_"></span><span id="_SUBDEVICE_"></span><dl> <dt>**"Subdevice"**</dt> <dt>3</dt> </dl>                     | Bei dem Subgerät handelt es sich um ein WMI-Objekt, das nicht über einen übergeordneten Verweis verfügt, sondern nur von einem virtuellen Gerät gesteuert wird, das nur einmal pro virtuellem Computer Das WMI-Objekt kann jedoch vielfachen vorhanden sein.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM \_ virtualsystemresourcecomponent** -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

 

