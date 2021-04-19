---
description: Stellt eine generische Zuordnung zwischen einem übergeordneten verwalteten Element und einem untergeordneten verwalteten Element dar, bei dem das untergeordnete Element eine Komponente oder einen Teil des übergeordneten Elements darstellt.
ms.assetid: b5cef452-2d00-483c-8e70-f804f1e3536b
title: CIM_Component-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Component
- CIM_Component.GroupComponent
- CIM_Component.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 56ff83a4da51ba18205a8d8ab5e6e57ea1a7794b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359113"
---
# <a name="cim_component-class-hyper-v-management"></a>CIM_Component-Klasse (Hyper-V-Verwaltung)

Stellt eine generische Zuordnung zwischen einem übergeordneten verwalteten Element und einem untergeordneten verwalteten Element dar, bei dem das untergeordnete Element eine Komponente oder einen Teil des übergeordneten Elements darstellt.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Abstract, Aggregation, Version("2.7.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Component
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a>Member

Die **CIM- \_ Komponenten** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ Komponenten** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ managedelta**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**Aggregat**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Das übergeordnete Element in der Zuordnung.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ managedelta**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Das untergeordnete-Element in der Zuordnung.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

