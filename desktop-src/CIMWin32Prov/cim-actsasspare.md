---
description: Die \_ CIM-Zuordnung "ActsAsSpare" gibt an, welche Elemente verschont oder andere aggregierte Elemente ersetzt werden können. Ein Ersatz kann im modus &\# 0034;hot-standby&\# 0034; wie auf Element-für-Element-Basis angegeben betrieben werden.
ms.assetid: bed8c552-f782-4af9-9441-ff3268182c3b
ms.tgt_platform: multiple
title: CIM_ActsAsSpare-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActsAsSpare
- CIM_ActsAsSpare.Group
- CIM_ActsAsSpare.HotStandby
- CIM_ActsAsSpare.Spare
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6b76b9dbd4a5a3302d1aae328bcd096dee5cd03e1615d3c7e30c58f3344ea67f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119080954"
---
# <a name="cim_actsasspare-class"></a>CIM \_ ActsAsSpare-Klasse

Die **\_ CIM-Zuordnung "ActsAsSpare"** gibt an, welche Elemente verschont oder andere aggregierte Elemente ersetzt werden können. Ein Ersatz kann im Modus "Heißer Standbymodus" ausgeführt werden, wie auf Element-für-Element-Basis angegeben.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Association, UUID("{64C1726E-DB21-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ActsAsSpare
{
  CIM_SpareGroup           REF Group;
  boolean                      HotStandby;
  CIM_ManagedSystemElement REF Spare;
};
```

## <a name="members"></a>Member

Die **CIM \_ ActsAsSpare-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ ActsAsSpare-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Gruppe**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ SpareGroup**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf die **Group-Eigenschaft,** die die [**CIM \_ SpareGroup-Klasse**](cim-sparegroup.md) darstellt.

</dd> <dt>

**HotStandby**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True **gibt an,** dass der Ersatz als Standbymodus "Hot" ausgeführt wird.

</dd> <dt>

**Ersatz**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ManagedSystemElement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf ein verwaltetes Systemelement, das als Ersatz verwendet wird und teil der Ersatzgruppe ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

WMI implementiert diese Klasse nicht.

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden. Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[CIM-Klassen](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

