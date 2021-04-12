---
description: Die CIM \_ cardoncard-Zuordnung beschreibt die Beziehungen zu Karten, die an den über Ladungen/Baseboards, daughtercards eines Adapters oder Karten mit speziellen Karten ähnlichen Modulen angeschlossen werden können.
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
ms.openlocfilehash: 15f94bb8d0f159e71cac44f069f9d8e7d9453509
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393118"
---
# <a name="cim_cardoncard-class"></a>CIM \_ cardoncard-Klasse

Die **CIM \_ cardoncard** -Zuordnung beschreibt die Beziehungen zu Karten, die an den über Ladungen/Baseboards, daughtercards eines Adapters oder Karten mit speziellen Karten ähnlichen Modulen angeschlossen werden können.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

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

Die **CIM \_ cardoncard** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ cardoncard** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Karte**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Eine [**CIM- \_ Karte**](cim-card.md) , die die Karte beschreibt, die eine andere Karte hostet.

</dd> <dt>

**Locationwithincontainer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine frei Form Zeichenfolge, die die Positionierung des physischen Elements innerhalb des physischen Pakets darstellt. Informationen in Bezug auf die stationären Elemente im Container (z. b. "Second Drive Bay from the Top"), Winkel, Höhen und andere Daten können in dieser Eigenschaft aufgezeichnet werden. Diese Zeichenfolge kann anstelle der Instanziierung des [**CIM- \_ Speicherort**](cim-location.md) Objekts ergänzt oder verwendet werden.

Diese Eigenschaft wird vom [**CIM- \_ Container**](cim-container.md)geerbt.

</dd> <dt>

**Mountor slotdescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Hier wird beschrieben, wie die Karte an der Karte "Other" eingebunden oder an diese angeschlossen wird. Slotinformationen können in dieses Feld eingeschlossen werden und sind möglicherweise für bestimmte Verwaltungszwecke ausreichend. Dadurch wird das Erstellen von Instanziierungen von Connector/Slot-Objekten vermieden, um die Beziehung von Karten zu hostingboards oder anderen Adaptern zu modellieren. Wenn die Informationen zum Slot und zum Connector verfügbar sind, können Sie dieses Feld verwenden, um ausführliche Einfügungs-oder einfügeeinfügedaten bereitzustellen.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Karte**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Eine [**CIM- \_ Karte**](cim-card.md) , die die Karte beschreibt, die an eine andere Karte angeschlossen ist oder anderweitig bereitgestellt wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **CIM \_ cardoncard** -Klasse wird vom [**CIM- \_ Container**](cim-container.md)abgeleitet.

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

[**CIM- \_ Container**](cim-container.md)
</dt> </dl>

 

