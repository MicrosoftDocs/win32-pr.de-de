---
description: Die CIM Card-Klasse stellt einen physischen Containertyp dar, der an eine andere Karte oder ein Hostingboard angeschlossen werden kann, oder ist selbst ein Hostingboard bzw. eine Hauptplatine \_ in einem Gehäuse.
ms.assetid: edbbfe43-c8e8-4cde-9507-e0a248c15ca7
ms.tgt_platform: multiple
title: CIM_Card-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Card
- CIM_Card.Caption
- CIM_Card.Description
- CIM_Card.InstallDate
- CIM_Card.Name
- CIM_Card.Status
- CIM_Card.CreationClassName
- CIM_Card.Manufacturer
- CIM_Card.Model
- CIM_Card.OtherIdentifyingInfo
- CIM_Card.PartNumber
- CIM_Card.PoweredOn
- CIM_Card.SerialNumber
- CIM_Card.SKU
- CIM_Card.Tag
- CIM_Card.Version
- CIM_Card.Depth
- CIM_Card.Height
- CIM_Card.HotSwappable
- CIM_Card.Removable
- CIM_Card.Replaceable
- CIM_Card.Weight
- CIM_Card.Width
- CIM_Card.HostingBoard
- CIM_Card.RequirementsDescription
- CIM_Card.RequiresDaughterBoard
- CIM_Card.SlotLayout
- CIM_Card.SpecialRequirements
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9ea55b96fda6493d0f0790c3a75e5a4876131bab686b0f8aef1101dc98674f61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119284520"
---
# <a name="cim_card-class"></a>CIM \_ Card-Klasse

Die **CIM \_ Card-Klasse** stellt einen physischen Containertyp dar, der an eine andere Karte oder ein Hostingboard angeschlossen werden kann, oder ist selbst ein Hostingboard bzw. eine Hauptplatine in einem Gehäuse. Diese Klasse enthält alle Pakete, die Signale tragen und einen Bereitstellungspunkt für physische Komponenten bereitstellen können, z. B. Chips oder andere physische Pakete, z. B. andere Karten.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[abstract, UUID("{FAF76B76-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Card : CIM_PhysicalPackage
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   Manufacturer;
  string   Model;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Tag;
  string   Version;
  real32   Depth;
  real32   Height;
  boolean  HotSwappable;
  boolean  Removable;
  boolean  Replaceable;
  real32   Weight;
  real32   Width;
  boolean  HostingBoard;
  string   RequirementsDescription;
  boolean  RequiresDaughterBoard;
  string   SlotLayout;
  boolean  SpecialRequirements;
};
```

## <a name="members"></a>Member

Die **CIM \_ Card-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **CIM \_ Card-Klasse** verfügt über diese Methoden.



| Methode                                                        | Beschreibung                                                                                                                                    |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**IsCompatible**](iscompatible-method-in-class-cim-card.md) | Überprüft, ob das physische Element, auf das verwiesen wird, im physischen Paket enthalten oder in dieses eingefügt werden kann. Nicht von WMI implementiert.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **CIM \_ Card-Klasse** verfügt über diese Eigenschaften.

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

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**\_ CIM-Schlüssel,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird. Bei Verwendung mit anderen Schlüsseleigenschaften der -Klasse ermöglicht diese Eigenschaft, dass alle Instanzen der Klasse und deren Unterklassen eindeutig identifiziert werden.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement geerbt.**](cim-physicalelement.md)

</dd> <dt>

**Tiefe**
</dt> <dd> <dl> <dt>

Datentyp: **real32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zoll")
</dt> </dl>

Tiefe des physischen Pakets in Zoll.

Diese Eigenschaft wird von [**CIM \_ PhysicalPackage geerbt.**](cim-physicalpackage.md)

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Eine Textbeschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**Height**
</dt> <dd> <dl> <dt>

Datentyp: **real32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zoll")
</dt> </dl>

Höhe des physischen Pakets in Zoll.

Diese Eigenschaft wird von [**CIM \_ PhysicalPackage geerbt.**](cim-physicalpackage.md)

</dd> <dt>

**HostingBoard**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True **gibt an,** dass es sich bei dieser Karte um eine Hauptplatine oder allgemeiner um ein Baseboard in einem Gehäuse handelt.

</dd> <dt>

**HotSwappable**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True **gibt an,** dass das Paket im heißen Tausch verwendet werden kann. Ein physisches Paket kann im Hot-Swap-Format ausgetauscht werden, wenn das Element durch ein physisch anderes (aber äquivalentes) ersetzt werden kann, während das enthaltende Paket aktiviert ist. Beispielsweise kann eine Lüfterkomponente so entworfen werden, dass sie hot-swaped ist. Alle Komponenten, die im Hot-Swap-System ausgetauscht werden können, sind grundsätzlich austauschbar und austauschbar.

Diese Eigenschaft wird von [**CIM \_ PhysicalPackage geerbt.**](cim-physicalpackage.md)

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

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Name der Organisation, die für die Erstellung des physischen Elements verantwortlich ist. Weitere Informationen finden Sie unter der **Vendor-Eigenschaft** von [**CIM \_ Product**](cim-product.md).

Diese Eigenschaft wird von [**CIM \_ PhysicalElement geerbt.**](cim-physicalelement.md)

</dd> <dt>

**Modell**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Name, unter dem das physische Element allgemein bekannt ist.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement geerbt.**](cim-physicalelement.md)

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Bezeichnung, unter der das Objekt bekannt ist. Bei Unterklassen kann diese Eigenschaft überschrieben werden, um eine Schlüsseleigenschaft zu sein.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zusätzliche Daten, die über Assettaginformationen hinausgehen und zum Identifizieren eines physischen Elements verwendet werden können. Ein Beispiel sind Balkencodedaten, die einem Element zugeordnet sind, das ebenfalls über ein Assettag verfügt. Beachten Sie, dass diese Eigenschaft NULL und die Barcodedaten als Klassenschlüssel in der **Tag-Eigenschaft** verwendet werden, wenn nur Balkencodedaten verfügbar sind und eindeutig sind und als Elementschlüssel verwendet werden können.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement geerbt.**](cim-physicalelement.md)

</dd> <dt>

**PartNumber**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Teilenummer, die von der Organisation zugewiesen wird, die für die Produktion oder Herstellung des physischen Elements verantwortlich ist.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**PoweredOn**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True gibt an, dass das physische Element eingeschaltet ist. Andernfalls ist sie derzeit deaktiviert.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**Abnehmbare**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True gibt an, dass das Paket so konzipiert ist, dass es in den physischen Container, in dem es normalerweise gefunden wird, ein- und aus dem Paket aufgenommen wird, ohne die Funktion der gesamten Paketierung zu beeinträchtigen. Ein Paket gilt auch dann als wechselbar, wenn die Stromversorgung ausgeschaltet sein muss, um die Entfernung durchzuführen. Wenn die Stromversorgung eingeschaltet und das Paket entfernt werden kann, ist das Element wechselbar und kann im laufenden Betrieb ausgetauscht werden. Beispielsweise kann ein aktualisierbarer Prozessorchip entfernt werden.

Diese Eigenschaft wird von [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)geerbt.

</dd> <dt>

**Austauschbare**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True gibt an, dass das Element durch ein physisch anderes ersetzt werden kann. Einige Computersysteme ermöglichen beispielsweise das Upgrade des Hauptprozessorchips auf eine höhere Uhrbewertung. In diesem Fall wird der Prozessor als ersetzbar bezeichnet. Alle Wechselkomponenten sind grundsätzlich austauschbar.

Diese Eigenschaft wird von [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)geerbt.

</dd> <dt>

**RequirementsDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ CIM-Karte**.**SpecialRequirements**")
</dt> </dl>

Freiformzeichenfolge, die beschreibt, wie die Karte physisch von anderen Karten eindeutig ist. Diese Eigenschaft hat nur dann eine Bedeutung, wenn die entsprechende boolesche Eigenschaft **SpecialRequirements** auf **TRUE** festgelegt ist.

</dd> <dt>

**RequiresDaughterBoard**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True gibt an, dass mindestens ein Brett oder eine Hilfskarte erforderlich ist, um ordnungsgemäß zu funktionieren.

</dd> <dt>

**Serialnumber**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Vom Hersteller zugeordnete Nummer, die zum Identifizieren des physischen Elements verwendet wird.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**SKU**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Lagerhaltungseinheitennummer für dieses physische Element.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**SlotLayout**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Freiformzeichenfolge, die die Slotpositionierung, typische Nutzung, Einschränkungen, einzelne Slotabstande oder andere relevante Informationen für die Slots auf einer Karte beschreibt.

</dd> <dt>

**SpecialRequirements**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ CIM-Karte**.**RequirementsDescription**")
</dt> </dl>

True gibt an, dass die Karte physisch von anderen Karten desselben Typs eindeutig ist und daher einen speziellen Slot erfordert. Beispielsweise erfordert eine karte mit doppelter Breite zwei Slots. Ein weiteres Beispiel ist, wenn eine bestimmte Karte für dieselbe allgemeine Funktion wie andere Karten verwendet werden kann, aber einen speziellen Slot erfordert (z. B. eine zusätzliche Länge). während andere Karten in einem beliebigen verfügbaren Slot platziert werden können. True gibt an, dass die entsprechende **RequirementsDescription-Eigenschaft** die Art der Eindeutigkeit oder des Zwecks der Karte angeben soll.

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

**Tag**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**\_ CIM-Schlüssel,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identifiziert das physische Element eindeutig und dient als Schlüssel des Elements. Diese Eigenschaft kann Informationen enthalten, z. B. Assettag- oder Seriennummerndaten. Der Schlüssel für [**CIM \_ PhysicalElement**](cim-physicalelement.md) wird sehr hoch in der Objekthierarchie platziert, um die Hardware oder Entität unabhängig von der physischen Platzierung in Schränken, Adaptern usw. zu identifizieren. Beispielsweise kann eine Wechselkomponente, die im laufenden Betrieb ausgetauscht werden kann, aus dem enthaltenden Paket (Bereichspaket) entnommen und vorübergehend nicht verwendet werden. Das Objekt ist weiterhin vorhanden und kann sogar in einen anderen Bereichscontainer eingefügt werden. Der Schlüssel für ein physisches Element ist eine beliebige Zeichenfolge, die unabhängig von der Platzierung oder der standortorientierten Hierarchie definiert ist.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Gibt die Version des physischen Elements an.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

Datentyp: **real32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Kilos")
</dt> </dl>

Gewichtung des physischen Pakets in Kilos.

Diese Eigenschaft wird von [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)geerbt.

</dd> <dt>

**Width**
</dt> <dd> <dl> <dt>

Datentyp: **real32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zoll")
</dt> </dl>

Breite des physischen Pakets in Zoll.

Diese Eigenschaft wird von [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **CIM \_ Card-Klasse** wird von [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)abgeleitet.

WMI implementiert diese Klasse nicht. Weitere Informationen zu Klassen, die von **\_ CIM-Karten** abgeleitet wurden, finden Sie unter [Win32-Klassen.](win32-provider.md)

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

[**CIM \_ PhysicalPackage**](cim-physicalpackage.md)
</dt> </dl>

 

