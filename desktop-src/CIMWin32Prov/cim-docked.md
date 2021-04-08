---
description: Die in CIM \_ angedockte Zuordnung stellt die Beziehung zwischen zwei Chassis dar. Beispielsweise kann ein Laptop (ein Typ von Chassis) an einer Docking Station (einem anderen Typ von Chassis) angedockt werden. Diese typische Beziehung wird explizit beschrieben.
ms.assetid: 72cb36bb-f79e-4d1a-a859-4024031e4ebc
ms.tgt_platform: multiple
title: CIM_Docked-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Docked
- CIM_Docked.Dependent
- CIM_Docked.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 899b85d63293861f0a36df3d3c30610f8cff05ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748489"
---
# <a name="cim_docked-class"></a>CIM- \_ angedockte Klasse

Die in **CIM \_ angedockte** Zuordnung stellt die Beziehung zwischen zwei Chassis dar. Beispielsweise kann ein Laptop (ein Typ von Chassis) an einer Docking Station (einem anderen Typ von Chassis) angedockt werden. Diese typische Beziehung wird explizit beschrieben.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, MappingStrings("MIF.DMTF|Dynamic States|001.2"), UUID("{FAF76B75-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Docked : CIM_Dependency
{
  CIM_Chassis REF Dependent;
  CIM_Chassis REF Antecedent;
};
```

## <a name="members"></a>Member

Die **CIM- \_ angedockte** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die von **CIM \_ angedockte** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Chassis**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ein [**CIM- \_ Chassis**](cim-chassis.md) , das die Docking Station beschreibt.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Chassis**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ein [**CIM- \_ Chassis**](cim-chassis.md) , das den angedockten Laptop beschreibt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **CIM- \_ angedockte** Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.

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

 

