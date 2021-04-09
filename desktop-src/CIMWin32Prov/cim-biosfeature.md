---
description: Stellt die Funktionen der Low-Level-Software dar, die zum Starten und Konfigurieren eines Computer Systems verwendet wird.
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
ms.openlocfilehash: 538dc9e4c18d976901519ae0e2d6f5249fd25c35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861416"
---
# <a name="cim_biosfeature-class"></a><span data-ttu-id="a1d05-103">CIM \_ biosfeature-Klasse</span><span class="sxs-lookup"><span data-stu-id="a1d05-103">CIM\_BIOSFeature class</span></span>

<span data-ttu-id="a1d05-104">Die **CIM \_ biosfeature** -Klasse stellt die Funktionen der Low-Level-Software dar, die zum Starten und Konfigurieren eines Computer Systems verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a1d05-104">The **CIM\_BIOSFeature** class represents the capabilities of the low-level software that is used to start and configure a computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a1d05-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a1d05-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a1d05-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a1d05-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a1d05-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="a1d05-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a1d05-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a1d05-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1d05-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1d05-109">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="a1d05-110">Member</span><span class="sxs-lookup"><span data-stu-id="a1d05-110">Members</span></span>

<span data-ttu-id="a1d05-111">Die **CIM \_ biosfeature** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a1d05-111">The **CIM\_BIOSFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="a1d05-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a1d05-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a1d05-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a1d05-113">Properties</span></span>

<span data-ttu-id="a1d05-114">Die **CIM \_ biosfeature** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a1d05-114">The **CIM\_BIOSFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a1d05-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a1d05-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1d05-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1d05-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1d05-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1d05-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1d05-118">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a1d05-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a1d05-119">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a1d05-119">A short textual description of the object.</span></span>

<span data-ttu-id="a1d05-120">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1d05-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1d05-121">**Charakteristicbeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="a1d05-121">**CharacteristicDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1d05-122">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="a1d05-122">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a1d05-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1d05-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1d05-124">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| BIOS-Merkmal \| 003,4 "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ biosfeature**.**Merkmale**")</span><span class="sxs-lookup"><span data-stu-id="a1d05-124">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|BIOS Characteristic\|003.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_BIOSFeature**.**Characteristics**")</span></span>
</dt> </dl>

<span data-ttu-id="a1d05-125">Array von Freiform-Zeichen folgen, das ausführliche Erläuterungen zu den BIOS-Funktionen bereitstellt, die im **Merkmal** Array angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="a1d05-125">Array of free-form strings that provides detailed explanations of the BIOS features indicated in the **Characteristics** array.</span></span>

> [!Note]  
> <span data-ttu-id="a1d05-126">Jeder Eintrag in diesem Array bezieht sich auf den Eintrag im Array **Merkmale** , der sich am selben Index befindet.</span><span class="sxs-lookup"><span data-stu-id="a1d05-126">Each entry in this array is related to the entry in the **Characteristics** array, which is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="a1d05-127">**Characteristics**</span><span class="sxs-lookup"><span data-stu-id="a1d05-127">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1d05-128">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="a1d05-128">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a1d05-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1d05-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1d05-130">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| BIOS-Merkmal \| 003,3 "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ biosfeature**.**Charakteristicbeschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="a1d05-130">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|BIOS Characteristic\|003.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_BIOSFeature**.**CharacteristicDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="a1d05-131">Ein Array von ganzen Zahlen, das die vom BIOS unterstützten Funktionen angibt.</span><span class="sxs-lookup"><span data-stu-id="a1d05-131">Array of integers that specifies the features supported by the BIOS.</span></span> <span data-ttu-id="a1d05-132">Der Wert 3 ist im CIM-Schema ungültig, da er angibt, dass in DMI keine BIOS-Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a1d05-132">The value 3 is not valid in the CIM schema because it represents that no BIOS features are supported in DMI.</span></span> <span data-ttu-id="a1d05-133">In diesem Fall sollte dieses Objekt nicht instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="a1d05-133">In which case, this object should not be instantiated.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a1d05-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="a1d05-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a1d05-135">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="a1d05-135">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a1d05-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="a1d05-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a1d05-137">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="a1d05-137">Unknown.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="a1d05-138"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Nicht **definiert** (3)</span><span class="sxs-lookup"><span data-stu-id="a1d05-138"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a1d05-139">Nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="a1d05-139">Undefined.</span></span>

</dd> <dt>

<span id="ISA_Support"></span><span id="isa_support"></span><span id="ISA_SUPPORT"></span>

<span data-ttu-id="a1d05-140"><span id="ISA_Support"></span><span id="isa_support"></span><span id="ISA_SUPPORT"></span>**ISA-Unterstützung** (4)</span><span class="sxs-lookup"><span data-stu-id="a1d05-140"><span id="ISA_Support"></span><span id="isa_support"></span><span id="ISA_SUPPORT"></span>**ISA Support** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a1d05-141">ISA-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="a1d05-141">ISA support.</span></span>

</dd> <dt>

<span id="MCA_Support"></span><span id="mca_support"></span><span id="MCA_SUPPORT"></span>

<span data-ttu-id="a1d05-142"><span id="MCA_Support"></span><span id="mca_support"></span><span id="MCA_SUPPORT"></span>**MCA-Unterstützung** (5)</span><span class="sxs-lookup"><span data-stu-id="a1d05-142"><span id="MCA_Support"></span><span id="mca_support"></span><span id="MCA_SUPPORT"></span>**MCA Support** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a1d05-143">MCA-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="a1d05-143">MCA support.</span></span>

</dd> <dt>

<span id="EISA_Support"></span><span id="eisa_support"></span><span id="EISA_SUPPORT"></span>

<span data-ttu-id="a1d05-144"><span id="EISA_Support"></span><span id="eisa_support"></span><span id="EISA_SUPPORT"></span>**EISA-Unterstützung** (6)</span><span class="sxs-lookup"><span data-stu-id="a1d05-144"><span id="EISA_Support"></span><span id="eisa_support"></span><span id="EISA_SUPPORT"></span>**EISA Support** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a1d05-145">EISA-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="a1d05-145">EISA support.</span></span>

</dd> <dt>

<span id="PCI_Support"></span><span id="pci_support"></span><span id="PCI_SUPPORT"></span>

<span data-ttu-id="a1d05-146"><span id="PCI_Support"></span><span id="pci_support"></span><span id="PCI_SUPPORT"></span>**PCI-Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="a1d05-146"><span id="PCI_Support"></span><span id="pci_support"></span><span id="PCI_SUPPORT"></span>**PCI Support** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a1d05-147">PCI-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="a1d05-147">PCI support.</span></span>

</dd> <dt>

<span id="PCMCIA_Support"></span><span id="pcmcia_support"></span><span id="PCMCIA_SUPPORT"></span>

<span data-ttu-id="a1d05-148"><span id="PCMCIA_Support"></span><span id="pcmcia_support"></span><span id="PCMCIA_SUPPORT"></span>**Unterstützung für PCMCIA** (8)</span><span class="sxs-lookup"><span data-stu-id="a1d05-148"><span id="PCMCIA_Support"></span><span id="pcmcia_support"></span><span id="PCMCIA_SUPPORT"></span>**PCMCIA Support** (8)</span></span>


</dt> <dd>

<span data-ttu-id="a1d05-149">Unterstützung für PCMCIA.</span><span class="sxs-lookup"><span data-stu-id="a1d05-149">PCMCIA support.</span></span>

</dd> <dt>

<span id="PnP_Support"></span><span id="pnp_support"></span><span id="PNP_SUPPORT"></span>

<span data-ttu-id="a1d05-150"><span id="PnP_Support"></span><span id="pnp_support"></span><span id="PNP_SUPPORT"></span>**PNP-Unterstützung** (9)</span><span class="sxs-lookup"><span data-stu-id="a1d05-150"><span id="PnP_Support"></span><span id="pnp_support"></span><span id="PNP_SUPPORT"></span>**PnP Support** (9)</span></span>


</dt> <dd>

<span data-ttu-id="a1d05-151">PNP-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="a1d05-151">PnP support.</span></span>

</dd> <dt>

<span id="APM_Support"></span><span id="apm_support"></span><span id="APM_SUPPORT"></span>

<span data-ttu-id="a1d05-152"><span id="APM_Support"></span><span id="apm_support"></span><span id="APM_SUPPORT"></span>**APM-Unterstützung** (10)</span><span class="sxs-lookup"><span data-stu-id="a1d05-152"><span id="APM_Support"></span><span id="apm_support"></span><span id="APM_SUPPORT"></span>**APM Support** (10)</span></span>


</dt> <dd>

<span data-ttu-id="a1d05-153">APM-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="a1d05-153">APM support.</span></span>

</dd> <dt>

<span id="Upgradeable_BIOS"></span><span id="upgradeable_bios"></span><span id="UPGRADEABLE_BIOS"></span>

<span data-ttu-id="a1d05-154"><span id="Upgradeable_BIOS"></span><span id="upgradeable_bios"></span><span id="UPGRADEABLE_BIOS"></span>**Aktualisier bares BIOS** (11)</span><span class="sxs-lookup"><span data-stu-id="a1d05-154"><span id="Upgradeable_BIOS"></span><span id="upgradeable_bios"></span><span id="UPGRADEABLE_BIOS"></span>**Upgradeable BIOS** (11)</span></span>


</dt> <dd>

<span data-ttu-id="a1d05-155">Aktualisier bares BIOS.</span><span class="sxs-lookup"><span data-stu-id="a1d05-155">Upgradeable BIOS.</span></span>

</dd> <dt>

<span id="BIOS_Shadowing_Allowed"></span><span id="bios_shadowing_allowed"></span><span id="BIOS_SHADOWING_ALLOWED"></span>

<span data-ttu-id="a1d05-156"><span id="BIOS_Shadowing_Allowed"></span><span id="bios_shadowing_allowed"></span><span id="BIOS_SHADOWING_ALLOWED"></span>**BIOS-shadodown zulässig** (12)</span><span class="sxs-lookup"><span data-stu-id="a1d05-156"><span id="BIOS_Shadowing_Allowed"></span><span id="bios_shadowing_allowed"></span><span id="BIOS_SHADOWING_ALLOWED"></span>**BIOS Shadowing Allowed** (12)</span></span>


</dt> <dd>

<span data-ttu-id="a1d05-157">BIOS-shadodown zulässig.</span><span class="sxs-lookup"><span data-stu-id="a1d05-157">BIOS shadowing allowed.</span></span>

</dd> <dt>

<span id="VL_VESA_Support"></span><span id="vl_vesa_support"></span><span id="VL_VESA_SUPPORT"></span>

<span data-ttu-id="a1d05-158"><span id="VL_VESA_Support"></span><span id="vl_vesa_support"></span><span id="VL_VESA_SUPPORT"></span>**VL VESA-Unterstützung** (13)</span><span class="sxs-lookup"><span data-stu-id="a1d05-158"><span id="VL_VESA_Support"></span><span id="vl_vesa_support"></span><span id="VL_VESA_SUPPORT"></span>**VL VESA Support** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a1d05-159">VL VESA-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="a1d05-159">VL VESA support.</span></span>

</dd> <dt>

<span id="ESCD_Support"></span><span id="escd_support"></span><span id="ESCD_SUPPORT"></span>

<span data-ttu-id="a1d05-160"><span id="ESCD_Support"></span><span id="escd_support"></span><span id="ESCD_SUPPORT"></span>**ESCD-Unterstützung** (14)</span><span class="sxs-lookup"><span data-stu-id="a1d05-160"><span id="ESCD_Support"></span><span id="escd_support"></span><span id="ESCD_SUPPORT"></span>**ESCD Support** (14)</span></span>


</dt> <dd>

<span data-ttu-id="a1d05-161">ESCD-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="a1d05-161">ESCD support.</span></span>

</dd> <dt>

<span id="LS-120_Support"></span><span id="ls-120_support"></span><span id="LS-120_SUPPORT"></span>

<span data-ttu-id="a1d05-162"><span id="LS-120_Support"></span><span id="ls-120_support"></span><span id="LS-120_SUPPORT"></span>**Unterstützung für LS-120** (15)</span><span class="sxs-lookup"><span data-stu-id="a1d05-162"><span id="LS-120_Support"></span><span id="ls-120_support"></span><span id="LS-120_SUPPORT"></span>**LS-120 Support** (15)</span></span>


</dt> <dd>

<span data-ttu-id="a1d05-163">Unterstützung für LS-120.</span><span class="sxs-lookup"><span data-stu-id="a1d05-163">LS-120 support.</span></span>

</dd> <dt>

<span id="ACPI_Support"></span><span id="acpi_support"></span><span id="ACPI_SUPPORT"></span>

<span data-ttu-id="a1d05-164"><span id="ACPI_Support"></span><span id="acpi_support"></span><span id="ACPI_SUPPORT"></span>**ACPI-Unterstützung** (16)</span><span class="sxs-lookup"><span data-stu-id="a1d05-164"><span id="ACPI_Support"></span><span id="acpi_support"></span><span id="ACPI_SUPPORT"></span>**ACPI Support** (16)</span></span>


</dt> <dd>

<span data-ttu-id="a1d05-165">ACPI-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="a1d05-165">ACPI support.</span></span>

</dd> <dt>

<span id="I2O_Boot_Support"></span><span id="i2o_boot_support"></span><span id="I2O_BOOT_SUPPORT"></span>

<span data-ttu-id="a1d05-166"><span id="I2O_Boot_Support"></span><span id="i2o_boot_support"></span><span id="I2O_BOOT_SUPPORT"></span>**I2O-Start Unterstützung** (17)</span><span class="sxs-lookup"><span data-stu-id="a1d05-166"><span id="I2O_Boot_Support"></span><span id="i2o_boot_support"></span><span id="I2O_BOOT_SUPPORT"></span>**I2O Boot Support** (17)</span></span>


</dt> <dd>

<span data-ttu-id="a1d05-167">I2O-Start Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="a1d05-167">I2O boot support.</span></span>

</dd> <dt>

<span id="USB_Legacy_Support"></span><span id="usb_legacy_support"></span><span id="USB_LEGACY_SUPPORT"></span>

<span data-ttu-id="a1d05-168"><span id="USB_Legacy_Support"></span><span id="usb_legacy_support"></span><span id="USB_LEGACY_SUPPORT"></span>**Unterstützung für USB-Legacy** (18)</span><span class="sxs-lookup"><span data-stu-id="a1d05-168"><span id="USB_Legacy_Support"></span><span id="usb_legacy_support"></span><span id="USB_LEGACY_SUPPORT"></span>**USB Legacy Support** (18)</span></span>


</dt> <dd>

<span data-ttu-id="a1d05-169">Unterstützung für USB-Legacy.</span><span class="sxs-lookup"><span data-stu-id="a1d05-169">USB legacy support.</span></span>

</dd> <dt>

<span id="AGP_Support"></span><span id="agp_support"></span><span id="AGP_SUPPORT"></span>

<span data-ttu-id="a1d05-170"><span id="AGP_Support"></span><span id="agp_support"></span><span id="AGP_SUPPORT"></span>**AGP-Unterstützung** (19)</span><span class="sxs-lookup"><span data-stu-id="a1d05-170"><span id="AGP_Support"></span><span id="agp_support"></span><span id="AGP_SUPPORT"></span>**AGP Support** (19)</span></span>


</dt> <dd>

<span data-ttu-id="a1d05-171">AGP-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="a1d05-171">AGP support.</span></span>

</dd> <dt>

<span id="PC_Card"></span><span id="pc_card"></span><span id="PC_CARD"></span>

<span data-ttu-id="a1d05-172"><span id="PC_Card"></span><span id="pc_card"></span><span id="PC_CARD"></span>**PC-Karte** (20)</span><span class="sxs-lookup"><span data-stu-id="a1d05-172"><span id="PC_Card"></span><span id="pc_card"></span><span id="PC_CARD"></span>**PC Card** (20)</span></span>


</dt> <dd>

<span data-ttu-id="a1d05-173">PC-Karte.</span><span class="sxs-lookup"><span data-stu-id="a1d05-173">PC card.</span></span>

</dd> <dt>

<span id="IR"></span><span id="ir"></span>

<span data-ttu-id="a1d05-174"><span id="IR"></span><span id="ir"></span>**IR** (21)</span><span class="sxs-lookup"><span data-stu-id="a1d05-174"><span id="IR"></span><span id="ir"></span>**IR** (21)</span></span>


</dt> <dd>

<span data-ttu-id="a1d05-175">XI.</span><span class="sxs-lookup"><span data-stu-id="a1d05-175">IR.</span></span>

</dd> <dt>

<span id="1394"></span>

<span data-ttu-id="a1d05-176"><span id="1394"></span>**1394** (22)</span><span class="sxs-lookup"><span data-stu-id="a1d05-176"><span id="1394"></span>**1394** (22)</span></span>


</dt> <dd>

1394.

</dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="a1d05-177"><span id="I2C"></span><span id="i2c"></span>**I2C** (23)</span><span class="sxs-lookup"><span data-stu-id="a1d05-177"><span id="I2C"></span><span id="i2c"></span>**I2C** (23)</span></span>


</dt> <dd>

<span data-ttu-id="a1d05-178">San.</span><span class="sxs-lookup"><span data-stu-id="a1d05-178">I2C.</span></span>

</dd> <dt>

<span id="Smart_Battery"></span><span id="smart_battery"></span><span id="SMART_BATTERY"></span>

<span data-ttu-id="a1d05-179"><span id="Smart_Battery"></span><span id="smart_battery"></span><span id="SMART_BATTERY"></span>**Intelligenter Akku** (24)</span><span class="sxs-lookup"><span data-stu-id="a1d05-179"><span id="Smart_Battery"></span><span id="smart_battery"></span><span id="SMART_BATTERY"></span>**Smart Battery** (24)</span></span>


</dt> <dd>

<span data-ttu-id="a1d05-180">Intelligenter Akku.</span><span class="sxs-lookup"><span data-stu-id="a1d05-180">Smart battery.</span></span>

</dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="a1d05-181"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="a1d05-181"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span></span>


</dt> <dd>

<span data-ttu-id="a1d05-182">PC-98.</span><span class="sxs-lookup"><span data-stu-id="a1d05-182">PC-98.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a1d05-183">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a1d05-183">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1d05-184">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1d05-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1d05-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1d05-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1d05-186">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="a1d05-186">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a1d05-187">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a1d05-187">A textual description of the object.</span></span>

<span data-ttu-id="a1d05-188">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1d05-188">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1d05-189">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="a1d05-189">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1d05-190">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1d05-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1d05-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1d05-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1d05-192">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM- \_ Produkt**](cim-product.md).**Identifyingnumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="a1d05-192">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="a1d05-193">Produktidentifizierung, z. b. eine Seriennummer auf Software oder eine Zahl auf einem Hardware Chip.</span><span class="sxs-lookup"><span data-stu-id="a1d05-193">Product identification, such as a serial number on software or a die number on a hardware chip.</span></span>

<span data-ttu-id="a1d05-194">Diese Eigenschaft wird von [**CIM \_ Softwarefeature**](cim-softwarefeature.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1d05-194">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1d05-195">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a1d05-195">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1d05-196">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="a1d05-196">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a1d05-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1d05-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1d05-198">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="a1d05-198">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a1d05-199">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a1d05-199">Indicates when the object was installed.</span></span> <span data-ttu-id="a1d05-200">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="a1d05-200">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a1d05-201">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1d05-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1d05-202">**Name**</span><span class="sxs-lookup"><span data-stu-id="a1d05-202">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1d05-203">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1d05-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1d05-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1d05-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1d05-205">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a1d05-205">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a1d05-206">Die Name-Eigenschaft definiert die Bezeichnung, mit der das Objekt außerhalb des Datenverarbeitungssystems der Welt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="a1d05-206">The Name property defines the label by which the object is known to the world outside the data processing system.</span></span> <span data-ttu-id="a1d05-207">Diese Bezeichnung ist ein lesbarer Name, der das Element im Kontext des Namespace des Elements eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a1d05-207">This label is a human-readable name that uniquely identifies the element in the context of the element's namespace.</span></span>

<span data-ttu-id="a1d05-208">Diese Eigenschaft wird von [**CIM \_ Softwarefeature**](cim-softwarefeature.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1d05-208">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1d05-209">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="a1d05-209">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1d05-210">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1d05-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1d05-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1d05-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1d05-212">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM- \_ Produkt**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="a1d05-212">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="a1d05-213">Häufig verwendeter Produktname.</span><span class="sxs-lookup"><span data-stu-id="a1d05-213">Commonly used product name.</span></span>

<span data-ttu-id="a1d05-214">Diese Eigenschaft wird von [**CIM \_ Softwarefeature**](cim-softwarefeature.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1d05-214">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1d05-215">**Status**</span><span class="sxs-lookup"><span data-stu-id="a1d05-215">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1d05-216">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1d05-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1d05-217">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1d05-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1d05-218">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="a1d05-218">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a1d05-219">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="a1d05-219">String that indicates the current status of the object.</span></span> <span data-ttu-id="a1d05-220">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="a1d05-220">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="a1d05-221">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="a1d05-221">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="a1d05-222">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="a1d05-222">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="a1d05-223">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="a1d05-223">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a1d05-224">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="a1d05-224">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a1d05-225">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="a1d05-225">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a1d05-226">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1d05-226">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a1d05-227">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="a1d05-227">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a1d05-228">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a1d05-228">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a1d05-229">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="a1d05-229">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a1d05-230">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="a1d05-230">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a1d05-231">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="a1d05-231">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a1d05-232">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="a1d05-232">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a1d05-233">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="a1d05-233">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a1d05-234">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="a1d05-234">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a1d05-235">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="a1d05-235">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a1d05-236">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="a1d05-236">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a1d05-237">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="a1d05-237">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a1d05-238">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="a1d05-238">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a1d05-239">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="a1d05-239">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a1d05-240">**Hersteller**</span><span class="sxs-lookup"><span data-stu-id="a1d05-240">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1d05-241">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1d05-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1d05-242">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1d05-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1d05-243">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM- \_ Produkt**](cim-product.md).**Vendor**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="a1d05-243">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Vendor**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="a1d05-244">Der Name des Lieferanten des Produkts, der der **Vendor** -Eigenschaft im Product-Objekt des DMTF-Lösungs Austausch Standards entspricht.</span><span class="sxs-lookup"><span data-stu-id="a1d05-244">Name of the product's supplier, which corresponds to the **Vendor** property in the product object of the DMTF Solution Exchange Standard.</span></span>

<span data-ttu-id="a1d05-245">Diese Eigenschaft wird von [**CIM \_ Softwarefeature**](cim-softwarefeature.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1d05-245">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1d05-246">**Version**</span><span class="sxs-lookup"><span data-stu-id="a1d05-246">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1d05-247">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1d05-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1d05-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1d05-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1d05-249">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM- \_ Produkt**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="a1d05-249">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="a1d05-250">Produkt Versionsinformationen, die der **Version** -Eigenschaft im Product-Objekt des DMTF-Lösungs Austausch Standards entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a1d05-250">Product version information, which corresponds to the **Version** property in the product object of the DMTF Solution Exchange Standard.</span></span>

<span data-ttu-id="a1d05-251">Diese Eigenschaft wird von [**CIM \_ Softwarefeature**](cim-softwarefeature.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a1d05-251">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a1d05-252">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1d05-252">Remarks</span></span>

<span data-ttu-id="a1d05-253">Die **CIM \_ biosfeature** -Klasse wird von [**CIM \_ Softwarefeature**](cim-softwarefeature.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a1d05-253">The **CIM\_BIOSFeature** class is derived from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

<span data-ttu-id="a1d05-254">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="a1d05-254">WMI does not implement this class.</span></span>

<span data-ttu-id="a1d05-255">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a1d05-255">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a1d05-256">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a1d05-256">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1d05-257">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1d05-257">Requirements</span></span>



| <span data-ttu-id="a1d05-258">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1d05-258">Requirement</span></span> | <span data-ttu-id="a1d05-259">Wert</span><span class="sxs-lookup"><span data-stu-id="a1d05-259">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1d05-260">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a1d05-260">Minimum supported client</span></span><br/> | <span data-ttu-id="a1d05-261">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a1d05-261">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a1d05-262">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a1d05-262">Minimum supported server</span></span><br/> | <span data-ttu-id="a1d05-263">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1d05-263">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a1d05-264">Namespace</span><span class="sxs-lookup"><span data-stu-id="a1d05-264">Namespace</span></span><br/>                | <span data-ttu-id="a1d05-265">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a1d05-265">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a1d05-266">MOF</span><span class="sxs-lookup"><span data-stu-id="a1d05-266">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a1d05-267"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a1d05-267"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a1d05-268">DLL</span><span class="sxs-lookup"><span data-stu-id="a1d05-268">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1d05-269"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1d05-269"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1d05-270">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1d05-270">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1d05-271">**CIM- \_ Softwarefeature**</span><span class="sxs-lookup"><span data-stu-id="a1d05-271">**CIM\_SoftwareFeature**</span></span>](cim-softwarefeature.md)
</dt> </dl>

 

