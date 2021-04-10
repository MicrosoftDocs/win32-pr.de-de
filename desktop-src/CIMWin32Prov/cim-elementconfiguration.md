---
description: Die CIM-ElementConfiguration-Zuordnung verknüpft \_ ein CIM- \_ Konfigurationsobjekt mit einem oder mehreren verwalteten Systemelementen. Das CIM- \_ Konfigurationsobjekt stellt ein bestimmtes Verhalten oder einen gewünschten funktionalen Zustand für das zugeordnete CIM \_ ManagedSystemElement dar.
ms.assetid: 4d2af009-7466-4394-af42-72c8d96e0786
ms.tgt_platform: multiple
title: CIM_ElementConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementConfiguration
- CIM_ElementConfiguration.Configuration
- CIM_ElementConfiguration.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7707338a3c2268cba51146aa8462b3b244b149ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041452"
---
# <a name="cim_elementconfiguration-class"></a>CIM \_ ElementConfiguration-Klasse

Die **CIM- \_ ElementConfiguration** -Zuordnung verknüpft ein [**CIM- \_ Konfigurations**](cim-configuration.md) Objekt mit einem oder mehreren verwalteten Systemelementen. Das **CIM- \_ Konfigurations** Objekt stellt ein bestimmtes Verhalten oder einen gewünschten funktionalen Zustand für das zugeordnete [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)dar.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{FC049DCE-DB29-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ElementConfiguration
{
  CIM_Configuration        REF Configuration;
  CIM_ManagedSystemElement REF Element;
};
```

## <a name="members"></a>Member

Die **CIM \_ ElementConfiguration** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ ElementConfiguration** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Configuration**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Konfiguration**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf das [**CIM- \_ Konfigurations**](cim-configuration.md) Objekt, das die dem verwalteten System Element zugeordneten Einstellungen und Abhängigkeiten gruppiert.

</dd> <dt>

**Element**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ManagedSystemElement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf das verwaltete System Element.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Klasse wird von WMI nicht implementiert.

Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet. Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




