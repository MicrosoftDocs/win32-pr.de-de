---
description: Die CIM SoftwareFeatureServiceImplementation-Klasse stellt eine Zuordnung zwischen einem Dienst und seiner \_ Umsetzung in Software dar.
ms.assetid: fa80cc91-8dd7-4726-a24a-5c4dfa3e786b
ms.tgt_platform: multiple
title: CIM_SoftwareFeatureServiceImplementation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureServiceImplementation
- CIM_SoftwareFeatureServiceImplementation.Dependent
- CIM_SoftwareFeatureServiceImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b89be16ac5b462d9a4b10441699c6c160a91bd3ef5222b2a7cd642413c4c2081
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919200"
---
# <a name="cim_softwarefeatureserviceimplementation-class"></a>CIM \_ SoftwareFeatureServiceImplementation-Klasse

Die **CIM \_ SoftwareFeatureServiceImplementation-Klasse** stellt eine Zuordnung zwischen einem Dienst und seiner Umsetzung in Software dar. Ein Dienst kann von mehr als einem Softwarefeature bereitgestellt werden, das in Verbindung miteinander ausgeführt wird. Darüber hinaus kann ein Softwarefeature mehrere Dienste bereitstellen. Wenn einem einzelnen Dienst mehrere Softwarefeatures zugeordnet sind, wird davon ausgegangen, dass die Elemente in Verbindung mit der Bereitstellung des Diensts funktionieren. Wenn verschiedene Implementierungen eines Diensts vorhanden sind, führt jede Implementierung zu einzelnen Instanziierungen des Dienstobjekts. Einzelne Instanziierungen würden dann Zuordnungen zu den eindeutigen Implementierungen haben.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[UUID("{8AC984F4-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureServiceImplementation : CIM_Dependency
{
  CIM_Service         REF Dependent;
  CIM_SoftwareFeature REF Antecedent;
};
```

## <a name="members"></a>Member

Die **CIM \_ SoftwareFeatureServiceImplementation-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ SoftwareFeatureServiceImplementation-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ SoftwareFeature**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Ein [**\_ CIM-SoftwareFeature,**](cim-softwarefeature.md) das die vorigen Softwarefeatures beschreibt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Dienst**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Min.**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("Abhängig")
</dt> </dl>

Ein [**\_ CIM-Dienst,**](cim-service.md) der den abhängigen Dienst beschreibt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **CIM \_ SoftwareFeatureServiceImplementation-Klasse** wird von [**der CIM-Abhängigkeit \_ abgeleitet.**](cim-dependency.md)

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_CIM-Abhängigkeit**](cim-dependency.md)
</dt> </dl>

 

