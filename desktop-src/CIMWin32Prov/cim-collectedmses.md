---
description: Die CIM \_ CollectedMSEs-Zuordnungsklasse stellt die Member des Gruppierungsobjekts dar, eine CollectionOfMSEs-Klasse.
ms.assetid: 3dca2094-57f1-447e-809c-f924f88a185a
ms.tgt_platform: multiple
title: CIM_CollectedMSEs-Klasse (CIMWin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedMSEs
- CIM_CollectedMSEs.Collection
- CIM_CollectedMSEs.Member
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 82ffbf9e3c00a9a0463e1337ee5c5ed6ab188dc5258c622cfa6b41eb717d8589
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959079"
---
# <a name="cim_collectedmses-class-cimwin32-wmi-providers"></a>CIM_CollectedMSEs-Klasse (CIMWin32-WMI-Anbieter)

Die **CIM \_ CollectedMSEs-Zuordnungsklasse** stellt die Member des Gruppierungsobjekts dar, eine [**CollectionOfMSEs-Klasse.**](cim-collectionofmses.md)

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
class CIM_CollectedMSEs
{
  CM_CollectionOfMSEs      REF Collection;
  CIM_ManagedSystemElement REF Member;
};
```

## <a name="members"></a>Member

Die **CIM \_ CollectedMSEs-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ CollectedMSEs-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Sammlung**
</dt> <dd> <dl> <dt>

Datentyp: **CM \_ CollectionOfMSEs**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf das Gruppierungs- oder Bag-Objekt, das die Auflistung darstellt.

</dd> <dt>

**Member**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ManagedSystemElement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf einen Member der Auflistung.

</dd> </dl>

## <a name="remarks"></a>Hinweise

WMI implementiert diese Klasse nicht. Weitere Informationen zu WMI-Klassen, die von **CIM \_ CollectedMSEs** abgeleitet wurden, finden Sie unter [Win32-Klassen.](win32-provider.md)

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von dmtf veröffentlicht wurden. Möglicherweise hat Microsoft Änderungen vorgenommen, um kleinere Fehler zu korrigieren, den Dokumentationsstandards des Microsoft SDK zu entsprechen oder weitere Informationen bereitzustellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




