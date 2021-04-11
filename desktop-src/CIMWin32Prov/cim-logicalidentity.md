---
description: Die CIM \_ logicalidentity-Klasse ist eine abstrakte und generische Zuordnung, die angibt, dass zwei logische Elemente verschiedene Aspekte der gleichen zugrunde liegenden Entität darstellen.
ms.assetid: 624a52bf-001d-4f18-af77-87a5d1cfa1ff
ms.tgt_platform: multiple
title: CIM_LogicalIdentity-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalIdentity
- CIM_LogicalIdentity.SameElement
- CIM_LogicalIdentity.SystemElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 52780144a48cbb424ee037f71a56e238bb864311
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958247"
---
# <a name="cim_logicalidentity-class-cimwin32-wmi-providers"></a>CIM_LogicalIdentity-Klasse (cimwin32-WMI-Anbieter)

Die **CIM \_ logicalidentity** -Klasse ist eine abstrakte und generische Zuordnung, die angibt, dass zwei logische Elemente verschiedene Aspekte der gleichen zugrunde liegenden Entität darstellen. Die Zuordnung stellt dar, was mit Mehrfachvererbung definiert werden kann, und ist auf die logischen Aspekte eines verwalteten System Elements beschränkt. In den meisten Szenarios wird die Identitäts Beziehung durch die Äquivalenz von Schlüsseln oder einige andere identifizierende Eigenschaften der zugehörigen Elemente festgelegt.

Die Zuordnung sollte nur in Szenarios verwendet werden, die gut interpretiert werden und eine konkretere Definition und Klärung in Unterklassen ermöglichen. Ein Szenario, in dem die Beziehung vernünftig ist, stellt z. b. ein Gerät dar, das sowohl eine busentität als auch eine funktionale Entität ist, bei der es sich um eine USB-(Bus) und eine Tastatur (funktionale) Einheit handelt

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class CIM_LogicalIdentity
{
  CIM_LogicalElement REF SameElement;
  CIM_LogicalElement REF SystemElement;
};
```

## <a name="members"></a>Member

Die **CIM \_ logicalidentity** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ logicalidentity** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**SameElement**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LogicalElement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf einen alternativen Aspekt der System Entität.

</dd> <dt>

**Systemelement**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LogicalElement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf einen Aspekt des logischen Elements.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Klasse wird von WMI nicht implementiert. Informationen zu Klassen, die von **CIM \_ logicalidentity** abgeleitet sind, finden Sie unter [Win32 Classes](win32-provider.md).

Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet. Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




