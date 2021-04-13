---
title: Metadatenfeatures
description: Metadaten werden in ASF-Dateien verwendet, um Dateiinhalte und-Eigenschaften zu beschreiben.
ms.assetid: 01ba09d7-11be-46b1-a0f2-4e35ca5502a8
keywords:
- Windows Media-Format-SDK, Metadatenfeatures
- Windows Media-Format-SDK, Features
- Advanced Systems Format (ASF), Metadatenfeatures
- ASF (Advanced Systems Format), Metadatenfeatures
- Advanced Systems Format (ASF), Features
- ASF (Advanced Systems Format), Features
- Metadaten, Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ea31885a1c1635ee4778683858876572e32262
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104390056"
---
# <a name="metadata-features"></a><span data-ttu-id="be4c1-110">Metadatenfeatures</span><span class="sxs-lookup"><span data-stu-id="be4c1-110">Metadata Features</span></span>

<span data-ttu-id="be4c1-111">Metadaten werden in ASF-Dateien verwendet, um Dateiinhalte und-Eigenschaften zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="be4c1-111">Metadata is used in ASF files to describe file contents and properties.</span></span> <span data-ttu-id="be4c1-112">Alle von Ihnen erstellten ASF-Dateien sollten entsprechende Metadaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="be4c1-112">All ASF files you create should include appropriate metadata.</span></span> <span data-ttu-id="be4c1-113">(Eine Übersicht finden Sie unter [Metadaten](metadata.md).) Das Windows Media-Format SDK bietet Unterstützung für die Metadatenbearbeitung über das Writer-Objekt, das Metadaten-Editor-Objekt und die Reader-und synchronen Reader-Objekte.</span><span class="sxs-lookup"><span data-stu-id="be4c1-113">(For an overview, see [Metadata](metadata.md).) The Windows Media Format SDK includes support for metadata editing through the writer object, the metadata editor object, and both the reader and synchronous reader objects.</span></span> <span data-ttu-id="be4c1-114">Systemeigene Unterstützung für eine Vielzahl von Metadatenattributen ist enthalten.</span><span class="sxs-lookup"><span data-stu-id="be4c1-114">Native support for a wide variety of metadata attributes is included.</span></span> <span data-ttu-id="be4c1-115">Eine Liste der vordefinierten Attribute finden Sie unter [Attribute](attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="be4c1-115">See [Attributes](attributes.md) for a list of the predefined attributes.</span></span>

<span data-ttu-id="be4c1-116">Die Metadatenunterstützung, die von den verschiedenen Objekten des Windows Media Format SDK bereitgestellt wird, ist flexibel und leistungsstark.</span><span class="sxs-lookup"><span data-stu-id="be4c1-116">The metadata support provided by the various objects of the Windows Media Format SDK is flexible and powerful.</span></span> <span data-ttu-id="be4c1-117">Die wichtigsten Metadatenfeatures werden in der folgenden Liste zusammengefasst:</span><span class="sxs-lookup"><span data-stu-id="be4c1-117">The main metadata features are summarized in the following list:</span></span>

-   <span data-ttu-id="be4c1-118">Flexible Attribut Größe.</span><span class="sxs-lookup"><span data-stu-id="be4c1-118">Flexible attribute size.</span></span> <span data-ttu-id="be4c1-119">Metadatenattribute sind nicht in der Größe beschränkt.</span><span class="sxs-lookup"><span data-stu-id="be4c1-119">Metadata attributes are not limited in size.</span></span>
-   <span data-ttu-id="be4c1-120">Attribute auf Streamebene.</span><span class="sxs-lookup"><span data-stu-id="be4c1-120">Stream-level attributes.</span></span> <span data-ttu-id="be4c1-121">Metadaten in ASF-Dateien können der Datei als Ganzes oder einem bestimmten Stream zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="be4c1-121">Metadata in ASF files can be assigned to the file as a whole, or to a particular stream.</span></span>
-   <span data-ttu-id="be4c1-122">Doppelte Attribute.</span><span class="sxs-lookup"><span data-stu-id="be4c1-122">Duplicated attributes.</span></span> <span data-ttu-id="be4c1-123">Ein benanntes Attribut kann mehrmals in derselben Datei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="be4c1-123">A named attribute can be used multiple times in the same file.</span></span> <span data-ttu-id="be4c1-124">Diese Funktion wird besonders beim Zuweisen von beschreibenden Inhalts Attributen verwendet.</span><span class="sxs-lookup"><span data-stu-id="be4c1-124">This feature is of particular use when assigning content descriptive attributes.</span></span> <span data-ttu-id="be4c1-125">Ein-Song kann z. b. mehrere Autoren aufweisen, die jeweils ein separates **Author** -Attribut in der Datei erfordern.</span><span class="sxs-lookup"><span data-stu-id="be4c1-125">For example, a song may have several authors, each requiring a separate **Author** attribute in the file.</span></span>
-   <span data-ttu-id="be4c1-126">Mehrere Sprachen.</span><span class="sxs-lookup"><span data-stu-id="be4c1-126">Multiple languages.</span></span> <span data-ttu-id="be4c1-127">Jedem Attribut ist eine Sprache zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="be4c1-127">Every attribute has a language associated with it.</span></span> <span data-ttu-id="be4c1-128">Sie können die unterstützten Sprachen festlegen und dann einem Attribut zuweisen, das Sie schreiben.</span><span class="sxs-lookup"><span data-stu-id="be4c1-128">You can set the supported languages and then assign one to each attribute you write.</span></span> <span data-ttu-id="be4c1-129">Da Sie Attribute duplizieren können, können Sie die wichtigsten Attribute in mehreren Sprachen bereitstellen, um eine größere Zielgruppe zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="be4c1-129">Because you can duplicate attributes, you can provide the most important attributes in several languages to reach a larger audience.</span></span> <span data-ttu-id="be4c1-130">Wenn Sie keine Sprache angeben, wird die Standardsprache (abgerufen aus dem Betriebssystem des Computers, auf dem die Anwendung ausgeführt wird) verwendet.</span><span class="sxs-lookup"><span data-stu-id="be4c1-130">If you do not specify a language, the default language (obtained from the operating system of the computer running your application) will be used.</span></span>
-   <span data-ttu-id="be4c1-131">Komplexe Attribute.</span><span class="sxs-lookup"><span data-stu-id="be4c1-131">Complex attributes.</span></span> <span data-ttu-id="be4c1-132">Einige der vordefinierten Attribute unterstützen strukturierte Daten.</span><span class="sxs-lookup"><span data-stu-id="be4c1-132">Some of the predefined attributes support structured data.</span></span> <span data-ttu-id="be4c1-133">Für diese Attribute ist der Datentyp binär, aber der Wert ist eine Struktur, die in diesem SDK definiert ist.</span><span class="sxs-lookup"><span data-stu-id="be4c1-133">For these attributes, the data type is binary, but the value is a structure defined in this SDK.</span></span>

<span data-ttu-id="be4c1-134">In den folgenden Themen werden die anderen unterstützten Metadatenfeatures erläutert.</span><span class="sxs-lookup"><span data-stu-id="be4c1-134">The following topics discuss the other supported metadata features.</span></span>



| <span data-ttu-id="be4c1-135">Thema</span><span class="sxs-lookup"><span data-stu-id="be4c1-135">Topic</span></span>                                  | <span data-ttu-id="be4c1-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be4c1-136">Description</span></span>                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="be4c1-137">ID3-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="be4c1-137">ID3 Support</span></span>](id3.md)                 | <span data-ttu-id="be4c1-138">Erläutert die Unterstützung für ID3-Frames mithilfe der Objekte des Windows Media-Format-SDKs.</span><span class="sxs-lookup"><span data-stu-id="be4c1-138">Discusses the support for ID3 frames using the objects of the Windows Media Format SDK.</span></span> |
| [<span data-ttu-id="be4c1-139">Benutzerdefinierte Metadaten</span><span class="sxs-lookup"><span data-stu-id="be4c1-139">Custom Metadata</span></span>](custom-metadata.md) | <span data-ttu-id="be4c1-140">Erläutert die Auswirkungen der Verwendung von benutzerdefinierten Metadaten.</span><span class="sxs-lookup"><span data-stu-id="be4c1-140">Discusses the implications of using custom metadata.</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="be4c1-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="be4c1-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be4c1-142">**Aspekte**</span><span class="sxs-lookup"><span data-stu-id="be4c1-142">**Features**</span></span>](features.md)
</dt> <dt>

[<span data-ttu-id="be4c1-143">**Iwmheaderinfo-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="be4c1-143">**IWMHeaderInfo Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[<span data-ttu-id="be4c1-144">**IWMHeaderInfo2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="be4c1-144">**IWMHeaderInfo2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)
</dt> <dt>

[<span data-ttu-id="be4c1-145">**IWMHeaderInfo3-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="be4c1-145">**IWMHeaderInfo3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)
</dt> <dt>

[<span data-ttu-id="be4c1-146">**Metadaten**</span><span class="sxs-lookup"><span data-stu-id="be4c1-146">**Metadata**</span></span>](metadata.md)
</dt> </dl>

 

 




