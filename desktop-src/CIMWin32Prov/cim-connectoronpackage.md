---
description: Die \_ CIM-ConnectorOnPackage-Klasse stellt eine Zuordnung dar, die explizit die Einschlüssebeziehung zwischen Connectors und Paketen zuordnt. Physische Pakete enthalten Connectors sowie andere physische Elemente.
ms.assetid: 67cfb8c7-b952-452c-aeb4-0f06b2b0570b
ms.tgt_platform: multiple
title: CIM_ConnectorOnPackage-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConnectorOnPackage
- CIM_ConnectorOnPackage.LocationWithinContainer
- CIM_ConnectorOnPackage.PartComponent
- CIM_ConnectorOnPackage.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a135d70fcac745591b8d08ea4d116cde1e74f2276f0dd1ec839b05f569fec37d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119924920"
---
# <a name="cim_connectoronpackage-class"></a>\_CIM-ConnectorOnPackage-Klasse

Die **\_ CIM-ConnectorOnPackage-Klasse** stellt eine Zuordnung dar, die explizit die Einschlüssebeziehung zwischen Connectors und Paketen zuordnt. Physische Pakete enthalten Connectors sowie andere physische Elemente.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{FAF76B8C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ConnectorOnPackage : CIM_Container
{
  string                    LocationWithinContainer;
  CIM_PhysicalConnector REF PartComponent;
  CIM_PhysicalPackage   REF GroupComponent;
};
```

## <a name="members"></a>Member

Die **CIM \_ ConnectorOnPackage-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ ConnectorOnPackage-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ PhysicalPackage**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ein [**CIM \_ PhysicalPackage,**](cim-physicalpackage.md) das das physische Paket beschreibt, das über einen Connector verfügt.

</dd> <dt>

**LocationWithinContainer**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Freiformzeichenfolge, die die Positionierung des physischen Elements innerhalb des physischen Pakets darstellt. Informationen relativ zu den stationären Elementen im Container (z. B. "Zweiter Laufwerksschacht von oben"), Winkel, Höhe und andere Daten können in dieser Eigenschaft aufgezeichnet werden. Diese Zeichenfolge kann das CIM Location-Objekt ergänzen oder verwenden, statt [**es \_ zu**](cim-location.md) instanziieren.

Diese Eigenschaft wird vom [**\_ CIM-Container geerbt.**](cim-container.md)

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ PhysicalConnector**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Ein [**CIM \_ PhysicalConnector,**](cim-physicalconnector.md) der den physischen Connector beschreibt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\_ CIM-ConnectorOnPackage-Klasse** wird von [**\_ CIM-Container abgeleitet.**](cim-container.md)

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-Container**](cim-container.md)
</dt> </dl>

 

