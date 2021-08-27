---
description: Beschreibt ein Profil, auf das von einem anderen registrierten Profil verwiesen wird.
ms.assetid: 36FC0161-C57F-488A-9B4A-C86C6EB481D7
title: Msvm_ReferencedProfile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencedProfile
- Msvm_ReferencedProfile.Antecedent
- Msvm_ReferencedProfile.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1dbfe81dede2e3a6eb8b902ff03fe034deda1b5ab8160e830376e3380fe811c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046400"
---
# <a name="msvm_referencedprofile-class"></a>Msvm \_ ReferencedProfile-Klasse

Beschreibt ein Profil, auf das von einem anderen registrierten Profil verwiesen wird.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
class Msvm_ReferencedProfile : CIM_ReferencedProfile
{
  CIM_RegisteredProfile REF Antecedent;
  CIM_RegisteredProfile REF Dependent;
};
```

## <a name="members"></a>Member

Die **Msvm \_ ReferencedProfile-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ ReferencedProfile-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das registrierte Profil, auf das das abhängige **Profil** verweist.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein registriertes Profil, das auf andere Profile verweist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\Stamm-Interop<br/>                                                                                |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

