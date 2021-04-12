---
description: Die Tabelle "upgradedfile \_ OptionalData" enthält Informationen zu bestimmten Dateien in einem aktualisierten Image. Diese Tabelle ist in der Datenbank für die Patcherstellung (PCP-Datei) optional und wird von der uikreatepatchpackageex-Funktion verwendet.
ms.assetid: 8b96a83a-2bfa-47b7-bde0-896bdcc97d29
title: UpgradedFiles_OptionalData Tabelle (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2a648623e2a0cde11af34a3b948b4f2ac6fba59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218202"
---
# <a name="upgradedfiles_optionaldata-table-patchwizdll"></a><span data-ttu-id="c1423-104">Tabelle "upgradedfiles" \_ (OptionalData) (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="c1423-104">UpgradedFiles\_OptionalData Table (Patchwiz.dll)</span></span>

<span data-ttu-id="c1423-105">Die Tabelle "upgradedfile \_ OptionalData" enthält Informationen zu bestimmten Dateien in einem aktualisierten Image.</span><span class="sxs-lookup"><span data-stu-id="c1423-105">The UpgradedFile\_OptionalData table contains information about specific files in an upgraded image.</span></span> <span data-ttu-id="c1423-106">Diese Tabelle ist in der Datenbank für die Patcherstellung (PCP-Datei) optional und wird von der [uikreatepatchpackageex](uicreatepatchpackageex--patchwiz-dll-.md) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="c1423-106">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="c1423-107">Die Tabelle "upgradedfile" \_ enthält die folgenden Spalten.</span><span class="sxs-lookup"><span data-stu-id="c1423-107">The UpgradedFile\_OptionalData table has the following columns.</span></span>



| <span data-ttu-id="c1423-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="c1423-108">Column</span></span>                  | <span data-ttu-id="c1423-109">Typ</span><span class="sxs-lookup"><span data-stu-id="c1423-109">Type</span></span>    | <span data-ttu-id="c1423-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="c1423-110">Key</span></span> | <span data-ttu-id="c1423-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="c1423-111">Nullable</span></span> |
|-------------------------|---------|-----|----------|
| <span data-ttu-id="c1423-112">Upgraded</span><span class="sxs-lookup"><span data-stu-id="c1423-112">Upgraded</span></span>                | <span data-ttu-id="c1423-113">text</span><span class="sxs-lookup"><span data-stu-id="c1423-113">text</span></span>    | <span data-ttu-id="c1423-114">J</span><span class="sxs-lookup"><span data-stu-id="c1423-114">Y</span></span>   | <span data-ttu-id="c1423-115">N</span><span class="sxs-lookup"><span data-stu-id="c1423-115">N</span></span>        |
| <span data-ttu-id="c1423-116">FTK</span><span class="sxs-lookup"><span data-stu-id="c1423-116">FTK</span></span>                     | <span data-ttu-id="c1423-117">text</span><span class="sxs-lookup"><span data-stu-id="c1423-117">text</span></span>    | <span data-ttu-id="c1423-118">J</span><span class="sxs-lookup"><span data-stu-id="c1423-118">Y</span></span>   | <span data-ttu-id="c1423-119">N</span><span class="sxs-lookup"><span data-stu-id="c1423-119">N</span></span>        |
| <span data-ttu-id="c1423-120">SymbolPath</span><span class="sxs-lookup"><span data-stu-id="c1423-120">SymbolPaths</span></span>             | <span data-ttu-id="c1423-121">text</span><span class="sxs-lookup"><span data-stu-id="c1423-121">text</span></span>    |     | <span data-ttu-id="c1423-122">J</span><span class="sxs-lookup"><span data-stu-id="c1423-122">Y</span></span>        |
| <span data-ttu-id="c1423-123">Zuordnung von "Zuweisung</span><span class="sxs-lookup"><span data-stu-id="c1423-123">AllowIgnoreOnPatchError</span></span> | <span data-ttu-id="c1423-124">integer</span><span class="sxs-lookup"><span data-stu-id="c1423-124">integer</span></span> |     | <span data-ttu-id="c1423-125">J</span><span class="sxs-lookup"><span data-stu-id="c1423-125">Y</span></span>        |
| <span data-ttu-id="c1423-126">Includewholefile</span><span class="sxs-lookup"><span data-stu-id="c1423-126">IncludeWholeFile</span></span>        | <span data-ttu-id="c1423-127">integer</span><span class="sxs-lookup"><span data-stu-id="c1423-127">integer</span></span> |     | <span data-ttu-id="c1423-128">J</span><span class="sxs-lookup"><span data-stu-id="c1423-128">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="c1423-129">Spalten</span><span class="sxs-lookup"><span data-stu-id="c1423-129">Columns</span></span>

<dl> <dt>

<span data-ttu-id="c1423-130"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Aktualisiert</span><span class="sxs-lookup"><span data-stu-id="c1423-130"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Upgraded</span></span>
</dt> <dd>

<span data-ttu-id="c1423-131">Fremdschlüssel für die aktualisierte Spalte der [Tabelle "UpgradedImages" (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="c1423-131">Foreign key to the Upgraded column of the [UpgradedImages Table (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1423-132"><span id="FTK"></span><span id="ftk"></span>FTK</span><span class="sxs-lookup"><span data-stu-id="c1423-132"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="c1423-133">Datei Tabellenschlüssel.</span><span class="sxs-lookup"><span data-stu-id="c1423-133">File table key.</span></span> <span data-ttu-id="c1423-134">Fremdschlüssel in die [Dateitabelle](file-table.md) der MSI-Datei des aktualisierten Abbilds.</span><span class="sxs-lookup"><span data-stu-id="c1423-134">Foreign key into [File table](file-table.md) of the .msi file of the upgraded image.</span></span> <span data-ttu-id="c1423-135">Wenn mindestens zwei aktualisierte Images innerhalb einer Familie denselben FTK-Wert aufweisen, muss der Wert auf dieselbe Datei verweisen.</span><span class="sxs-lookup"><span data-stu-id="c1423-135">If two or more upgraded images within a family have the same FTK value, the value must refer to the same file.</span></span> <span data-ttu-id="c1423-136">Dateien, die von mehreren upgradeimages gemeinsam genutzt werden, sollten dieselbe FTK aufweisen, um die Größe der CAB-Datei</span><span class="sxs-lookup"><span data-stu-id="c1423-136">Files shared by multiple upgrade images should have the same FTK to minimize cabinet file size.</span></span>

</dd> <dt>

<span data-ttu-id="c1423-137"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPath</span><span class="sxs-lookup"><span data-stu-id="c1423-137"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="c1423-138">Der Wert in diesem Feld wird der durch Semikolons getrennten Liste der Ordner in der SymbolPath-Spalte der [UpgradedImages-Tabelle (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md) hinzugefügt, wenn der Patch generiert wird, und kann zum Hinzufügen von Symbol Dateien für eine bestimmte Datei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c1423-138">The value in this field is added to the semicolon-delimited list of folders in the SymbolPaths column of the [UpgradedImages Table (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md) when the patch is generated, and can be used to add symbol files for a specific file.</span></span>

</dd> <dt>

<span data-ttu-id="c1423-139"><span id="AllowIgnoreOnPatchError"></span><span id="allowignoreonpatcherror"></span><span id="ALLOWIGNOREONPATCHERROR"></span>Zuordnung von "Zuweisung</span><span class="sxs-lookup"><span data-stu-id="c1423-139"><span id="AllowIgnoreOnPatchError"></span><span id="allowignoreonpatcherror"></span><span id="ALLOWIGNOREONPATCHERROR"></span>AllowIgnoreOnPatchError</span></span>
</dt> <dd>

<span data-ttu-id="c1423-140">Legen Sie den Wert auf 1 fest, um anzugeben, dass der Patch nicht von Bedeutung ist.</span><span class="sxs-lookup"><span data-stu-id="c1423-140">Set to 1 to indicate that the patch is non-vital.</span></span> <span data-ttu-id="c1423-141">Legen Sie auf 0 fest, um anzugeben, dass der Patch wichtig ist.</span><span class="sxs-lookup"><span data-stu-id="c1423-141">Set to 0 to indicate that the patch is vital.</span></span> <span data-ttu-id="c1423-142">Wenn beim Anwenden dieses Patches auf die in der Spalte FTK angegebene Datei Windows Installer ein Problem auftritt, bestimmt der Wert in diesem Feld, ob das Fehlermeldungs Feld die Schaltfläche **ignorieren** enthält, damit der Benutzer den Patchvorgang fortsetzen kann.</span><span class="sxs-lookup"><span data-stu-id="c1423-142">If Windows Installer encounters a problem when applying this patch to the file specified in the FTK column, the value in this field determines whether the error message box includes an **Ignore** button to enable the user to continue the patching process.</span></span>

</dd> <dt>

<span data-ttu-id="c1423-143"><span id="IncludeWholeFile"></span><span id="includewholefile"></span><span id="INCLUDEWHOLEFILE"></span>Includewholefile</span><span class="sxs-lookup"><span data-stu-id="c1423-143"><span id="IncludeWholeFile"></span><span id="includewholefile"></span><span id="INCLUDEWHOLEFILE"></span>IncludeWholeFile</span></span>
</dt> <dd>

<span data-ttu-id="c1423-144">Legen Sie auf einen Wert ungleich 0 (null) fest, wenn die gesamte in der FTK-Spalte angegebene Datei installiert werden soll, anstatt einen binären Patch zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c1423-144">Set to a nonzero value if the entire file specified in the FTK column should be installed rather than creating a binary patch.</span></span>

</dd> </dl>

 

 



