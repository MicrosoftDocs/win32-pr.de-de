---
description: Die Tabelle "patchmetadata" enthält Informationen zu einem Windows Installer Patch, der zum Entfernen eines Patches erforderlich ist und das von "Software" verwendet wird.
ms.assetid: 09a06de4-0713-4e92-ab29-f34f6c94b677
title: Patchmetadata-Tabelle (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e2521684714b91d8d172f8eb56bab984ffea87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366299"
---
# <a name="patchmetadata-table-patchwizdll"></a><span data-ttu-id="d59db-103">Patchmetadata-Tabelle (PATCHWIZ.DLL)</span><span class="sxs-lookup"><span data-stu-id="d59db-103">PatchMetadata Table (PATCHWIZ.DLL)</span></span>

<span data-ttu-id="d59db-104">Die Tabelle "patchmetadata" enthält Informationen zu einem Windows Installer Patch, der zum Entfernen eines Patches erforderlich ist und das von "Software" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d59db-104">The PatchMetadata Table contains information about a Windows Installer patch that is required to remove a patch and that is used by Add/Remove Programs.</span></span> <span data-ttu-id="d59db-105">Alle Eigenschaften in der Tabelle patchmetadata werden der [MsiPatchMetadata-Tabelle](msipatchmetadata-table.md) der MSP-Datei für einen Patch hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d59db-105">All the properties in the PatchMetadata Table are added to the [MsiPatchMetadata Table](msipatchmetadata-table.md) of the .msp file for a patch.</span></span>

<span data-ttu-id="d59db-106">Die patchmetadata-Tabelle ist in den Eigenschaften Dateien der Patcherstellung (PCP-Dateien) erforderlich, deren minimumrequirements dmsiversion 300 in der [Properties-Tabelle](properties-table-patchwiz-dll-.md)entspricht.</span><span class="sxs-lookup"><span data-stu-id="d59db-106">The PatchMetadata Table is required in patch creation properties files (.pcp files) that have a MinimumRequiredMsiVersion equal to 300 in the [Properties Table](properties-table-patchwiz-dll-.md).</span></span> <span data-ttu-id="d59db-107">Die Tabelle ist optional, wenn minimumrequirements dmsiversion nicht gleich 300 ist.</span><span class="sxs-lookup"><span data-stu-id="d59db-107">The table is optional if MinimumRequiredMsiVersion is not equal to 300.</span></span>

<span data-ttu-id="d59db-108">Die patchmetadata-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="d59db-108">The PatchMetadata Table has the following columns.</span></span>



| <span data-ttu-id="d59db-109">Spalte</span><span class="sxs-lookup"><span data-stu-id="d59db-109">Column</span></span>   | <span data-ttu-id="d59db-110">Typ</span><span class="sxs-lookup"><span data-stu-id="d59db-110">Type</span></span> | <span data-ttu-id="d59db-111">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="d59db-111">Key</span></span> | <span data-ttu-id="d59db-112">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="d59db-112">Nullable</span></span> |
|----------|------|-----|----------|
| <span data-ttu-id="d59db-113">Company</span><span class="sxs-lookup"><span data-stu-id="d59db-113">Company</span></span>  | <span data-ttu-id="d59db-114">text</span><span class="sxs-lookup"><span data-stu-id="d59db-114">text</span></span> | <span data-ttu-id="d59db-115">J</span><span class="sxs-lookup"><span data-stu-id="d59db-115">Y</span></span>   | <span data-ttu-id="d59db-116">J</span><span class="sxs-lookup"><span data-stu-id="d59db-116">Y</span></span>        |
| <span data-ttu-id="d59db-117">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d59db-117">Property</span></span> | <span data-ttu-id="d59db-118">text</span><span class="sxs-lookup"><span data-stu-id="d59db-118">text</span></span> | <span data-ttu-id="d59db-119">J</span><span class="sxs-lookup"><span data-stu-id="d59db-119">Y</span></span>   | <span data-ttu-id="d59db-120">N</span><span class="sxs-lookup"><span data-stu-id="d59db-120">N</span></span>        |
| <span data-ttu-id="d59db-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d59db-121">Value</span></span>    | <span data-ttu-id="d59db-122">text</span><span class="sxs-lookup"><span data-stu-id="d59db-122">text</span></span> |     | <span data-ttu-id="d59db-123">J</span><span class="sxs-lookup"><span data-stu-id="d59db-123">Y</span></span>        |



 

### <a name="columns"></a><span data-ttu-id="d59db-124">Spalten</span><span class="sxs-lookup"><span data-stu-id="d59db-124">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d59db-125"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Geschäfts</span><span class="sxs-lookup"><span data-stu-id="d59db-125"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Company</span></span>
</dt> <dd>

<span data-ttu-id="d59db-126">Der Name des Unternehmens.</span><span class="sxs-lookup"><span data-stu-id="d59db-126">The name of the company.</span></span> <span data-ttu-id="d59db-127">Ein leeres Feld (ein NULL-Wert) gibt an, dass diese Zeile eine der standardmetadateneigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="d59db-127">An empty field (a Null value) indicates that this row contains one of the standard metadata properties.</span></span> <span data-ttu-id="d59db-128">Ein Unternehmen kann den Eigenschaften Satz erweitern, indem er der Tabelle eine Zeile hinzufügt und einen Firmennamen in dieses Feld eingeben.</span><span class="sxs-lookup"><span data-stu-id="d59db-128">A company can extend the property set by adding a row to the table, and entering a company name in this field.</span></span>

</dd> <dt>

<span data-ttu-id="d59db-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span><span class="sxs-lookup"><span data-stu-id="d59db-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="d59db-130">Der Name einer Metadateneigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d59db-130">The name of a metadata property.</span></span> <span data-ttu-id="d59db-131">Die Eigenschaften allowremoval, ManufacturerName, targetproductname, MoreInfoUrl, Display Name, Description und Classification sind in der Tabelle patchmetadata erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d59db-131">The AllowRemoval, ManufacturerName, TargetProductName, MoreInfoURL, DisplayName, Description, and Classification properties are required in the PatchMetadata Table .</span></span> <span data-ttu-id="d59db-132">Dieses Feld muss eine der folgenden standardmetadateneigenschaften enthalten, wenn das Feld "Company" leer ist (ein NULL-Wert).</span><span class="sxs-lookup"><span data-stu-id="d59db-132">This field must contain one of the following standard metadata properties if the Company field is empty (a Null value).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d59db-133">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d59db-133">Property</span></span></th>
<th><span data-ttu-id="d59db-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d59db-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d59db-135">Allowremoval</span><span class="sxs-lookup"><span data-stu-id="d59db-135">AllowRemoval</span></span></td>
<td><span data-ttu-id="d59db-136">Ein ganzzahliger Wert, der angibt, ob der Patch ein <a href="uninstallable-patches.md">nicht installier barer Patch</a>ist.</span><span class="sxs-lookup"><span data-stu-id="d59db-136">An integer value that indicates whether or not the patch is an <a href="uninstallable-patches.md">Uninstallable Patch</a>.</span></span> <span data-ttu-id="d59db-137">Wenn das Wertfeld einen Wert von 0 (null) enthält, kann der Patch nicht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="d59db-137">If the Value field contains a 0 (zero), the patch cannot be removed.</span></span> <span data-ttu-id="d59db-138">Wenn das Wertfeld 1 (eins) enthält, ist der Patch ein nicht installier barer Patch.</span><span class="sxs-lookup"><span data-stu-id="d59db-138">If the Value field contains 1 (one), the patch is an Uninstallable Patch.</span></span> <span data-ttu-id="d59db-139">Diese Eigenschaft ist erforderlich. Diese Eigenschaft ist registriert, und ihr Wert kann mithilfe der Funktion " <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>msigetpatchinfoex</strong></a> " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d59db-139">This property is required.This property is registered and its value can be obtain by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d59db-140">ManufacturerName</span><span class="sxs-lookup"><span data-stu-id="d59db-140">ManufacturerName</span></span></td>
<td><span data-ttu-id="d59db-141">Ein Zeichen folgen Wert, der den Namen des Herstellers der Anwendung enthält.</span><span class="sxs-lookup"><span data-stu-id="d59db-141">A string value that contains the name of the manufacturer of the application.</span></span> <span data-ttu-id="d59db-142">Diese Eigenschaft ist obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="d59db-142">This property is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d59db-143">Minorupdatetargetrtm</span><span class="sxs-lookup"><span data-stu-id="d59db-143">MinorUpdateTargetRTM</span></span></td>
<td><span data-ttu-id="d59db-144">Gibt an, dass der Patch die RTM-Version des Produkts oder den neuesten wichtigen Upgradepatch als Ziel hat.</span><span class="sxs-lookup"><span data-stu-id="d59db-144">Indicates that the patch targets the RTM version of the product or the most recent major upgrade patch.</span></span> <span data-ttu-id="d59db-145">Erstellen Sie diese optionale Eigenschaft in hilfsupgradepatches, die Sequenz Informationen enthalten, um anzugeben, dass der Patch alle Patches bis zur RTM-Version des Produkts entfernt hat, oder bis zum neuesten wichtigen Upgradepatch.</span><span class="sxs-lookup"><span data-stu-id="d59db-145">Author this optional property in minor upgrade patches that contain sequencing information to indicate that the patch removes of all patches up to the RTM version of the product, or up to the most recent major upgrade patch.</span></span> <span data-ttu-id="d59db-146">Diese Eigenschaft ist ab Windows Installer 3,1 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d59db-146">This property is available beginning with Windows Installer 3.1.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="d59db-147">Legen Sie die Eigenschaft Minimum Requirements dmsiversion in der <a href="properties-table-patchwiz-dll-.md">Tabelle Properties</a> der PCP-Datei auf 310 fest, damit Windows Installer 3,1 installiert werden muss, damit der Patch angewendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d59db-147">To require that Windows Installer 3.1 be installed to apply the patch, set the MinimumRequiredMsiVersion property to 310 in the <a href="properties-table-patchwiz-dll-.md">Properties Table</a> of the .pcp file.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d59db-148">Targetproductname</span><span class="sxs-lookup"><span data-stu-id="d59db-148">TargetProductName</span></span></td>
<td><span data-ttu-id="d59db-149">Ein Zeichen folgen Wert, der den Namen der Anwendung oder der Ziel Anwendungssuite enthält.</span><span class="sxs-lookup"><span data-stu-id="d59db-149">A string value that contains the name of the application or target application suite.</span></span> <span data-ttu-id="d59db-150">Diese Eigenschaft ist obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="d59db-150">This property is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d59db-151">MoreInfoUrl</span><span class="sxs-lookup"><span data-stu-id="d59db-151">MoreInfoURL</span></span></td>
<td><span data-ttu-id="d59db-152">Ein Zeichen folgen Wert, der eine URL enthält, die auf Informationen für diesen Patch zeigt.</span><span class="sxs-lookup"><span data-stu-id="d59db-152">A string value that contains a URL pointing to information for this patch.</span></span> <span data-ttu-id="d59db-153">Diese erforderliche Eigenschaft ist registriert, und ihr Wert kann mithilfe der Funktion " <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>msigetpatchinfoex</strong></a> " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d59db-153">This required property is registered and its value can be obtained by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <span data-ttu-id="d59db-154">Ab Windows XP mit Service Pack 2 (SP2) kann dieser Wert der Support-Link für den in Software angezeigte Patch sein.</span><span class="sxs-lookup"><span data-stu-id="d59db-154">Beginning with Windows XP with Service Pack 2 (SP2), this value can be the support link for the patch displayed in Add/Remove Programs.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d59db-155">"Kreationtimeutc"</span><span class="sxs-lookup"><span data-stu-id="d59db-155">CreationTimeUTC</span></span></td>
<td><span data-ttu-id="d59db-156">Ein Zeichen folgen Wert, der die Erstellungszeit der MSP-Datei im Format mm-dd-yy HH: mm (month-day-year Hour: Minute) enthält.</span><span class="sxs-lookup"><span data-stu-id="d59db-156">A string value that contains the creation time of the .msp file in the form mm-dd-yy HH:MM (month-day-year hour:minute).</span></span> <span data-ttu-id="d59db-157">Diese Eigenschaft ist optional.</span><span class="sxs-lookup"><span data-stu-id="d59db-157">This property is optional.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d59db-158">DisplayName</span><span class="sxs-lookup"><span data-stu-id="d59db-158">DisplayName</span></span></td>
<td><span data-ttu-id="d59db-159">Ein Zeichen folgen Wert, der den Titel für den Patch enthält, der für die öffentliche Anzeige geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="d59db-159">A string value that contains the title for the patch that is suitable for public display.</span></span> <span data-ttu-id="d59db-160">Diese Eigenschaft ist obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="d59db-160">This property is required.</span></span> <span data-ttu-id="d59db-161">Diese Eigenschaft ist registriert, und ihr Wert kann mithilfe der Funktion " <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>msigetpatchinfoex</strong></a> " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d59db-161">This property is registered and its value can be obtain by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <span data-ttu-id="d59db-162">Ab Windows XP mit SP2 ist dieser Wert der Name des Patches, der ab Windows XP mit SP2 unter "Programme hinzufügen/entfernen" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d59db-162">Beginning with Windows XP with SP2, this value is the name of the patch displayed in Add/Remove Programs beginning with Windows XP with SP2.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d59db-163">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d59db-163">Description</span></span></td>
<td><span data-ttu-id="d59db-164">Ein Zeichen folgen Wert, der eine kurze Beschreibung des Patches enthält.</span><span class="sxs-lookup"><span data-stu-id="d59db-164">A string value that contains a brief description of the patch.</span></span> <span data-ttu-id="d59db-165">Diese Eigenschaft ist obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="d59db-165">This property is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d59db-166">Klassifizierung</span><span class="sxs-lookup"><span data-stu-id="d59db-166">Classification</span></span></td>
<td><span data-ttu-id="d59db-167">Ein Zeichen folgen Wert, der die beliebige Kategorie von Updates enthält, wie vom Autor des Patches definiert.</span><span class="sxs-lookup"><span data-stu-id="d59db-167">A string value that contains the arbitrary category of updates as defined by the author of the patch.</span></span> <span data-ttu-id="d59db-168">Beispielsweise können patchautoren angeben, dass jeder Patch als Hotfix, Sicherheitsrollup, wichtiges Update, Update, Service Pack oder Updaterollup klassifiziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d59db-168">For example, patch authors can specify that each patch be classified as a Hotfix, Security Rollup, Critical Update, Update, Service Pack, or Update Rollup.</span></span> <span data-ttu-id="d59db-169">Diese Eigenschaft ist obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="d59db-169">This property is required.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d59db-170">OptimizedInstallMode</span><span class="sxs-lookup"><span data-stu-id="d59db-170">OptimizedInstallMode</span></span></td>
<td><span data-ttu-id="d59db-171">Wenn diese Eigenschaft in allen Patches, die in einer Transaktion angewendet werden sollen, auf 1 (eins) festgelegt ist, wird die Anwendung des Patches nach Möglichkeit optimiert.</span><span class="sxs-lookup"><span data-stu-id="d59db-171">If this property is set to 1 (one) in all the patches to be applied in a transaction, the application of the patch is optimized if possible.</span></span> <span data-ttu-id="d59db-172">Weitere Informationen finden Sie unter <a href="patch-optimization.md">Patch Optimization</a>.</span><span class="sxs-lookup"><span data-stu-id="d59db-172">For information, see <a href="patch-optimization.md">Patch Optimization</a>.</span></span> <span data-ttu-id="d59db-173">Verfügbar ab Windows Installer 3,1.</span><span class="sxs-lookup"><span data-stu-id="d59db-173">Available beginning with Windows Installer 3.1.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="d59db-174"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert</span><span class="sxs-lookup"><span data-stu-id="d59db-174"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="d59db-175">Der Wert der Metadateneigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d59db-175">Value of the metadata property.</span></span> <span data-ttu-id="d59db-176">Dies kann niemals NULL oder eine leere Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="d59db-176">This can never be Null or an empty string.</span></span> <span data-ttu-id="d59db-177">Dieser Wert kann lokalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d59db-177">This value can be localized.</span></span>

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="d59db-178">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d59db-178">Remarks</span></span>

<span data-ttu-id="d59db-179">Verfügbar ab Windows Installer 3,0.</span><span class="sxs-lookup"><span data-stu-id="d59db-179">Available beginning in Windows Installer 3.0.</span></span>

<span data-ttu-id="d59db-180">Alle Eigenschaften, die in der Tabelle patchmetadata erstellt wurden, werden der MsiPatchMetadata-Tabelle der MSP-Datei hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d59db-180">All properties authored into the PatchMetadata Table are added to the MsiPatchMetadata table of the msp file.</span></span> <span data-ttu-id="d59db-181">Die Eigenschaften "allowremoval", "MoreInfoUrl" und "Display Name" sind registriert und können über " [**msigetpatchinfoex**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)" aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d59db-181">AllowRemoval, MoreInfoURL and DisplayName properties are registered and are accessible through the [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).</span></span>

 

 




