---
description: In der Tabelle patchpackage werden alle Patchpakete beschrieben, die auf dieses Produkt angewendet wurden. Für jedes Patchpaket wird der eindeutige Bezeichner für den Patch sowie Informationen zum Medien Abbild bereitgestellt, auf dem sich der Patch befindet.
ms.assetid: 212d99dd-c80c-42ca-9dfa-819ae1813006
title: Patchpakettabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13bf9fc03012ca54a0b2144e97c828c968c68da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218522"
---
# <a name="patchpackage-table"></a><span data-ttu-id="e3c7f-104">Patchpakettabelle</span><span class="sxs-lookup"><span data-stu-id="e3c7f-104">PatchPackage Table</span></span>

<span data-ttu-id="e3c7f-105">In der Tabelle patchpackage werden alle Patchpakete beschrieben, die auf dieses Produkt angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="e3c7f-105">The PatchPackage table describes all patch packages that have been applied to this product.</span></span> <span data-ttu-id="e3c7f-106">Für jedes Patchpaket wird der eindeutige Bezeichner für den Patch sowie Informationen zum Medien Abbild bereitgestellt, auf dem sich der Patch befindet.</span><span class="sxs-lookup"><span data-stu-id="e3c7f-106">For each patch package, the unique identifier for the patch is provided along with information about the media image the on which the patch is located.</span></span>

<span data-ttu-id="e3c7f-107">Die patchpakettabelle enthält die folgenden Spalten.</span><span class="sxs-lookup"><span data-stu-id="e3c7f-107">The PatchPackage table has the following columns.</span></span>



| <span data-ttu-id="e3c7f-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="e3c7f-108">Column</span></span>  | <span data-ttu-id="e3c7f-109">Typ</span><span class="sxs-lookup"><span data-stu-id="e3c7f-109">Type</span></span>                   | <span data-ttu-id="e3c7f-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="e3c7f-110">Key</span></span> | <span data-ttu-id="e3c7f-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="e3c7f-111">Nullable</span></span> |
|---------|------------------------|-----|----------|
| <span data-ttu-id="e3c7f-112">PatchID</span><span class="sxs-lookup"><span data-stu-id="e3c7f-112">PatchId</span></span> | [<span data-ttu-id="e3c7f-113">GUID</span><span class="sxs-lookup"><span data-stu-id="e3c7f-113">GUID</span></span>](guid.md)       | <span data-ttu-id="e3c7f-114">J</span><span class="sxs-lookup"><span data-stu-id="e3c7f-114">Y</span></span>   | <span data-ttu-id="e3c7f-115">N</span><span class="sxs-lookup"><span data-stu-id="e3c7f-115">N</span></span>        |
| <span data-ttu-id="e3c7f-116">Medien\_</span><span class="sxs-lookup"><span data-stu-id="e3c7f-116">Media\_</span></span> | [<span data-ttu-id="e3c7f-117">Integer</span><span class="sxs-lookup"><span data-stu-id="e3c7f-117">Integer</span></span>](integer.md) | <span data-ttu-id="e3c7f-118">N</span><span class="sxs-lookup"><span data-stu-id="e3c7f-118">N</span></span>   | <span data-ttu-id="e3c7f-119">N</span><span class="sxs-lookup"><span data-stu-id="e3c7f-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="e3c7f-120">Spalten</span><span class="sxs-lookup"><span data-stu-id="e3c7f-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="e3c7f-121"><span id="PatchId"></span><span id="patchid"></span><span id="PATCHID"></span>PatchID</span><span class="sxs-lookup"><span data-stu-id="e3c7f-121"><span id="PatchId"></span><span id="patchid"></span><span id="PATCHID"></span>PatchId</span></span>
</dt> <dd>

<span data-ttu-id="e3c7f-122">Diese Spalte enthält einen eindeutigen Bezeichner für diesen Patch.</span><span class="sxs-lookup"><span data-stu-id="e3c7f-122">This column contains a unique identifier for this particular patch.</span></span>

</dd> <dt>

<span data-ttu-id="e3c7f-123"><span id="Media_"></span><span id="media_"></span><span id="MEDIA_"></span>Medien\_</span><span class="sxs-lookup"><span data-stu-id="e3c7f-123"><span id="Media_"></span><span id="media_"></span><span id="MEDIA_"></span>Media\_</span></span>
</dt> <dd>

<span data-ttu-id="e3c7f-124">Diese Spalte ist ein Fremdschlüssel für die DiskId-Spalte der [Medien Tabelle](media-table.md) und gibt den Datenträger an, der das Patchpaket enthält.</span><span class="sxs-lookup"><span data-stu-id="e3c7f-124">This column is a foreign key to the DiskId column of the [Media Table](media-table.md) and indicates the disk containing the patch package.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3c7f-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3c7f-125">Remarks</span></span>

<span data-ttu-id="e3c7f-126">Die patchpakettabelle ist in jedem Patchpaket erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e3c7f-126">The PatchPackage table is required in every patch package.</span></span> <span data-ttu-id="e3c7f-127">Wenn die Tabelle fehlt, tritt beim Versuch, den Patch zu installieren, ein Fehler auf: "Fehler 2768: die Transformation im Patchpaket ist ungültig."</span><span class="sxs-lookup"><span data-stu-id="e3c7f-127">If the table is missing, attempts to install the patch fail with "Error 2768: Transform in patch package is invalid."</span></span> <span data-ttu-id="e3c7f-128">Diese Tabelle wird normalerweise durch eine Transformation aus einem Patchpaket zum Installationspaket hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e3c7f-128">This table is usually added to the install package by a transform from a patch package.</span></span> <span data-ttu-id="e3c7f-129">Sie wird in der Regel nicht direkt in ein Installationspaket verfasst.</span><span class="sxs-lookup"><span data-stu-id="e3c7f-129">It is usually not authored directly into an install package.</span></span>

## <a name="validation"></a><span data-ttu-id="e3c7f-130">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="e3c7f-130">Validation</span></span>

<dl>

[<span data-ttu-id="e3c7f-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="e3c7f-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="e3c7f-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="e3c7f-132">ICE06</span></span>](ice06.md)  
</dl>

 

 



