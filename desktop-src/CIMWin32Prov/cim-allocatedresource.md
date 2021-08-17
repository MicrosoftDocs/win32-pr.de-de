---
description: Die CIM AllocatedResource-Klasse stellt eine Zuordnung zwischen logischen Geräten und Systemressourcen dar und gibt an, dass die Ressource \_ dem Gerät zugewiesen ist.
ms.assetid: e1702635-32f5-4280-8c02-3940fd858106
ms.tgt_platform: multiple
title: CIM_AllocatedResource-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AllocatedResource
- CIM_AllocatedResource.Dependent
- CIM_AllocatedResource.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2caf51e4b6a76693a64253e1046ea74c6ec19b8f5895618419aa693a10260f56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322700"
---
# <a name="cim_allocatedresource-class"></a>CIM \_ AllocatedResource-Klasse

Die **CIM \_ AllocatedResource-Klasse** stellt eine Zuordnung zwischen logischen Geräten und Systemressourcen dar und gibt an, dass die Ressource dem Gerät zugewiesen ist.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{8502C579-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_AllocatedResource : CIM_Dependency
{
  CIM_LogicalDevice  REF Dependent;
  CIM_SystemResource REF Antecedent;
};
```

## <a name="members"></a>Member

Die **CIM \_ AllocatedResource-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ AllocatedResource-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ SystemResource**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorerst")
</dt> </dl>

Ein [**\_ CIM-SystemResource,**](cim-systemresource.md) das die Ressource beschreibt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LogicalDevice**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("Abhängig")
</dt> </dl>

Ein [**CIM \_ LogicalDevice,das**](cim-logicaldevice.md) das logische Gerät enthält, dem die Ressource zugewiesen ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **CIM \_ AllocatedResource-Klasse** wird von der [**\_ CIM-Abhängigkeit abgeleitet.**](cim-dependency.md)

WMI implementiert diese Klasse nicht. Weitere Informationen zu Klassen, die von **CIM \_ AllocatedResource abgeleitet werden,** finden Sie unter [Win32-Klassen.](win32-provider.md)

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden. Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.

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

[**\_CIM-Abhängigkeit**](cim-dependency.md)
</dt> </dl>

 

