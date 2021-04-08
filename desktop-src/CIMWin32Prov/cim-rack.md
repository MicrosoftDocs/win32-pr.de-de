---
description: Die CIM- \_ Rack-Klasse stellt ein Gestell (ein physischer Frame oder Gehäuse) dar, in dem das Chassis gespeichert wird. In der Regel stellt ein Rack das Gehäuse dar. Alle funktionierenden Komponenten werden in das Chassis gepackt.
ms.assetid: 1e0273ce-2a09-4f75-a82e-d0555d6a831e
ms.tgt_platform: multiple
title: CIM_Rack-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Rack
- CIM_Rack.AudibleAlarm
- CIM_Rack.BreachDescription
- CIM_Rack.CableManagementStrategy
- CIM_Rack.Caption
- CIM_Rack.CountryDesignation
- CIM_Rack.CreationClassName
- CIM_Rack.Depth
- CIM_Rack.Description
- CIM_Rack.Height
- CIM_Rack.HotSwappable
- CIM_Rack.InstallDate
- CIM_Rack.LockPresent
- CIM_Rack.Manufacturer
- CIM_Rack.Model
- CIM_Rack.Name
- CIM_Rack.OtherIdentifyingInfo
- CIM_Rack.PartNumber
- CIM_Rack.PoweredOn
- CIM_Rack.Removable
- CIM_Rack.Replaceable
- CIM_Rack.SecurityBreach
- CIM_Rack.SerialNumber
- CIM_Rack.ServiceDescriptions
- CIM_Rack.ServicePhilosophy
- CIM_Rack.SKU
- CIM_Rack.Status
- CIM_Rack.Tag
- CIM_Rack.TypeOfRack
- CIM_Rack.Version
- CIM_Rack.VisibleAlarm
- CIM_Rack.Weight
- CIM_Rack.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2eb5234e8dd65d7df86acec7ab121ef961c2121
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748233"
---
# <a name="cim_rack-class"></a>CIM- \_ Rack-Klasse

Die **CIM- \_ Rack** -Klasse stellt ein Gestell (ein physischer Frame oder Gehäuse) dar, in dem das Chassis gespeichert wird. In der Regel stellt ein Rack das Gehäuse dar. Alle funktionierenden Komponenten werden in das Chassis gepackt.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{FAF76B71-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Rack : CIM_PhysicalFrame
{
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  string   Caption;
  string   CountryDesignation;
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  boolean  LockPresent;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  uint16   SecurityBreach;
  string   SerialNumber;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  string   SKU;
  string   Status;
  string   Tag;
  uint16   TypeOfRack;
  string   Version;
  boolean  VisibleAlarm;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a>Member

Die **CIM- \_ Rack** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **CIM- \_ Rack** -Klasse verfügt über diese Methoden.



| Methode                                                        | BESCHREIBUNG                                                                                                                                      |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iskompatibel**](iscompatible-method-in-class-cim-rack.md) | Überprüft, ob das physische-Element, auf das verwiesen wird, in das physische Paket eingefügt oder darin eingefügt werden kann. Wird nicht von WMI implementiert.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ Rack** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Audiblealarm**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass der Frame mit einem hörbaren Alarm ausgestattet ist.

Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.

</dd> <dt>

**BreachDescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ physicalframe**](cim-physicalframe.md).**Securityverletzungs**")
</dt> </dl>

Eine frei Form Zeichenfolge, die Informationen bereitstellt, wenn die **securityverletzungs** -Eigenschaft angibt, dass eine Sicherheitsverletzung oder ein anderes Sicherheits bezogenes Ereignis aufgetreten ist.

Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.

</dd> <dt>

**CableManagementStrategy**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine frei Form Zeichenfolge, die Informationen darüber enthält, wie die verschiedenen Kabel mit dem Frame verbunden und gebündelt werden. Dank vieler Netzwerk-, Speicher-und Netzkabel kann die Kabel Verwaltung ein komplexes und anspruchsvolles Unterfangen sein. Diese Zeichen folgen Eigenschaft enthält Informationen, um die Assembly und den Dienst des Frames zu unterstützen.

Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Kurze Textbeschreibung des-Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Countrybezeichnung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Rack**".**TypeOfRack**")
</dt> </dl>

Das Land oder die Region, für das das Gestell entworfen wurde. Code Zeichenfolgen für Länder oder Regionen sind gemäß ISO/IEC 3166 definiert. Der Rack-Typ wird in der **TypeOfRack** -Eigenschaft angegeben.

</dd> <dt>

**"Name der Klassenname"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird. Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**Tiefe**
</dt> <dd> <dl> <dt>

Datentyp: **real32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Zoll")
</dt> </dl>

Die Tiefe des physischen Pakets in Zoll.

Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Die Textbeschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Height**
</dt> <dd> <dl> <dt>

Datentyp: **real32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Height"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("US")
</dt> </dl>

Die Höhe des physischen Pakets mithilfe der Maßeinheit "U". Ein "U" ist eine Standard Maßeinheit für die Höhe eines Rasters oder einer Regal baren Komponente und ist gleich 1,75 Zoll oder 4,445 Zentimeter.

Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.

</dd> <dt>

**"Anappable"**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass das Paket im laufenden Betrieb ausgetauscht werden kann. Ein physisches Paket kann mit einem ausgetauschten Element ersetzt werden, wenn das Element durch ein physisch anderes (aber gleichwertiges) Element ersetzt werden kann, während das enthaltende Paket eingeschaltet ist. Beispielsweise kann eine Lüfter-Komponente so entworfen werden, dass Sie im laufenden Betrieb ausgetauscht wird. Alle Komponenten, bei denen es sich um eine ausgetauschte Komponente handelt, sind von Natur aus austauschbar und austauschbar.

Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")
</dt> </dl>

Datum und Uhrzeit der Installation des-Objekts. Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Sperre vorhanden**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass der Frame durch eine Sperre geschützt wird.

Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der Name der Organisation, die das physische Element erzeugt hat. Weitere Informationen finden Sie unter der **Hersteller** Eigenschaft des [**CIM- \_ Produkts**](cim-product.md).

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**Modell**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Der Name, mit dem das physische Element allgemein bekannt ist.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Die Bezeichnung, nach der das-Objekt bekannt ist. Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zusätzliche Daten, über die Informationen zu Asset-Tags hinausgehen, die zum Identifizieren eines physischen Elements verwendet werden könnten. Ein Beispiel hierfür sind Barcode-Daten, die einem Element zugeordnet sind, das auch über ein Bestands Kennzeichen verfügt. Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

> [!Note]  
> Wenn nur Barcode Daten verfügbar sind und eindeutig sind und als Element Schlüssel verwendet werden können, ist diese Eigenschaft NULL, und die Barcode Daten werden als Klassen Schlüssel in der **Tag** -Eigenschaft verwendet.

 

</dd> <dt>

**PartNumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Die Teilenummer, die von der Organisation zugewiesen wurde, die das physische Element erstellt oder hergestellt hat.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**Poweredon**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass das physische Element eingeschaltet ist.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**Ab**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass dieses Element in den physischen Container übernommen werden soll, in dem es normalerweise gefunden wird, ohne die Funktion der gesamten Paket Erstellung zu beeinträchtigen. Ein Paket gilt auch dann als austauschbar, wenn die Stromversorgung "Off" lauten muss, um das Entfernen auszuführen. Wenn die Stromversorgung "on" und das Paket entfernt werden kann, ist das-Element austauschbar und kann im laufenden Betrieb ausgetauscht werden. Beispielsweise ist ein zusätzlicher Akku in einem Laptop austauschbar, ebenso wie ein Laufwerk, das mithilfe von SCA-Connectors eingefügt wurde. der letztere kann jedoch im laufenden Betrieb ausgetauscht werden. Die Anzeige eines Laptops kann nicht entfernt werden, und es handelt sich nicht um eine nicht redundante Netzteil. Das Entfernen dieser Komponenten wirkt sich auf die Funktion der Gesamt Verpackung aus oder ist aufgrund der engen Integration des Pakets nicht möglich.

Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.

</dd> <dt>

**Replaceable**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wenn der Wert **true** ist, kann das-Element durch einen physisch anderen ersetzt werden. Beispielsweise ist für einige Computersysteme das Upgrade des Hauptprozessor-Chips auf eine höhere Bewertungsstufe möglich. In diesem Fall wird der Prozessor als ersetzbar bezeichnet. Alle wechselkomponenten sind von Natur aus ersetzbar.

Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.

</dd> <dt>

**Security-Verletzung**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Physischer DMTF- \| Container Global Table \| 002,12 "), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ physicalframe**](cim-physicalframe.md).**BreachDescription**")
</dt> </dl>

Gibt an, ob ein physischer Verstoß gegen den Frame versucht wurde, jedoch nicht erfolgreich war oder ob versucht wurde. Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

**Keine Verletzung** (3)


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

**Versuchte Sicherheitsverletzung** (4)


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

**Verletzung erfolgreich** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Vom Hersteller zugewiesene Nummer, die zum Identifizieren des Racks verwendet wird.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**Service Beschreibungen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ physicalframe**](cim-physicalframe.md).**ServicePhilosophy**")
</dt> </dl>

Freiform-Zeichen folgen, die ausführliche Erläuterungen zu Einträgen im **ServicePhilosophy** -Array bereitstellen. Beachten Sie, dass jeder Eintrag des Arrays mit dem Eintrag in **ServicePhilosophy** verknüpft ist, der sich im gleichen Index befindet.

Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.

</dd> <dt>

**ServicePhilosophy**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ physicalframe**](cim-physicalframe.md).**Service Beschreibungen**")
</dt> </dl>

Gibt an, ob der Frame vom oberen Rand, von der Vorderseite, von hinten oder von der Seite bedient wird. und ob Schiebe Fächer oder Wechsel Seiten vorhanden sind, und ob der Frame beweglich ist (z. b. über Walzen).

Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

**Dienst von oben** (2)


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

**Dienst von Front** (3)


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

**Dienst von hinten** (4)


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

**Dienst von Seite** (5)


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

**Gleitende Tabletts** (6)


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

Wechsel **Seiten** (7)


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

**Verschiebbare** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**SKU**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Die Stock Keeping Unit-Nummer für das physische Element.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Aktueller Status des Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

Folgende Werte sind gültig:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Fehler** ("Fehler")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

Herunter **gestuft ("** heruntergestuft")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** ("unbekannt")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred-** Fehler ("pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

Wird **gestartet** ("wird gestartet")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

Wird **beendet ("wird angehalten** ")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Dienst** ("Dienst")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Betont** ("gestresst")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Nicht wiederherstellen** ("nicht wiederherstellen")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Kein Kontakt** ("kein Kontakt")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Verlorene** Kommunikations ("verlorene Kommunikations-")


</dt> <dd></dd> </dl>

</dd> <dt>

**Tag**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Eine beliebige Zeichenfolge, die das physische Element eindeutig identifiziert und als Schlüssel des Elements fungiert. Diese Eigenschaft kann Informationen enthalten, z. b. Daten zu Bestands Kennzeichen oder Seriennummer. Der Schlüssel für [**CIM \_ PhysicalElement**](cim-physicalelement.md) wird in der Objekthierarchie sehr hoch platziert, um die Hardware oder Entität unabhängig von der physischen Platzierung in (oder in) Schränken, Adaptern usw. unabhängig voneinander zu identifizieren. Beispielsweise kann eine Wechsel Komponente, für die ein ausgetauschte Vorgang ausgeführt werden kann, aus dem enthaltenden (Bereichs bezogenen) Paket entnommen und vorübergehend nicht verwendet werden. Das Objekt bleibt weiterhin vorhanden und kann sogar in einen anderen Bereichs Container eingefügt werden. Der Schlüssel für ein physisches Element ist eine beliebige Zeichenfolge, die unabhängig von der Platzierung oder der Speicherort orientierten Hierarchie definiert wird.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**TypeOfRack**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Rack**".**Countrybezeichnung**")
</dt> </dl>

Der Typ des Racks.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Standard_19_Inch"></span><span id="standard_19_inch"></span><span id="STANDARD_19_INCH"></span>

<span id="Standard_19_Inch"></span><span id="standard_19_inch"></span><span id="STANDARD_19_INCH"></span>**Standard 19 Zoll** (1)


</dt> <dd>

Standard 19 Zoll

</dd> <dt>

<span id="Telco"></span><span id="telco"></span><span id="TELCO"></span>

<span id="Telco"></span><span id="telco"></span><span id="TELCO"></span>**Telco** (2)


</dt> <dd></dd> <dt>

<span id="Equipment_Shelf"></span><span id="equipment_shelf"></span><span id="EQUIPMENT_SHELF"></span>

<span id="Equipment_Shelf"></span><span id="equipment_shelf"></span><span id="EQUIPMENT_SHELF"></span>**Geräte Regal** (3)


</dt> <dd></dd> <dt>

<span id="Non-Standard"></span><span id="non-standard"></span><span id="NON-STANDARD"></span>

<span id="Non-Standard"></span><span id="non-standard"></span><span id="NON-STANDARD"></span>**Nicht Standard** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Version des physischen Elements.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**Visiblealarm**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass die Ausrüstung einen sichtbaren Alarm enthält.

Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

Datentyp: **real32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pfund")
</dt> </dl>

Gewichtung des physischen Pakets in Pfund.

Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.

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

Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **CIM- \_ Rack** -Klasse wird von [**CIM \_ physicalframe**](cim-physicalframe.md)abgeleitet.

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

[**CIM- \_ physicalframe**](cim-physicalframe.md)
</dt> </dl>

 

