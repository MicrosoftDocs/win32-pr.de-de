---
description: Das CIM \_ CollectionOfMSEs-Objekt ermöglicht das Gruppieren von CIM \_ ManagedSystemElement-Objekten zum Zweck der Zuordnung von Einstellungen und Konfigurationen. Es ist abstrakt, eine weitere Definition und semantische Optimierung in Unterklassen zu erfordern.
ms.assetid: 9448a7a1-defc-4bac-9ce6-29ec2406d573
ms.tgt_platform: multiple
title: CIM_CollectionOfMSEs-Klasse (cimwin32-WMI-Anbieter)
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
ms.openlocfilehash: 57942dd6e00d819e4375ddd316e5e15126621b97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127109"
---
# <a name="cim_collectionofmses-class-cimwin32-wmi-providers"></a>CIM_CollectionOfMSEs-Klasse (cimwin32-WMI-Anbieter)

Das **CIM \_ CollectionOfMSEs** -Objekt ermöglicht das Gruppieren von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) -Objekten zum Zweck der Zuordnung von Einstellungen und Konfigurationen. Es ist abstrakt, eine weitere Definition und semantische Optimierung in Unterklassen zu erfordern.

Das **CIM \_ CollectionOfMSEs** -Objekt enthält keine Zustands-oder Statusinformationen, sondern stellt nur eine Gruppierung von Elementen dar. Aus diesem Grund ist es nicht möglich, Unterklassen Gruppen mit dem Status/Status von **CIM \_ CollectionOfMSEs** zu unterordnen. ein Beispiel hierfür ist [**CIM \_ redundant cygroup**](cim-redundancygroup.md) (die ordnungsgemäß von [**CIM \_ LogicalElement**](cim-logicalelement.md)untergeordnet ist). Auflistungen aggregieren üblicherweise "like"-Objekte und stellen eine Optimierung dar. Ohne Auflistungen ist es gezwungen, einzelne [**CIM- \_ Element Setting**](cim-elementsetting.md) -und [**CIM \_ Element Configuration**](cim-elementconfiguration.md) -Zuordnungen zu definieren, um Einstellungen und Konfigurationsobjekte an einzelne [**CIM \_ ManagedSystemElements**](cim-managedsystemelement.md)zu binden. Es kann sehr viel dupliziert werden, wenn die gleiche Einstellung mehreren Objekten zugewiesen wird. Außerdem ermöglicht die Verwendung des Auflistungs Objekts die Bestimmung, dass die Einstellungs-und Konfigurations Zuordnungen für die Mitglieder der Auflistung tatsächlich identisch sind. Diese Informationen würden Sie andernfalls erhalten, indem Sie die Auflistung auf proprietäre Weise definieren und dann die CIM- **\_ Element Setting** -und **CIM \_ ElementConfiguration** -Zuordnungen Abfragen, um zu ermitteln, ob der Sammlungs Satz vollständig abgedeckt ist.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

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

Die **CIM \_ CollectionOfMSEs** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ CollectionOfMSEs** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Kurze Textbeschreibung für das CollectionOfMSEs-Objekt.

</dd> <dt>

**Sammlungs**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Identifikation des Auflistungs Objekts. Bei einer Unterklasse kann die CollectionId-Eigenschaft als Schlüsseleigenschaft überschrieben werden.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Textbeschreibung des CollectionOfMSEs-Objekts.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Klasse wird von WMI nicht implementiert. Siehe [Win32-Klassen](win32-provider.md) für WMI-Klassen, die von **CIM \_ CollectionOfMSEs** abgeleitet sind.

Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet. Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




