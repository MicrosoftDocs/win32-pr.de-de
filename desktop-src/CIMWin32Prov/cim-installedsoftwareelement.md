---
description: Die CIM \_ InstalledSoftwareElement-Klasse ordnet ein Computersystem einem installierten Softwareelement zu.
ms.assetid: b9a570ed-b4e0-4f73-82e3-6d2bd1708e16
ms.tgt_platform: multiple
title: CIM_InstalledSoftwareElement-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_InstalledSoftwareElement
- CIM_InstalledSoftwareElement.Software
- CIM_InstalledSoftwareElement.System
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd082477b2e2ba194163784b74883872b1edb6a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126960"
---
# <a name="cim_installedsoftwareelement-class"></a>CIM \_ InstalledSoftwareElement-Klasse

Die **CIM \_ InstalledSoftwareElement** -Klasse ordnet ein Computersystem einem installierten Softwareelement zu.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[UUID("{A7B05028-DB2A-11d2-85FC-0000F8102E5F}"), Association, Abstract, AMENDMENT]
class CIM_InstalledSoftwareElement
{
  CIM_SoftwareElement REF Software;
  CIM_ComputerSystem  REF System;
};
```

## <a name="members"></a>Member

Die **CIM \_ InstalledSoftwareElement** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ InstalledSoftwareElement** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Software**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ Softwareelement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false)
</dt> </dl>

Verweis auf das Softwareelement, das auf dem Computersystem installiert ist.

</dd> <dt>

**System**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ Computersystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false)
</dt> </dl>

Verweis auf das Computersystem, das ein bestimmtes Softwareelement gehostet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Klasse wird von WMI nicht implementiert. Informationen zu Klassen, die von **CIM \_ InstalledSoftwareElement** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).

Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet. Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

