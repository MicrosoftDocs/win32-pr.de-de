---
description: Stellt die Funktionen der Low-Level-Software dar, die zum Starten und Konfigurieren eines Computersystems verwendet wird.
ms.assetid: 54d03539-d908-4571-b8fd-934b972e8d84
ms.tgt_platform: multiple
title: CIM_BIOSFeature-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSFeature
- CIM_BIOSFeature.Caption
- CIM_BIOSFeature.Description
- CIM_BIOSFeature.InstallDate
- CIM_BIOSFeature.Status
- CIM_BIOSFeature.IdentifyingNumber
- CIM_BIOSFeature.ProductName
- CIM_BIOSFeature.Vendor
- CIM_BIOSFeature.Version
- CIM_BIOSFeature.Name
- CIM_BIOSFeature.CharacteristicDescriptions
- CIM_BIOSFeature.Characteristics
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8fb99bffde80e16d5e37764ecbb49581cacc117f554abfec5603e9b3a3e76ec9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119218590"
---
# <a name="cim_biosfeature-class"></a>CIM \_ BIOSFeature-Klasse

Die **CIM \_ BIOSFeature-Klasse** stellt die Funktionen der Low-Level-Software dar, die zum Starten und Konfigurieren eines Computersystems verwendet wird.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[UUID("{7D33100E-E3D3-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_BIOSFeature : CIM_SoftwareFeature
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   IdentifyingNumber;
  string   ProductName;
  string   Vendor;
  string   Version;
  string   Name;
  string   CharacteristicDescriptions[];
  uint16   Characteristics[];
};
```

## <a name="members"></a>Member

Die **CIM \_ BIOSFeature-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ BIOSFeature-Klasse** verfügt über diese Eigenschaften.

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

**CharacteristicDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indiziert"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| BIOS Characteristic \| 003.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ BIOSFeature**.**Merkmale**")
</dt> </dl>

Array von Freiformzeichenfolgen, das ausführliche Erläuterungen zu den BIOS-Features bereitstellt, die im **Array Characteristics** angegeben sind.

> [!Note]  
> Jeder Eintrag in diesem Array bezieht sich auf den Eintrag im **Characteristics-Array,** das sich am gleichen Index befindet.

 

</dd> <dt>

**Characteristics**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indiziert"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| BIOS Characteristic \| 003.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ BIOSFeature**.**CharacteristicDescriptions**")
</dt> </dl>

Array von ganzen Zahlen, das die vom BIOS unterstützten Features angibt. Der Wert 3 ist im CIM-Schema ungültig, da er darstellt, dass keine BIOS-Features in DMI unterstützt werden. In diesem Fall sollte dieses Objekt nicht instanziiert werden.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Andere** (1)


</dt> <dd>

Sonstiges

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)


</dt> <dd>

Unbekannt

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Nicht definiert** (3)


</dt> <dd>

Nicht definiert.

</dd> <dt>

<span id="ISA_Support"></span><span id="isa_support"></span><span id="ISA_SUPPORT"></span>

<span id="ISA_Support"></span><span id="isa_support"></span><span id="ISA_SUPPORT"></span>**ISA-Unterstützung** (4)


</dt> <dd>

ISA-Unterstützung.

</dd> <dt>

<span id="MCA_Support"></span><span id="mca_support"></span><span id="MCA_SUPPORT"></span>

<span id="MCA_Support"></span><span id="mca_support"></span><span id="MCA_SUPPORT"></span>**MCA-Unterstützung** (5)


</dt> <dd>

MCA-Unterstützung.

</dd> <dt>

<span id="EISA_Support"></span><span id="eisa_support"></span><span id="EISA_SUPPORT"></span>

<span id="EISA_Support"></span><span id="eisa_support"></span><span id="EISA_SUPPORT"></span>**EISA-Unterstützung** (6)


</dt> <dd>

EISA-Unterstützung.

</dd> <dt>

<span id="PCI_Support"></span><span id="pci_support"></span><span id="PCI_SUPPORT"></span>

<span id="PCI_Support"></span><span id="pci_support"></span><span id="PCI_SUPPORT"></span>**PCI-Unterstützung** (7)


</dt> <dd>

PCI-Unterstützung.

</dd> <dt>

<span id="PCMCIA_Support"></span><span id="pcmcia_support"></span><span id="PCMCIA_SUPPORT"></span>

<span id="PCMCIA_Support"></span><span id="pcmcia_support"></span><span id="PCMCIA_SUPPORT"></span>**PCMCIA-Unterstützung** (8)


</dt> <dd>

PCMCIA-Unterstützung.

</dd> <dt>

<span id="PnP_Support"></span><span id="pnp_support"></span><span id="PNP_SUPPORT"></span>

<span id="PnP_Support"></span><span id="pnp_support"></span><span id="PNP_SUPPORT"></span>**PnP-Unterstützung** (9)


</dt> <dd>

PnP-Unterstützung.

</dd> <dt>

<span id="APM_Support"></span><span id="apm_support"></span><span id="APM_SUPPORT"></span>

<span id="APM_Support"></span><span id="apm_support"></span><span id="APM_SUPPORT"></span>**APM-Unterstützung** (10)


</dt> <dd>

APM-Unterstützung.

</dd> <dt>

<span id="Upgradeable_BIOS"></span><span id="upgradeable_bios"></span><span id="UPGRADEABLE_BIOS"></span>

<span id="Upgradeable_BIOS"></span><span id="upgradeable_bios"></span><span id="UPGRADEABLE_BIOS"></span>**Upgradefähiges BIOS** (11)


</dt> <dd>

Upgradefähiges BIOS.

</dd> <dt>

<span id="BIOS_Shadowing_Allowed"></span><span id="bios_shadowing_allowed"></span><span id="BIOS_SHADOWING_ALLOWED"></span>

<span id="BIOS_Shadowing_Allowed"></span><span id="bios_shadowing_allowed"></span><span id="BIOS_SHADOWING_ALLOWED"></span>**BIOS Shadowing zulässig** (12)


</dt> <dd>

BIOS-Shadowing zulässig.

</dd> <dt>

<span id="VL_VESA_Support"></span><span id="vl_vesa_support"></span><span id="VL_VESA_SUPPORT"></span>

<span id="VL_VESA_Support"></span><span id="vl_vesa_support"></span><span id="VL_VESA_SUPPORT"></span>**VL VESA-Unterstützung** (13)


</dt> <dd>

VL VESA-Unterstützung.

</dd> <dt>

<span id="ESCD_Support"></span><span id="escd_support"></span><span id="ESCD_SUPPORT"></span>

<span id="ESCD_Support"></span><span id="escd_support"></span><span id="ESCD_SUPPORT"></span>**ESCD-Unterstützung** (14)


</dt> <dd>

ESCD-Unterstützung.

</dd> <dt>

<span id="LS-120_Support"></span><span id="ls-120_support"></span><span id="LS-120_SUPPORT"></span>

<span id="LS-120_Support"></span><span id="ls-120_support"></span><span id="LS-120_SUPPORT"></span>**LS-120-Unterstützung** (15)


</dt> <dd>

LS-120-Unterstützung.

</dd> <dt>

<span id="ACPI_Support"></span><span id="acpi_support"></span><span id="ACPI_SUPPORT"></span>

<span id="ACPI_Support"></span><span id="acpi_support"></span><span id="ACPI_SUPPORT"></span>**ACPI-Unterstützung** (16)


</dt> <dd>

ACPI-Unterstützung.

</dd> <dt>

<span id="I2O_Boot_Support"></span><span id="i2o_boot_support"></span><span id="I2O_BOOT_SUPPORT"></span>

<span id="I2O_Boot_Support"></span><span id="i2o_boot_support"></span><span id="I2O_BOOT_SUPPORT"></span>**I2O-Startunterstützung** (17)


</dt> <dd>

I2O-Startunterstützung.

</dd> <dt>

<span id="USB_Legacy_Support"></span><span id="usb_legacy_support"></span><span id="USB_LEGACY_SUPPORT"></span>

<span id="USB_Legacy_Support"></span><span id="usb_legacy_support"></span><span id="USB_LEGACY_SUPPORT"></span>**USB Legacy-Unterstützung** (18)


</dt> <dd>

USB-Legacyunterstützung.

</dd> <dt>

<span id="AGP_Support"></span><span id="agp_support"></span><span id="AGP_SUPPORT"></span>

<span id="AGP_Support"></span><span id="agp_support"></span><span id="AGP_SUPPORT"></span>**AGP-Unterstützung** (19)


</dt> <dd>

AGP-Unterstützung.

</dd> <dt>

<span id="PC_Card"></span><span id="pc_card"></span><span id="PC_CARD"></span>

<span id="PC_Card"></span><span id="pc_card"></span><span id="PC_CARD"></span>**PC-Karte** (20)


</dt> <dd>

PC-Karte.

</dd> <dt>

<span id="IR"></span><span id="ir"></span>

<span id="IR"></span><span id="ir"></span>**IR** (21)


</dt> <dd>

Ir.

</dd> <dt>

<span id="1394"></span>

<span id="1394"></span>**1394** (22)


</dt> <dd>

1394.

</dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span id="I2C"></span><span id="i2c"></span>**I2C** (23)


</dt> <dd>

I2c.

</dd> <dt>

<span id="Smart_Battery"></span><span id="smart_battery"></span><span id="SMART_BATTERY"></span>

<span id="Smart_Battery"></span><span id="smart_battery"></span><span id="SMART_BATTERY"></span>**Intelligenter Akku** (24)


</dt> <dd>

Intelligenter Akku.

</dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)


</dt> <dd>

PC-98.

</dd> </dl>

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

**IdentifyingNumber**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Weitergegeben**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ CIM-Produkt**](cim-product.md).**IdentifyingNumber**), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF \| ComponentID \| 001.4")
</dt> </dl>

Produktidentifikation, z. B. eine Seriennummer auf Software oder eine Würznummer auf einem Hardwarechip.

Diese Eigenschaft wird von [**CIM \_ SoftwareFeature**](cim-softwarefeature.md)geerbt.

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

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Die Name-Eigenschaft definiert die Bezeichnung, mit der das Objekt der Welt außerhalb des Datenverarbeitungssystems bekannt ist. Diese Bezeichnung ist ein lesbarer Name, der das Element im Kontext des Namespace des Elements eindeutig identifiziert.

Diese Eigenschaft wird von [**CIM \_ SoftwareFeature**](cim-softwarefeature.md)geerbt.

</dd> <dt>

**ProductName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Weitergegeben**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ CIM-Produkt**](cim-product.md).**Name**), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF \| ComponentID \| 001.2")
</dt> </dl>

Häufig verwendeter Produktname.

Diese Eigenschaft wird von [**CIM \_ SoftwareFeature**](cim-softwarefeature.md)geerbt.

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

**Hersteller**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Weitergegeben**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ CIM-Produkt**](cim-product.md).**Vendor**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF \| ComponentID \| 001.1")
</dt> </dl>

Name des Lieferanten des Produkts, der der **Vendor-Eigenschaft** im Produktobjekt der DMTF-Lösung Exchange Standard entspricht.

Diese Eigenschaft wird von [**CIM \_ SoftwareFeature**](cim-softwarefeature.md)geerbt.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Weitergegeben**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ CIM-Produkt**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF \| ComponentID \| 001.3")
</dt> </dl>

Produktversionsinformationen, die der **Version-Eigenschaft** im Produktobjekt der DMTF-Projektmappe Exchange Standard entsprechen.

Diese Eigenschaft wird von [**CIM \_ SoftwareFeature**](cim-softwarefeature.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **CIM \_ BIOSFeature-Klasse** wird von [**CIM \_ SoftwareFeature**](cim-softwarefeature.md)abgeleitet.

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

[**CIM \_ SoftwareFeature**](cim-softwarefeature.md)
</dt> </dl>

 

