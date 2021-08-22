---
description: Das CIM \_ CollectionOfMSEs-Objekt ermöglicht die Gruppierung von CIM \_ ManagedSystemElement-Objekten zum Zuordnen von Einstellungen und Konfigurationen. Es ist abstrakt, eine weitere Definition und semantische Optimierung in Unterklassen zu erfordern.
ms.assetid: 9448a7a1-defc-4bac-9ce6-29ec2406d573
ms.tgt_platform: multiple
title: CIM_CollectionOfMSEs-Klasse (CIMWin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfMSEs
- CIM_CollectionOfMSEs.Caption
- CIM_CollectionOfMSEs.CollectionID
- CIM_CollectionOfMSEs.Description
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d67b51e90a9a3c2eff420a5251c1b4e75f323d48e796a3190b662fb844c1517a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579050"
---
# <a name="cim_collectionofmses-class-cimwin32-wmi-providers"></a>CIM_CollectionOfMSEs-Klasse (CIMWin32-WMI-Anbieter)

Das **CIM \_ CollectionOfMSEs-Objekt** ermöglicht die Gruppierung von [**CIM \_ ManagedSystemElement-Objekten**](cim-managedsystemelement.md) zum Zuordnen von Einstellungen und Konfigurationen. Es ist abstrakt, eine weitere Definition und semantische Optimierung in Unterklassen zu erfordern.

Das **CIM \_ CollectionOfMSEs-Objekt** enthält keine Zustands- oder Statusinformationen, sondern stellt nur eine Gruppierung von Elementen dar. Aus diesem Grund ist es falsch, Unterklassengruppen mit Status/Status aus **CIM \_ CollectionOfMSEs** zu versehen. Ein Beispiel ist [**CIM \_ RedundancyGroup**](cim-redundancygroup.md) (die ordnungsgemäß aus [**CIM \_ LogicalElement**](cim-logicalelement.md)untergliedert ist). Sammlungen aggregieren in der Regel "like"-Objekte und stellen eine Optimierung dar. Ohne Sammlungen ist es erforderlich, einzelne [**CIM \_ ElementSetting-**](cim-elementsetting.md) und [**CIM \_ ElementConfiguration-Zuordnungen**](cim-elementconfiguration.md) zu definieren, um Einstellungen und Konfigurationsobjekte an einzelne [**CIM \_ ManagedSystemElements**](cim-managedsystemelement.md)zu binden. Es kann zu einer großen Duplizierung kommen, wenn die gleiche Einstellung mehreren Objekten zugewiesen wird. Darüber hinaus ermöglicht die Verwendung des Sammlungsobjekts die Bestimmung, dass die Einstellungs- und Konfigurationszuordnungen für die Elemente der Sammlung tatsächlich identisch sind. Diese Informationen würden andernfalls abgerufen werden, indem die Auflistung auf proprietäre Weise definiert und dann die **CIM \_ ElementSetting-** und **CIM \_ ElementConfiguration-Zuordnungen** abgefragt werden, um zu bestimmen, ob der Sammlungssatz vollständig abgedeckt ist.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
class CIM_CollectionOfMSEs
{
  string Caption;
  string CollectionID;
  string Description;
};
```

## <a name="members"></a>Member

Die **CIM \_ CollectionOfMSEs-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ CollectionOfMSEs-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Kurze Textbeschreibung des CollectionOfMSEs-Objekts.

</dd> <dt>

**CollectionID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Identifikation des Collection-Objekts. Bei einer Unterklasse kann die CollectionID-Eigenschaft als Key-Eigenschaft überschrieben werden.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Textbeschreibung des CollectionOfMSEs-Objekts.

</dd> </dl>

## <a name="remarks"></a>Hinweise

WMI implementiert diese Klasse nicht. Weitere Informationen finden Sie unter [Win32-Klassen](win32-provider.md) für WMI-Klassen, die von **CIM \_ CollectionOfMSEs** abgeleitet wurden.

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von dmtf veröffentlicht wurden. Möglicherweise hat Microsoft Änderungen vorgenommen, um kleinere Fehler zu korrigieren, den Dokumentationsstandards des Microsoft SDK zu entsprechen oder weitere Informationen bereitzustellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




