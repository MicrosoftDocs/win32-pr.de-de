---
description: Die CIM OSProcess-Klasse ordnet das Betriebssystem und einen oder mehrere Prozesse zu, die \_ im Kontext des Betriebssystems ausgeführt werden.
ms.assetid: 59d52b29-9d97-464f-bbbc-4191305df8c7
ms.tgt_platform: multiple
title: CIM_OSProcess-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OSProcess
- CIM_OSProcess.PartComponent
- CIM_OSProcess.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 62cb209f37a89fd0d2456c2f9760060a69af8cbb45d2dd15b608a1201409c509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921310"
---
# <a name="cim_osprocess-class"></a>CIM \_ OSProcess-Klasse

Die **CIM \_ OSProcess-Klasse** ordnet das Betriebssystem und einen oder mehrere Prozesse zu, die im Kontext des Betriebssystems ausgeführt werden.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{A361A7AE-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_OSProcess : CIM_Component
{
  CIM_Process         REF PartComponent;
  CIM_OperatingSystem REF GroupComponent;
};
```

## <a name="members"></a>Member

Die **CIM \_ OSProcess-Klasse** verfügt über diese Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ OSProcess-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ OperatingSystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Max.**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min.**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Ein [**\_ CIM-Betriebssystem,**](cim-operatingsystem.md) das das Betriebssystem beschreibt.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Prozess**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Schwach**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Ein [**\_ CIM-Prozess,**](cim-process.md) der den Prozess beschreibt, der im Kontext des Betriebssystems ausgeführt wird.

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

[**\_CIM-Komponente**](cim-component.md)
</dt> </dl>

 

