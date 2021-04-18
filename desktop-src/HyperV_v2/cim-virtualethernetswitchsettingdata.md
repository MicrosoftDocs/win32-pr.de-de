---
description: Beschreibt die Einstellungsdaten für einen virtuellen Ethernet-Switch.
ms.assetid: 462cff06-5ba6-410a-b091-5c6abab13f03
title: CIM_VirtualEthernetSwitchSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualEthernetSwitchSettingData
- CIM_VirtualEthernetSwitchSettingData.VLANConnection
- CIM_VirtualEthernetSwitchSettingData.AssociatedResourcePool
- CIM_VirtualEthernetSwitchSettingData.MaxNumMACAddress
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 64d7053364aebe1fab5739cd75389b1a9343efe0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343831"
---
# <a name="cim_virtualethernetswitchsettingdata-class"></a>CIM \_ virtualethernetzwitchsettingdata-Klasse

Beschreibt die Einstellungsdaten für einen virtuellen Ethernet-Switch.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualEthernetSwitchSettingData : CIM_VirtualSystemSettingData
{
  string VLANConnection[];
  string AssociatedResourcePool[];
  uint32 MaxNumMACAddress;
};
```

## <a name="members"></a>Member

Die **CIM- \_ virtualethernetzwitchsettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ virtualethernetzwitchsettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Associatedresourcepool**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array, das die derzeit zugeordneten Host Ressourcenpools enthält, oder, die dem Ethernet-Switch zugeordnet werden sollen, um Ethernet-Verbindungen zwischen dem Ethernet-Switch und einem virtuellen Computer zuzuordnen. Jeder Wert, der nicht NULL ist, muss mit dem **WBEM- \_ URI \_ untypedinstancepath** übereinstimmen, wie in der DMTF-Spezifikation "DSP0207" definiert.

</dd> <dt>

**Maxnummacaddress**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl der eindeutigen MAC-Adressen, die der Switch für Mac-Address Learning erlernen kann, wie im IEEE 802,1-Standard definiert.

</dd> <dt>

**Vlanconnection**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array, das die VLAN-IDs enthält, auf die der Switch zugreifen kann.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md)
</dt> </dl>

 

 




