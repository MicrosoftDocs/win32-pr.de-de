---
description: Die msipatchheaders-Tabelle enthält die binären patchheader-Datenströme, die für die patchvalidierung verwendet werden.
ms.assetid: aefdd365-1681-43e4-8470-04a5d6efd993
title: Msipatchheaders-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a3fa4e037a31f3e913f13ff9c96735ed6760dc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216359"
---
# <a name="msipatchheaders-table"></a><span data-ttu-id="e785d-103">Msipatchheaders-Tabelle</span><span class="sxs-lookup"><span data-stu-id="e785d-103">MsiPatchHeaders Table</span></span>

<span data-ttu-id="e785d-104">Die msipatchheaders-Tabelle enthält die binären patchheader-Datenströme, die für die patchvalidierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e785d-104">The MsiPatchHeaders table holds the binary patch header streams used for patch validation.</span></span>

<span data-ttu-id="e785d-105">Die msipatchheaders-Tabelle wird verwendet, wenn bei langen [Datei Tabellen](file-table.md) Schlüsseln ein Fehler beim Generieren des patchheader-Streams in der [patchtabelle](patch-table.md)auftritt.</span><span class="sxs-lookup"><span data-stu-id="e785d-105">The MsiPatchHeaders table is used when long [File table](file-table.md) keys result in a failure to generate the patch header stream in the [Patch table](patch-table.md).</span></span> <span data-ttu-id="e785d-106">Dies kann an der in [OLE-Einschränkungen für Streams](ole-limitations-on-streams.md)beschriebenen Datenstrom-namens Einschränkung liegen.</span><span class="sxs-lookup"><span data-stu-id="e785d-106">This can be due to the stream name limitation described in [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span> <span data-ttu-id="e785d-107">In diesem Fall kann die patchtabelle auf die msipatchheaders-Tabelle verweisen, um den Patch-Header Datenstrom zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e785d-107">In this case, the Patch table can reference the MsiPatchHeaders table to create the patch header stream.</span></span>

<span data-ttu-id="e785d-108">Die msipatchheaders-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="e785d-108">The MsiPatchHeaders table has the following columns.</span></span>



| <span data-ttu-id="e785d-109">Spalte</span><span class="sxs-lookup"><span data-stu-id="e785d-109">Column</span></span>    | <span data-ttu-id="e785d-110">Typ</span><span class="sxs-lookup"><span data-stu-id="e785d-110">Type</span></span>                         | <span data-ttu-id="e785d-111">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="e785d-111">Key</span></span> | <span data-ttu-id="e785d-112">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="e785d-112">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="e785d-113">Streamref</span><span class="sxs-lookup"><span data-stu-id="e785d-113">StreamRef</span></span> | [<span data-ttu-id="e785d-114">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="e785d-114">Identifier</span></span>](identifier.md) | <span data-ttu-id="e785d-115">J</span><span class="sxs-lookup"><span data-stu-id="e785d-115">Y</span></span>   | <span data-ttu-id="e785d-116">N</span><span class="sxs-lookup"><span data-stu-id="e785d-116">N</span></span>        |
| <span data-ttu-id="e785d-117">Header</span><span class="sxs-lookup"><span data-stu-id="e785d-117">Header</span></span>    | [<span data-ttu-id="e785d-118">Binär (Binary)</span><span class="sxs-lookup"><span data-stu-id="e785d-118">Binary</span></span>](binary.md)         | <span data-ttu-id="e785d-119">N</span><span class="sxs-lookup"><span data-stu-id="e785d-119">N</span></span>   | <span data-ttu-id="e785d-120">N</span><span class="sxs-lookup"><span data-stu-id="e785d-120">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="e785d-121">Spalten</span><span class="sxs-lookup"><span data-stu-id="e785d-121">Columns</span></span>

<dl> <dt>

<span data-ttu-id="e785d-122"><span id="StreamRef"></span><span id="streamref"></span><span id="STREAMREF"></span>Streamref</span><span class="sxs-lookup"><span data-stu-id="e785d-122"><span id="StreamRef"></span><span id="streamref"></span><span id="STREAMREF"></span>StreamRef</span></span>
</dt> <dd>

<span data-ttu-id="e785d-123">Der Primärschlüssel für die Tabelle, die einen bestimmten patchheader eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e785d-123">The primary key for the table that uniquely identifies a particular patch header.</span></span>

</dd> <dt>

<span data-ttu-id="e785d-124"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header</span><span class="sxs-lookup"><span data-stu-id="e785d-124"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header</span></span>
</dt> <dd>

<span data-ttu-id="e785d-125">Diese Spalte ist der binäre Stream-patchheader, der für die patchvalidierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e785d-125">This column is the binary stream patch header used for patch validation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e785d-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e785d-126">Remarks</span></span>

<span data-ttu-id="e785d-127">Diese Tabelle wird von der [Aktion PATCHFILES](patchfiles-action.md)verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="e785d-127">This table is processed by the [PatchFiles action](patchfiles-action.md).</span></span> <span data-ttu-id="e785d-128">Diese Tabelle wird normalerweise durch eine Transformation aus einem Patchpaket zum Installationspaket hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e785d-128">This table is usually added to the install package by a transform from a patch package.</span></span> <span data-ttu-id="e785d-129">Sie wird in der Regel nicht direkt in ein Installationspaket verfasst.</span><span class="sxs-lookup"><span data-stu-id="e785d-129">It is usually not authored directly into an installation package.</span></span>

## <a name="validation"></a><span data-ttu-id="e785d-130">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="e785d-130">Validation</span></span>

<dl>

[<span data-ttu-id="e785d-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="e785d-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="e785d-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="e785d-132">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="e785d-133">ICE29</span><span class="sxs-lookup"><span data-stu-id="e785d-133">ICE29</span></span>](ice29.md)  
</dl>

 

 



