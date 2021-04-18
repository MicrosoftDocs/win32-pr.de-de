---
description: Stellt die Software auf niedriger Ebene dar, die in einen nicht flüchtigen Speicher geladen und zum Starten und Konfigurieren eines Computer Systems (CIM \_ Computersystem) verwendet wird.
ms.assetid: e34c9b00-2723-4858-805e-5e3e51a5dfd2
title: CIM_BIOSElement-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSElement
- CIM_BIOSElement.Version
- CIM_BIOSElement.Manufacturer
- CIM_BIOSElement.PrimaryBIOS
- CIM_BIOSElement.ListOfLanguages
- CIM_BIOSElement.CurrentLanguage
- CIM_BIOSElement.LoadedStartingAddress
- CIM_BIOSElement.LoadedEndingAddress
- CIM_BIOSElement.LoadUtilityInformation
- CIM_BIOSElement.ReleaseDate
- CIM_BIOSElement.RegistryURIs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f97cbb495fb8105be012c44942aeedb39377e3d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366244"
---
# <a name="cim_bioselement-class-hyper-v-management"></a><span data-ttu-id="c54c2-103">CIM_BIOSElement-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="c54c2-103">CIM_BIOSElement class (Hyper-V management)</span></span>

<span data-ttu-id="c54c2-104">Stellt die Software auf niedriger Ebene dar, die in einen nicht flüchtigen Speicher geladen und zum Starten und Konfigurieren eines Computer Systems ([**CIM \_ Computersystem**](cim-computersystem.md)) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c54c2-104">Represents the low-level software that is loaded into non-volatile storage and used to start up and configure a computer system ([**CIM\_ComputerSystem**](cim-computersystem.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="c54c2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c54c2-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.17.0"), UMLPackagePath("CIM::Application::BIOS"), AMENDMENT]
class CIM_BIOSElement : CIM_SoftwareElement
{
  string   Version;
  string   Manufacturer;
  boolean  PrimaryBIOS;
  string   ListOfLanguages[];
  string   CurrentLanguage;
  uint64   LoadedStartingAddress;
  uint64   LoadedEndingAddress;
  string   LoadUtilityInformation;
  datetime ReleaseDate;
  string   RegistryURIs[];
};
```

## <a name="members"></a><span data-ttu-id="c54c2-106">Member</span><span class="sxs-lookup"><span data-stu-id="c54c2-106">Members</span></span>

<span data-ttu-id="c54c2-107">Die CIM-Klasse " **\_ bioselements** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c54c2-107">The **CIM\_BIOSElement** class has these types of members:</span></span>

-   [<span data-ttu-id="c54c2-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c54c2-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c54c2-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c54c2-109">Properties</span></span>

<span data-ttu-id="c54c2-110">Die CIM-Klasse " **\_ bioselements** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c54c2-110">The **CIM\_BIOSElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c54c2-111">**CurrentLanguage**</span><span class="sxs-lookup"><span data-stu-id="c54c2-111">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c54c2-112">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c54c2-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c54c2-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-114">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ bioseless**".**ListOf-Sprachen**")</span><span class="sxs-lookup"><span data-stu-id="c54c2-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_BIOSElement**.**ListOfLanguages**")</span></span>
</dt> </dl>

<span data-ttu-id="c54c2-115">Die aktuell für das BIOS ausgewählte Sprache.</span><span class="sxs-lookup"><span data-stu-id="c54c2-115">The currently selected language for the BIOS.</span></span> <span data-ttu-id="c54c2-116">Diese Informationen können aus dem Systemverwaltungs-BIOS (Systemverwaltungs-BIOS) abgerufen werden, wobei das aktuelle sprach Attribut der Type 13-Struktur verwendet wird, um in die Zeichen folgen Liste zu indizieren, die der Struktur folgt.</span><span class="sxs-lookup"><span data-stu-id="c54c2-116">This information can be obtained from the System Management BIOS (SMBIOS) using the Current Language attribute of the Type 13 structure to index into the string list that follows the structure.</span></span> <span data-ttu-id="c54c2-117">Diese Eigenschaft wird mit dem Namen der ISO 639-Sprache formatiert, gefolgt vom ISO 3166 Territory-Namen und der Codierungsmethode.</span><span class="sxs-lookup"><span data-stu-id="c54c2-117">This property is formatted using the ISO 639 Language Name, and may be followed by the ISO 3166 Territory Name and the encoding method.</span></span>

</dd> <dt>

<span data-ttu-id="c54c2-118">**ListOf-Sprachen**</span><span class="sxs-lookup"><span data-stu-id="c54c2-118">**ListOfLanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c54c2-119">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="c54c2-119">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c54c2-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c54c2-121">Eine Liste installier barer Sprachen für das BIOS.</span><span class="sxs-lookup"><span data-stu-id="c54c2-121">A list of installable languages for the BIOS.</span></span> <span data-ttu-id="c54c2-122">Diese Informationen können aus der Zeichen folgen Liste abgerufen werden, die der Struktur des Typs 13 folgt.</span><span class="sxs-lookup"><span data-stu-id="c54c2-122">This information can be obtained from SMBIOS, from the string list that follows the Type 13 structure.</span></span> <span data-ttu-id="c54c2-123">Der Name der ISO 639-Sprache sollte zum Angeben der installierbaren BIOS-Sprachen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c54c2-123">An ISO 639 Language Name should be used to specify the BIOS' installable languages.</span></span> <span data-ttu-id="c54c2-124">Der Name des Gebiets namens ISO 3166 und die Codierungsmethode können auch nach dem Namen der Sprache angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c54c2-124">The ISO 3166 Territory Name and the encoding method may also be specified, following the Language Name.</span></span>

</dd> <dt>

<span data-ttu-id="c54c2-125">**Loadedendingaddress**</span><span class="sxs-lookup"><span data-stu-id="c54c2-125">**LoadedEndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c54c2-126">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c54c2-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c54c2-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-128">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System-BIOS \| 001,6 ")</span><span class="sxs-lookup"><span data-stu-id="c54c2-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="c54c2-129">Die Endadresse des vom BIOS belegten Speichers.</span><span class="sxs-lookup"><span data-stu-id="c54c2-129">The ending address of the memory that is occupied by the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="c54c2-130">**Loadedstartingaddress**</span><span class="sxs-lookup"><span data-stu-id="c54c2-130">**LoadedStartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c54c2-131">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c54c2-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c54c2-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-133">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System-BIOS \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="c54c2-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="c54c2-134">Die Startadresse des vom BIOS belegten Speichers.</span><span class="sxs-lookup"><span data-stu-id="c54c2-134">The starting address of the memory that is occupied by the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="c54c2-135">**Loadutilityinformation**</span><span class="sxs-lookup"><span data-stu-id="c54c2-135">**LoadUtilityInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c54c2-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c54c2-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c54c2-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-138">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System-BIOS \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="c54c2-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="c54c2-139">Eine frei Form Zeichenfolge, die das BIOS-Hilfsprogramm für Flash/Ladevorgang beschreibt, das zum Aktualisieren des **CIM \_** -Objekts für die Objekt Verwaltung erforderlich ist</span><span class="sxs-lookup"><span data-stu-id="c54c2-139">A free form string that describes the BIOS flash/load utility that is required to update the **CIM\_BIOSElement** object.</span></span> <span data-ttu-id="c54c2-140">Die Version und andere Informationen können in dieser Eigenschaft angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c54c2-140">Version and other information may be indicated in this property.</span></span>

</dd> <dt>

<span data-ttu-id="c54c2-141">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="c54c2-141">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c54c2-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c54c2-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c54c2-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-144">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hersteller"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System-BIOS \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="c54c2-144">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="c54c2-145">Der Hersteller des Software Elements.</span><span class="sxs-lookup"><span data-stu-id="c54c2-145">The manufacturer of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="c54c2-146">**Primarybios**</span><span class="sxs-lookup"><span data-stu-id="c54c2-146">**PrimaryBIOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c54c2-147">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c54c2-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c54c2-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-149">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System-BIOS \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="c54c2-149">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="c54c2-150">True, wenn dies das primäre BIOS des Computer Systems ist. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="c54c2-150">True if this is the primary BIOS of the computer system; otherwise, false.</span></span>

</dd> <dt>

<span data-ttu-id="c54c2-151">**Registryuris**</span><span class="sxs-lookup"><span data-stu-id="c54c2-151">**RegistryURIs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c54c2-152">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="c54c2-152">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c54c2-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c54c2-154">Der Veröffentlichungs Speicherort der BIOS-Attribut Registrierungen, denen die BIOS-Implementierung entspricht.</span><span class="sxs-lookup"><span data-stu-id="c54c2-154">The publication location of the BIOS attribute registries to which the BIOS implementation complies.</span></span>

</dd> <dt>

<span data-ttu-id="c54c2-155">**ReleaseDate**</span><span class="sxs-lookup"><span data-stu-id="c54c2-155">**ReleaseDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c54c2-156">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="c54c2-156">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c54c2-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-158">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System-BIOS \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="c54c2-158">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="c54c2-159">Das Datum, an dem dieses BIOS freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="c54c2-159">The Date on which this BIOS was released.</span></span>

</dd> <dt>

<span data-ttu-id="c54c2-160">**Version**</span><span class="sxs-lookup"><span data-stu-id="c54c2-160">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c54c2-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c54c2-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c54c2-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c54c2-163">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System-BIOS \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="c54c2-163">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="c54c2-164">Die Version des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="c54c2-164">The version of the operation.</span></span> <span data-ttu-id="c54c2-165">Die Version des Vorgangs sollte eine der folgenden Formen aufweisen:</span><span class="sxs-lookup"><span data-stu-id="c54c2-165">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="c54c2-166">*<major>*.*<minor>*.*<revision>*</span><span class="sxs-lookup"><span data-stu-id="c54c2-166">*<major>*.*<minor>*.*<revision>*</span></span>
-   <span data-ttu-id="c54c2-167">*<major>*.*<minor><letter><revision>*</span><span class="sxs-lookup"><span data-stu-id="c54c2-167">*<major>*.*<minor><letter><revision>*</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c54c2-168">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c54c2-168">Requirements</span></span>



| <span data-ttu-id="c54c2-169">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c54c2-169">Requirement</span></span> | <span data-ttu-id="c54c2-170">Wert</span><span class="sxs-lookup"><span data-stu-id="c54c2-170">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c54c2-171">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c54c2-171">Minimum supported client</span></span><br/> | <span data-ttu-id="c54c2-172">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c54c2-172">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="c54c2-173">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c54c2-173">Minimum supported server</span></span><br/> | <span data-ttu-id="c54c2-174">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c54c2-174">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="c54c2-175">Namespace</span><span class="sxs-lookup"><span data-stu-id="c54c2-175">Namespace</span></span><br/>                | <span data-ttu-id="c54c2-176">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="c54c2-176">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c54c2-177">MOF</span><span class="sxs-lookup"><span data-stu-id="c54c2-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c54c2-178"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c54c2-178"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c54c2-179">DLL</span><span class="sxs-lookup"><span data-stu-id="c54c2-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c54c2-180"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c54c2-180"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c54c2-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c54c2-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c54c2-182">**CIM- \_ Softwareelement**</span><span class="sxs-lookup"><span data-stu-id="c54c2-182">**CIM\_SoftwareElement**</span></span>](cim-softwareelement.md)
</dt> </dl>

 

