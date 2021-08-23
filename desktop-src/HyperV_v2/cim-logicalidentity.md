---
description: Stellt eine generische Zuordnung zwischen zwei verwalteten Elementen dar, die verschiedene Aspekte derselben zugrunde liegenden Entität darstellen.
ms.assetid: 28d153de-ce9c-4cd3-8995-0d959846be4d
title: CIM_LogicalIdentity-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalIdentity
- CIM_LogicalIdentity.SystemElement
- CIM_LogicalIdentity.SameElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9520817a2099901d1b6e61ab37ccacf1c2e2a61e76c57a9f327bdef32df63285
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695450"
---
# <a name="cim_logicalidentity-class-hyper-v-management"></a>CIM_LogicalIdentity-Klasse (Hyper-V-Verwaltung)

Stellt eine generische Zuordnung zwischen zwei verwalteten Elementen dar, die verschiedene Aspekte derselben zugrunde liegenden Entität darstellen.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_LogicalIdentity
{
  CIM_ManagedElement REF SystemElement;
  CIM_ManagedElement REF SameElement;
};
```

## <a name="members"></a>Member

Die **CIM \_ LogicalIdentity-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ LogicalIdentity-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**SameElement**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ManagedElement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Der zweite Aspekt in der Zuordnung.

</dd> <dt>

**SystemElement**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ManagedElement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Der erste Aspekt in der Zuordnung. Die Verwendung von System im Eigenschaftennamen schränkt den Bereich der Zuordnung nicht ein.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

