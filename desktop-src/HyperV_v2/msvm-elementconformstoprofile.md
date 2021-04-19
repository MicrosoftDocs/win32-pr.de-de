---
description: Definiert die registrierten Profile, denen das referenzierte System entspricht.
ms.assetid: F01E79BE-82D9-49E0-AB0C-FD1B48BC4A55
title: Msvm_ElementConformsToProfile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementConformsToProfile
- Msvm_ElementConformsToProfile.ConformantStandard
- Msvm_ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6b0afdc7dd9d55a036de0695f9a88a95d2b01308
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363592"
---
# <a name="msvm_elementconformstoprofile-class"></a>MSVM \_ elementreformstoprofile-Klasse

Definiert die registrierten Profile, denen das referenzierte System entspricht. Diese Zuordnung kann auf ein beliebiges verwaltetes Element angewendet werden. Die typische Verwendung wird auf eine Instanz höherer Ebene angewendet, z. b. auf ein System, einen Namespace oder einen Dienst. Wenn Sie auf eine Instanz einer höheren Ebene angewendet werden, müssen sich alle Bestandteile entsprechend der Unterstützung der Übereinstimmung des verwalteten Elements mit dem benannten registrierten Profil Verhalten.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
class Msvm_ElementConformsToProfile : CIM_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a>Member

Die **MSVM \_ elementkonformstoprofile** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ ElementConfiguration** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Conformantstandard**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM \_ registeredprofile**](msvm-registeredprofile.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **override**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Ein Verweis auf eine Instanz der [**MSVM \_ registeredprofile**](msvm-registeredprofile.md) -Klasse, die das registrierte Profil darstellt, dem das System entspricht.

</dd> <dt>

**"Managedelement"**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM \_ Computersystem**](msvm-computersystem.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **override**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Ein Verweis auf eine Instanz der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse, die das System darstellt, das dem registrierten Profil entspricht.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

