---
description: Die Win32 \_ -Klasse implementedcategory Association WMI verknüpft eine Komponenten Kategorie und die Component Object Model (com)-Klasse mithilfe ihrer Schnittstellen.
ms.assetid: 7cf32b50-9ae6-44e5-b364-bc74dea3dc17
ms.tgt_platform: multiple
title: Win32_ImplementedCategory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ImplementedCategory
- Win32_ImplementedCategory.Category
- Win32_ImplementedCategory.Component
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1d885c8c8e92ea661e06b46f338924355438ff9a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749016"
---
# <a name="win32_implementedcategory-class"></a>Win32 \_ implementedcategory-Klasse

Die **Win32-Klasse \_ implementedcategory** Association [WMI](/windows/desktop/WmiSdk/retrieving-a-class) verknüpft eine Komponenten Kategorie und die Component Object Model (com)-Klasse mithilfe ihrer Schnittstellen.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5B-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ImplementedCategory
{
  Win32_ComponentCategory REF Category;
  Win32_ClassicCOMClass   REF Component;
};
```

## <a name="members"></a>Member

Die **Win32 \_ implementedcategory** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ implementedcategory** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Kategorie**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ componentcategory**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ componentcategory")
</dt> </dl>

Verweis auf die-Instanz, die die von der com-Klasse verwendete Komponenten Kategorie darstellt.

</dd> <dt>

**Komponente**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ classiccomclass**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ classiccomclass")
</dt> </dl>

Verweis auf die-Instanz, die die com-Klasse unter Verwendung der zugeordneten Kategorie darstellt.

</dd> </dl>

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

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

