---
description: Die MsiPatchMetadata-Tabelle enthält Informationen zu einem Windows Installer Patch, der erforderlich ist, um den Patch zu entfernen, und der von "Software" verwendet wird.
ms.assetid: b1c30e16-6c91-451a-8b75-7ddbcefcc092
title: MsiPatchMetadata-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2642661a8f9dc067086926f8e993fc32c95a4a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350159"
---
# <a name="msipatchmetadata-table"></a><span data-ttu-id="a7bd2-103">MsiPatchMetadata-Tabelle</span><span class="sxs-lookup"><span data-stu-id="a7bd2-103">MsiPatchMetadata Table</span></span>

<span data-ttu-id="a7bd2-104">Die MsiPatchMetadata-Tabelle enthält Informationen zu einem Windows Installer Patch, der erforderlich ist, um den Patch zu entfernen, und **der von "** Software" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-104">The MsiPatchMetadata Table contains information about a Windows Installer patch that is required to remove the patch and that is used by **Add/Remove Programs**.</span></span>

<span data-ttu-id="a7bd2-105">Patches, die ohne diese Tabelle in der Patchdatenbank (MSP-Datei) installiert werden, können nicht entfernt werden, und es fehlen **Informationen von Software**.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-105">Patches installed without this table present in the patch database (.msp file) cannot be removed, and are missing some information from **Add/Remove Programs**.</span></span> <span data-ttu-id="a7bd2-106">Die Tabelle muss sich in der Datenbank der Patchdatei befinden und nicht in einer Transformation im Patch.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-106">The table must be in the database of the patch file and not in a transform in the patch.</span></span>

<span data-ttu-id="a7bd2-107">Die MsiPatchMetadata-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-107">The MsiPatchMetadata Table has the following columns.</span></span>



| <span data-ttu-id="a7bd2-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="a7bd2-108">Column</span></span>   | <span data-ttu-id="a7bd2-109">Typ</span><span class="sxs-lookup"><span data-stu-id="a7bd2-109">Type</span></span>                         | <span data-ttu-id="a7bd2-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="a7bd2-110">Key</span></span> | <span data-ttu-id="a7bd2-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="a7bd2-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="a7bd2-112">Company</span><span class="sxs-lookup"><span data-stu-id="a7bd2-112">Company</span></span>  | [<span data-ttu-id="a7bd2-113">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="a7bd2-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="a7bd2-114">J</span><span class="sxs-lookup"><span data-stu-id="a7bd2-114">Y</span></span>   | <span data-ttu-id="a7bd2-115">J</span><span class="sxs-lookup"><span data-stu-id="a7bd2-115">Y</span></span>        |
| <span data-ttu-id="a7bd2-116">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a7bd2-116">Property</span></span> | [<span data-ttu-id="a7bd2-117">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="a7bd2-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="a7bd2-118">J</span><span class="sxs-lookup"><span data-stu-id="a7bd2-118">Y</span></span>   | <span data-ttu-id="a7bd2-119">N</span><span class="sxs-lookup"><span data-stu-id="a7bd2-119">N</span></span>        |
| <span data-ttu-id="a7bd2-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a7bd2-120">Value</span></span>    | [<span data-ttu-id="a7bd2-121">Text</span><span class="sxs-lookup"><span data-stu-id="a7bd2-121">Text</span></span>](text.md)             | <span data-ttu-id="a7bd2-122">N</span><span class="sxs-lookup"><span data-stu-id="a7bd2-122">N</span></span>   | <span data-ttu-id="a7bd2-123">N</span><span class="sxs-lookup"><span data-stu-id="a7bd2-123">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="a7bd2-124">Spalten</span><span class="sxs-lookup"><span data-stu-id="a7bd2-124">Columns</span></span>

<dl> <dt>

<span data-ttu-id="a7bd2-125"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Geschäfts</span><span class="sxs-lookup"><span data-stu-id="a7bd2-125"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Company</span></span>
</dt> <dd>

<span data-ttu-id="a7bd2-126">Der Name des Unternehmens.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-126">The name of the company.</span></span> <span data-ttu-id="a7bd2-127">Ein leeres Feld (ein NULL-Wert) gibt an, dass die Zeile eine der standardmetadateneigenschaften der Windows Installer enthält.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-127">An empty field (a Null value) indicates that the row contains one of the standard metadata properties of the Windows Installer.</span></span> <span data-ttu-id="a7bd2-128">Weitere Informationen finden Sie im Abschnitt "Hinweise" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-128">For more information, see the Remarks section of this topic.</span></span>

<span data-ttu-id="a7bd2-129">Wenn Sie der Tabelle eine Zeile hinzufügen und einen Firmennamen in dieses Feld eingeben, können Sie ein beliebiges Unternehmen hinzufügen, um den Eigenschaften Satz zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-129">By adding a row to the table and entering a company name in this field, you can add any company to extend the property set.</span></span>

</dd> <dt>

<span data-ttu-id="a7bd2-130"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span><span class="sxs-lookup"><span data-stu-id="a7bd2-130"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="a7bd2-131">Der Name einer Metadateneigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-131">The name of a metadata property.</span></span>

</dd> <dt>

<span data-ttu-id="a7bd2-132"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert</span><span class="sxs-lookup"><span data-stu-id="a7bd2-132"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="a7bd2-133">Der Wert der Metadateneigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-133">The value of the metadata property.</span></span> <span data-ttu-id="a7bd2-134">Dies kann niemals NULL oder eine leere Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-134">This can never be Null or an empty string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7bd2-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7bd2-135">Remarks</span></span>

<span data-ttu-id="a7bd2-136">Verfügbar in Windows Installer 3,0 und höher.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-136">Available in Windows Installer 3.0 and later.</span></span>

<span data-ttu-id="a7bd2-137">Zeilen in der MsiPatchMetadata-Tabelle, die einen NULL-Wert im Feld "Unternehmenname" enthalten, verweisen auf eine der folgenden Standard-Windows Installer Metadateneigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-137">Rows in the MsiPatchMetadata Table that contain a Null value in the CompanyName field refer to one of the following standard Windows Installer metadata properties.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a7bd2-138">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a7bd2-138">Property</span></span></th>
<th><span data-ttu-id="a7bd2-139">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a7bd2-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a7bd2-140">Allowremoval</span><span class="sxs-lookup"><span data-stu-id="a7bd2-140">AllowRemoval</span></span></td>
<td><span data-ttu-id="a7bd2-141">Gibt an, ob der Patch ein <a href="uninstallable-patches.md">nicht installier barer Patch</a>ist.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-141">Indicates whether or not the patch is an <a href="uninstallable-patches.md">Uninstallable Patch</a>.</span></span> <span data-ttu-id="a7bd2-142">Wenn das Wertfeld 0 (null) enthält, kann der Patch nicht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-142">If the value field contains 0 (zero), the patch cannot be removed.</span></span> <span data-ttu-id="a7bd2-143">Wenn das Wertfeld eins (1) enthält, ist der Patch ein nicht installier barer Patch. diese Eigenschaft wird registriert, und ihr Wert kann mithilfe der Funktion " <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>msigetpatchinfoex</strong></a> " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-143">If the value field contains one (1), the patch is an Uninstallable Patch.This property is registered and its value can be obtain by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7bd2-144">ManufacturerName</span><span class="sxs-lookup"><span data-stu-id="a7bd2-144">ManufacturerName</span></span></td>
<td><span data-ttu-id="a7bd2-145">Der Name des Herstellers der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-145">Name of the manufacturer of the application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7bd2-146">Minorupdatetargetrtm</span><span class="sxs-lookup"><span data-stu-id="a7bd2-146">MinorUpdateTargetRTM</span></span></td>
<td><span data-ttu-id="a7bd2-147">Gibt an, dass der Patch die RTM-Version des Produkts oder den neuesten wichtigen Upgradepatch als Ziel hat.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-147">Indicates that the patch targets the RTM version of the product or the most recent major upgrade patch.</span></span> <span data-ttu-id="a7bd2-148">Erstellen Sie diese optionale Eigenschaft in hilfsupgradepatches, die Sequenz Informationen enthalten, um anzugeben, dass der Patch alle Patches bis zur RTM-Version des Produkts entfernt hat, oder bis zum neuesten wichtigen Upgradepatch.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-148">Author this optional property in minor upgrade patches that contain sequencing information to indicate that the patch removes of all patches up to the RTM version of the product, or up to the most recent major upgrade patch.</span></span> <span data-ttu-id="a7bd2-149">Diese Eigenschaft ist in Windows Installer 3,1 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-149">This property is available in Windows Installer 3.1 and later.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7bd2-150">Targetproductname</span><span class="sxs-lookup"><span data-stu-id="a7bd2-150">TargetProductName</span></span></td>
<td><span data-ttu-id="a7bd2-151">Der Name der Anwendungs-oder Ziel Anwendungssuite.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-151">Name of the application or target application suite.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7bd2-152">MoreInfoUrl</span><span class="sxs-lookup"><span data-stu-id="a7bd2-152">MoreInfoURL</span></span></td>
<td><span data-ttu-id="a7bd2-153">Eine URL, die für diesen Patch spezifische Informationen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-153">A URL that provides information specific to this patch.</span></span> <span data-ttu-id="a7bd2-154">Diese Eigenschaft ist registriert, und ihr Wert kann mithilfe der Funktion " <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>msigetpatchinfoex</strong></a> " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-154">This property is registered and its value can be obtained by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <span data-ttu-id="a7bd2-155">Ab Windows XP mit Service Pack 2 (SP2) kann dieser Wert der Support-Link für <strong>den in Software</strong>angezeigte Patch sein.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-155">Beginning with Windows XP with Service Pack 2 (SP2), this value can be the support link for the patch displayed in <strong>Add/Remove Programs</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7bd2-156">"Kreationtimeutc"</span><span class="sxs-lookup"><span data-stu-id="a7bd2-156">CreationTimeUTC</span></span></td>
<td><span data-ttu-id="a7bd2-157">Erstellungszeit der MSP-Datei im Format mm-dd-yy HH: mm (month-day-year Hour: Minute).</span><span class="sxs-lookup"><span data-stu-id="a7bd2-157">Creation time of the .msp file in the form of mm-dd-yy HH:MM (month-day-year hour:minute).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7bd2-158">DisplayName</span><span class="sxs-lookup"><span data-stu-id="a7bd2-158">DisplayName</span></span></td>
<td><span data-ttu-id="a7bd2-159">Ein Titel für den Patch, der für die öffentliche Anzeige geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-159">A title for the patch that is okay for public display.</span></span> <span data-ttu-id="a7bd2-160">Diese Eigenschaft ist registriert, und ihr Wert kann mithilfe der Funktion " <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>msigetpatchinfoex</strong></a> " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-160">This property is registered, and its value can be obtained by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <span data-ttu-id="a7bd2-161">Ab Windows XP mit SP2 ist dieser Wert der Name des Patches, der unter "Software" angezeigt <strong>wird.</strong></span><span class="sxs-lookup"><span data-stu-id="a7bd2-161">Beginning with Windows XP with SP2, this value is the name of the patch that is displayed in <strong>Add/Remove Programs</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7bd2-162">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a7bd2-162">Description</span></span></td>
<td><span data-ttu-id="a7bd2-163">Kurze Beschreibung des Patches.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-163">Brief description of the patch.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7bd2-164">Klassifizierung</span><span class="sxs-lookup"><span data-stu-id="a7bd2-164">Classification</span></span></td>
<td><span data-ttu-id="a7bd2-165">Ein Zeichen folgen Wert, der die beliebige Kategorie von Updates enthält, wie vom Autor des Patches definiert.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-165">A string value that contains the arbitrary category of updates as defined by the author of the patch.</span></span> <span data-ttu-id="a7bd2-166">Beispielsweise können patchautoren angeben, dass jeder Patch als Hotfix, Sicherheitsrollup, wichtiges Update, Update, Service Pack oder Updaterollup klassifiziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-166">For example, patch authors can specify that each patch be classified as a Hotfix, Security Rollup, Critical Update, Update, Service Pack, or Update Rollup.</span></span> <span data-ttu-id="a7bd2-167">Diese Eigenschaft ist obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-167">This property is required.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7bd2-168">Optimizeca</span><span class="sxs-lookup"><span data-stu-id="a7bd2-168">OptimizeCA</span></span></td>
<td><span data-ttu-id="a7bd2-169">Gibt an, ob die Windows Installer beim Anwenden des Patches benutzerdefinierte Aktionen überspringen soll.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-169">Indicates whether the Windows Installer should skip custom actions when applying the patch.</span></span> <span data-ttu-id="a7bd2-170">Dadurch kann die Zeit, die zum Anwenden des Patches erforderlich ist, reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-170">This can reduce the time required to apply the patch.</span></span> <span data-ttu-id="a7bd2-171">Die optimizeca-Eigenschaft kann einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="a7bd2-171">The OptimizeCA property can have one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="a7bd2-172">0-keine benutzerdefinierten Aktionen überspringen.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-172">0 - Do not skip any custom actions.</span></span></li>
<li><span data-ttu-id="a7bd2-173">1-überspringen Sie benutzerdefinierte Aktionen für die Eigenschaft und Verzeichnis Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-173">1 - Skip property and directory assignment custom actions.</span></span> <span data-ttu-id="a7bd2-174">Der benutzerdefinierte <a href="custom-action-type-35.md">Aktionstyp 35</a> und der <a href="custom-action-type-51.md">benutzerdefinierte Aktionstyp 51</a> können benutzerdefinierte Aktionen der Eigenschaft und Verzeichnis Zuweisung sein.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-174"><a href="custom-action-type-35.md">Custom Action Type 35</a> and <a href="custom-action-type-51.md">Custom Action Type 51</a> can be property and directory assignment custom actions.</span></span></li>
<li><span data-ttu-id="a7bd2-175">2: überspringen Sie unmittelbare benutzerdefinierte Aktionen, die nicht in die Eigenschaften-oder Verzeichnis Zuweisungen fallen.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-175">2 - Skip immediate custom actions that do not fall into the property or directory assignments.</span></span> <span data-ttu-id="a7bd2-176">Die benutzerdefinierten Aktionen enthalten in der Type-Spalte der <a href="customaction-table.md">CustomAction-Tabelle</a>nicht die msidbcustomaction typeinscript-Option.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-176">The immediate custom actions do not include msidbCustomActionTypeInScript option in the Type column of the <a href="customaction-table.md">CustomAction Table</a>.</span></span></li>
<li><span data-ttu-id="a7bd2-177">4: überspringen Sie benutzerdefinierte Aktionen, die im Skript ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-177">4 - Skip custom actions that run within the script.</span></span></li>
</ul>
<span data-ttu-id="a7bd2-178">Der Wert von optimizeca muss für alle Patches, die installiert werden, identisch sein, oder es werden keine benutzerdefinierten Aktionen übersprungen.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-178">The value of OptimizeCA must be the same for all patches that are being installed or no custom actions are skipped.</span></span> <span data-ttu-id="a7bd2-179">Wenn beispielsweise zwei Patches installiert werden und optimizeca auf die Werte 1 und 2 festgelegt ist, werden keine benutzerdefinierten Aktionen übersprungen.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-179">For example, if two patches are being installed, and OptimizeCA is set to the values 1 and 2 respectively, no custom actions are skipped.</span></span> <br/> <span data-ttu-id="a7bd2-180">Die Werte von optimizeca können kombiniert werden, wenn mehrere neue Patches verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-180">The values of OptimizeCA can be combined when processing multiple new patches.</span></span> <span data-ttu-id="a7bd2-181">Wenn alle Patches über eine (eins) in den Werten verfügen, werden alle benutzerdefinierten Aktionen der Eigenschaft und Verzeichnis Zuweisung übersprungen.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-181">If all patches have a 1 (one) included in the values, then all property and directory assignment custom actions are skipped.</span></span> <span data-ttu-id="a7bd2-182">Wenn ein Patch den Wert 3 (drei) für die-Eigenschaft aufweist und ein Patch den Wert 1 (eins) für die-Eigenschaft aufweist, werden die benutzerdefinierten Eigenschaften und Verzeichnis Zuweisungs Aktionen übersprungen.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-182">If one patch has the value 3 (three)for the property, and one patch has the value 1 (one) for the property, the property and directory assignment custom actions are skipped.</span></span> <span data-ttu-id="a7bd2-183">Die anderen unmittelbaren benutzerdefinierten Aktionen werden jedoch ausgeführt, da nicht alle angeforderten Patches übersprungen werden.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-183">However, the other immediate custom actions run, because not all of the patches requested are skipped.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7bd2-184">OptimizedInstallMode</span><span class="sxs-lookup"><span data-stu-id="a7bd2-184">OptimizedInstallMode</span></span></td>
<td><span data-ttu-id="a7bd2-185">Wenn diese Eigenschaft in allen Patches, die in einer Transaktion angewendet werden sollen, auf 1 (eins) festgelegt ist, wird nach Möglichkeit eine Anwendung des Patches optimiert.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-185">If this property is set to 1 (one) in all the patches to be applied in a transaction, an application of the patch is optimized if possible.</span></span> <span data-ttu-id="a7bd2-186">Weitere Informationen finden Sie unter <a href="patch-optimization.md">Patch Optimization</a>.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-186">For more information, see <a href="patch-optimization.md">Patch Optimization</a>.</span></span> <span data-ttu-id="a7bd2-187">Verfügbar ab Windows Installer 3,1.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-187">Available beginning with Windows Installer 3.1.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="validation"></a><span data-ttu-id="a7bd2-188">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="a7bd2-188">Validation</span></span>

<dl>

[<span data-ttu-id="a7bd2-189">ICE03</span><span class="sxs-lookup"><span data-stu-id="a7bd2-189">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="a7bd2-190">ICE06</span><span class="sxs-lookup"><span data-stu-id="a7bd2-190">ICE06</span></span>](ice06.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="a7bd2-191">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a7bd2-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7bd2-192">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a7bd2-192">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




