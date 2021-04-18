---
title: Download Collection-Objekt
description: Download Collection-Objekt
ms.assetid: e943b391-386e-43c5-a314-55ea31b2eefa
keywords:
- Windows Media Player Online Stores, Download Collection-Objekt
- Online Stores, downloadcollection-Objekt
- Typ 2 Online Stores, downloadcollection-Objekt
- Download Sammlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8275cbd2661bdce9c428800206c14b9c55942c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339216"
---
# <a name="downloadcollection-object"></a><span data-ttu-id="0fe48-107">Download Collection-Objekt</span><span class="sxs-lookup"><span data-stu-id="0fe48-107">DownloadCollection Object</span></span>

> [!Note]  
> <span data-ttu-id="0fe48-108">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="0fe48-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="0fe48-109">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0fe48-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="0fe48-110">Das **downloadcollection** -Objekt enthält Eigenschaften und Methoden zum Verarbeiten von Auflistungen von Download Elementen.</span><span class="sxs-lookup"><span data-stu-id="0fe48-110">The **DownloadCollection** object contains properties and methods to handle collections of download items.</span></span> <span data-ttu-id="0fe48-111">Sie kann von Webseiten verwendet werden, die im vollständigen Windows-Media Player gehostet werden und Zugriff auf das **externe** Objekt haben, z. b. Online Stores.</span><span class="sxs-lookup"><span data-stu-id="0fe48-111">It can be used by webpages that are hosted in the full mode Windows Media Player and that have access to the **External** object, such as online stores.</span></span>

<span data-ttu-id="0fe48-112">Das **downloadcollection** -Objekt unterstützt die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0fe48-112">The **DownloadCollection** object supports the following properties.</span></span>



| <span data-ttu-id="0fe48-113">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0fe48-113">Property</span></span>                              | <span data-ttu-id="0fe48-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0fe48-114">Description</span></span>                                  |
|---------------------------------------|----------------------------------------------|
| [<span data-ttu-id="0fe48-115">count</span><span class="sxs-lookup"><span data-stu-id="0fe48-115">count</span></span>](downloadcollection-count.md) | <span data-ttu-id="0fe48-116">Ruft die Anzahl der ausstehenden Downloads ab.</span><span class="sxs-lookup"><span data-stu-id="0fe48-116">Retrieves the number of pending downloads.</span></span>   |
| [<span data-ttu-id="0fe48-117">id</span><span class="sxs-lookup"><span data-stu-id="0fe48-117">id</span></span>](downloadcollection-id.md)       | <span data-ttu-id="0fe48-118">Ruft die ID der Download Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="0fe48-118">Retrieves the ID of the download collection.</span></span> |



 

<span data-ttu-id="0fe48-119">Das **downloadcollection** -Objekt unterstützt die folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="0fe48-119">The **DownloadCollection** object supports the following methods.</span></span>



| <span data-ttu-id="0fe48-120">Methode</span><span class="sxs-lookup"><span data-stu-id="0fe48-120">Method</span></span>                                                | <span data-ttu-id="0fe48-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0fe48-121">Description</span></span>                                   |
|-------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="0fe48-122">Löschen</span><span class="sxs-lookup"><span data-stu-id="0fe48-122">Clear</span></span>](downloadcollection-clear.md)                 | <span data-ttu-id="0fe48-123">Entfernt alle Elemente aus einer Download Auflistung.</span><span class="sxs-lookup"><span data-stu-id="0fe48-123">Removes all items from a download collection.</span></span> |
| [<span data-ttu-id="0fe48-124">item</span><span class="sxs-lookup"><span data-stu-id="0fe48-124">item</span></span>](downloadcollection-item.md)                   | <span data-ttu-id="0fe48-125">Ruft ein ausstehendes Download Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="0fe48-125">Retrieves a pending download object.</span></span>          |
| [<span data-ttu-id="0fe48-126">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="0fe48-126">removeItem</span></span>](downloadcollection-removeitem.md)       | <span data-ttu-id="0fe48-127">Entfernt ein Download Element aus einer Sammlung.</span><span class="sxs-lookup"><span data-stu-id="0fe48-127">Removes a download item from a collection.</span></span>    |
| [<span data-ttu-id="0fe48-128">startDownload</span><span class="sxs-lookup"><span data-stu-id="0fe48-128">startDownload</span></span>](downloadcollection-startdownload.md) | <span data-ttu-id="0fe48-129">Fügt einen Download in die Warteschlange</span><span class="sxs-lookup"><span data-stu-id="0fe48-129">Queues a download.</span></span>                            |



 

<span data-ttu-id="0fe48-130">Der Zugriff auf das **downloadcollection** -Objekt erfolgt über die folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="0fe48-130">The **DownloadCollection** object is accessed through the following methods.</span></span>



| <span data-ttu-id="0fe48-131">Object</span><span class="sxs-lookup"><span data-stu-id="0fe48-131">Object</span></span>                                        | <span data-ttu-id="0fe48-132">Methode</span><span class="sxs-lookup"><span data-stu-id="0fe48-132">Method</span></span>                                                                   |
|-----------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="0fe48-133">Download Manager</span><span class="sxs-lookup"><span data-stu-id="0fe48-133">DownloadManager</span></span>](downloadmanager-object.md) | [<span data-ttu-id="0fe48-134">"kreatedownloadcollection"</span><span class="sxs-lookup"><span data-stu-id="0fe48-134">createDownloadCollection</span></span>](downloadmanager-createdownloadcollection.md) |
| [<span data-ttu-id="0fe48-135">Download Manager</span><span class="sxs-lookup"><span data-stu-id="0fe48-135">DownloadManager</span></span>](downloadmanager-object.md) | [<span data-ttu-id="0fe48-136">getdownloadcollection</span><span class="sxs-lookup"><span data-stu-id="0fe48-136">getDownloadCollection</span></span>](downloadmanager-getdownloadcollection.md)       |



 

<span data-ttu-id="0fe48-137">Zum Zweck der Veranschaulichung **Download Manager**. **getdownloadcollection**(*CollectionId*) wird in den Abschnitten der Verweis Syntax verwendet.</span><span class="sxs-lookup"><span data-stu-id="0fe48-137">For purposes of illustration, **DownloadManager**.**getDownloadCollection**(*collectionId*) is used in the reference syntax sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0fe48-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0fe48-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fe48-139">**Referenz für Typ 2-Onlineshops**</span><span class="sxs-lookup"><span data-stu-id="0fe48-139">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




