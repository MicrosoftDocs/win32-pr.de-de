---
description: Die CIM \_ SoftwareFeatureSAPImplementation-Klasse stellt eine Zuordnung zwischen einem Dienstzugriffspunkt (SAP) und ihrer Implementierung in Software dar.
ms.assetid: d9a5a747-b37b-4005-a661-2bfc6a83bbb2
ms.tgt_platform: multiple
title: CIM_SoftwareFeatureSAPImplementation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureSAPImplementation
- CIM_SoftwareFeatureSAPImplementation.Dependent
- CIM_SoftwareFeatureSAPImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ca763199f346936431671d99190595455cc4142d78e749183bcbf5183fc65995
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119817830"
---
# <a name="cim_softwarefeaturesapimplementation-class"></a>CIM \_ SoftwareFeatureSAPImplementation-Klasse

Die **CIM \_ SoftwareFeatureSAPImplementation-Klasse** stellt eine Zuordnung zwischen einem Dienstzugriffspunkt (SAP) und ihrer Implementierung in Software dar. Ein SAP kann von mehreren Softwarefeatures bereitgestellt werden, um in Verbindung miteinander zu arbeiten. Darüber hinaus kann ein Softwarefeature mehrere SAP-Funktionen bereitstellen. Wenn viele Softwarefeatures einem einzelnen SAP zugeordnet sind, wird davon ausgegangen, dass die Elemente zusammen ausgeführt werden, um den Zugriffspunkt bereitzustellen. Wenn unterschiedliche Implementierungen eines SAP vorhanden sind, würde jede Implementierung zu einzelnen Instanziierungen des SAP-Objekts führen. Einzelne Instanziierungen verfügen dann über Zuordnungen zu den eindeutigen Implementierungen.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird aus Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[UUID("{7EFCC186-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureSAPImplementation : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_SoftwareFeature    REF Antecedent;
};
```

## <a name="members"></a>Member

Die **CIM \_ SoftwareFeatureSAPImplementation-Klasse** verfügt über folgende Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ SoftwareFeatureSAPImplementation-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ SoftwareFeature**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Min.**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")
</dt> </dl>

Ein [**CIM \_ SoftwareFeature,**](cim-softwarefeature.md) das das Vorgängersoftwarefeature beschreibt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ServiceAccessPoint**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Min.**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("abhängig")
</dt> </dl>

Ein [**CIM \_ ServiceAccessPoint,**](cim-serviceaccesspoint.md) der den abhängigen Dienstzugriffspunkt beschreibt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **CIM \_ SoftwareFeatureSAPImplementation-Klasse** wird von [**\_ CIM-Abhängigkeit**](cim-dependency.md)abgeleitet.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-Abhängigkeit**](cim-dependency.md)
</dt> </dl>

 

