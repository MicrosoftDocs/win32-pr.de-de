---
description: Die CIM \_ StorageRedundancyGroup-Klasse stellt Massenspeicherbezogene Redundanzinformationen dar.
ms.assetid: 6bc81680-672a-4872-8951-11d7f10acbc7
ms.tgt_platform: multiple
title: CIM_StorageRedundancyGroup-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageRedundancyGroup
- CIM_StorageRedundancyGroup.Caption
- CIM_StorageRedundancyGroup.Description
- CIM_StorageRedundancyGroup.InstallDate
- CIM_StorageRedundancyGroup.Name
- CIM_StorageRedundancyGroup.Status
- CIM_StorageRedundancyGroup.CreationClassName
- CIM_StorageRedundancyGroup.RedundancyStatus
- CIM_StorageRedundancyGroup.TypeOfAlgorithm
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 888da618a0c51fbbb81923e8ff5885d815c3327ab99f8bfa4f76571602059d9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119817810"
---
# <a name="cim_storageredundancygroup-class"></a>CIM \_ StorageRedundancyGroup-Klasse

Die **CIM \_ StorageRedundancyGroup-Klasse** stellt Massenspeicherbezogene Redundanzinformationen dar. Storage Redundanzgruppen werden verwendet, um Benutzerdaten zu schützen. Sie bestehen aus mindestens einem physischen Oder mehreren physischen Aggregatgrößen. Storage Redundanzgruppen können sich überschneiden. die zugrunde liegenden Erweiterungen innerhalb der Überlappung sollten jedoch keine Überprüfungsdaten enthalten.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird aus Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{6D477DBC-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_StorageRedundancyGroup : CIM_RedundancyGroup
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  uint16   RedundancyStatus;
  uint16   TypeOfAlgorithm;
};
```

## <a name="members"></a>Member

Die **CIM \_ StorageRedundancyGroup-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ StorageRedundancyGroup-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Eine kurze Textbeschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel,**](/windows/desktop/WmiSdk/key-qualifier) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird. Bei Verwendung mit anderen Schlüsseleigenschaften der -Klasse ermöglicht diese Eigenschaft die eindeutige Identifizierung aller Instanzen der -Klasse und ihrer Unterklassen.

Diese Eigenschaft wird von [**CIM \_ RedundancyGroup**](cim-redundancygroup.md)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Beschreibung")
</dt> </dl>

Eine Textbeschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Installationsdatum")
</dt> </dl>

Gibt an, wann das Objekt installiert wurde. Das Fehlen eines Werts gibt nicht an, dass das Objekt nicht installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Bezeichnung, mit der das Objekt bekannt ist. Bei Einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**RedundancyStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Informationen zum Status der Redundanzgruppe.

Diese Eigenschaft wird von [**CIM \_ RedundancyGroup**](cim-redundancygroup.md)geerbt.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd>

Unbekannt

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Andere** (1)


</dt> <dd>

Sonstiges

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Vollständig redundant** (2)


</dt> <dd>

Die gesamte konfigurierte Redundanz ist verfügbar.

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Heruntergestufte Redundanz** (3)


</dt> <dd>

Aufgrund einiger Fehler ist weniger Redundanz verfügbar.

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundanz verloren** (4)


</dt> <dd>

Redundanz ist aufgrund einer ausreichenden Anzahl von Fehlern nicht verfügbar. Der nächste Fehler führt zu einem Gesamtfehler.

</dd> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Zeichenfolge, die den aktuellen Status des Objekts angibt. Der Betriebsstatus und der nicht betriebsbereite Status können definiert werden. Der Betriebsstatus kann "OK", "Heruntergestuft" und "Fehler vor dem Fehler" enthalten. "Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. B. ein SMART-fähiges Festplattenlaufwerk).

Nicht betriebsbereite Status können "Error", "Starting", "Stopping" und "Service" sein. "Dienst" kann während der Datenträgerspiegelung, beim erneuten Laden einer Benutzerberechtigungsliste oder bei anderen Administrativen Arbeiten angewendet werden. Nicht alle dieser Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

Folgende Werte sind gültig:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Fehler** ("Fehler")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Heruntergestuft** ("Heruntergestuft")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** ("Unbekannt")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred Fail** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Wird gestartet** ("Wird gestartet")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Beenden** ("Wird beendet")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Dienst** ("Dienst")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Mannslast** ("1000")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Kein Kontakt** ("Kein Kontakt")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Verlorenes Komma** ("Verlorenes Komma")


</dt> <dd></dd> </dl>

</dd> <dt>

**TypeOfAlgorithm**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|DMTF-Redundanzgruppe \| 001.2")
</dt> </dl>

Algorithmus, der für Datenredundanz und -wiederherstellung verwendet wird. Der Wert 0 ist im CIM-Schema ungültig, da er darstellt, dass keine Redundanz in DMI vorhanden ist. In diesem Fall sollte das Objekt nicht instanziiert werden.

<dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

**Nicht definiert** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Andere** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="Copy"></span><span id="copy"></span><span id="COPY"></span>

**Kopieren** (3)


</dt> <dd></dd> <dt>

<span id="XOR"></span><span id="xor"></span>

**XOR** (4)


</dt> <dd></dd> <dt>

<span id="P_Q"></span><span id="p_q"></span>

**P+Q** (5)


</dt> <dd></dd> <dt>

<span id="S"></span><span id="s"></span>

**S** (6)


</dt> <dd></dd> <dt>

<span id="P_S"></span><span id="p_s"></span>

**P+S** (7)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **CIM \_ StorageRedundancyGroup-Klasse** wird von [**CIM \_ RedundancyGroup abgeleitet.**](cim-redundancygroup.md)

WMI implementiert diese Klasse nicht.

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden. Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ RedundancyGroup**](cim-redundancygroup.md)
</dt> </dl>

 

