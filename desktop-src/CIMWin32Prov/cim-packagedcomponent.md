---
description: Die CIM PackagedComponent-Zuordnung stellt eine explizite Beziehung dar, in der eine Komponente in der Regel in einem physischen Paket enthalten ist, z. B. einem Gehäuse \_ oder einer Karte.
ms.assetid: ef0cdbc4-41ee-4517-92ca-61cfcbe64c36
ms.tgt_platform: multiple
title: CIM_PackagedComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackagedComponent
- CIM_PackagedComponent.LocationWithinContainer
- CIM_PackagedComponent.PartComponent
- CIM_PackagedComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: deda43cc153baf320f5c927438314114edf3ec2d92d9e96af95707d1b7805e56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118422030"
---
# <a name="cim_packagedcomponent-class"></a>CIM \_ PackagedComponent-Klasse

Die **CIM \_ PackagedComponent-Zuordnung** stellt eine explizite Beziehung dar, in der eine Komponente in der Regel in einem physischen Paket enthalten ist, z. B. einem Gehäuse oder einer Karte.

**Hinweis:**  Eine Komponente kann aus dem enthaltenden Paket entfernt oder noch nicht  in das enthaltende Paket eingefügt werden (d. h., die boolesche Wechseleigenschaft ist **TRUE).** Daher ist eine Komponente möglicherweise nicht immer einem Container zugeordnet.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{FAF76B79-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackagedComponent : CIM_Container
{
  string                    LocationWithinContainer;
  CIM_PhysicalComponent REF PartComponent;
  CIM_PhysicalPackage   REF GroupComponent;
};
```

## <a name="members"></a>Member

Die **CIM \_ PackagedComponent-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ PackagedComponent-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ PhysicalPackage**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ein [**CIM \_ PhysicalPackage,**](cim-physicalpackage.md) das das physische Paket beschreibt, das Komponenten enthält.

</dd> <dt>

**LocationWithinContainer**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Freiformzeichenfolge, die die Positionierung des physischen Elements innerhalb des physischen Pakets darstellt. Informationen relativ zu stationären Elementen im Container (z. B. "Zweiter Laufwerksschacht von oben"), Winkel, Höhe und andere Daten können in dieser Eigenschaft aufgezeichnet werden. Diese Zeichenfolge kann das CIM Location-Objekt ergänzen oder verwenden, statt es [**\_ zu**](cim-location.md) instanziieren.

Diese Eigenschaft wird vom [**\_ CIM-Container geerbt.**](cim-container.md)

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ PhysicalComponent**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Eine [**CIM \_ PhysicalComponent,**](cim-physicalcomponent.md) die die physische Komponente beschreibt, die im Paket enthalten ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **CIM \_ PackagedComponent-Klasse** wird von [**CIM Container \_ abgeleitet.**](cim-container.md)

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

[**\_CIM-Container**](cim-container.md)
</dt> </dl>

 

