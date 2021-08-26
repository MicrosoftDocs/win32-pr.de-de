---
description: Die \_ CIM-Abhängigkeitsklasse stellt eine Zuordnung dar, die Abhängigkeitsbeziehungen zwischen Objekten herstellt.
ms.assetid: ff0d6b50-0920-443e-a984-e6a9ab4402b1
ms.tgt_platform: multiple
title: CIM_Dependency-Klasse (CIMWin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Dependency
- CIM_Dependency.Antecedent
- CIM_Dependency.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1a2c1c568eeb8a3d753479c8663cc04293e76d38c5efb9919ab494b198657efa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921940"
---
# <a name="cim_dependency-class-cimwin32-wmi-providers"></a>CIM_Dependency-Klasse (CIMWin32-WMI-Anbieter)

Die **\_ CIM-Abhängigkeitsklasse** stellt eine Zuordnung dar, die Abhängigkeitsbeziehungen zwischen Objekten herstellt.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Abstract, UUID("{8502C53A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Dependency
{
  CIM_ManagedSystemElement REF Antecedent;
  CIM_ManagedSystemElement REF Dependent;
};
```

## <a name="members"></a>Member

Die **\_ CIM-Abhängigkeitsklasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ CIM-Abhängigkeitsklasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ManagedSystemElement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf das unabhängige Objekt in dieser Zuordnung.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ManagedSystemElement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf das Objekt, das von der **Vorgängereigenschaft** abhängig ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

WMI implementiert diese Klasse nicht. Weitere Informationen zu Klassen, die von **\_ CIM-Abhängigkeit** abgeleitet wurden, finden Sie unter [Win32-Klassen.](win32-provider.md)

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von dmtf veröffentlicht wurden. Möglicherweise hat Microsoft Änderungen vorgenommen, um kleinere Fehler zu korrigieren, den Dokumentationsstandards des Microsoft SDK zu entsprechen oder weitere Informationen bereitzustellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




