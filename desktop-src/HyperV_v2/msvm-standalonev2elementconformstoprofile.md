---
description: Definiert die registrierten Profile, denen das eigenständige System, auf das verwiesen wird, entspricht.
ms.assetid: d9ede8d0-c6f3-48bd-84a9-7f2c31637819
title: Msvm_StandaloneV2ElementConformsToProfile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StandaloneV2ElementConformsToProfile
- Msvm_StandaloneV2ElementConformsToProfile.ConformantStandard
- Msvm_StandaloneV2ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c492ad5bdd0e50bbbe86fd220000099269501ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959276"
---
# <a name="msvm_standalonev2elementconformstoprofile-class"></a>MSVM \_ StandaloneV2ElementConformsToProfile-Klasse

Definiert die registrierten Profile, denen das eigenständige System, auf das verwiesen wird, entspricht.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
class Msvm_StandaloneV2ElementConformsToProfile : Msvm_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard = $SVP;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a>Member

Die **MSVM \_ StandaloneV2ElementConformsToProfile** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM- \_ StandaloneV2ElementConformsToProfile** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Conformantstandard**
</dt> <dd> <dl> <dt>

Datentyp: **MSVM \_ registeredprofile**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **override**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Das registrierte Profil, dem das eigenständige System entspricht.

</dd> <dt>

**"Managedelement"**
</dt> <dd> <dl> <dt>

Datentyp: **MSVM \_ Computersystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers), **MSFT \_ targetNamespace** ("root \\ \\ Virtualization \\ \\ V2")
</dt> </dl>

Das eigenständige System, das dem registrierten Profil entspricht.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | Root- \\ Interop<br/>                                                                                |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ elementreformstoprofile**](msvm-elementconformstoprofile.md)
</dt> </dl>

 

