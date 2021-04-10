---
description: Eine Common Information Model (CIM)-Zuordnungs Klasse, mit der Beziehungen zwischen einem System und den verwalteten Systemelementen hergestellt werden, von denen es zusammengesetzt wird.
ms.assetid: 11ad6dc1-a09a-4bab-bb1d-2131a8fdb812
ms.tgt_platform: multiple
title: CIM_SystemComponent-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemComponent
- CIM_SystemComponent.PartComponent
- CIM_SystemComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9d9aae4e4ef916916f54bddea814844f23ed7315
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127101"
---
# <a name="cim_systemcomponent-class-cimwin32-wmi-providers"></a>CIM_SystemComponent-Klasse (cimwin32-WMI-Anbieter)

Die **CIM- \_ SystemComponent** -Klasse ist eine Common Information Model (CIM)-Zuordnungs Klasse, die Beziehungen zwischen einem System und den verwalteten Systemelementen herstellt, aus denen es besteht.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{527BC6CE-BAFE-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class CIM_SystemComponent : CIM_Component
{
  CIM_ManagedSystemElement REF PartComponent;
  CIM_System               REF GroupComponent;
};
```

## <a name="members"></a>Member

Die **CIM \_ SystemComponent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ SystemComponent** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ System**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Ein [**CIM- \_ System**](cim-system.md) , das das übergeordnete System in der Zuordnung beschreibt.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ManagedSystemElement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Ein [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) , das das untergeordnete Element beschreibt, das eine Komponente eines Systems ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Klasse wird von WMI nicht implementiert. Informationen zu WMI-Klassen, die von **CIM \_ SystemComponent** abgeleitet sind, finden Sie unter [Win32](win32-provider.md)

Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet. Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Komponente**](cim-component.md)
</dt> </dl>

 

