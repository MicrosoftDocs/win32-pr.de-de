---
description: Stellt die Eigenschaften dar, die einem physischen Systemgehäuse zugeordnet sind.
ms.assetid: a8244dc0-a95e-4940-9b92-7820bdf14916
ms.tgt_platform: multiple
title: Win32_SystemEnclosure-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemEnclosure
- Win32_SystemEnclosure.IsCompatible
- Win32_SystemEnclosure.AudibleAlarm
- Win32_SystemEnclosure.BreachDescription
- Win32_SystemEnclosure.CableManagementStrategy
- Win32_SystemEnclosure.Caption
- Win32_SystemEnclosure.ChassisTypes
- Win32_SystemEnclosure.CreationClassName
- Win32_SystemEnclosure.CurrentRequiredOrProduced
- Win32_SystemEnclosure.Depth
- Win32_SystemEnclosure.Description
- Win32_SystemEnclosure.HeatGeneration
- Win32_SystemEnclosure.Height
- Win32_SystemEnclosure.HotSwappable
- Win32_SystemEnclosure.InstallDate
- Win32_SystemEnclosure.LockPresent
- Win32_SystemEnclosure.Manufacturer
- Win32_SystemEnclosure.Model
- Win32_SystemEnclosure.Name
- Win32_SystemEnclosure.NumberOfPowerCords
- Win32_SystemEnclosure.OtherIdentifyingInfo
- Win32_SystemEnclosure.PartNumber
- Win32_SystemEnclosure.PoweredOn
- Win32_SystemEnclosure.Removable
- Win32_SystemEnclosure.Replaceable
- Win32_SystemEnclosure.SecurityBreach
- Win32_SystemEnclosure.SecurityStatus
- Win32_SystemEnclosure.SerialNumber
- Win32_SystemEnclosure.ServiceDescriptions
- Win32_SystemEnclosure.ServicePhilosophy
- Win32_SystemEnclosure.SKU
- Win32_SystemEnclosure.SMBIOSAssetTag
- Win32_SystemEnclosure.Status
- Win32_SystemEnclosure.Tag
- Win32_SystemEnclosure.TypeDescriptions
- Win32_SystemEnclosure.Version
- Win32_SystemEnclosure.VisibleAlarm
- Win32_SystemEnclosure.Weight
- Win32_SystemEnclosure.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c7f3b65f6435d8ff828aebf5310f9b21a2ea7f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958574"
---
# <a name="win32_systemenclosure-class"></a>Win32 \_ systemenclosure-Klasse

Die **Win32 \_ systemenclosure** - [WMI-Klasse](../wmisdk/retrieving-a-class.md) stellt die Eigenschaften dar, die einem physischen Systemgehäuse zugeordnet sind.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B94-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_SystemEnclosure : CIM_Chassis
{
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  string   Caption;
  uint16   ChassisTypes[];
  string   CreationClassName;
  sint16   CurrentRequiredOrProduced;
  real32   Depth;
  string   Description;
  uint16   HeatGeneration;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  boolean  LockPresent;
  string   Manufacturer;
  string   Model;
  string   Name;
  uint16   NumberOfPowerCords;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  uint16   SecurityBreach;
  uint16   SecurityStatus;
  string   SerialNumber;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  string   SKU;
  string   SMBIOSAssetTag;
  string   Status;
  string   Tag;
  string   TypeDescriptions[];
  string   Version;
  boolean  VisibleAlarm;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a>Member

Die **Win32- \_ systemenclosure** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32- \_ systemenclosure** -Klasse verfügt über diese Methoden.



| Methode           | BESCHREIBUNG                 |
|:-----------------|:----------------------------|
| **Iskompatibel** | Nicht implementiert.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **Win32- \_ systemenclosure** -Klasse verfügt über diese Eigenschaften.

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

Qualifizierer: [**modelkorrespondenz**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ physicalframe**](cim-physicalframe.md).**Securityverletzungs**")
</dt> </dl>

Eine frei Form Zeichenfolge, die weitere Informationen bereitstellt, wenn die **securityverletzungs** -Eigenschaft angibt, dass ein Sicherheits bezogenes Ereignis aufgetreten ist.

Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.

</dd> <dt>

**CableManagementStrategy**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine frei Form Zeichenfolge, die Informationen darüber enthält, wie die verschiedenen Kabel mit dem Frame verbunden und gebündelt werden. Dank vieler Netzwerk-, Speicher-und Netzkabel kann die Kabel Verwaltung ein komplexes und anspruchsvolles Unterfangen sein. Diese Eigenschaft enthält Informationen, um die Assembly und den Dienst des Frames zu unterstützen.

Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Kurze Beschreibung des Objekts – eine einzeilige Zeichenfolge.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**ChassisTypes**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indiziert"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". Physischer DMTF- \| Container globale Tabelle \| 002,1 "), [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ Chassis**](cim-chassis.md)".**Typebeschreibungen**")
</dt> </dl>

Array von Chassistypen.

Dieser Wert stammt vom **Typmember** des **System Gehäuses oder der Gehäuse** Struktur in den SMBIOS-Informationen.

Diese Eigenschaft wird vom [**CIM- \_ Chassis**](cim-chassis.md)geerbt.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

**Desktop** (3)


</dt> <dd></dd> <dt>

<span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>

**Desktop mit niedrigem Profil** (4)


</dt> <dd></dd> <dt>

<span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>

**Pizza Box** (5)


</dt> <dd></dd> <dt>

<span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>

**Mini Turm** (6)


</dt> <dd></dd> <dt>

<span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>

**Turm** (7)


</dt> <dd></dd> <dt>

<span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>

**Portabel** (8)


</dt> <dd></dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

**Laptop** (9)


</dt> <dd></dd> <dt>

<span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>

**Notebook** (10)


</dt> <dd></dd> <dt>

<span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>

**Hand gehalten** (11)


</dt> <dd></dd> <dt>

<span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>

**Docking Station** (12)


</dt> <dd></dd> <dt>

<span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>

**Alle in eins** (13)


</dt> <dd></dd> <dt>

<span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>

**Sub Notebook** (14)


</dt> <dd></dd> <dt>

<span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>

**Speicherplatz** (15)


</dt> <dd></dd> <dt>

<span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>

**Mittags Feld** (16)


</dt> <dd></dd> <dt>

<span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>

**Haupt Betriebssystem-Chassis** (17)


</dt> <dd></dd> <dt>

<span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>

**Erweiterungs Chassis** (18)


</dt> <dd></dd> <dt>

<span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>

**Subchassis** (19)


</dt> <dd></dd> <dt>

<span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>

**Buserweiterungs Chassis** (20)


</dt> <dd></dd> <dt>

<span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>

**Peripherie Chassis** (21)


</dt> <dd></dd> <dt>

<span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>

**Speicherchassis** (22)


</dt> <dd></dd> <dt>

<span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>

**Rack Mount Chassis** (23)


</dt> <dd></dd> <dt>

<span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>

**Sealed-Case-PC** (24)

</dt> <dd></dd> <dt>

<span id="Tablet"></span><span id="tablet"></span><span id="TABLET"></span>

**Tablet** (30)

</dt> <dd></dd> <dt>

<span id="Convertible"></span><span id="Convertible"></span><span id="Convertible"></span>

**Konvertierbar** (31)

</dt> <dd></dd> <dt>

<span id="Detachable"></span><span id="Detachable "></span><span id="Detachable "></span>

**Ablösbar (32** )


</dt> <dd></dd> </dl>

</dd> <dt>

**"Name der Klassenname"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt wird, die bei der Erstellung einer Instanz verwendet wird. Wenn diese Eigenschaft mit den anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**Currentrequirements dorerzeugte**
</dt> <dd> <dl> <dt>

Datentyp: **sint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Amps bei 120 Volt")
</dt> </dl>

Aktuell, der vom Chassis bei 120V benötigt wird. Wenn die Stromversorgung vom Chassis bereitgestellt wird – wie bei einer unterbrechungsfreien Stromversorgung (USV) – kann diese Eigenschaft auf die erzeugte AMPERAGE (als negative Zahl) hindeuten.

Diese Eigenschaft wird vom [**CIM- \_ Chassis**](cim-chassis.md)geerbt.

</dd> <dt>

**Tiefe**
</dt> <dd> <dl> <dt>

Datentyp: **real32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Zoll")
</dt> </dl>

Tiefe des physischen Pakets – in Zoll.

Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Eine Beschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Heatgene Ration**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("BTU pro Stunde")
</dt> </dl>

Menge der Wärme, die vom Gehäuse in BTU/Stunde generiert wird.

Diese Eigenschaft wird vom [**CIM- \_ Chassis**](cim-chassis.md)geerbt.

</dd> <dt>

**Height**
</dt> <dd> <dl> <dt>

Datentyp: **real32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Zoll")
</dt> </dl>

Höhe des physischen Pakets – in Zoll.

Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.

</dd> <dt>

**"Anappable"**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass ein physisches Paket im laufenden Betrieb ausgetauscht werden kann (wenn es möglich ist, das Element durch einen physisch abweichenden, aber entsprechenden Wert zu ersetzen, während für das enthaltene Paket eine Stromversorgung angewendet wurde). Beispielsweise ist ein Laufwerks Paket, das mithilfe von SCA-Connectors eingefügt wird, wechselseitig austauschbar. Alle Pakete, die sich im laufenden Betrieb austauschen lassen, sind von Natur aus austauschbar und austauschbar.

Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")
</dt> </dl>

Datum und Uhrzeit der Installation des-Objekts. Diese Eigenschaft erfordert keinen Wert, um anzugeben, dass das-Objekt installiert ist.

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

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Der Name der Organisation, die das physische Element erzeugt.

Dieser Wert stammt aus dem **Hersteller** Mitglied des **System Gehäuses oder der Gehäuse** Struktur in den SMBIOS-Informationen.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**Modell**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Der Name, mit dem das physische Element bekannt ist.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Die Bezeichnung, nach der das-Objekt bekannt ist. Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Anzahl von powercords**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der Netzkabel, die mit dem Chassis verbunden werden müssen, damit alle Komponenten funktionieren.

Diese Eigenschaft wird vom [**CIM- \_ Chassis**](cim-chassis.md)geerbt.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zusätzliche Daten, über die Informationen zu Asset-Tags hinausgehen, die zum Identifizieren eines physischen Elements verwendet werden können. Ein Beispiel hierfür sind Barcode-Daten, die einem Element zugeordnet sind, das auch über ein Bestands Kennzeichen verfügt. Beachten Sie Folgendes: Wenn nur Barcode Daten verfügbar sind und eindeutig sind oder als Element Schlüssel verwendet werden können, ist diese Eigenschaft **null** und die Barcode-Daten, die als Klassen Schlüssel verwendet werden, in der Tag-Eigenschaft.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**PartNumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Teilenummer, die von der Organisation zugewiesen wird, die das physische Element erzeugt oder herstellt.

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

**True** gibt an, dass ein physisches Paket entfernt werden kann (wenn es so konzipiert ist, dass es in den physischen Container übernommen wird, in dem es normalerweise gefunden wird, ohne dass die Funktion der gesamten Paket Erstellung beeinträchtigt wird). Ein Paket kann weiterhin entfernt werden, wenn die Stromversorgung "Off" sein muss, um das Entfernen auszuführen. Wenn das Paket entfernt werden kann, während die Stromversorgung aktiviert ist, kann das Element entfernt werden, und das Element kann im laufenden Betrieb ausgetauscht werden. Beispielsweise ist ein zusätzlicher Akku in einem Laptop Wechsel Datenträger, ebenso wie ein Laufwerks Paket, das mithilfe von SCA-Connectors (Server Configuration Application) eingefügt wird. Der letztere kann jedoch im laufenden Betrieb ausgetauscht werden. Eine Laptop Anzeige kann nicht entfernt werden, und es handelt sich nicht um eine nicht redundante Netzteil. Das Entfernen dieser Komponenten wirkt sich auf die Funktion der Gesamt Verpackung aus oder ist aufgrund der engen Integration des Pakets nicht möglich.

Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.

</dd> <dt>

**Replaceable**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass diese physische Medien Komponente durch eine physisch andere ersetzt werden kann. Beispielsweise ist für einige Computersysteme das Upgrade des Hauptprozessor-Chips auf eine höhere Bewertungsstufe möglich. In diesem Fall wird der Prozessor als ersetzbar bezeichnet. Ein weiteres Beispiel ist ein Stromversorgung-Paket, das auf gleitenden Schienen eingebunden ist. Alle Wechsel Pakete sind von Natur aus austauschbar.

Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.

</dd> <dt>

**Security-Verletzung**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". Physischer DMTF- \| Container Global Table \| 002,12 "), [**modelkorrespondenz**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ physicalframe**](cim-physicalframe.md).**BreachDescription**")
</dt> </dl>

Status einer physischen Verletzung des Frames.

Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.

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

**SecurityStatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS- \| Typ 3 \| Sicherheits Status")
</dt> </dl>

Sicherheitseinstellungen für externe Eingaben, z. b. eine Tastatur, auf einen Computer.

Dieser Wert stammt aus dem **Sicherheits Status** Mitglied des **System Gehäuses oder der Gehäuse** Struktur in den SMBIOS-Informationen.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Keine** (3)


</dt> <dd></dd> <dt>

<span id="External_interface_locked_out"></span><span id="external_interface_locked_out"></span><span id="EXTERNAL_INTERFACE_LOCKED_OUT"></span>

**Externe Schnittstelle gesperrt** (4)


</dt> <dd></dd> <dt>

<span id="External_interface_enabled"></span><span id="external_interface_enabled"></span><span id="EXTERNAL_INTERFACE_ENABLED"></span>

**Externe Schnittstelle aktiviert** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Vom Hersteller zugewiesene Nummer, mit der das physische Element identifiziert wird.

Dieser Wert stammt aus dem **Seriennummern** Element des **System Gehäuses oder der Gehäuse** Struktur in den SMBIOS-Informationen.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**Service Beschreibungen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indiziert"), [**modelkorrespondenz**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ physicalframe**](cim-physicalframe.md).**ServicePhilosophy**")
</dt> </dl>

Array Ausführlichere Erläuterungen zu den Einträgen im **ServicePhilosophy** -Array. Beachten Sie, dass jeder Eintrag dieses Arrays mit dem Eintrag in **ServicePhilosophy** verknüpft ist, der sich im gleichen Index befindet.

Diese Eigenschaft wird von [**CIM \_ physicalframe**](cim-physicalframe.md)geerbt.

</dd> <dt>

**ServicePhilosophy**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indiziert"), [**modelkorrespondenz**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ physicalframe**](cim-physicalframe.md).**Service Beschreibungen**")
</dt> </dl>

Ein Array, das einschließt, ob der Frame vom oberen, dem Vorder-oder Seitenrand bedient wird, ob der Frame gleitende tablettfächer oder Wechsel Seiten aufweist und ob der Frame beweglich ist – z. b. mithilfe von Walzen.

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

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Die Stock Keeping Unit-Nummer für das physische Element.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

</dd> <dt>

**SMBIOSAssetTag**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 3 \| Asset Tag")
</dt> </dl>

Assettagnummer des System Gehäuses.

Dieser Wert stammt aus dem **Asset-tagnummern** Element des **System Gehäuses oder der Gehäuse** Struktur in den SMBIOS-Informationen.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Aktueller Status des Objekts. Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden. Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen). Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service". Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden. Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

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

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Eindeutiger Bezeichner des System Gehäuses.

Diese Eigenschaft wird von [**CIM \_ PhysicalElement**](cim-physicalelement.md)geerbt.

Beispiel: "System Gehäuse 1"

</dd> <dt>

**Typebeschreibungen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indiziert"), [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ Chassis**](cim-chassis.md).**ChassisTypes**")
</dt> </dl>

Array mit weiteren Informationen über die **ChassisTypes** -Array Einträge. Beachten Sie, dass jeder Eintrag dieses Arrays mit dem Eintrag in **ChassisTypes** verknüpft ist, der sich im gleichen Index befindet.

Diese Eigenschaft wird vom [**CIM- \_ Chassis**](cim-chassis.md)geerbt.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Version des physischen Elements.

Dieser Wert stammt aus dem  Versionsmember des **System Gehäuses oder der Gehäuse** Struktur in den SMBIOS-Informationen.

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

Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Pfund")
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

Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Zoll")
</dt> </dl>

Breite des physischen Pakets in Zoll.

Diese Eigenschaft wird von [**CIM \_ physicalpackage**](cim-physicalpackage.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32- \_ systemenclosure** -Klasse wird vom [**CIM- \_ Chassis**](cim-chassis.md)abgeleitet.

## <a name="examples"></a>Beispiele

Das PowerShell-Beispiel für [Multithreaded-System Ressourcen mit PowerShell](https://Gallery.TechNet.Microsoft.Com/Multithreaded-System-Asset-856a8f7c) in der TechNet Gallery verwendet eine Reihe von Klassen, einschließlich **Win32- \_ systemenclosure**, um Daten von einem System abzurufen.

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

[**CIM- \_ Chassis**](cim-chassis.md)
</dt> <dt>

[Computer System-Hardware Klassen](computer-system-hardware-classes.md)
</dt> <dt>

[WMI-Tasks: Computer Hardware](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> </dl>

 

 
