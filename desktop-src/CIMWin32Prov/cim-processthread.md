---
description: Die CIM \_ ProcessThread-Klasse stellt eine Verknüpfung zwischen einem Prozess und den Threads dar, die im Kontext des Prozesses ausgeführt werden.
ms.assetid: e71543c5-d9b3-4f98-93a6-08f977a26305
ms.tgt_platform: multiple
title: CIM_ProcessThread-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProcessThread
- CIM_ProcessThread.PartComponent
- CIM_ProcessThread.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dfc8e900704d165215b38b55d8f129e6583a47477152287687bd4644230b58ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118421891"
---
# <a name="cim_processthread-class"></a>CIM \_ ProcessThread-Klasse

Die **CIM \_ ProcessThread-Klasse** stellt eine Verknüpfung zwischen einem Prozess und den Threads dar, die im Kontext des Prozesses ausgeführt werden.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{B7E6042C-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ProcessThread : CIM_Component
{
  CIM_Thread  REF PartComponent;
  CIM_Process REF GroupComponent;
};
```

## <a name="members"></a>Member

Die **CIM \_ ProcessThread-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ ProcessThread-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Prozess**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Max(**](/windows/desktop/WmiSdk/standard-qualifiers) 1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Ein [**\_ CIM-Prozess,**](cim-process.md) der den Prozess beschreibt.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Thread**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Schwach**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Ein [**\_ CIM-Thread,**](cim-thread.md) der den Thread beschreibt, der im Kontext des Prozesses ausgeführt wird.

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

 

