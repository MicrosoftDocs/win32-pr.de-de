---
title: Arbeiten mit Metadaten
description: Arbeiten mit Metadaten
ms.assetid: 15d835c2-e227-4e69-a8b2-9b1c6d671022
keywords:
- Windows Media-Format-SDK, Übersicht über Metadaten
- Advanced Systems Format (ASF), Übersicht über Metadaten
- ASF (Advanced Systems Format), Übersicht über Metadaten
- Metadaten, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050336d18947059373ddccf3f18e5d4295834293
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104390064"
---
# <a name="working-with-metadata"></a><span data-ttu-id="d1cfd-107">Arbeiten mit Metadaten</span><span class="sxs-lookup"><span data-stu-id="d1cfd-107">Working with Metadata</span></span>

<span data-ttu-id="d1cfd-108">Metadatenunterstützung wird durch das Writer-Objekt, das Reader-und das synchrone Reader-Objekt und das Metadaten-Editor-Objekt bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d1cfd-108">Metadata support is provided by the writer object, the reader and synchronous reader objects, and the metadata editor object.</span></span> <span data-ttu-id="d1cfd-109">Allgemeine Informationen zu Metadaten finden Sie unter [Metadaten](metadata.md).</span><span class="sxs-lookup"><span data-stu-id="d1cfd-109">For general information about metadata, see [Metadata](metadata.md).</span></span> <span data-ttu-id="d1cfd-110">Informationen zu den Funktionen, die Metadaten im Windows Media Format SDK unterstützen, finden Sie unter [Metadatenfeatures](metadata-features.md).</span><span class="sxs-lookup"><span data-stu-id="d1cfd-110">For information about the features supporting metadata in the Windows Media Format SDK, see [Metadata Features](metadata-features.md).</span></span>

<span data-ttu-id="d1cfd-111">Die Schnittstelle für die Metadatenbearbeitung ist [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3). Diese können Sie abrufen, indem Sie die **QueryInterface** -Methode einer beliebigen Schnittstelle in einem der oben aufgeführten Objekte aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d1cfd-111">The interface for metadata editing is [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), which you can obtain by calling the **QueryInterface** method of any interface in one of the objects listed above.</span></span> <span data-ttu-id="d1cfd-112">**IWMHeaderInfo3** erbt die Methoden von " [**iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) " und " [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)".</span><span class="sxs-lookup"><span data-stu-id="d1cfd-112">**IWMHeaderInfo3** inherits the methods of [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) and [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2).</span></span> <span data-ttu-id="d1cfd-113">Die Methoden von **IWMHeaderInfo3** , die sich mit Metadatenattributen befassen, stellen einen anderen Ansatz für den Zugriff auf Metadaten dar als die, die von den Methoden von **iwmheaderinfo** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1cfd-113">The methods of **IWMHeaderInfo3** that deal with metadata attributes represent a different approach to accessing metadata than that used by the methods of **IWMHeaderInfo**.</span></span> <span data-ttu-id="d1cfd-114">Die neueren Methoden sollten immer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1cfd-114">You should always use the newer methods.</span></span>

<span data-ttu-id="d1cfd-115">Metadaten in einer ASF-Datei werden durch einen Index und eine streamnummer identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d1cfd-115">Metadata in an ASF file is identified by an index and a stream number.</span></span> <span data-ttu-id="d1cfd-116">Attributen auf Dateiebene wird eine streamnummer von 0 zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="d1cfd-116">File-level attributes are assigned a stream number of 0.</span></span> <span data-ttu-id="d1cfd-117">In früheren Versionen des SDK für den Windows Media-Format konnten Attribute anhand des Namens identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="d1cfd-117">In previous versions of the Windows Media Format SDK, attributes could be identified by name.</span></span> <span data-ttu-id="d1cfd-118">Da Sie nun jedoch Attributnamen innerhalb eines Streams duplizieren können, ist dies nicht mehr möglich.</span><span class="sxs-lookup"><span data-stu-id="d1cfd-118">However, because you can now duplicate attribute names within a stream, this is no longer possible.</span></span> <span data-ttu-id="d1cfd-119">Stattdessen können Sie alle Indizes abrufen, die mit einem Namen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="d1cfd-119">Instead, you can retrieve all the indexes matching a name.</span></span> <span data-ttu-id="d1cfd-120">Weitere Informationen finden Sie unter [Abrufen von Metadatenattributen](retrieving-metadata-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="d1cfd-120">For more information, see [Retrieving Metadata Attributes](retrieving-metadata-attributes.md).</span></span>

<span data-ttu-id="d1cfd-121">Um das Auffinden von Attributen zu erleichtern, können Sie eine spezielle streamnummer (0xFFFF) verwenden.</span><span class="sxs-lookup"><span data-stu-id="d1cfd-121">To aid in finding attributes quickly, you can use a special stream number, 0xFFFF.</span></span> <span data-ttu-id="d1cfd-122">Verwenden Sie diese streamnummer, um die Datei als Ganzes zu identifizieren, anstatt einen bestimmten Stream oder die Attribute auf Dateiebene.</span><span class="sxs-lookup"><span data-stu-id="d1cfd-122">Use this stream number to identify the file as a whole, rather than a specific stream or the file-level attributes.</span></span> <span data-ttu-id="d1cfd-123">Die Objekte des Windows Media Format SDK behalten separate Indizes für jeden Stream und die Attribute auf Dateiebene.</span><span class="sxs-lookup"><span data-stu-id="d1cfd-123">The objects of the Windows Media Format SDK maintain separate indexes for each stream and for the file-level attributes.</span></span> <span data-ttu-id="d1cfd-124">Wenn Sie Stream 0xFFFF verwenden, unterscheiden sich die Indizes von den Indizes, die Sie beim Angeben eines bestimmten Datenstroms verwenden.</span><span class="sxs-lookup"><span data-stu-id="d1cfd-124">When using stream 0xFFFF, the indexes are different from those you use when specifying a specific stream.</span></span> <span data-ttu-id="d1cfd-125">Beispielsweise ist das-Attribut, das Index 0 für Stream 0 ist, nicht mit dem-Attribut identisch, das Index 0 für Stream 0xFFFF ist.</span><span class="sxs-lookup"><span data-stu-id="d1cfd-125">For example, the attribute that is index 0 for stream 0 will not be the same as the attribute that is index 0 for stream 0xFFFF.</span></span>

<span data-ttu-id="d1cfd-126">In den folgenden Abschnitten wird die Verwendung von Metadaten ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d1cfd-126">The following sections describe the use of metadata in greater detail.</span></span>



| <span data-ttu-id="d1cfd-127">`Section`</span><span class="sxs-lookup"><span data-stu-id="d1cfd-127">Section</span></span>                                                                    | <span data-ttu-id="d1cfd-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d1cfd-128">Description</span></span>                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="d1cfd-129">Abrufen von Metadatenattributen</span><span class="sxs-lookup"><span data-stu-id="d1cfd-129">Retrieving Metadata Attributes</span></span>](retrieving-metadata-attributes.md)       | <span data-ttu-id="d1cfd-130">Beschreibt, wie Metadatenattribute aus einem Dateiheader gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="d1cfd-130">Describes how to read metadata attributes from a file header.</span></span>                     |
| [<span data-ttu-id="d1cfd-131">Festlegen von Metadatenattributen</span><span class="sxs-lookup"><span data-stu-id="d1cfd-131">Setting Metadata Attributes</span></span>](setting-metadata-attributes.md)             | <span data-ttu-id="d1cfd-132">Beschreibt das Hinzufügen neuer Metadatenattribute zu einem Dateiheader.</span><span class="sxs-lookup"><span data-stu-id="d1cfd-132">Describes how to add new metadata attributes to a file header.</span></span>                    |
| [<span data-ttu-id="d1cfd-133">Bearbeiten von Metadatenattributen</span><span class="sxs-lookup"><span data-stu-id="d1cfd-133">Editing Metadata Attributes</span></span>](editing-metadata-attributes.md)             | <span data-ttu-id="d1cfd-134">Beschreibt, wie vorhandene Metadatenattribute bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="d1cfd-134">Describes how to edit existing metadata attributes.</span></span>                               |
| [<span data-ttu-id="d1cfd-135">Entfernen von Metadatenattributen</span><span class="sxs-lookup"><span data-stu-id="d1cfd-135">Removing Metadata Attributes</span></span>](removing-metadata-attributes.md)           | <span data-ttu-id="d1cfd-136">Beschreibt, wie vorhandene Metadatenattribute entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="d1cfd-136">Describes how to remove existing metadata attributes.</span></span>                             |
| [<span data-ttu-id="d1cfd-137">Verwenden komplexer Metadatenattribute</span><span class="sxs-lookup"><span data-stu-id="d1cfd-137">Using Complex Metadata Attributes</span></span>](using-complex-metadata-attributes.md) | <span data-ttu-id="d1cfd-138">Beschreibt, wie Sie mit Attributen arbeiten, deren Werte durch-Strukturen dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d1cfd-138">Describes how to work with attributes whose values are represented by structures.</span></span> |



 

<span data-ttu-id="d1cfd-139">Einige der Beispielanwendungen zeigen, wie Metadaten abgerufen und bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="d1cfd-139">Several of the sample applications show how to retrieve and edit metadata.</span></span> <span data-ttu-id="d1cfd-140">Lesen Sie insbesondere das MetadataEdit-Beispiel, das sowohl in der C++-als auch in der c#-Version verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d1cfd-140">In particular, see the MetadataEdit sample, which comes in both C++ and C# versions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1cfd-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d1cfd-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1cfd-142">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="d1cfd-142">**Attributes**</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="d1cfd-143">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="d1cfd-143">**Programming Guide**</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="d1cfd-144">**Beispielanwendungen**</span><span class="sxs-lookup"><span data-stu-id="d1cfd-144">**Sample Applications**</span></span>](sample-applications.md)
</dt> </dl>

 

 




