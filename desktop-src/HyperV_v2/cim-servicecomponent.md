---
description: Stellt eine Zuordnung dar, bei der ein Dienst eine Komponente eines übergeordneten Diensts ist, die zusammen einen übergeordneten Dienst bilden.
ms.assetid: c629d59d-d9d3-4019-a378-cd1d4d31a5d9
title: CIM_ServiceComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceComponent
- CIM_ServiceComponent.GroupComponent
- CIM_ServiceComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a7684b22bc7488093702e5050524ac6c36f719dd985f537570e0eb1395756e7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118647545"
---
# <a name="cim_servicecomponent-class"></a>CIM \_ ServiceComponent-Klasse

Stellt eine Zuordnung dar, bei der ein Dienst eine Komponente eines übergeordneten Diensts ist, die zusammen einen übergeordneten Dienst bilden.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::Service")]
class CIM_ServiceComponent : CIM_Component
{
  CIM_Service REF GroupComponent;
  CIM_Service REF PartComponent;
};
```

## <a name="members"></a>Member

Die **CIM \_ ServiceComponent-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ ServiceComponent-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Dienst**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Aggregieren, Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent") [](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Der übergeordnete Dienst.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Dienst**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Der Komponentendienst.

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

[**\_CIM-Komponente**](cim-component.md)
</dt> </dl>

 

