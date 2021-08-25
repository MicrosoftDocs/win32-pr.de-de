---
description: Stellt einen Switchdienst dar, der Frames zwischen Switchports umschaltet.
ms.assetid: ee2d4831-df00-408c-b350-26d2d1d3e8aa
title: CIM_SwitchesAmong-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchesAmong
- CIM_SwitchesAmong.Antecedent
- CIM_SwitchesAmong.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7a12d4ffa10f8a1a921b64fab26082a9b99e00022d2ae6363a1d093a0627b044
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899637"
---
# <a name="cim_switchesamong-class"></a>CIM \_ SwitchesAmong-Klasse

Stellt einen Switchdienst dar, der Frames zwischen Switchports umschaltet.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::SwitchingBridging")]
class CIM_SwitchesAmong : CIM_ForwardsAmong
{
  CIM_SwitchPort    REF Antecedent;
  CIM_SwitchService REF Dependent;
};
```

## <a name="members"></a>Member

Die **CIM \_ SwitchesAmong-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ SwitchesAmong-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ SwitchPort**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Ein [**CIM \_ SwitchPort-Verweis**](cim-switchport.md) auf den Switchport.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ SwitchService**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ein [**CIM \_ SwitchService-Verweis**](cim-switchservice.md) auf den Wechseldienst.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ ForwardsAmong**](cim-forwardsamong.md)
</dt> </dl>

 

