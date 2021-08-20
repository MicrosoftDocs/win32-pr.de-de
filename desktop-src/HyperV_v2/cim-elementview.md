---
description: Stellt eine Ansicht und eine Zuordnung zwischen einer Sicht und einer -Instanz dar, die die normalisierte Ansicht einer verwalteten Ressource darstellt.
ms.assetid: 9c6eb3d5-7366-4954-9e64-12f889c64114
title: CIM_ElementView-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementView
- CIM_ElementView.Antecedent
- CIM_ElementView.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 06a627668fd8a7b9550f92c65918a85448ec1f23ba1d92630379ec205660f58d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117812176"
---
# <a name="cim_elementview-class"></a>CIM \_ ElementView-Klasse

Stellt eine Ansicht und eine Zuordnung zwischen einer Sicht und einer -Instanz dar, die die normalisierte Ansicht einer verwalteten Ressource darstellt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Association, Experimental, Version("2.21.1"), UMLPackagePath("CIM::Core::CoreElements")]
class CIM_ElementView : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_View           REF Dependent;
};
```

## <a name="members"></a>Member

Die **CIM \_ ElementView-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ CIM-ElementView-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ManagedElement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")
</dt> </dl>

Die -Instanz, die die normalisierte Ansicht der verwalteten Ressource darstellt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Ansicht**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("abhängig")
</dt> </dl>

Die Sicht, die eine denormierte oder aggregierte Ansicht der verwalteten Ressource darstellt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-Abhängigkeit**](cim-dependency.md)
</dt> </dl>

 

