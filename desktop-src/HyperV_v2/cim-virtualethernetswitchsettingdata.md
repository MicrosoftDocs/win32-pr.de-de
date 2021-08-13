---
description: Beschreibt Einstellungsdaten für einen virtuellen Ethernet-Switch.
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
ms.openlocfilehash: 6243e86ec53213f959ea0b8f420543a9dca619de9d12593a73619aab2805091d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118646458"
---
# <a name="cim_virtualethernetswitchsettingdata-class"></a>CIM \_ VirtualEthernetSwitchSettingData-Klasse

Beschreibt Einstellungsdaten für einen virtuellen Ethernet-Switch.

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

Die **CIM \_ VirtualEthernetSwitchSettingData-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ VirtualEthernetSwitchSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AssociatedResourcePool**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array, das die Hostressourcenpools enthält, die derzeit zugeordnet sind, oder das dem Ethernet-Switch zugeordnet werden soll, um Ethernetverbindungen zwischen dem Ethernet-Switch und einem virtuellen Computer zuzuordnen. Jeder Wert ungleich NULL dieser Eigenschaft muss dem **WBEM-URI \_ \_ UntypedInstancePath** entsprechen, wie in der DMTF-Spezifikation "DSP0207" definiert.

</dd> <dt>

**MaxNumMACAddress**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl eindeutiger MAC-Adressen, die der Switch für das Lernen von MAC-Adressen erlernen kann, wie im IEEE 802.1-Standard definiert.

</dd> <dt>

**VLANConnection**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
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
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md)
</dt> </dl>

 

 




