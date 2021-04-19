---
description: Die Tabelle "upgradedfilestoignore" verhindert, dass bestimmte Dateien, die tatsächlich im aktualisierten Image geändert wurden, relativ zu den Ziel Images aktualisiert werden.
ms.assetid: 3b5f4360-887a-4a21-8f16-faa84da34328
title: Tabelle "Upgrade dfilestoignore" (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4a235759251ac3dadbe01b030c0d984d1f66b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362961"
---
# <a name="upgradedfilestoignore-table-patchwizdll"></a><span data-ttu-id="c1a48-103">Tabelle "Upgrade dfilestoignore" (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="c1a48-103">UpgradedFilesToIgnore Table (Patchwiz.dll)</span></span>

<span data-ttu-id="c1a48-104">Die Tabelle "upgradedfilestoignore" verhindert, dass bestimmte Dateien, die tatsächlich im aktualisierten Image geändert wurden, relativ zu den Ziel Images aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c1a48-104">The UpgradedFilesToIgnore table prevents the updating of specific files that are in fact changed in the upgraded image relative to the target images.</span></span> <span data-ttu-id="c1a48-105">In bestimmten Fällen ist es möglicherweise hilfreich, dies zu tun.</span><span class="sxs-lookup"><span data-stu-id="c1a48-105">It may be useful to do this in certain cases.</span></span> <span data-ttu-id="c1a48-106">Beispielsweise muss ein Patchpaket, das nur für die Verwendung mit nicht administrativen Installationen vorgesehen ist, keine Dateien für das Patchen enthalten, die nur Teil von administrativen Images sind.</span><span class="sxs-lookup"><span data-stu-id="c1a48-106">For example, a patch package intended only for use with non-administrative installations does not need to include patching files that are only part of administrative images.</span></span> <span data-ttu-id="c1a48-107">Das Ausschließen von Dateien, die nur in administrativen Images verwendet werden, kann die Größe des Patchpakets verringern. Administratoren sollten jedoch darüber informiert werden, wie Sie diese Dateien separat aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c1a48-107">Excluding such files used only in administrative images can reduce the size of the patch package; however, administrators should be informed on how to update these files separately.</span></span> <span data-ttu-id="c1a48-108">Diese Tabelle ist in der Datenbank für die Patcherstellung (PCP-Datei) optional und wird von der [uikreatepatchpackageex](uicreatepatchpackageex--patchwiz-dll-.md) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="c1a48-108">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="c1a48-109">Die Tabelle "Upgrade dfilestoignore" weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="c1a48-109">The UpgradedFilesToIgnore table has the following columns.</span></span>



| <span data-ttu-id="c1a48-110">Spalte</span><span class="sxs-lookup"><span data-stu-id="c1a48-110">Column</span></span>   | <span data-ttu-id="c1a48-111">Typ</span><span class="sxs-lookup"><span data-stu-id="c1a48-111">Type</span></span> | <span data-ttu-id="c1a48-112">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="c1a48-112">Key</span></span> | <span data-ttu-id="c1a48-113">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="c1a48-113">Nullable</span></span> |
|----------|------|-----|----------|
| <span data-ttu-id="c1a48-114">Upgraded</span><span class="sxs-lookup"><span data-stu-id="c1a48-114">Upgraded</span></span> | <span data-ttu-id="c1a48-115">text</span><span class="sxs-lookup"><span data-stu-id="c1a48-115">text</span></span> | <span data-ttu-id="c1a48-116">J</span><span class="sxs-lookup"><span data-stu-id="c1a48-116">Y</span></span>   | <span data-ttu-id="c1a48-117">N</span><span class="sxs-lookup"><span data-stu-id="c1a48-117">N</span></span>        |
| <span data-ttu-id="c1a48-118">FTK</span><span class="sxs-lookup"><span data-stu-id="c1a48-118">FTK</span></span>      | <span data-ttu-id="c1a48-119">text</span><span class="sxs-lookup"><span data-stu-id="c1a48-119">text</span></span> | <span data-ttu-id="c1a48-120">J</span><span class="sxs-lookup"><span data-stu-id="c1a48-120">Y</span></span>   | <span data-ttu-id="c1a48-121">N</span><span class="sxs-lookup"><span data-stu-id="c1a48-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="c1a48-122">Spalten</span><span class="sxs-lookup"><span data-stu-id="c1a48-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="c1a48-123"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Aktualisiert</span><span class="sxs-lookup"><span data-stu-id="c1a48-123"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Upgraded</span></span>
</dt> <dd>

<span data-ttu-id="c1a48-124">Fremdschlüssel für die aktualisierte Spalte der [Tabelle "UpgradedImages" (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="c1a48-124">Foreign key to the Upgraded column of the [UpgradedImages Table (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).</span></span> <span data-ttu-id="c1a48-125">Das Tool für die Patcherstellung schließt die Aktualisierung der in der FTK-Spalte der Tabelle "upgradedfilestoignore" angegebenen Datei aus, wenn ein Ziel auf das im aktualisierten Feld angegebene Bild aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="c1a48-125">The patch creation tool excludes updating the file specified in the FTK column of the UpgradedFilesToIgnore table when upgrading a target to the image specified in the Upgraded field.</span></span> <span data-ttu-id="c1a48-126">Geben Sie \* im Feld aktualisiert den Wert "" ein, um das Aktualisieren der Datei auf alle aktualisierten Images auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="c1a48-126">Enter a value of "\*" in the Upgraded field to exclude updating the file for all upgraded images.</span></span>

</dd> <dt>

<span data-ttu-id="c1a48-127"><span id="FTK"></span><span id="ftk"></span>FTK</span><span class="sxs-lookup"><span data-stu-id="c1a48-127"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="c1a48-128">Fremdschlüssel in die [Dateitabelle](file-table.md) des aktualisierten Abbilds.</span><span class="sxs-lookup"><span data-stu-id="c1a48-128">Foreign key into the [File table](file-table.md) of the upgraded image.</span></span> <span data-ttu-id="c1a48-129">Ein Wert im <prefix> \* Format "" entspricht allen Datei Tabellen Schlüsseln in der Dateitabelle, die mit diesem Präfix beginnen.</span><span class="sxs-lookup"><span data-stu-id="c1a48-129">A value of the form "<prefix>\*" matches all file table keys in the File table that begin with that prefix.</span></span> <span data-ttu-id="c1a48-130">Es kann kein Text auf das Sternchen folgen.</span><span class="sxs-lookup"><span data-stu-id="c1a48-130">No text can follow the asterisk.</span></span>

</dd> </dl>

 

 



