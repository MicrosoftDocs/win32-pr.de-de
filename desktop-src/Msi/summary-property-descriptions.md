---
description: In den folgenden Tabellen werden die Zusammenfassungs Eigenschaften für Installationspakete, Transformationen und Patches beschrieben.
ms.assetid: b44b24b7-7fc4-4c3c-9d10-7e2f3c43cf36
title: Beschreibungen der Zusammenfassungs Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41addb58571b6d18e1cccc4a34c3026f3d0544cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352552"
---
# <a name="summary-property-descriptions"></a><span data-ttu-id="7cb4c-103">Beschreibungen der Zusammenfassungs Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7cb4c-103">Summary Property Descriptions</span></span>

<span data-ttu-id="7cb4c-104">In den folgenden Tabellen werden die Zusammenfassungs Eigenschaften für Installationspakete, Transformationen und Patches beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-104">Summary properties for installation packages, transforms, and patches are described in the following tables.</span></span> <span data-ttu-id="7cb4c-105">Beachten Sie, dass die Bedeutung einer bestimmten Zusammenfassungs Eigenschaft je nachdem, ob die Datenbank zu einem Installationspaket, einer Transformation oder einem Patchpaket gehört, unterschiedlich sein kann.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-105">Note that the meaning of a particular summary property can be different depending on whether the database belongs to an installation package, transform, or patch package.</span></span> <span data-ttu-id="7cb4c-106">Weitere Informationen zu den Eigenschaften-IDs, PIDs und Typen finden Sie unter [Summary Information Stream-Eigenschaften Satz](summary-information-stream-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="7cb4c-106">For more information about the property IDs, PIDs, and types, see [Summary Information Stream Property Set](summary-information-stream-property-set.md).</span></span>

## <a name="installation-packages"></a><span data-ttu-id="7cb4c-107">Installationspakete</span><span class="sxs-lookup"><span data-stu-id="7cb4c-107">Installation Packages</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7cb4c-108">Summary-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7cb4c-108">Summary property</span></span></th>
<th><span data-ttu-id="7cb4c-109">Bedeutung dieser Eigenschaft in einer Installations Datenbank</span><span class="sxs-lookup"><span data-stu-id="7cb4c-109">Meaning of this property in an Installation database</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7cb4c-110"><a href="title-summary.md"><strong>Titel</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cb4c-110"><a href="title-summary.md"><strong>Title</strong></a></span></span></td>
<td><span data-ttu-id="7cb4c-111">Eine Beschreibung dieser Datei als Installationspaket.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-111">A description of this file as an installation package.</span></span> <span data-ttu-id="7cb4c-112">Die Beschreibung sollte den Begriff &quot; <a href="about-the-installer-database.md">Installations Datenbank</a>enthalten.&quot;</span><span class="sxs-lookup"><span data-stu-id="7cb4c-112">The description should include the phrase &quot;<a href="about-the-installer-database.md">Installation Database</a>.&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cb4c-113"><a href="subject-summary.md"><strong>Subject</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cb4c-113"><a href="subject-summary.md"><strong>Subject</strong></a></span></span></td>
<td><span data-ttu-id="7cb4c-114">Der Name des Produkts, das von diesem Paket installiert wird.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-114">The name of the product installed by this package.</span></span> <span data-ttu-id="7cb4c-115">Dabei sollte es sich um den gleichen Namen wie in der <a href="productname.md"><strong>ProductName</strong></a> -Eigenschaft handeln.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-115">This should be the same name as in the <a href="productname.md"><strong>ProductName</strong></a> property.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cb4c-116"><a href="author-summary.md"><strong>Autor</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cb4c-116"><a href="author-summary.md"><strong>Author</strong></a></span></span></td>
<td><span data-ttu-id="7cb4c-117">Der Name des Herstellers dieses Produkts.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-117">The name of the manufacturer of this product.</span></span> <span data-ttu-id="7cb4c-118">Dabei sollte es sich um den gleichen Namen wie in der <a href="manufacturer.md"><strong>Hersteller</strong></a> Eigenschaft handeln.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-118">This should be the same name as in the <a href="manufacturer.md"><strong>Manufacturer</strong></a> property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cb4c-119"><a href="keywords-summary.md"><strong>Keywords</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cb4c-119"><a href="keywords-summary.md"><strong>Keywords</strong></a></span></span></td>
<td><span data-ttu-id="7cb4c-120">Eine Liste von Schlüsselwörtern, die von Datei Browsern verwendet werden können, um nach einer Datei zu suchen.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-120">A list of keywords that may be used by file browsers to do keyword searches for a file.</span></span> <span data-ttu-id="7cb4c-121">Die Schlüsselwörter sollten &quot; &quot; sowohl Installer als auch produktspezifische Schlüsselwörter enthalten.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-121">The keywords should include &quot;Installer&quot; as well as product-specific keywords.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cb4c-122"><a href="comments-summary.md"><strong>Kommentare</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cb4c-122"><a href="comments-summary.md"><strong>Comments</strong></a></span></span></td>
<td><span data-ttu-id="7cb4c-123">Enthält den Ausdruck: &quot; Diese Installerdatenbank enthält die Logik und die Daten, die erforderlich sind, um <<em>Produktnamen</em>zu installieren > .&quot;</span><span class="sxs-lookup"><span data-stu-id="7cb4c-123">Contains the phrase: &quot;This installer database contains the logic and data required to install <<em>product name</em>>.&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cb4c-124"><a href="template-summary.md"><strong>Vorlage</strong></a> (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="7cb4c-124"><a href="template-summary.md"><strong>Template</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="7cb4c-125">Die Plattform und die Sprachen, die mit diesem Installationspaket kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-125">The platform and languages compatible with this installation package.</span></span> <span data-ttu-id="7cb4c-126">Die Syntax finden Sie unter <a href="template-summary.md"><strong>Template</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7cb4c-126">See <a href="template-summary.md"><strong>Template</strong></a> for syntax.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cb4c-127"><a href="last-saved-by-summary.md"><strong>Zuletzt gespeichert von</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cb4c-127"><a href="last-saved-by-summary.md"><strong>Last Saved By</strong></a></span></span></td>
<td><span data-ttu-id="7cb4c-128">Entwickler von Tools zur Datenbankbearbeitung können diese Eigenschaft während des Entwicklungsprozesses verwenden, um die letzte Person zum Ändern der Installations Datenbank zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-128">Developers of database editing tools may use this property during the development process to track the last person to modify the installation database.</span></span> <span data-ttu-id="7cb4c-129">Diese Eigenschaft sollte in einer abschließenden Versand Datenbank auf NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-129">This property should be set to Null in a final shipping database.</span></span> <span data-ttu-id="7cb4c-130">Diese Eigenschaft wird von dem Installer während einer <a href="administrative-installation.md"><strong>administrativen Installation</strong></a>auf den Wert der <a href="logonuser.md"><strong>LogonUser</strong></a> -Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-130">The installer sets this property to the value of the <a href="logonuser.md"><strong>LogonUser</strong></a> property during an <a href="administrative-installation.md"><strong>administrative installation</strong></a>.</span></span> <span data-ttu-id="7cb4c-131">Das Installationsprogramm verwendet diese Eigenschaft nie, und ein Benutzer muss Sie nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-131">The installer never uses this property and a user never needs to modify it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cb4c-132"><a href="revision-number-summary.md"><strong>Revisionsnummer</strong></a> (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="7cb4c-132"><a href="revision-number-summary.md"><strong>Revision Number</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="7cb4c-133">Enthält den <a href="package-codes.md">Paket Code</a> für das Installer-Paket.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-133">Contains the <a href="package-codes.md">package code</a> for the installer package.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cb4c-134"><a href="last-printed-summary.md"><strong>Zuletzt gedruckt</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cb4c-134"><a href="last-printed-summary.md"><strong>Last Printed</strong></a></span></span></td>
<td><span data-ttu-id="7cb4c-135">Kann auf das Datum und die Uhrzeit während einer <a href="administrative-installation.md">administrativen Installation</a> festgelegt werden, um aufzuzeichnen, wann das administrative Image erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-135">May be set to the date and time during an <a href="administrative-installation.md">administrative installation</a> to record when the administrative image was created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cb4c-136"><a href="create-time-date-summary.md"><strong>Uhrzeit/Datum erstellen</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cb4c-136"><a href="create-time-date-summary.md"><strong>Create Time/Date</strong></a></span></span></td>
<td><span data-ttu-id="7cb4c-137">Das Datum und die Uhrzeit, zu der die Installer-Datenbank erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-137">The time and date when this installer database was created.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cb4c-138"><a href="last-saved-time-date-summary.md"><strong>Letzte gespeicherte Uhrzeit/Datum</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cb4c-138"><a href="last-saved-time-date-summary.md"><strong>Last Saved Time/Date</strong></a></span></span></td>
<td><span data-ttu-id="7cb4c-139">Die aktuelle Systemzeit und das aktuelle Datum zum Zeitpunkt der letzten Speicherung der Installer-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-139">The current system time and date at the time the installer database was last saved.</span></span> <span data-ttu-id="7cb4c-140">Anfänglich NULL.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-140">Initially null.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cb4c-141"><a href="page-count-summary.md"><strong>Seitenanzahl</strong></a> (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="7cb4c-141"><a href="page-count-summary.md"><strong>Page Count</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="7cb4c-142">Enthält einen Wert, der verwendet wird, um die für dieses Installationspaket erforderliche mindestinstallerversion zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-142">Contains a value used to identify the minimum installer version required by this installation package.</span></span> <span data-ttu-id="7cb4c-143">Wenn das Paket z. b. mindestens die Version 2,0 des Installers erfordert, sollte diese Eigenschaft auf eine ganze Zahl 200 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-143">For example, if the package requires at minimum the 2.0 version of the installer, this property should be set to an integer of 200.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="7cb4c-144">Der Wert dieser Eigenschaft muss bei <a href="64-bit-windows-installer-packages.md">64-Bit-Windows Installer Paketen</a>200 oder größer sein.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-144">The value of this property must be 200 or greater with <a href="64-bit-windows-installer-packages.md">64-bit Windows Installer Packages</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cb4c-145"><a href="word-count-summary.md"><strong>Wort Anzahl</strong></a> (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="7cb4c-145"><a href="word-count-summary.md"><strong>Word Count</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="7cb4c-146">Der Typ des Quelldatei Bilds.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-146">The type of the source file image.</span></span> <span data-ttu-id="7cb4c-147">Wird anstelle der Standard Count-Eigenschaft gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-147">Stored in place of the standard Count property.</span></span> <span data-ttu-id="7cb4c-148">Diese Eigenschaft ist ein Bitfeld.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-148">This property is a bit field.</span></span> <span data-ttu-id="7cb4c-149">Die Werte finden Sie im Thema <a href="word-count-summary.md"><strong>Wort Anzahl</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7cb4c-149">See the <a href="word-count-summary.md"><strong>Word Count</strong></a> topic for the values.</span></span><br/> <span data-ttu-id="7cb4c-150">Ab Windows Installer Version 4,0 unter Windows Vista schließt diese Eigenschaft Bits ein, um anzugeben, ob erhöhte Rechte erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-150">Starting with Windows Installer version 4.0 on Windows Vista, this property includes bits to specify whether elevated privileges are required.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cb4c-151"><a href="character-count-summary.md"><strong>Zeichen Anzahl</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cb4c-151"><a href="character-count-summary.md"><strong>Character Count</strong></a></span></span></td>
<td><span data-ttu-id="7cb4c-152">Null</span><span class="sxs-lookup"><span data-stu-id="7cb4c-152">Null</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cb4c-153"><a href="creating-application-summary.md"><strong>Anwendung wird erstellt</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cb4c-153"><a href="creating-application-summary.md"><strong>Creating Application</strong></a></span></span></td>
<td><span data-ttu-id="7cb4c-154">Enthält den Namen der Software, mit der diese Installations Datenbank erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-154">Contains the name of the software used to author this installation database.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cb4c-155"><a href="security-summary.md"><strong>Sicherheit</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cb4c-155"><a href="security-summary.md"><strong>Security</strong></a></span></span></td>
<td><span data-ttu-id="7cb4c-156">Der Wert dieser Eigenschaft sollte "2-empfohlen" lauten.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-156">The value of this property should be 2 - Recommended read-only.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cb4c-157"><a href="codepage-summary.md"><strong>Codepage</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cb4c-157"><a href="codepage-summary.md"><strong>Codepage</strong></a></span></span></td>
<td><span data-ttu-id="7cb4c-158">Der numerische Wert der ANSI-Codepage, die verwendet wird, um die Zusammenfassungs Informationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-158">The numeric value of the ANSI code page used to display the Summary Information.</span></span> <span data-ttu-id="7cb4c-159">Diese Eigenschaft muss festgelegt werden, bevor alle Zeichen folgen Eigenschaften in den Zusammenfassungs Informationen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-159">This property must be set before any string properties are set in the summary information.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="transforms"></a><span data-ttu-id="7cb4c-160">Transformationen</span><span class="sxs-lookup"><span data-stu-id="7cb4c-160">Transforms</span></span>



| <span data-ttu-id="7cb4c-161">Summary-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7cb4c-161">Summary property</span></span>                                              | <span data-ttu-id="7cb4c-162">Bedeutung dieser Eigenschaft in einer Transformation</span><span class="sxs-lookup"><span data-stu-id="7cb4c-162">Meaning of this property in a Transform</span></span>                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7cb4c-163">**Titel**</span><span class="sxs-lookup"><span data-stu-id="7cb4c-163">**Title**</span></span>](title-summary.md)                                | <span data-ttu-id="7cb4c-164">Eine Beschreibung dieser Datei als Transformation.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-164">A description of this file as a transform.</span></span> <span data-ttu-id="7cb4c-165">Die Beschreibung sollte den folgenden Ausdruck enthalten: "[Transform](database-transforms.md)".</span><span class="sxs-lookup"><span data-stu-id="7cb4c-165">The description should include the phrase: "[Transform](database-transforms.md)."</span></span>                                                                                                                                                                     |
| [<span data-ttu-id="7cb4c-166">**Subject**</span><span class="sxs-lookup"><span data-stu-id="7cb4c-166">**Subject**</span></span>](subject-summary.md)                            | <span data-ttu-id="7cb4c-167">Der Name des Produkts, das vom ursprünglichen Installationspaket installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-167">The name of the product installed by the original installation package.</span></span> <span data-ttu-id="7cb4c-168">Dabei sollte es sich um den gleichen Wert wie die Eigenschaft " [**betreffzusammenfassung**](subject-summary.md) " im ursprünglichen Installationspaket handeln.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-168">This should be the same value as the [**Subject Summary**](subject-summary.md) property in the original installation package.</span></span>                                                                                            |
| [<span data-ttu-id="7cb4c-169">**Autor**</span><span class="sxs-lookup"><span data-stu-id="7cb4c-169">**Author**</span></span>](author-summary.md)                              | <span data-ttu-id="7cb4c-170">Der Name des Herstellers dieser Transformation.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-170">The name of the manufacturer of this transform.</span></span>                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="7cb4c-171">**Keywords**</span><span class="sxs-lookup"><span data-stu-id="7cb4c-171">**Keywords**</span></span>](keywords-summary.md)                          | <span data-ttu-id="7cb4c-172">Eine Liste von Schlüsselwörtern, die von Datei Browsern verwendet werden können, um nach einer Datei zu suchen.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-172">A list of keywords that may be used by file browsers to do keyword searches for a file.</span></span> <span data-ttu-id="7cb4c-173">Die Schlüsselwörter sollten "Installer" und produktspezifische Schlüsselwörter enthalten.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-173">The keywords should include "Installer" as well as product-specific keywords.</span></span>                                                                                                                             |
| [<span data-ttu-id="7cb4c-174">**Kommentare**</span><span class="sxs-lookup"><span data-stu-id="7cb4c-174">**Comments**</span></span>](comments-summary.md)                          | <span data-ttu-id="7cb4c-175">Enthält den folgenden Ausdruck: "Diese Transformation enthält die Logik und die Daten, die für die Installation <*Produkt namens*> erforderlich sind."</span><span class="sxs-lookup"><span data-stu-id="7cb4c-175">Contains the phrase: "This transform contains the logic and data required to install <*product name*>."</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="7cb4c-176">[**Vorlage**](template-summary.md) (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="7cb4c-176">[**Template**](template-summary.md) (REQUIRED)</span></span>               | <span data-ttu-id="7cb4c-177">Die Plattform-und Sprachversionen, die mit dieser Transformation kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-177">The platform and language versions compatible with this transform.</span></span> <span data-ttu-id="7cb4c-178">Wenn keine Einschränkungen vorliegen, wird dieser Wert möglicherweise leer gelassen.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-178">This value may be left blank if there are no restrictions.</span></span> <span data-ttu-id="7cb4c-179">Für eine Transformation kann nur eine Sprache angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-179">Only one language can be specified for a transform.</span></span> <span data-ttu-id="7cb4c-180">Weitere Informationen zur Syntax finden Sie unter [**Template**](template-summary.md).</span><span class="sxs-lookup"><span data-stu-id="7cb4c-180">For more information about the syntax, see [**Template**](template-summary.md).</span></span>                                |
| [<span data-ttu-id="7cb4c-181">**Zuletzt gespeichert von**</span><span class="sxs-lookup"><span data-stu-id="7cb4c-181">**Last Saved By**</span></span>](last-saved-by-summary.md)                | <span data-ttu-id="7cb4c-182">Die Plattform-und Sprach-IDs, die die Datenbank nach dem Transformieren hat.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-182">The platform and language ID(s) that the database has after it has been transformed.</span></span> <span data-ttu-id="7cb4c-183">Die [**Vorlagen Zusammenfassungs**](template-summary.md) Eigenschaft in der neuen Datenbank sollte auf die gleichen Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-183">The [**Template Summary**](template-summary.md) property in the new database should be set to the same values.</span></span>                                                                                              |
| <span data-ttu-id="7cb4c-184">[**Revisionsnummer**](revision-number-summary.md) (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="7cb4c-184">[**Revision Number**](revision-number-summary.md) (REQUIRED)</span></span> | <span data-ttu-id="7cb4c-185">Eine Liste der Produktcode-GUIDs und-Versionen der neuen und ursprünglichen Produkte sowie der UpgradeCode-GUID.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-185">A list of the product code GUIDs and version of the new and original products and the upgrade code GUID.</span></span> <span data-ttu-id="7cb4c-186">Die Liste wird wie folgt durch Semikolons getrennt.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-186">The list is separated by semicolons as follows.</span></span> <span data-ttu-id="7cb4c-187">*Original-Product-Code Original-Product-Version*; *New-Product Code New-Product-Version*; *UpgradeCode*</span><span class="sxs-lookup"><span data-stu-id="7cb4c-187">*Original-Product-Code Original-Product-Version*;*New-Product Code New-Product-Version*; *Upgrade-Code*</span></span><br/>                       |
| [<span data-ttu-id="7cb4c-188">**Zuletzt gedruckt**</span><span class="sxs-lookup"><span data-stu-id="7cb4c-188">**Last Printed**</span></span>](last-printed-summary.md)                  | <span data-ttu-id="7cb4c-189">Null</span><span class="sxs-lookup"><span data-stu-id="7cb4c-189">Null</span></span>                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="7cb4c-190">**Uhrzeit/Datum erstellen**</span><span class="sxs-lookup"><span data-stu-id="7cb4c-190">**Create Time/Date**</span></span>](create-time-date-summary.md)          | <span data-ttu-id="7cb4c-191">Das Datum und die Uhrzeit der Erstellung der Transformation.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-191">The time and date when the transform was created.</span></span>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="7cb4c-192">**Letzte gespeicherte Uhrzeit/Datum**</span><span class="sxs-lookup"><span data-stu-id="7cb4c-192">**Last Saved Time/Date**</span></span>](last-saved-time-date-summary.md)  | <span data-ttu-id="7cb4c-193">Die aktuelle Systemzeit und das aktuelle Datum zum Zeitpunkt der Speicherung der Transformation.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-193">The current system time and date at the time the transform was saved.</span></span> <span data-ttu-id="7cb4c-194">Anfänglich NULL.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-194">Initially null.</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="7cb4c-195">[**Seitenanzahl**](page-count-summary.md) (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="7cb4c-195">[**Page Count**](page-count-summary.md) (REQUIRED)</span></span>           | <span data-ttu-id="7cb4c-196">Ein-Wert, mit dem die für die Verarbeitung der Transformation erforderliche mindestinstallerversion angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-196">A value used to indicate the minimum installer version required to process the transform.</span></span> <span data-ttu-id="7cb4c-197">Der Wert sollte auf die größere der beiden Eigenschaften Werte der [**Seitenanzahl**](page-count-summary.md) festgelegt werden, die zu den Datenbanken gehören, die zum Generieren der Transformation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-197">The value should be set to the greater of the two [**Page Count**](page-count-summary.md) property values that belong to the databases used to generate the transform.</span></span>                                 |
| <span data-ttu-id="7cb4c-198">[**Wort Anzahl**](word-count-summary.md) (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="7cb4c-198">[**Word Count**](word-count-summary.md) (REQUIRED)</span></span>           | <span data-ttu-id="7cb4c-199">Null</span><span class="sxs-lookup"><span data-stu-id="7cb4c-199">Null</span></span>                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="7cb4c-200">**Zeichen Anzahl**</span><span class="sxs-lookup"><span data-stu-id="7cb4c-200">**Character Count**</span></span>](character-count-summary.md)            | <span data-ttu-id="7cb4c-201">Dieser Teil des Zusammenfassungs Informationsdaten Stroms ist in 2 16-Bit-Wörter unterteilt.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-201">This part of the summary information stream is divided into two 16-bit words.</span></span> <span data-ttu-id="7cb4c-202">Das obere Wort enthält [*Transformations-Validierungsflags*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7cb4c-202">The upper word contains [*transform validation flags*](t-gly.md).</span></span> <span data-ttu-id="7cb4c-203">Das untere Wort enthält [*Transformations fehlerbedingungs-Flags*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7cb4c-203">Lower word contains [*transform error condition flags*](t-gly.md).</span></span> |
| [<span data-ttu-id="7cb4c-204">**Anwendung wird erstellt**</span><span class="sxs-lookup"><span data-stu-id="7cb4c-204">**Creating Application**</span></span>](creating-application-summary.md)  | <span data-ttu-id="7cb4c-205">Enthält den Namen der Software, die zum Erstellen dieser Transformation verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-205">Contains the name of the software used to create this transform.</span></span>                                                                                                                                                                                                                                  |
| [<span data-ttu-id="7cb4c-206">**Sicherheit**</span><span class="sxs-lookup"><span data-stu-id="7cb4c-206">**Security**</span></span>](security-summary.md)                          | <span data-ttu-id="7cb4c-207">Der Wert dieser Eigenschaft sollte 4-erzwungen lauten.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-207">The value of this property should be 4 - Enforced read-only.</span></span>                                                                                                                                                                                                                                      |
| [<span data-ttu-id="7cb4c-208">**Codepage**</span><span class="sxs-lookup"><span data-stu-id="7cb4c-208">**Codepage**</span></span>](codepage-summary.md)                          | <span data-ttu-id="7cb4c-209">Der numerische Wert der ANSI-Codepage, die verwendet wird, um die Zusammenfassungs Informationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-209">The numeric value of the ANSI code page used to display the Summary Information.</span></span> <span data-ttu-id="7cb4c-210">Diese Eigenschaft muss festgelegt werden, bevor in den Zusammenfassungs Informationen Zeichen folgen Eigenschaften festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-210">This property must be set before any string properties can be set in the summary information.</span></span>                                                                                                                    |



 

## <a name="patch-packages"></a><span data-ttu-id="7cb4c-211">Patch-Pakete</span><span class="sxs-lookup"><span data-stu-id="7cb4c-211">Patch Packages</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7cb4c-212">Summary-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7cb4c-212">Summary property</span></span></th>
<th><span data-ttu-id="7cb4c-213">Bedeutung dieser Eigenschaft in einem Patchpaket</span><span class="sxs-lookup"><span data-stu-id="7cb4c-213">Meaning of this property in a Patch package</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7cb4c-214"><a href="title-summary.md"><strong>Titel</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cb4c-214"><a href="title-summary.md"><strong>Title</strong></a></span></span></td>
<td><span data-ttu-id="7cb4c-215">Eine Beschreibung dieser Datei als Patchpaket.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-215">A description of this file as a patch package.</span></span> <span data-ttu-id="7cb4c-216">Die Beschreibung sollte den folgenden Ausdruck enthalten: &quot; <a href="patch-packages.md">Patch</a>.&quot;</span><span class="sxs-lookup"><span data-stu-id="7cb4c-216">The description should include the phrase: &quot;<a href="patch-packages.md">Patch</a>.&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cb4c-217"><a href="subject-summary.md"><strong>Subject</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cb4c-217"><a href="subject-summary.md"><strong>Subject</strong></a></span></span></td>
<td><span data-ttu-id="7cb4c-218">Eine Beschreibung des Patches, die den Namen des Produkts enthält.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-218">A description of the patch that includes the name of the product.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cb4c-219"><a href="author-summary.md"><strong>Autor</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cb4c-219"><a href="author-summary.md"><strong>Author</strong></a></span></span></td>
<td><span data-ttu-id="7cb4c-220">Der Name des Herstellers des Patchpakets.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-220">The name of the manufacturer of the patch package.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cb4c-221"><a href="keywords-summary.md"><strong>Keywords</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cb4c-221"><a href="keywords-summary.md"><strong>Keywords</strong></a></span></span></td>
<td><span data-ttu-id="7cb4c-222">Eine durch Semikolons getrennte Liste der Quellen des Patches.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-222">A semicolon delimited list of sources of the patch.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cb4c-223"><a href="comments-summary.md"><strong>Kommentare</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cb4c-223"><a href="comments-summary.md"><strong>Comments</strong></a></span></span></td>
<td><span data-ttu-id="7cb4c-224">Enthält den Ausdruck: &quot; dieser Patch enthält die Logik und die Daten, die erforderlich sind, um <<em>Produktnamen</em>zu installieren > .&quot;</span><span class="sxs-lookup"><span data-stu-id="7cb4c-224">Contains the phrase: &quot;This patch contains the logic and data required to install <<em>product name</em>>.&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cb4c-225"><a href="template-summary.md"><strong>Vorlage</strong></a> (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="7cb4c-225"><a href="template-summary.md"><strong>Template</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="7cb4c-226">Eine durch Semikolons getrennte Liste der Produktcodes, die diesen Patch annehmen können.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-226">A semicolon delimited list of the product codes that can accept this patch.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cb4c-227"><a href="last-saved-by-summary.md"><strong>Zuletzt gespeichert von</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cb4c-227"><a href="last-saved-by-summary.md"><strong>Last Saved By</strong></a></span></span></td>
<td><span data-ttu-id="7cb4c-228">Eine durch Semikolons getrennte Liste der Namen der Transformations unter Speicher in der Reihenfolge, in der Sie von diesem Patch angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-228">A semicolon delimited list of transform substorage names in the order they are applied by this patch.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cb4c-229"><a href="revision-number-summary.md"><strong>Revisionsnummer</strong></a> (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="7cb4c-229"><a href="revision-number-summary.md"><strong>Revision Number</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="7cb4c-230">Enthält den GUID-Patchcode für den Patch.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-230">Contains the GUID patch code for the patch.</span></span> <span data-ttu-id="7cb4c-231">Auf diese kann eine Liste von Patchcode-GUIDs für Patches folgen, die beim Anwenden dieses Patches entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-231">This may be followed by a list of patch code GUIDs for patches that are removed when this patch is applied.</span></span> <span data-ttu-id="7cb4c-232">Die Patchcodes werden ohne Trennzeichen verkettet, in denen GUIDs in der Liste getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-232">The patch codes are concatenated with no delimiters separating GUIDs in the list.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="7cb4c-233">Wenn das Patchpaket eine <a href="msipatchsequence-table.md"><strong>msipatchsequence</strong></a> -Tabelle enthält, entfernt der Patch keine Patches, die nach der GUID des aktuellen Patches aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-233">If the patch package contains a <a href="msipatchsequence-table.md"><strong>MsiPatchSequence</strong></a> table, the patch does not remove patches listed after the current patch's GUID.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cb4c-234"><a href="last-printed-summary.md"><strong>Zuletzt gedruckt</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cb4c-234"><a href="last-printed-summary.md"><strong>Last Printed</strong></a></span></span></td>
<td><span data-ttu-id="7cb4c-235">Null</span><span class="sxs-lookup"><span data-stu-id="7cb4c-235">Null</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cb4c-236"><a href="create-time-date-summary.md"><strong>Uhrzeit/Datum erstellen</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cb4c-236"><a href="create-time-date-summary.md"><strong>Create Time/Date</strong></a></span></span></td>
<td><span data-ttu-id="7cb4c-237">Das Datum und die Uhrzeit der Erstellung der Patchdatei.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-237">The time and date when patch file was created.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cb4c-238"><a href="last-saved-time-date-summary.md"><strong>Letzte gespeicherte Uhrzeit/Datum</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cb4c-238"><a href="last-saved-time-date-summary.md"><strong>Last Saved Time/Date</strong></a></span></span></td>
<td><span data-ttu-id="7cb4c-239">Die aktuelle Systemzeit und das aktuelle Datum zum Zeitpunkt der Speicherung des Patchpakets.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-239">The current system time and date at the time the patch package was saved.</span></span> <span data-ttu-id="7cb4c-240">Dieser Wert ist anfänglich NULL.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-240">This value is initially null.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cb4c-241"><a href="page-count-summary.md"><strong>Seitenanzahl</strong></a> (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="7cb4c-241"><a href="page-count-summary.md"><strong>Page Count</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="7cb4c-242">Null</span><span class="sxs-lookup"><span data-stu-id="7cb4c-242">Null</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cb4c-243"><a href="word-count-summary.md"><strong>Wort Anzahl</strong></a> (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="7cb4c-243"><a href="word-count-summary.md"><strong>Word Count</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="7cb4c-244">Enthält einen Wert, der die minimale Windows Installer Version angibt, die für die Installation des Patches erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-244">Contains a value that indicates the minimum Windows Installer version that is required to install the patch.</span></span> <span data-ttu-id="7cb4c-245">Für einen Patch mit einem Wort Zähl Wert von 4 ist Windows Installer Version 3,0 oder höher erforderlich, damit der Patch angewendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-245">A patch with a word count value of 4 requires Windows Installer version 3.0 or higher for the patch to be applied.</span></span> <span data-ttu-id="7cb4c-246">Der Wert 3 gibt an, dass Windows Installer Version 2,0 oder höher erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-246">A value of 3 indicates that Windows Installer version 2.0 or higher is required.</span></span> <span data-ttu-id="7cb4c-247">Der Wert 2 gibt an, dass Windows Installer Version 1,2 oder höher erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-247">A value of 2 indicates that Windows Installer version 1.2 or higher is required.</span></span> <span data-ttu-id="7cb4c-248">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-248">The default value is 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cb4c-249"><a href="character-count-summary.md"><strong>Zeichen Anzahl</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cb4c-249"><a href="character-count-summary.md"><strong>Character Count</strong></a></span></span></td>
<td><span data-ttu-id="7cb4c-250">Null</span><span class="sxs-lookup"><span data-stu-id="7cb4c-250">Null</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cb4c-251"><a href="creating-application-summary.md"><strong>Anwendung wird erstellt</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cb4c-251"><a href="creating-application-summary.md"><strong>Creating Application</strong></a></span></span></td>
<td><span data-ttu-id="7cb4c-252">Der Name der zum Erstellen des Patches verwendeten Software.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-252">The name of the software used to create the patch.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cb4c-253"><a href="security-summary.md"><strong>Sicherheit</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cb4c-253"><a href="security-summary.md"><strong>Security</strong></a></span></span></td>
<td><span data-ttu-id="7cb4c-254">Der Wert dieser Eigenschaft sollte 4-erzwungen lauten.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-254">The value of this property should be 4 - Enforced read-only.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cb4c-255"><a href="codepage-summary.md"><strong>Codepage</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cb4c-255"><a href="codepage-summary.md"><strong>Codepage</strong></a></span></span></td>
<td><span data-ttu-id="7cb4c-256">Der numerische Wert der ANSI-Codepage, die verwendet wird, um die Zusammenfassungs Informationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-256">The numeric value of the ANSI code page used to display the Summary Information.</span></span> <span data-ttu-id="7cb4c-257">Diese Eigenschaft muss festgelegt werden, bevor alle Zeichen folgen Eigenschaften in den Zusammenfassungs Informationen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7cb4c-257">This property must be set before any string properties are set in the summary information.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




