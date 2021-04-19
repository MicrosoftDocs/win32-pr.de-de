---
description: Die CIM \_ videobiosfeature-Klasse stellt die Funktionen der Low-Level-Software dar, die zum Konfigurieren und Zugreifen auf den Videocontroller und die Anzeige eines Computer Systems verwendet wird.
ms.assetid: a12ca387-5b12-487f-84fd-381afe266338
ms.tgt_platform: multiple
title: CIM_VideoBIOSFeature-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoBIOSFeature
- CIM_VideoBIOSFeature.Caption
- CIM_VideoBIOSFeature.CharacteristicDescriptions
- CIM_VideoBIOSFeature.Characteristics
- CIM_VideoBIOSFeature.Description
- CIM_VideoBIOSFeature.IdentifyingNumber
- CIM_VideoBIOSFeature.InstallDate
- CIM_VideoBIOSFeature.Name
- CIM_VideoBIOSFeature.ProductName
- CIM_VideoBIOSFeature.Status
- CIM_VideoBIOSFeature.Vendor
- CIM_VideoBIOSFeature.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 45f9fd2feabdcd1f9e650e7e7a913a394e8ef67d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344956"
---
# <a name="cim_videobiosfeature-class"></a><span data-ttu-id="2c838-103">CIM \_ videobiosfeature-Klasse</span><span class="sxs-lookup"><span data-stu-id="2c838-103">CIM\_VideoBIOSFeature class</span></span>

<span data-ttu-id="2c838-104">Die **CIM \_ videobiosfeature** -Klasse stellt die Funktionen der Low-Level-Software dar, die zum Konfigurieren und Zugreifen auf den Videocontroller und die Anzeige eines Computer Systems verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2c838-104">The **CIM\_VideoBIOSFeature** class represents the capabilities of the low-level software used to configure and access a computer system's video controller and display.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2c838-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2c838-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2c838-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2c838-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2c838-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2c838-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="2c838-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="2c838-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c838-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c838-109">Syntax</span></span>

``` syntax
[UUID("{BAE20634-E3D4-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_VideoBIOSFeature : CIM_SoftwareFeature
{
  string   Caption;
  string   CharacteristicDescriptions[];
  uint16   Characteristics[];
  string   Description;
  string   IdentifyingNumber;
  datetime InstallDate;
  string   Name;
  string   ProductName;
  string   Status;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="2c838-110">Member</span><span class="sxs-lookup"><span data-stu-id="2c838-110">Members</span></span>

<span data-ttu-id="2c838-111">Die **CIM \_ videobiosfeature** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2c838-111">The **CIM\_VideoBIOSFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="2c838-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2c838-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2c838-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2c838-113">Properties</span></span>

<span data-ttu-id="2c838-114">Die **CIM \_ videobiosfeature** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2c838-114">The **CIM\_VideoBIOSFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2c838-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2c838-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c838-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2c838-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c838-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2c838-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c838-118">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="2c838-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2c838-119">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="2c838-119">Short textual description of the object.</span></span>

<span data-ttu-id="2c838-120">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2c838-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c838-121">**Charakteristicbeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="2c838-121">**CharacteristicDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c838-122">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="2c838-122">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2c838-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2c838-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c838-124">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video-BIOS-Merkmal \| 001,4 "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ videobiosfeature**.**Merkmale**")</span><span class="sxs-lookup"><span data-stu-id="2c838-124">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video BIOS Characteristic\|001.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoBIOSFeature**.**Characteristics**")</span></span>
</dt> </dl>

<span data-ttu-id="2c838-125">Freiform-Zeichen folgen, die ausführliche Beschreibungen der im Array **Merkmale** angegebenen Grafik-BIOS-Funktionen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="2c838-125">Free-form strings that provide detailed descriptions for the video BIOS features indicated in the **Characteristics** array.</span></span>

> [!Note]  
> <span data-ttu-id="2c838-126">Jeder Eintrag dieses Arrays bezieht sich auf den Eintrag im Array **Merkmale** , der sich am selben Index befindet.</span><span class="sxs-lookup"><span data-stu-id="2c838-126">Each entry of this array is related to the entry in the **Characteristics** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="2c838-127">**Characteristics**</span><span class="sxs-lookup"><span data-stu-id="2c838-127">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c838-128">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="2c838-128">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2c838-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2c838-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c838-130">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video-BIOS-Merkmal \| 001,3 "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ videobiosfeature**.**Charakteristicbeschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="2c838-130">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video BIOS Characteristic\|001.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoBIOSFeature**.**CharacteristicDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="2c838-131">Funktionen, die vom Video-BIOS unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="2c838-131">Features supported by the video BIOS.</span></span> <span data-ttu-id="2c838-132">Beispielsweise kann die Unterstützung für die VESA-Energie Verwaltung oder die Video-BIOS-shadowingtung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2c838-132">For example, support for VESA power management or video BIOS shadowing could be indicated.</span></span> <span data-ttu-id="2c838-133">Der Wert 3 ("unknown") ist im CIM-Schema ungültig, da er angibt, dass in DMI keine BIOS-Funktionen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="2c838-133">The value 3 ("Unknown") is not valid in the CIM schema since it represents that no BIOS features are supported in DMI.</span></span> <span data-ttu-id="2c838-134">In diesem Fall sollte das Objekt nicht instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="2c838-134">In which case, the object should not be instantiated.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2c838-135">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="2c838-135">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c838-136">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="2c838-136">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="2c838-137">Nicht **definiert** (3)</span><span class="sxs-lookup"><span data-stu-id="2c838-137">**Undefined** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Standard_Video_BIOS"></span><span id="standard_video_bios"></span><span id="STANDARD_VIDEO_BIOS"></span>

<span data-ttu-id="2c838-138">**Standard-Grafik-BIOS** (4)</span><span class="sxs-lookup"><span data-stu-id="2c838-138">**Standard Video BIOS** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA_BIOS_Extensions_Supported"></span><span id="vesa_bios_extensions_supported"></span><span id="VESA_BIOS_EXTENSIONS_SUPPORTED"></span>

<span data-ttu-id="2c838-139">**Unterstützte VESA-BIOS-Erweiterungen** (5)</span><span class="sxs-lookup"><span data-stu-id="2c838-139">**VESA BIOS Extensions Supported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA_Power_Management_Supported"></span><span id="vesa_power_management_supported"></span><span id="VESA_POWER_MANAGEMENT_SUPPORTED"></span>

<span data-ttu-id="2c838-140">**Unterstützte VESA-Energie Verwaltung** (6)</span><span class="sxs-lookup"><span data-stu-id="2c838-140">**VESA Power Management Supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA_Display_Data_Channel_Supported"></span><span id="vesa_display_data_channel_supported"></span><span id="VESA_DISPLAY_DATA_CHANNEL_SUPPORTED"></span>

<span data-ttu-id="2c838-141">**VESA-Anzeigedaten Kanal unterstützt** (7)</span><span class="sxs-lookup"><span data-stu-id="2c838-141">**VESA Display Data Channel Supported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_BIOS_Shadowing_Allowed"></span><span id="video_bios_shadowing_allowed"></span><span id="VIDEO_BIOS_SHADOWING_ALLOWED"></span>

<span data-ttu-id="2c838-142">**Video-BIOS-shadodown zulässig** (8)</span><span class="sxs-lookup"><span data-stu-id="2c838-142">**Video BIOS Shadowing Allowed** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_BIOS_Upgradeable"></span><span id="video_bios_upgradeable"></span><span id="VIDEO_BIOS_UPGRADEABLE"></span>

<span data-ttu-id="2c838-143">**Video-BIOS-aktualisierbar** (9)</span><span class="sxs-lookup"><span data-stu-id="2c838-143">**Video BIOS Upgradeable** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2c838-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2c838-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c838-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2c838-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c838-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2c838-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c838-147">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="2c838-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2c838-148">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="2c838-148">Textual description of the object.</span></span>

<span data-ttu-id="2c838-149">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2c838-149">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c838-150">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="2c838-150">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c838-151">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2c838-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c838-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2c838-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c838-153">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM- \_ Produkt**](cim-product.md).**Identifyingnumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="2c838-153">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="2c838-154">Produktidentifizierung, z. b. eine Seriennummer auf Software oder eine Zahl auf einem Hardware Chip.</span><span class="sxs-lookup"><span data-stu-id="2c838-154">Product identification, such as a serial number on software or a die number on a hardware chip.</span></span> <span data-ttu-id="2c838-155">Diese Eigenschaft wird von [**CIM \_ Softwarefeature**](cim-softwarefeature.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2c838-155">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c838-156">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2c838-156">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c838-157">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="2c838-157">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2c838-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2c838-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c838-159">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="2c838-159">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2c838-160">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="2c838-160">Date and time the object was installed.</span></span> <span data-ttu-id="2c838-161">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="2c838-161">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="2c838-162">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2c838-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c838-163">**Name**</span><span class="sxs-lookup"><span data-stu-id="2c838-163">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c838-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2c838-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c838-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2c838-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c838-166">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2c838-166">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2c838-167">Die Bezeichnung, mit der das Objekt außerhalb des Datenverarbeitungssystems bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="2c838-167">Label by which the object is known outside of the data processing system.</span></span> <span data-ttu-id="2c838-168">Diese Bezeichnung ist ein Name, der das Element im Kontext des Namespace des Elements eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2c838-168">This label is a name that uniquely identifies the element in the context of the element's namespace.</span></span>

<span data-ttu-id="2c838-169">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2c838-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c838-170">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="2c838-170">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c838-171">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2c838-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c838-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2c838-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c838-173">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM- \_ Produkt**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="2c838-173">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="2c838-174">Häufig verwendeter Produktname.</span><span class="sxs-lookup"><span data-stu-id="2c838-174">Commonly used product name.</span></span>

<span data-ttu-id="2c838-175">Diese Eigenschaft wird von [**CIM \_ Softwarefeature**](cim-softwarefeature.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2c838-175">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c838-176">**Status**</span><span class="sxs-lookup"><span data-stu-id="2c838-176">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c838-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2c838-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c838-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2c838-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c838-179">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="2c838-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2c838-180">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="2c838-180">Current status of the object.</span></span> <span data-ttu-id="2c838-181">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2c838-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2c838-182">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="2c838-182">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2c838-183">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="2c838-183">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2c838-184">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="2c838-184">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2c838-185">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="2c838-185">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c838-186">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="2c838-186">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2c838-187">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="2c838-187">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2c838-188">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="2c838-188">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2c838-189">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="2c838-189">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2c838-190">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="2c838-190">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2c838-191">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="2c838-191">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2c838-192">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="2c838-192">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2c838-193">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="2c838-193">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2c838-194">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="2c838-194">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2c838-195">**Hersteller**</span><span class="sxs-lookup"><span data-stu-id="2c838-195">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c838-196">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2c838-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c838-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2c838-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c838-198">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM- \_ Produkt**](cim-product.md).**Vendor**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="2c838-198">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Vendor**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="2c838-199">Der Name des Lieferanten des Produkts, der der **Vendor** -Eigenschaft im Product-Objekt der DMTF-Lösung Exchange Standard (SES) entspricht.</span><span class="sxs-lookup"><span data-stu-id="2c838-199">Name of the product's supplier, which corresponds to the **Vendor** property in the product object of the DMTF Solution Exchange Standard (SES).</span></span>

<span data-ttu-id="2c838-200">Diese Eigenschaft wird von [**CIM \_ Softwarefeature**](cim-softwarefeature.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2c838-200">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c838-201">**Version**</span><span class="sxs-lookup"><span data-stu-id="2c838-201">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c838-202">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2c838-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c838-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2c838-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c838-204">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM- \_ Produkt**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="2c838-204">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="2c838-205">Produkt Versionsinformationen, die der **Version** -Eigenschaft im Product-Objekt der DMTF-SES entsprechen.</span><span class="sxs-lookup"><span data-stu-id="2c838-205">Product version information, which corresponds to the **Version** property in the product object of the DMTF SES.</span></span>

<span data-ttu-id="2c838-206">Diese Eigenschaft wird von [**CIM \_ Softwarefeature**](cim-softwarefeature.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2c838-206">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c838-207">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c838-207">Remarks</span></span>

<span data-ttu-id="2c838-208">Die **CIM \_ videobiosfeature** -Klasse wird von [**CIM \_ Softwarefeature**](cim-softwarefeature.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="2c838-208">The **CIM\_VideoBIOSFeature** class is derived from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

<span data-ttu-id="2c838-209">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="2c838-209">WMI does not implement this class.</span></span>

<span data-ttu-id="2c838-210">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="2c838-210">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2c838-211">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="2c838-211">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c838-212">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c838-212">Requirements</span></span>



| <span data-ttu-id="2c838-213">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c838-213">Requirement</span></span> | <span data-ttu-id="2c838-214">Wert</span><span class="sxs-lookup"><span data-stu-id="2c838-214">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c838-215">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c838-215">Minimum supported client</span></span><br/> | <span data-ttu-id="2c838-216">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c838-216">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2c838-217">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c838-217">Minimum supported server</span></span><br/> | <span data-ttu-id="2c838-218">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c838-218">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2c838-219">Namespace</span><span class="sxs-lookup"><span data-stu-id="2c838-219">Namespace</span></span><br/>                | <span data-ttu-id="2c838-220">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2c838-220">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2c838-221">MOF</span><span class="sxs-lookup"><span data-stu-id="2c838-221">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c838-222"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2c838-222"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c838-223">DLL</span><span class="sxs-lookup"><span data-stu-id="2c838-223">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c838-224"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c838-224"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c838-225">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c838-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c838-226">**CIM- \_ Softwarefeature**</span><span class="sxs-lookup"><span data-stu-id="2c838-226">**CIM\_SoftwareFeature**</span></span>](cim-softwarefeature.md)
</dt> </dl>

 

