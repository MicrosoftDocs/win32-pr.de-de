---
description: Wird verwendet, um eine Cim \_ RegisteredProfile-Instanz einer Instanz von CIM \_ RegisteredProfile eines anderen Profils zuzuordnen, das auf das abhängige Profil als verknüpftes Profil verweist.
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
ms.openlocfilehash: 39cfa6dac2fd827b2ce690afa5cdd7126322c2f81182db674517c75911791a0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556811"
---
# <a name="cim_referencedprofile-class"></a>CIM \_ ReferencedProfile-Klasse

Wird verwendet, um eine [**Cim \_ RegisteredProfile-Instanz**](/previous-versions//ee309375(v=vs.85)) einer Instanz von **CIM \_ RegisteredProfile** eines anderen Profils zuzuordnen, das auf das abhängige Profil als verknüpftes Profil verweist.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

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

Die **CIM \_ ReferencedProfile-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ ReferencedProfile-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die [**CIM \_ RegisteredProfile-Instanz**](/previous-versions//ee309375(v=vs.85)) an, auf die vom **abhängigen** Profil verwiesen wird.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt eine [**\_ CIM RegisteredProfile-Instanz**](/previous-versions//ee309375(v=vs.85)) an, die auf andere Profile verweist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Verwendung der Eigenschaften **Dependent** und **Antecedent** in der **CIM \_ ReferencedProfile-Zuordnung** ist so definiert, dass das Profil, auf das verwiesen wird, der Vorgänger und das Profil, das auf den Verweis verweist, abhängig ist.

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von dmtf veröffentlicht wurden. Möglicherweise hat Microsoft Änderungen vorgenommen, um kleinere Fehler zu korrigieren, den Dokumentationsstandards des Microsoft SDK zu entsprechen oder weitere Informationen bereitzustellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                      |
| Namespace<br/>                | \\Root-Interop<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Interop.mof</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_CIM-Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

