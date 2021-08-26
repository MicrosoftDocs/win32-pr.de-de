---
description: Die CIM \_ PackageInChassis-Zuordnung stellt die Beziehung dar, in der ein Gehäuse andere Pakete enthalten kann, z. B. andere Gehäuse und Karten.
ms.assetid: 3243bc0f-ce20-4108-b6e3-838bcb8f2fec
ms.tgt_platform: multiple
title: CIM_PackageInChassis-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageInChassis
- CIM_PackageInChassis.LocationWithinContainer
- CIM_PackageInChassis.PartComponent
- CIM_PackageInChassis.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2dec66ed5ee930db9bff7917e942de44bdc9582ec130a987e83cbb9d633523cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921300"
---
# <a name="cim_packageinchassis-class"></a>CIM \_ PackageInChassis-Klasse

Die **CIM \_ PackageInChassis-Zuordnung** stellt die Beziehung dar, in der ein Gehäuse andere Pakete enthalten kann, z. B. andere Gehäuse und Karten.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird aus Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{FAF76B74-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageInChassis : CIM_Container
{
  string                  LocationWithinContainer;
  CIM_PhysicalPackage REF PartComponent;
  CIM_Chassis         REF GroupComponent;
};
```

## <a name="members"></a>Member

Die **CIM \_ PackageInChassis-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ PackageInChassis-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Gehäuse**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max.**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ein [**\_ CIM-Gehäuse,**](cim-chassis.md) das das Gehäuse beschreibt, das andere physische Pakete enthält.

</dd> <dt>

**LocationWithinContainer**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Freiformzeichenfolge, die die Positionierung des physischen Elements innerhalb des physischen Pakets darstellt. Informationen relativ zu stationären Elementen im Container (z. B. "zweite Laufwerkbucht von oben"), Winkel, Höhen und andere Daten können in dieser Eigenschaft aufgezeichnet werden. Diese Zeichenfolge kann anstelle der Instanziierung des [**\_ CIM-Speicherortobjekts**](cim-location.md) ergänzt oder verwendet werden.

Diese Eigenschaft wird vom [**\_ CIM-Container**](cim-container.md)geerbt.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ PhysicalPackage**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Ein [**CIM \_ PhysicalPackage,**](cim-physicalpackage.md) das das physische Paket beschreibt, das im Gehäuse enthalten ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **CIM \_ PackageInChassis-Klasse** wird vom [**\_ CIM-Container**](cim-container.md)abgeleitet.

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

[**\_CIM-Container**](cim-container.md)
</dt> </dl>

 

