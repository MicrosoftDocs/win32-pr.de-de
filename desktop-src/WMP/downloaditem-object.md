---
title: Download Item-Objekt
description: Download Item-Objekt
ms.assetid: 668ee632-0a3d-426b-baab-08e88b9fc607
keywords:
- Windows Media Player Online Stores, Downloader-Objekt
- Online Stores, Download Item-Objekt
- Typ 2 Online Stores, Downloader-Objekt
- Download Item
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c367eee37f2f4d8329d71f3d42a3c78771a50a6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337393"
---
# <a name="downloaditem-object"></a><span data-ttu-id="f9c74-107">Download Item-Objekt</span><span class="sxs-lookup"><span data-stu-id="f9c74-107">DownloadItem Object</span></span>

> [!Note]  
> <span data-ttu-id="f9c74-108">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="f9c74-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="f9c74-109">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f9c74-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="f9c74-110">Das **downloadaditem** -Objekt stellt eine Datei Download Anforderung dar.</span><span class="sxs-lookup"><span data-stu-id="f9c74-110">The **DownloadItem** object represents a file download request.</span></span> <span data-ttu-id="f9c74-111">Sie kann von Webseiten verwendet werden, die im vollständigen Windows-Media Player gehostet werden und Zugriff auf das **externe** Objekt haben, z. b. Premium-Dienste.</span><span class="sxs-lookup"><span data-stu-id="f9c74-111">It can be used by webpages that are hosted in the full mode Windows Media Player and that have access to the **External** object, such as premium services.</span></span>

<span data-ttu-id="f9c74-112">Das Objekt " **Downloader** " unterstützt die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f9c74-112">The **DownloadItem** object supports the following properties.</span></span>



| <span data-ttu-id="f9c74-113">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f9c74-113">Property</span></span>                                        | <span data-ttu-id="f9c74-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9c74-114">Description</span></span>                                      |
|-------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="f9c74-115">Download Status</span><span class="sxs-lookup"><span data-stu-id="f9c74-115">downloadState</span></span>](downloaditem-downloadstate.md) | <span data-ttu-id="f9c74-116">Ruft den Status des Downloads ab.</span><span class="sxs-lookup"><span data-stu-id="f9c74-116">Retrieves the state of the download.</span></span>             |
| [<span data-ttu-id="f9c74-117">Progress</span><span class="sxs-lookup"><span data-stu-id="f9c74-117">progress</span></span>](downloaditem-progress.md)           | <span data-ttu-id="f9c74-118">Ruft den Fortschritt des Downloads in Bytes ab.</span><span class="sxs-lookup"><span data-stu-id="f9c74-118">Retrieves the progress of the download in bytes.</span></span> |
| [<span data-ttu-id="f9c74-119">size</span><span class="sxs-lookup"><span data-stu-id="f9c74-119">size</span></span>](downloaditem-size.md)                   | <span data-ttu-id="f9c74-120">Ruft die Größe des Downloads ab.</span><span class="sxs-lookup"><span data-stu-id="f9c74-120">Retrieves the size of the download.</span></span>              |
| [<span data-ttu-id="f9c74-121">SourceURL</span><span class="sxs-lookup"><span data-stu-id="f9c74-121">sourceURL</span></span>](downloaditem-sourceurl.md)         | <span data-ttu-id="f9c74-122">Ruft die Quell-URL des Downloads ab.</span><span class="sxs-lookup"><span data-stu-id="f9c74-122">Retrieves the source URL of the download.</span></span>        |
| [<span data-ttu-id="f9c74-123">type</span><span class="sxs-lookup"><span data-stu-id="f9c74-123">type</span></span>](downloaditem-type.md)                   | <span data-ttu-id="f9c74-124">Ruft den Typ des Downloads ab.</span><span class="sxs-lookup"><span data-stu-id="f9c74-124">Retrieves the type of the download.</span></span>              |



 

<span data-ttu-id="f9c74-125">Das Objekt " **Downloader** " unterstützt die folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="f9c74-125">The **DownloadItem** object supports the following methods.</span></span>



| <span data-ttu-id="f9c74-126">Methode</span><span class="sxs-lookup"><span data-stu-id="f9c74-126">Method</span></span>                                      | <span data-ttu-id="f9c74-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9c74-127">Description</span></span>                                                |
|---------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="f9c74-128">cancel</span><span class="sxs-lookup"><span data-stu-id="f9c74-128">cancel</span></span>](downloaditem-cancel.md)           | <span data-ttu-id="f9c74-129">Bricht den Download ab.</span><span class="sxs-lookup"><span data-stu-id="f9c74-129">Cancels the download.</span></span>                                      |
| [<span data-ttu-id="f9c74-130">getItemInfo</span><span class="sxs-lookup"><span data-stu-id="f9c74-130">getItemInfo</span></span>](downloaditem-getiteminfo.md) | <span data-ttu-id="f9c74-131">Ruft den Wert eines Attributs für das Download Element ab.</span><span class="sxs-lookup"><span data-stu-id="f9c74-131">Retrieves the value of an attribute for the download item.</span></span> |
| [<span data-ttu-id="f9c74-132">pause</span><span class="sxs-lookup"><span data-stu-id="f9c74-132">pause</span></span>](downloaditem-pause.md)             | <span data-ttu-id="f9c74-133">Hält den Download an.</span><span class="sxs-lookup"><span data-stu-id="f9c74-133">Pauses the download.</span></span>                                       |
| [<span data-ttu-id="f9c74-134">zusetzen</span><span class="sxs-lookup"><span data-stu-id="f9c74-134">resume</span></span>](downloaditem-resume.md)           | <span data-ttu-id="f9c74-135">Der Download wird fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="f9c74-135">Resumes the download.</span></span>                                      |



 

<span data-ttu-id="f9c74-136">Der Zugriff auf das **Download** Item-Objekt erfolgt über die folgende Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f9c74-136">The **DownloadItem** object is accessed through the following property.</span></span>



| <span data-ttu-id="f9c74-137">Object</span><span class="sxs-lookup"><span data-stu-id="f9c74-137">Object</span></span>                                              | <span data-ttu-id="f9c74-138">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f9c74-138">Property</span></span>                            |
|-----------------------------------------------------|-------------------------------------|
| [<span data-ttu-id="f9c74-139">Download Sammlung</span><span class="sxs-lookup"><span data-stu-id="f9c74-139">DownloadCollection</span></span>](downloadcollection-object.md) | [<span data-ttu-id="f9c74-140">item</span><span class="sxs-lookup"><span data-stu-id="f9c74-140">item</span></span>](downloadcollection-item.md) |



 

<span data-ttu-id="f9c74-141">Zum Zweck der Veranschaulichung **Download Manager**. **getdownloadcollection**(*CollectionId*). **Item**(*ItemID*) wird in den Abschnitten der Verweis Syntax verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9c74-141">For purposes of illustration, **DownloadManager**.**getDownloadCollection**(*collectionId*).**item**(*itemId*) is used in the reference syntax sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9c74-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f9c74-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9c74-143">**Referenz für Typ 2-Onlineshops**</span><span class="sxs-lookup"><span data-stu-id="f9c74-143">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




