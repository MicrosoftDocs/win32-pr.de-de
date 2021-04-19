---
description: Msitran.exe verwendet msidatabasegeneratetransform, msikreatetransformsummaryinfo und msidatabaseapplytransform, um eine Transformations Datei zu generieren oder anzuwenden. Dieses Tool ist nur in den Windows SDK Komponenten für Windows Installer Entwickler verfügbar.
ms.assetid: cfc7b907-78d7-4a78-bab4-ede9012d5a36
title: Msitran.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a69936155fb3880f43e0f7563bc6aabd59f53703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364144"
---
# <a name="msitranexe"></a><span data-ttu-id="df2da-103">Msitran.exe</span><span class="sxs-lookup"><span data-stu-id="df2da-103">Msitran.exe</span></span>

<span data-ttu-id="df2da-104">Msitran.exe verwendet [**msidatabasegeneratetransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma), [**msikreatetransformsummaryinfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)und [**msidatabaseapplytransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) , um eine Transformations Datei zu generieren oder anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="df2da-104">Msitran.exe uses [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma), [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa), and [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) to generate or apply a transform file.</span></span>

<span data-ttu-id="df2da-105">Dieses Tool ist nur in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="df2da-105">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="df2da-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="df2da-106">Syntax</span></span>

<span data-ttu-id="df2da-107">Verwenden Sie die folgende Syntax, um eine Transformation zu generieren.</span><span class="sxs-lookup"><span data-stu-id="df2da-107">Use the following syntax to generate a transform.</span></span>

<span data-ttu-id="df2da-108">**MsiTran-g** *{Base DB} {Ref DB} {Transformations Dateiname} \[ {Fehlerbedingungen/Überprüfungs Bedingungen \] }*</span><span class="sxs-lookup"><span data-stu-id="df2da-108">**msitran -g** *{base db}{ref db}{transform file name}\[{error conditions / validation conditions}\]*</span></span>

<span data-ttu-id="df2da-109">Verwenden Sie die folgende Syntax, um eine Transformation anzuwenden:</span><span class="sxs-lookup"><span data-stu-id="df2da-109">Use the following syntax to apply a transform</span></span>

<span data-ttu-id="df2da-110">**MsiTran-a** *{Transform} {Database} \[ {Fehlerbedingungen} \]*</span><span class="sxs-lookup"><span data-stu-id="df2da-110">**msitran -a** *{transform}{database}\[{error conditions}\]*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="df2da-111">Befehlszeilenoptionen</span><span class="sxs-lookup"><span data-stu-id="df2da-111">Command Line Options</span></span>

<span data-ttu-id="df2da-112">Msitran.exe verwendet die folgenden Befehlszeilenoptionen für die Groß-und Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="df2da-112">Msitran.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="df2da-113">Ein Schrägstrich kann auch anstelle eines Bindestrichs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="df2da-113">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="df2da-114">Option</span><span class="sxs-lookup"><span data-stu-id="df2da-114">Option</span></span> | <span data-ttu-id="df2da-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="df2da-115">Description</span></span>            |
|--------|------------------------|
| <span data-ttu-id="df2da-116">-g</span><span class="sxs-lookup"><span data-stu-id="df2da-116">-g</span></span>     | <span data-ttu-id="df2da-117">Transformations Generierung.</span><span class="sxs-lookup"><span data-stu-id="df2da-117">Transform generation.</span></span>  |
| <span data-ttu-id="df2da-118">-a</span><span class="sxs-lookup"><span data-stu-id="df2da-118">-a</span></span>     | <span data-ttu-id="df2da-119">Transformieren Sie die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="df2da-119">Transform application.</span></span> |



 

<span data-ttu-id="df2da-120">Die folgenden Fehler können beim Anwenden einer Transformation unterdrückt werden.</span><span class="sxs-lookup"><span data-stu-id="df2da-120">The following errors may be suppressed when applying a transform.</span></span> <span data-ttu-id="df2da-121">Um einen Fehler zu unterdrücken, schließen Sie das entsprechende Zeichen in das Argument {error Conditions} ein.</span><span class="sxs-lookup"><span data-stu-id="df2da-121">To suppress an error, include the appropriate character in the {error conditions} argument.</span></span> <span data-ttu-id="df2da-122">Die mit-g angegebenen Bedingungen werden in die Zusammenfassungs Informationen der Transformation eingefügt, aber beim Anwenden einer Transformation mit-a nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="df2da-122">Conditions specified with -g are placed in the summary information of the transform, but are not used when applying a transform with -a.</span></span> <span data-ttu-id="df2da-123">Weitere Informationen finden Sie unter [**msidatabaseapplytransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma).</span><span class="sxs-lookup"><span data-stu-id="df2da-123">For information, see [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma).</span></span>



| <span data-ttu-id="df2da-124">Option</span><span class="sxs-lookup"><span data-stu-id="df2da-124">Option</span></span> | <span data-ttu-id="df2da-125">Unterdrückte Fehler</span><span class="sxs-lookup"><span data-stu-id="df2da-125">Suppressed error</span></span>           |
|--------|----------------------------|
| <span data-ttu-id="df2da-126">a</span><span class="sxs-lookup"><span data-stu-id="df2da-126">a</span></span>      | <span data-ttu-id="df2da-127">Fügen Sie eine vorhandene Zeile hinzu.</span><span class="sxs-lookup"><span data-stu-id="df2da-127">Add existing row.</span></span>          |
| <span data-ttu-id="df2da-128">b</span><span class="sxs-lookup"><span data-stu-id="df2da-128">b</span></span>      | <span data-ttu-id="df2da-129">Löschen Sie eine nicht vorhandene Zeile.</span><span class="sxs-lookup"><span data-stu-id="df2da-129">Delete non-existing row.</span></span>   |
| <span data-ttu-id="df2da-130">c</span><span class="sxs-lookup"><span data-stu-id="df2da-130">c</span></span>      | <span data-ttu-id="df2da-131">Fügen Sie eine vorhandene Tabelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="df2da-131">Add existing table.</span></span>        |
| <span data-ttu-id="df2da-132">d</span><span class="sxs-lookup"><span data-stu-id="df2da-132">d</span></span>      | <span data-ttu-id="df2da-133">Nicht vorhandene Tabelle löschen.</span><span class="sxs-lookup"><span data-stu-id="df2da-133">Delete non-existing table.</span></span> |
| <span data-ttu-id="df2da-134">e</span><span class="sxs-lookup"><span data-stu-id="df2da-134">e</span></span>      | <span data-ttu-id="df2da-135">Ändern Sie die vorhandene Zeile.</span><span class="sxs-lookup"><span data-stu-id="df2da-135">Modify existing row.</span></span>       |
| <span data-ttu-id="df2da-136">f</span><span class="sxs-lookup"><span data-stu-id="df2da-136">f</span></span>      | <span data-ttu-id="df2da-137">Ändern Sie die Codepage.</span><span class="sxs-lookup"><span data-stu-id="df2da-137">Change codepage.</span></span>           |



 

<span data-ttu-id="df2da-138">Die folgenden Validierungs Bedingungen können verwendet werden, um anzugeben, wann eine Transformation auf ein Paket angewendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="df2da-138">The following validation conditions may be used to indicate when a transform may be applied to a package.</span></span> <span data-ttu-id="df2da-139">Diese Bedingungen können mit-g, jedoch nicht mit-a angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="df2da-139">These conditions may be specified with -g, but not -a.</span></span>



| <span data-ttu-id="df2da-140">Option</span><span class="sxs-lookup"><span data-stu-id="df2da-140">Option</span></span> | <span data-ttu-id="df2da-141">Validierungs Bedingung</span><span class="sxs-lookup"><span data-stu-id="df2da-141">Validation condition</span></span>                                  |
|--------|-------------------------------------------------------|
| <span data-ttu-id="df2da-142">g</span><span class="sxs-lookup"><span data-stu-id="df2da-142">g</span></span>      | <span data-ttu-id="df2da-143">Aktivieren Sie den UpgradeCode.</span><span class="sxs-lookup"><span data-stu-id="df2da-143">Check upgrade code.</span></span>                                   |
| <span data-ttu-id="df2da-144">l</span><span class="sxs-lookup"><span data-stu-id="df2da-144">l</span></span>      | <span data-ttu-id="df2da-145">Sprache überprüfen.</span><span class="sxs-lookup"><span data-stu-id="df2da-145">Check language.</span></span>                                       |
| <span data-ttu-id="df2da-146">p</span><span class="sxs-lookup"><span data-stu-id="df2da-146">p</span></span>      | <span data-ttu-id="df2da-147">Plattform überprüfen.</span><span class="sxs-lookup"><span data-stu-id="df2da-147">Check platform.</span></span>                                       |
| <span data-ttu-id="df2da-148">r</span><span class="sxs-lookup"><span data-stu-id="df2da-148">r</span></span>      | <span data-ttu-id="df2da-149">Überprüfen Sie Product.</span><span class="sxs-lookup"><span data-stu-id="df2da-149">Check product.</span></span>                                        |
| <span data-ttu-id="df2da-150">s</span><span class="sxs-lookup"><span data-stu-id="df2da-150">s</span></span>      | <span data-ttu-id="df2da-151">Überprüfen Sie nur die Hauptversion.</span><span class="sxs-lookup"><span data-stu-id="df2da-151">Check major version only.</span></span>                             |
| <span data-ttu-id="df2da-152">t</span><span class="sxs-lookup"><span data-stu-id="df2da-152">t</span></span>      | <span data-ttu-id="df2da-153">Überprüfen Sie nur die Haupt-und neben Versionen.</span><span class="sxs-lookup"><span data-stu-id="df2da-153">Check major and minor versions only.</span></span>                  |
| <span data-ttu-id="df2da-154">u</span><span class="sxs-lookup"><span data-stu-id="df2da-154">u</span></span>      | <span data-ttu-id="df2da-155">Überprüfen Sie die Haupt-, neben-und upgradeversionen.</span><span class="sxs-lookup"><span data-stu-id="df2da-155">Check major, minor, and upgrade versions.</span></span>             |
| <span data-ttu-id="df2da-156">v</span><span class="sxs-lookup"><span data-stu-id="df2da-156">v</span></span>      | <span data-ttu-id="df2da-157">Die Version der Datenbankversion < Basisdaten Bank Version.</span><span class="sxs-lookup"><span data-stu-id="df2da-157">Applied database version < Base database version.</span></span>  |
| <span data-ttu-id="df2da-158">w</span><span class="sxs-lookup"><span data-stu-id="df2da-158">w</span></span>      | <span data-ttu-id="df2da-159">Angewendete Datenbankversion <= Basisdaten Bank Version.</span><span class="sxs-lookup"><span data-stu-id="df2da-159">Applied database version <= Base database version.</span></span> |
| <span data-ttu-id="df2da-160">x</span><span class="sxs-lookup"><span data-stu-id="df2da-160">x</span></span>      | <span data-ttu-id="df2da-161">Angewendete Datenbankversion = Basisdaten Bank Version.</span><span class="sxs-lookup"><span data-stu-id="df2da-161">Applied database version = Base database version.</span></span>     |
| <span data-ttu-id="df2da-162">Y</span><span class="sxs-lookup"><span data-stu-id="df2da-162">y</span></span>      | <span data-ttu-id="df2da-163">Angewendete Datenbankversion >= Basisdaten Bank Version.</span><span class="sxs-lookup"><span data-stu-id="df2da-163">Applied database version >= Base database version.</span></span> |
| <span data-ttu-id="df2da-164">z</span><span class="sxs-lookup"><span data-stu-id="df2da-164">z</span></span>      | <span data-ttu-id="df2da-165">Die Version der Datenbankversion > Basisdaten Bank Version.</span><span class="sxs-lookup"><span data-stu-id="df2da-165">Applied database version > Base database version.</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="df2da-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="df2da-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df2da-167">Entwicklungs Tools für Windows Installer</span><span class="sxs-lookup"><span data-stu-id="df2da-167">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="df2da-168">Daten Bank Transformationen</span><span class="sxs-lookup"><span data-stu-id="df2da-168">Database Transforms</span></span>](database-transforms.md)
</dt> <dt>

[<span data-ttu-id="df2da-169">Beispiel für eine Anpassungs Transformation</span><span class="sxs-lookup"><span data-stu-id="df2da-169">A Customization Transform Example</span></span>](a-customization-transform-example.md)
</dt> <dt>

[<span data-ttu-id="df2da-170">Veröffentlichte Versionen, Tools und verteilbare Dateien</span><span class="sxs-lookup"><span data-stu-id="df2da-170">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



