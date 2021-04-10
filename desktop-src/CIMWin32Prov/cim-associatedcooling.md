---
description: Die CIM \_ associatedcooling-Zuordnung gibt an, wann die Lüfter oder andere Kühlgeräte für ein Gerät spezifisch sind (im Gegensatz zur Bereitstellung von Gehäuse oder CAB-Kühlung).
ms.assetid: 7b20e429-593c-4365-a340-1aef9b0fadf5
ms.tgt_platform: multiple
title: CIM_AssociatedCooling-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedCooling
- CIM_AssociatedCooling.Dependent
- CIM_AssociatedCooling.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb838129226b225f024917e8f8e77ddc92ddf2ff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127213"
---
# <a name="cim_associatedcooling-class"></a>CIM \_ associatedcooling-Klasse

Die **CIM \_ associatedcooling** -Zuordnung gibt an, wann die Lüfter oder andere Kühlgeräte für ein Gerät spezifisch sind (im Gegensatz zur Bereitstellung von Gehäuse oder CAB-Kühlung).

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{306F88F2-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedCooling : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_CoolingDevice REF Antecedent;
};
```

## <a name="members"></a>Member

Die **CIM \_ associatedcooling** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ associatedcooling** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ coolingdevice**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")
</dt> </dl>

Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das das Kühlgerät beschreibt.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LogicalDevice**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")
</dt> </dl>

Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das auf das zu kühlende logische Gerät verweist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **CIM \_ associatedcooling** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Abhängigkeit**](cim-dependency.md)
</dt> </dl>

 

