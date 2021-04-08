---
description: Stellt den transparenten Überbrückungs Aspekt eines CIM \_ switchservice-Objekts dar.
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
ms.openlocfilehash: ed2c21c0f00bd89b0054667274a559ef25ce9326
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864112"
---
# <a name="cim_transparentbridgingservice-class"></a>CIM- \_ transparentbridgingservice-Klasse

Stellt den transparenten Überbrückungs Aspekt eines [**CIM \_ switchservice**](cim-switchservice.md) -Objekts dar.

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

Die CIM-Klasse " **\_ transparentbridgingservice** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die CIM-Klasse " **\_ transparentbridgingservice** " verfügt über diese Eigenschaften.

<dl> <dt>

**Agingtime**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dTpAgingTime ")
</dt> </dl>

Der Timeout Zeitraum (in Sekunden) für das Auslagern dynamisch erlernter Weiterleitungs Informationen. Der 802.1 d-1990-Standard empfiehlt einen Standardwert von 300 Sekunden.

</dd> <dt>

**Angestrebt**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Filtern von Daten Bank Bezeichnern, die von VLAN-fähigen Switches verwendet werden, die über mehrere Filter Datenbanken verfügen.

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

[**CIM- \_ weiterforwardingdienst**](cim-forwardingservice.md)
</dt> </dl>

 

