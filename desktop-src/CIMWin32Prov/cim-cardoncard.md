---
description: Die CIM \_ CardOnCard-Zuordnung beschreibt Beziehungen zu Karten, die in Hauptplatinen/Baseboards, Adapterkarten eines Adapters oder Karten, die spezielle kartenähnliche Module unterstützen, angeschlossen werden können.
ms.assetid: a500b29d-d836-4755-b5df-b296e3cbd2ab
ms.tgt_platform: multiple
title: CIM_CardOnCard-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CardOnCard
- CIM_CardOnCard.LocationWithinContainer
- CIM_CardOnCard.PartComponent
- CIM_CardOnCard.GroupComponent
- CIM_CardOnCard.MountOrSlotDescription
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2f6b20d95505f1e6dbbda31506660f3825541f8f2a0ecdcb6cf293d7d6d4a0df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322440"
---
# <a name="cim_cardoncard-class"></a>CIM \_ CardOnCard-Klasse

Die **CIM \_ CardOnCard-Zuordnung** beschreibt Beziehungen zu Karten, die in Hauptplatinen/Baseboards, Adapterkarten eines Adapters oder Karten, die spezielle kartenähnliche Module unterstützen, angeschlossen werden können.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{FAF76B77-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_CardOnCard : CIM_Container
{
  string       LocationWithinContainer;
  CIM_Card REF PartComponent;
  CIM_Card REF GroupComponent;
  string       MountOrSlotDescription;
};
```

## <a name="members"></a>Member

Die **CIM \_ CardOnCard-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ CardOnCard-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Karte**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max.**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Eine [**\_ CIM-Karte,**](cim-card.md) die die Karte beschreibt, die eine andere Karte hostet.

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

**MountOrSlotDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Beschreibt und identifiziert, wie die Karte auf der "anderen" Karte eingebunden oder in diese eingebunden wird. Slotinformationen können in diesem Feld enthalten sein und können für bestimmte Verwaltungszwecke ausreichen. Dadurch wird vermieden, dass Instanziierungen von Connector-/Slotobjekten erstellt werden, nur um die Beziehung von Karten zu Hostboards oder anderen Adaptern zu modellieren. Wenn andererseits Slot- und Connectorinformationen verfügbar sind, kann dieses Feld verwendet werden, um detaillierte Einbindungs- oder Einfügedaten für ein Slot bereitzustellen.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Karte**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Eine [**\_ CIM-Karte,**](cim-card.md) die die Karte beschreibt, die an eine andere Karte angeschlossen oder anderweitig eingebunden ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **CIM \_ CardOnCard-Klasse** wird von [**\_ CIM-Container**](cim-container.md)abgeleitet.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_CIM-Container**](cim-container.md)
</dt> </dl>

 

