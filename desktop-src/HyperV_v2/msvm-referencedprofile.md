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
ms.openlocfilehash: cbe95658556be8a15bed0e7e5b5b32dda23ff21d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348645"
---
# <a name="msvm_referencedprofile-class"></a>MSVM \_ referencedprofile-Klasse

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

Die **MSVM \_ referencedprofile** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ referencedprofile** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das registrierte Profil, auf das vom **abhängigen** Profil verwiesen wird.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein registriertes Profil, das auf andere Profile verweist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | Root- \\ Interop<br/>                                                                                |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

