---
title: Architektur des Download-Managers
description: Architektur des Download-Managers
ms.assetid: cbd46bf2-613f-40ae-8506-2f3c5eb84ada
keywords:
- Windows Media Player Online Stores, Download-Manager
- Online Stores, Download-Manager
- Typ 2 Online Stores, Download-Manager
- Windows Media Player, Download-Manager
- Windows Media Player Download-Manager
- Download-Manager
- Architektur für Download-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a0567c32430e0cc15ea589bed43e2e81ffb3a08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708561"
---
# <a name="download-manager-architecture"></a><span data-ttu-id="3c35e-110">Architektur des Download-Managers</span><span class="sxs-lookup"><span data-stu-id="3c35e-110">Download Manager Architecture</span></span>

<span data-ttu-id="3c35e-111">Der Windows Media Player Download-Manager verwendet die com-Technologie.</span><span class="sxs-lookup"><span data-stu-id="3c35e-111">The Windows Media Player Download Manager uses COM technology.</span></span> <span data-ttu-id="3c35e-112">Die Funktionalität wird in einer Reihe von Programmierschnittstellen destilliert. Sie können Programmiercode schreiben, der diese Schnittstellen mithilfe von Microsoft JScript oder C++ verwendet.</span><span class="sxs-lookup"><span data-stu-id="3c35e-112">The functionality is distilled into a set of programming interfaces; you can write programming code that uses these interfaces by using Microsoft JScript or C++.</span></span>

<span data-ttu-id="3c35e-113">Die Skriptsprachen verwenden das Konzept von-Objekten, um Programmierfunktionen zu unterteilen.</span><span class="sxs-lookup"><span data-stu-id="3c35e-113">The scripting languages use the concept of objects to divide programming functionality.</span></span> <span data-ttu-id="3c35e-114">Das **Download Manager** -Objektmodell verwendet mehrere Objekte, um die Methoden und Eigenschaften in eine logische Organisation aufzuteilen, in der semantisch verwandte Funktionen gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="3c35e-114">The **DownloadManager** object model uses several objects to divide the methods and properties into a logical organization that groups semantically related functions together.</span></span> <span data-ttu-id="3c35e-115">Die folgenden Abschnitte enthalten Informationen zu den Download-Manager-Objekten.</span><span class="sxs-lookup"><span data-stu-id="3c35e-115">The following sections contain information about the Download Manager objects.</span></span>



| <span data-ttu-id="3c35e-116">`Section`</span><span class="sxs-lookup"><span data-stu-id="3c35e-116">Section</span></span>                                                                     | <span data-ttu-id="3c35e-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3c35e-117">Description</span></span>                                                                                              |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c35e-118">Informationen zum Download Manager-Objekt</span><span class="sxs-lookup"><span data-stu-id="3c35e-118">About the DownloadManager Object</span></span>](#about-the-downloadmanager-object)       | <span data-ttu-id="3c35e-119">Das **Download Manager** -Objekt stellt das Stamm Objekt für den Windows Media Player Download-Manager dar.</span><span class="sxs-lookup"><span data-stu-id="3c35e-119">The **DownloadManager** object represents the root object for the Windows Media Player Download Manager.</span></span> |
| [<span data-ttu-id="3c35e-120">Informationen zum downloadcollection-Objekt</span><span class="sxs-lookup"><span data-stu-id="3c35e-120">About the DownloadCollection Object</span></span>](#about-the-downloadcollection-object) | <span data-ttu-id="3c35e-121">Das **downloadcollection** -Objekt stellt eine Auflistung von Download Elementen dar.</span><span class="sxs-lookup"><span data-stu-id="3c35e-121">The **DownloadCollection** object represents a collection of download items.</span></span>                             |
| [<span data-ttu-id="3c35e-122">Informationen zum "Downloader"-Objekt</span><span class="sxs-lookup"><span data-stu-id="3c35e-122">About the DownloadItem Object</span></span>](#about-the-downloaditem-object)             | <span data-ttu-id="3c35e-123">Das **downloadaditem** -Objekt stellt eine einzelne Download Anforderung dar.</span><span class="sxs-lookup"><span data-stu-id="3c35e-123">The **DownloadItem** object represents an individual download request.</span></span>                                   |



 

## <a name="about-the-downloadmanager-object"></a><span data-ttu-id="3c35e-124">Informationen zum Download Manager-Objekt</span><span class="sxs-lookup"><span data-stu-id="3c35e-124">About the DownloadManager Object</span></span>

<span data-ttu-id="3c35e-125">**Download Manager** ist das Stamm Objekt für den Windows Media Player Download-Manager.</span><span class="sxs-lookup"><span data-stu-id="3c35e-125">**DownloadManager** is the root object for the Windows Media Player Download Manager.</span></span> <span data-ttu-id="3c35e-126">Der Zugriff auf alle anderen Objekte erfolgt über dieses Objekt.</span><span class="sxs-lookup"><span data-stu-id="3c35e-126">All other objects are accessed through this object.</span></span> <span data-ttu-id="3c35e-127">Um Zugriff auf das **Download Manager** -Objekt zu erhalten, verwenden Sie die folgende JScript-Syntax:</span><span class="sxs-lookup"><span data-stu-id="3c35e-127">To gain access to the **DownloadManager** object, use the following JScript syntax:</span></span>


```C++
var DownloadManager = external.DownloadManager;
```



<span data-ttu-id="3c35e-128">Dadurch wird eine Instanz des **Downloadmanager** -Objekts erstellt, die dann zum Abrufen der untergeordneten Objekte verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3c35e-128">This creates an instance of the **DownloadManager** object, which can then be used to retrieve the child objects.</span></span> <span data-ttu-id="3c35e-129">Mit der folgenden Syntax wird z. b. das erste Element aus der Download Auflistung mit der ID-Nummer 253675 abgerufen:</span><span class="sxs-lookup"><span data-stu-id="3c35e-129">For example, the following syntax retrieves the first item from the download collection that has id number 253675:</span></span>


```C++
var firstItem = DownloadManager.getDownloadCollection(253675).item(0);
```



## <a name="about-the-downloadcollection-object"></a><span data-ttu-id="3c35e-130">Informationen zum downloadcollection-Objekt</span><span class="sxs-lookup"><span data-stu-id="3c35e-130">About the DownloadCollection Object</span></span>

<span data-ttu-id="3c35e-131">Das **downloadcollection** -Objekt stellt eine Auflistung der herunter zuladenden Dateien dar.</span><span class="sxs-lookup"><span data-stu-id="3c35e-131">The **DownloadCollection** object represents a collection of files to be downloaded.</span></span> <span data-ttu-id="3c35e-132">Mit diesem Objekt können Sie feststellen, wie viele Downloads in der Sammlung sind, Elemente aus der Sammlung entfernen, ein bestimmtes Download Element abrufen und einen neuen Download starten.</span><span class="sxs-lookup"><span data-stu-id="3c35e-132">You can use this object to determine how many downloads are in the collection, remove items from the collection, retrieve a specific download item, and to start a new download.</span></span> <span data-ttu-id="3c35e-133">Beim Starten eines neuen Downloads wird der Download automatisch der Sammlung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3c35e-133">Starting a new download automatically adds the download to the collection.</span></span>

## <a name="about-the-downloaditem-object"></a><span data-ttu-id="3c35e-134">Informationen zum "Downloader"-Objekt</span><span class="sxs-lookup"><span data-stu-id="3c35e-134">About the DownloadItem Object</span></span>

<span data-ttu-id="3c35e-135">Das **downloadaditem** -Objekt stellt einen einzelnen Download dar.</span><span class="sxs-lookup"><span data-stu-id="3c35e-135">The **DownloadItem** object represents an individual download.</span></span> <span data-ttu-id="3c35e-136">Download Elemente sind immer als Teil einer Download Sammlung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3c35e-136">Download items always exist as part of a download collection.</span></span> <span data-ttu-id="3c35e-137">Verwenden Sie dieses Objekt, um Informationen zum Download Element abzurufen und den aktuell ausgeführten Download anzuhalten, fortzusetzen oder abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="3c35e-137">Use this object to retrieve information about the download item and to pause, resume, or cancel the download in progress.</span></span>

<span data-ttu-id="3c35e-138">Wenn Sie einen Download abbrechen, bleibt das Download Element in der Download Sammlung erhalten.</span><span class="sxs-lookup"><span data-stu-id="3c35e-138">When you cancel a download, the download item remains in place in its download collection.</span></span> <span data-ttu-id="3c35e-139">In diesem Fall **downloadcollection**. **DownloadState** Ruft den Wert 4 ab, d. h. abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="3c35e-139">In this case, **downloadCollection**.**downloadState** retrieves a value of 4, meaning canceled.</span></span>

<span data-ttu-id="3c35e-140">Sie können " **Downloader**" verwenden. der **Fortschritt** , um den Benutzer darüber zu informieren, welcher Teil der Datei übertragen wurde oder wie viel heruntergeladen werden muss.</span><span class="sxs-lookup"><span data-stu-id="3c35e-140">You can use **downloadItem**.**progress** to inform the user about how much of the file has been transferred or how much remains to be downloaded.</span></span> <span data-ttu-id="3c35e-141">Sie können diesen Wert auch verwenden, um die verbleibende Zeit zu schätzen.</span><span class="sxs-lookup"><span data-stu-id="3c35e-141">You might use this value to estimate the time remaining as well.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c35e-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3c35e-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c35e-143">**Download-Manager**</span><span class="sxs-lookup"><span data-stu-id="3c35e-143">**Download Manager**</span></span>](download-manager.md)
</dt> </dl>

 

 




