---
description: Definiert die registrierten Profile, denen das eigenständige System entspricht, auf das verwiesen wird.
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
ms.openlocfilehash: 5506119f0e8938a29b94b298460a1f164dab97359d13d956bfa5ca74e97a081b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950239"
---
# <a name="msvm_standalonev2elementconformstoprofile-class"></a>Msvm \_ StandaloneV2ElementConformsToProfile-Klasse

Definiert die registrierten Profile, denen das eigenständige System entspricht, auf das verwiesen wird.

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

Die **Msvm \_ StandaloneV2ElementConformsToProfile-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ StandaloneV2ElementConformsToProfile-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ConformantStandard**
</dt> <dd> <dl> <dt>

Datentyp: **Msvm \_ RegisteredProfile**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Das registrierte Profil, dem das eigenständige System entspricht.

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Datentyp: **Msvm \_ ComputerSystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers)von , **MSFT \_ TargetNamespace** ("Root \\ \\ Virtualization \\ \\ v2")
</dt> </dl>

Das eigenständige System, das dem registrierten Profil entspricht.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stamm-Interop<br/>                                                                                |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_Msvm-ElementConformsToProfile**](msvm-elementconformstoprofile.md)
</dt> </dl>

 

