---
description: Beschreibt die Funktionen des zugeordneten MSVM \_ virtualethernetzwitchmanagementservice.
ms.assetid: daed7a02-bae8-4bda-abc6-0657df7dc4f8
title: Msvm_VirtualEthernetSwitchManagementCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementCapabilities
- Msvm_VirtualEthernetSwitchManagementCapabilities.InstanceID
- Msvm_VirtualEthernetSwitchManagementCapabilities.Caption
- Msvm_VirtualEthernetSwitchManagementCapabilities.Description
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementName
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementNameEditSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.MaxElementNameLen
- Msvm_VirtualEthernetSwitchManagementCapabilities.RequestedStatesSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementNameMask
- Msvm_VirtualEthernetSwitchManagementCapabilities.VirtualSystemTypesSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.SynchronousMethodsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.AsynchronousMethodsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.IndicationsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.IOVSupport
- Msvm_VirtualEthernetSwitchManagementCapabilities.IOVSupportReasons
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d66d73773b956ecbbbf4ca102b18bb6f8ece4190
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373115"
---
# <a name="msvm_virtualethernetswitchmanagementcapabilities-class"></a>MSVM \_ virtualethernetzwitchmanagementfunktionalitäten-Klasse

Beschreibt die Funktionen des zugeordneten [**MSVM \_ virtualethernetzwitchmanagementservice**](msvm-virtualethernetswitchmanagementservice.md).

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchManagementCapabilities : CIM_VirtualSystemManagementCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Virtual Ethernet Switch Management Service Capabilities";
  string  Description = "Defines Virtual Ethernet Switch Management Service Capabilities";
  string  ElementName = "Hyper-V Virtual Ethernet Switch Management Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  VirtualSystemTypesSupported[];
  uint16  SynchronousMethodsSupported[];
  uint16  AsynchronousMethodsSupported[];
  uint16  IndicationsSupported[];
  boolean IOVSupport;
  string  IOVSupportReasons[];
};
```

## <a name="members"></a>Member

Die **MSVM \_ virtualethernetzwitchmanagementfunktionsklasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ virtualethernetzwitchmanagementfunktionalitäten** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Asynchronousmethodssupported**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("CIM \_ virtualsystemmanagementfunktionalitäten. asynchronousmethodssupported")
</dt> </dl>

Ein Array von Methoden bezeichgern, von denen jedes eine Methode der [**MSVM \_ virtualethernettwitchmanagementservice**](msvm-virtualethernetswitchmanagementservice.md) -Klasse identifiziert, die asynchron von der-Implementierung unterstützt wird. Diese Eigenschaft wird von **CIM \_ virtualsystemmanagementfunktionalitäten** geerbt.

<dt>

<span id="DefineSystem"></span><span id="definesystem"></span><span id="DEFINESYSTEM"></span>

**Definesystem** (2)


</dt> <dd></dd> <dt>

<span id="DestroySystem"></span><span id="destroysystem"></span><span id="DESTROYSYSTEM"></span>

**Destroysystem** (3)


</dt> <dd></dd> <dt>

<span id="DestroySystemConfiguration"></span><span id="destroysystemconfiguration"></span><span id="DESTROYSYSTEMCONFIGURATION"></span>

**Destroysystemconfiguration** (4)


</dt> <dd></dd> <dt>

<span id="ModifyResourceSettings"></span><span id="modifyresourcesettings"></span><span id="MODIFYRESOURCESETTINGS"></span>

**Modifyresourcesettings** (5)


</dt> <dd></dd> <dt>

<span id="ModifySystemSettings"></span><span id="modifysystemsettings"></span><span id="MODIFYSYSTEMSETTINGS"></span>

**Modifysystemsettings** (6)


</dt> <dd></dd> <dt>

<span id="RemoveResources"></span><span id="removeresources"></span><span id="REMOVERESOURCES"></span>

**Removeresources** (7)


</dt> <dd></dd> <dt>

<span id="SelectSystemConfiguration"></span><span id="selectsystemconfiguration"></span><span id="SELECTSYSTEMCONFIGURATION"></span>

**Selectsystemconfiguration** (8)


</dt> <dd></dd> <dt>

<span id="SnapshotSystem"></span><span id="snapshotsystem"></span><span id="SNAPSHOTSYSTEM"></span>

**Snapshotsystem** (9)


</dt> <dd></dd> <dt>

<span id="AddResources"></span><span id="addresources"></span><span id="ADDRESOURCES"></span>

**Adressquellen** (10)


</dt> <dd></dd> <dt>

<span id="AddFeatureSettingsSupported"></span><span id="addfeaturesettingssupported"></span><span id="ADDFEATURESETTINGSSUPPORTED"></span>

**Addfeaturesettingssupported** (32779)


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettingsSupported"></span><span id="modifyfeaturesettingssupported"></span><span id="MODIFYFEATURESETTINGSSUPPORTED"></span>

**Modifyfeaturesettingssupported** (32780)


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettingsSupported"></span><span id="removefeaturesettingssupported"></span><span id="REMOVEFEATURESETTINGSSUPPORTED"></span>

**Removefeaturesettingssupported** (32781)


</dt> <dd></dd> <dt>

<span id="AddFeatureSettingsSupported"></span><span id="addfeaturesettingssupported"></span><span id="ADDFEATURESETTINGSSUPPORTED"></span>

**Addfeaturesettingssupported** (32779)


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettingsSupported"></span><span id="modifyfeaturesettingssupported"></span><span id="MODIFYFEATURESETTINGSSUPPORTED"></span>

**Modifyfeaturesettingssupported** (32780)


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettingsSupported"></span><span id="removefeaturesettingssupported"></span><span id="REMOVEFEATURESETTINGSSUPPORTED"></span>

**Removefeaturesettingssupported** (32781)


</dt> <dd></dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Hyper-V Virtual Ethernet Switch Management Service-Funktionen" festgelegt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Definieren von Verwaltungsdienst Funktionen für virtuelle Ethernet-Switches" festgelegt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeige Name für das-Objekt. Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Hyper-V Virtual Ethernet Switch Management Service-Funktionen" festgelegt.

</dd> <dt>

**Elementnameeditsupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **ElementName** -Eigenschaft geändert werden kann. Diese Eigenschaft wird von **CIM \_ enabledlogicalelementfunktionalitäten** geerbt.

</dd> <dt>

**Elementnamemask**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Einschränkungen für **ElementName** an, ausgedrückt als regulärer Ausdruck. Diese Eigenschaft wird von **CIM \_ enabledlogicalelementfunktionalitäten** geerbt.

</dd> <dt>

**Unterstützt**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von Indikator Bezeichner, das jeweils einen von der-Implementierung unterstützten Hinweis identifiziert. Diese Eigenschaft wird von **CIM \_ virtualsystemmanagementfunktionalitäten** geerbt.



| Wert                                                                                                                                                                                                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span><dl> <dt>**Virtualresourcestatuechanginattribuationssupported**</dt> <dt>2</dt> </dl> | Gibt an, ob die Implementierung Benachrichtigungen zu Zustandsänderungen von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -Instanzen unterstützt, die Ressourcen von virtuellen Systemen darstellen.<br/> |
| <span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span><dl> " <dt>**Concretejobstatus echangeinge-unterstützt**</dt> <dt>3</dt> " </dl>                 | Gibt an, ob die Implementierung Benachrichtigungen zu Zustandsänderungen von [**CIM- \_ concretejob**](/previous-versions//cc136808(v=vs.85)) -Instanzen unterstützt.<br/>                                                      |
| <span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span><dl> <dt>**Virtualsystemstatuechangin-Unterstützung**</dt> <dt>4</dt> </dl>         | Gibt an, ob die Implementierung Benachrichtigungen zu Zustandsänderungen von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanzen unterstützt, die virtuelle Systeme darstellen.<br/>            |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF reserviert**</dt> <dt>..</dt> </dl>                                                                                                                                    |                                                                                                                                                                                                       |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt> **Hersteller reserviert**</dt> <dt>32767.65535</dt> </dl>                                                                                                             |                                                                                                                                                                                                       |



 

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**IOVSupport**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein boolescher Wert, der angibt, ob die e/a-Virtualisierung (IOV) von der Plattform unterstützt wird. Wenn der Wert **true** ist, wird IOV von der Plattform unterstützt, und **iovsupporschatzist** leer. Andernfalls gibt die **iovsuppor-** Eigenschaft die Gründe dafür, warum IOV nicht unterstützt werden kann.

</dd> <dt>

**IOVSupportReasons**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von Zeichen folgen, das die möglichen Gründe angibt, warum IOV nicht unterstützt wird. Wenn der Wert von **iovsupport** den Wert **true** hat, ist dieses Array leer.

</dd> <dt>

**Maxelementnamelen**
</dt> <dd> <dl> <dt>

Datentyp: **unit16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxValue** (256)
</dt> </dl>

Gibt die maximal unterstützte Länge der **ElementName** -Eigenschaft an. Diese Eigenschaft wird von **CIM \_ enabledlogicalelementfunktionalitäten** geerbt.

</dd> <dt>

**Requestedstaatunter stützt**
</dt> <dd> <dl> <dt>

Datentyp: **unit16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die möglichen Zustände an, die bei Verwendung der **requestStateChange** -Methode für das aktivierte logische Element angefordert werden können. Diese Eigenschaft wird von **CIM \_ enabledlogicalelementfunktionalitäten** geerbt und ist immer **null**.

</dd> <dt>

**Synchronousmethodssupported**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von Methoden bezeichgern, von denen jedes eine Methode der [**MSVM \_ virtualethernettwitchmanagementservice**](msvm-virtualethernetswitchmanagementservice.md) -Klasse identifiziert, die von der-Implementierung synchron unterstützt wird. Diese Eigenschaft wird von **CIM \_ virtualsystemmanagementfunktionalitäten** geerbt.

<dl> <dt>

<span id="DefineSystem"></span><span id="definesystem"></span><span id="DEFINESYSTEM"></span>**Definesystem** (2)
</dt> <dt>

<span id="DestroySystem"></span><span id="destroysystem"></span><span id="DESTROYSYSTEM"></span>**Destroysystem** (3)
</dt> <dt>

<span id="DestroySystemConfiguration"></span><span id="destroysystemconfiguration"></span><span id="DESTROYSYSTEMCONFIGURATION"></span>**Destroysystemconfiguration** (4)
</dt> <dt>

<span id="ModifyResourceSettings"></span><span id="modifyresourcesettings"></span><span id="MODIFYRESOURCESETTINGS"></span>**Modifyresourcesettings** (5)
</dt> <dt>

<span id="ModifySystemSettings"></span><span id="modifysystemsettings"></span><span id="MODIFYSYSTEMSETTINGS"></span>**Modifysystemsettings** (6)
</dt> <dt>

<span id="RemoveResources"></span><span id="removeresources"></span><span id="REMOVERESOURCES"></span>**Removeresources** (7)
</dt> <dt>

<span id="SelectSystemConfiguration"></span><span id="selectsystemconfiguration"></span><span id="SELECTSYSTEMCONFIGURATION"></span>**Selectsystemconfiguration** (8)
</dt> <dt>

<span id="SnapshotSystem"></span><span id="snapshotsystem"></span><span id="SNAPSHOTSYSTEM"></span>**Snapshotsystem** (9)
</dt> <dt>

<span id="AddResources"></span><span id="addresources"></span><span id="ADDRESOURCES"></span>**Adressquellen** (10)
</dt> <dt>

<span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>**Addfeaturesettings** (32779)
</dt> <dt>

<span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>**Modifyfeaturesettings** (32780)
</dt> <dt>

<span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>**Removefeaturesettings** (32781)
</dt> </dl>

</dd> <dt>

**Virtualsystemtypessupported**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von Zeichen folgen, die jeweils einen virtuellen Systemtyp festlegen, der von der Implementierung unterstützt wird. Der Wert jedes Array Elements, das nicht **null** ist, muss mit dem Format übereinstimmen, das für die **virtualsystemtype** -Eigenschaft der [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) -Klasse definiert ist. Diese Eigenschaft wird von **CIM \_ virtualsystemmanagementfunktionalitäten** geerbt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

