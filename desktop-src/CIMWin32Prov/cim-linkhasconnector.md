---
description: Die CIM \_ LinkHasConnector-Klasse ordnet Kabel und Verbindungen zu, die als physische Connectors verwendet werden, die die physischen Elemente verbinden. Diese Zuordnung definiert explizit die Beziehung von Connectors für CIM \_ PhysicalLink.
ms.assetid: c8244b93-749a-424a-ab40-ce5ce79c8b02
ms.tgt_platform: multiple
title: CIM_LinkHasConnector-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LinkHasConnector
- CIM_LinkHasConnector.PartComponent
- CIM_LinkHasConnector.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ed60389736c95fdf9d3375a9a04892fa8a98991e3a410840ecbcceeb0e5d52b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923360"
---
# <a name="cim_linkhasconnector-class"></a>CIM \_ LinkHasConnector-Klasse

Die **CIM \_ LinkHasConnector-Klasse** ordnet Kabel und Verbindungen zu, die als physische Connectors verwendet werden, die die physischen Elemente verbinden. Diese Zuordnung definiert explizit die Beziehung von Connectors für [**CIM \_ PhysicalLink**](cim-physicallink.md).

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{FAF76B8B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_LinkHasConnector : CIM_Component
{
  CIM_PhysicalConnector REF PartComponent;
  CIM_PhysicalLink      REF GroupComponent;
};
```

## <a name="members"></a>Member

Die **CIM \_ LinkHasConnector-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ LinkHasConnector-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ PhysicalLink**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max.**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ein [**CIM \_ PhysicalLink,**](cim-physicallink.md) der den physischen Link beschreibt, der über einen Connector verfügt.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ PhysicalConnector**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Ein [**\_ CIM PhysicalConnector,**](cim-physicalconnector.md) der den physischen Connector beschreibt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

WMI implementiert diese Klasse nicht.

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von dmtf veröffentlicht wurden. Möglicherweise hat Microsoft Änderungen vorgenommen, um kleinere Fehler zu korrigieren, den Dokumentationsstandards des Microsoft SDK zu entsprechen oder weitere Informationen bereitzustellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_CIM-Komponente**](cim-component.md)
</dt> </dl>

 

