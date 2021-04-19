---
description: Wird verwendet, um eine Instanz CIM \_ registeredprofile einer Instanz von CIM \_ registeredprofile eines anderen Profils zuzuordnen, das auf das abhängige Profil als verknüpftes Profil verweist.
ms.assetid: 631003de-477b-4447-9633-1601a7f8eadb
ms.tgt_platform: multiple
title: CIM_ReferencedProfile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ReferencedProfile
- CIM_ReferencedProfile.Antecedent
- CIM_ReferencedProfile.Dependent
api_type:
- Schema
api_location:
- Root\interop
ms.openlocfilehash: 8fdc0d8dccd325ae7e13de971e09cce6faf93455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363317"
---
# <a name="cim_referencedprofile-class"></a>CIM \_ referencedprofile-Klasse

Wird verwendet, um eine Instanz [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85)) einer Instanz von **CIM \_ registeredprofile** eines anderen Profils zuzuordnen, das auf das abhängige Profil als verknüpftes Profil verweist.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Version("2.8.0"), UMLPackagePath("CIM::Interop"), AMENDMENT]
class CIM_ReferencedProfile : CIM_Dependency
{
  CIM_RegisteredProfile REF Antecedent;
  CIM_RegisteredProfile REF Dependent;
};
```

## <a name="members"></a>Member

Die **CIM \_ referencedprofile** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ referencedprofile** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die [**CIM- \_ registeredprofile**](/previous-versions//ee309375(v=vs.85)) -Instanz an, auf die vom **abhängigen** Profil verwiesen wird.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt eine [**CIM- \_ registeredprofile**](/previous-versions//ee309375(v=vs.85)) -Instanz an, die auf andere Profile verweist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Verwendung der **abhängigen** und der **Vorgänger** Eigenschaften in der **CIM \_ referencedprofile** -Zuordnung wird so definiert, dass das Profil, auf das verwiesen wird, der Vorgänger ist und dass das Profil, das die Referenzierung durchläuft, abhängig ist.

Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet. Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                      |
| Namespace<br/>                | Root- \\ Interop<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Interop. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

