---
description: Stellt den transparenten Bridgingaspekt eines CIM \_ SwitchService-Objekts dar.
ms.assetid: 24f650ab-22a1-41c8-8498-c6c30e63c83c
title: CIM_TransparentBridgingService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TransparentBridgingService
- CIM_TransparentBridgingService.AgingTime
- CIM_TransparentBridgingService.FID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8744bbac256d0cebc6d340ac83c4e8da746c03b298e2e3cd6c542310b3fc4914
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119254980"
---
# <a name="cim_transparentbridgingservice-class"></a>CIM \_ TransparentBridgingService-Klasse

Stellt den transparenten Bridgingaspekt eines [**CIM \_ SwitchService-Objekts**](cim-switchservice.md) dar.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_TransparentBridgingService : CIM_ForwardingService
{
  uint32 AgingTime = 300;
  uint32 FID;
};
```

## <a name="members"></a>Member

Die **CIM \_ TransparentBridgingService-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ TransparentBridgingService-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AgingTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Sekunden"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| BRIDGE-MIB.dot1dTpAgingTime")
</dt> </dl>

Der Timeoutzeitraum (in Sekunden) für das Ausreifen dynamisch erlernter Weiterleitungsinformationen. Der Standard 802.1D-1990 empfiehlt einen Standardwert von 300 Sekunden.

</dd> <dt>

**Fid**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Filtern des Datenbankbezeichners, der von VLAN-fähigen Switches mit mehreren Filterdatenbanken verwendet wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ ForwardingService**](cim-forwardingservice.md)
</dt> </dl>

 

