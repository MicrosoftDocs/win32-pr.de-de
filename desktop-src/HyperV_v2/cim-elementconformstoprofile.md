---
description: Stellt eine Zuordnung dar, in der ein verwaltetes Element dem Standard eines registrierten Profils entspricht.
ms.assetid: 9d5704b6-c764-4f68-bce3-384d5a244e28
title: CIM_ElementConformsToProfile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementConformsToProfile
- CIM_ElementConformsToProfile.ConformantStandard
- CIM_ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7034001641029099d1b52090b3cc518b6589dc50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355527"
---
# <a name="cim_elementconformstoprofile-class"></a>CIM \_ elementreformstoprofile-Klasse

Stellt eine Zuordnung dar, in der ein verwaltetes Element dem Standard eines registrierten Profils entspricht. Diese Zuordnung gilt normalerweise für eine Instanz höherer Ebene, z. b. ein System, einen Namespace oder einen Dienst. Wenn Sie auf eine Instanz einer höheren Ebene angewendet werden, müssen sich alle Bestandteile entsprechend der Unterstützung der Übereinstimmung von managedelta für das benannte registeredprofile Verhalten.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Interop")]
class CIM_ElementConformsToProfile
{
  CIM_RegisteredProfile REF ConformantStandard;
  CIM_ManagedElement    REF ManagedElement;
};
```

## <a name="members"></a>Member

Die **CIM \_ elementkonstoprofile** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ ElementConfiguration** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Conformantstandard**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ registeredprofile**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Das registrierte Profil, dem das verwaltete Element entspricht.

</dd> <dt>

**"Managedelement"**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ managedelta**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Das verwaltete Element, das dem registrierten Profil entspricht.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

