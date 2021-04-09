---
description: Stellt einen switchdienst dar, mit dem Frames zwischen Switchports gewechselt werden.
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
ms.openlocfilehash: 16a87797b4a138ef79be3d5ea8c6304d2ce4a942
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129689"
---
# <a name="cim_switchesamong-class"></a>CIM \_ switchesunter-Klasse

Stellt einen switchdienst dar, mit dem Frames zwischen Switchports gewechselt werden.

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

Die **CIM \_ Switchesin** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ Switchesin** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ Switchport**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")
</dt> </dl>

Ein [**CIM- \_ switchportverweis auf den Switchport**](cim-switchport.md) .

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ switchservice**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ein [**CIM \_ switchservice**](cim-switchservice.md) -Verweis auf den Wechseldienst.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ forwardsamong**](cim-forwardsamong.md)
</dt> </dl>

 

