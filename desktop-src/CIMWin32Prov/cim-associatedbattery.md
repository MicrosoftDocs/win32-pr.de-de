---
description: Die CIM \_ AssociatedBattery-Abhängigkeit ordnet einem logischen Gerät einen Akku zu. Verwenden Sie diese Zuordnung, um einzelne Akkus zu modellieren, die eine unterbrechungsfreie Stromversorgung (USV) machen.
ms.assetid: f8d8b3d3-edc5-438a-8be6-3ea4d765085b
ms.tgt_platform: multiple
title: CIM_AssociatedBattery-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedBattery
- CIM_AssociatedBattery.Dependent
- CIM_AssociatedBattery.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 76529a63b2600543602727c14aea4c7972e8b51f7c67924da9eb06f1185c427e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119284590"
---
# <a name="cim_associatedbattery-class"></a>CIM \_ AssociatedBattery-Klasse

Die **CIM \_ AssociatedBattery-Abhängigkeit** ordnet einem logischen Gerät einen Akku zu. Verwenden Sie diese Zuordnung, um einzelne Akkus zu modellieren, die eine unterbrechungsfreie Stromversorgung (USV) machen.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{8502C578-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedBattery : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_Battery       REF Antecedent;
};
```

## <a name="members"></a>Member

Die **CIM \_ AssociatedBattery-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ AssociatedBattery-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Akku**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Ein [**\_ CIM-Akku,**](cim-battery.md) der den Akku beschreibt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LogicalDevice**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Abhängig")
</dt> </dl>

Ein [**CIM \_ LogicalDevice-Gerät,**](cim-logicaldevice.md) das das logische Gerät enthält, das den Akku benötigt oder dem Akku zugeordnet ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **CIM \_ AssociatedBattery-Klasse** wird von der [**\_ CIM-Abhängigkeit abgeleitet.**](cim-dependency.md)

WMI implementiert diese Klasse nicht. Weitere Informationen zu Klassen, die von **CIM \_ AssociatedBattery abgeleitet werden,** finden Sie unter [Win32-Klassen.](win32-provider.md)

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

[**\_CIM-Abhängigkeit**](cim-dependency.md)
</dt> </dl>

 

