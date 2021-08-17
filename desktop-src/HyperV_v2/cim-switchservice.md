---
description: Stellt einen Switchdienst dar.
ms.assetid: cf6319fa-7d69-4820-b0e0-775aad8b190c
title: CIM_SwitchService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchService
- CIM_SwitchService.BridgeAddress
- CIM_SwitchService.NumPorts
- CIM_SwitchService.BridgeType
- CIM_SwitchService.BridgeAddressType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1cae4f157073721dc7cdd87585b39e1dbdb4c73b03a4aaf82a8ffd26796cbc78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118646782"
---
# <a name="cim_switchservice-class"></a>CIM \_ SwitchService-Klasse

Stellt einen Switchdienst dar.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging")]
class CIM_SwitchService : CIM_ForwardingService
{
  string BridgeAddress;
  uint16 NumPorts;
  uint8  BridgeType;
  uint16 BridgeAddressType;
};
```

## <a name="members"></a>Member

Die **CIM \_ SwitchService-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ SwitchService-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**BridgeAddress**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| BRIDGE-MIB.dot1dBaseBridgeAddress"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SwitchService**.**BridgeAddressType**")
</dt> </dl>

Die Adresse des Switchdiensts, der ein Teil des eindeutigen Bezeichners des Diensts ist.

</dd> <dt>

**BridgeAddressType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SwitchService**.**BridgeAddress**")
</dt> </dl>

Das Adressierungsformat, das für die Bridge und die **BridgeAddress-Eigenschaft verwendet** wird.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

**IPv4** (2)


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

**IPv6** (3)


</dt> <dd></dd> <dt>

<span id="MAC"></span><span id="mac"></span>

**MAC** (4)


</dt> <dd></dd> <dt>

<span id="MAC___Spanning_Tree_Priority"></span><span id="mac___spanning_tree_priority"></span><span id="MAC___SPANNING_TREE_PRIORITY"></span>

**MAC + Spanning Tree Priority** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**BridgeType**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| BRIDGE-MIB.dot1dBaseType")
</dt> </dl>

Der Typ des durchzuführenden Wechseldiensts.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (1)


</dt> <dd></dd> <dt>

<span id="Transparent-only"></span><span id="transparent-only"></span><span id="TRANSPARENT-ONLY"></span>

**Nur transparent** (2)


</dt> <dd></dd> <dt>

<span id="SourceRoute-only"></span><span id="sourceroute-only"></span><span id="SOURCEROUTE-ONLY"></span>

**Nur SourceRoute** (3)


</dt> <dd></dd> <dt>

<span id="SRT"></span><span id="srt"></span>

**SRT** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**NumPorts**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| BRIDGE-MIB.dot1dBaseNumPorts")
</dt> </dl>

Die Anzahl der Switchports, die von diesem Wechseldienst gesteuert werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ ForwardingService**](cim-forwardingservice.md)
</dt> </dl>

 

