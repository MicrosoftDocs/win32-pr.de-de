---
description: Die CIM \_ -Klasse "stestedaccesspoint" stellt eine Zuordnung zwischen einem Dienst Zugriffspunkt (SAP) und dem System dar, auf dem es bereitgestellt wird. Jedes System hostet möglicherweise viele SAPS.
ms.assetid: 7da9b781-a5cb-42f5-b03c-4fc818c94e88
ms.tgt_platform: multiple
title: CIM_HostedAccessPoint-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedAccessPoint
- CIM_HostedAccessPoint.Dependent
- CIM_HostedAccessPoint.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d451cec7ad42fa519b70c576fbd02a32d0289e8b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126973"
---
# <a name="cim_hostedaccesspoint-class-cimwin32-wmi-providers"></a>CIM_HostedAccessPoint-Klasse (cimwin32-WMI-Anbieter)

Die CIM-Klasse " **\_ stestedaccesspoint** " stellt eine Zuordnung zwischen einem Dienst Zugriffspunkt (SAP) und dem System dar, auf dem es bereitgestellt wird. Jedes System hostet möglicherweise viele SAPS.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{576C3C56-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedAccessPoint : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_System             REF Antecedent;
};
```

## <a name="members"></a>Member

Die CIM-Klasse " **\_ tarstedaccesspoint** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die CIM-Klasse " **\_ stestedaccesspoint** " verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ System**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ein [**CIM- \_ System**](cim-system.md) , das das Hostingsystem beschreibt.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ serviceaccesspoint**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig"), [**schwach**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Ein [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md) , der die SAP (s) beschreibt, die auf diesem System gehostet werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

**CIM \_ "Hustedaccesspoint** " ist von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.

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

 

