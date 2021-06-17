---
title: Attribute (Windows Media Format 11 SDK)
description: Erfahren Sie mehr über Attribute im Windows Media Format 11 SDK. Ein Attribut ist ein einzelnes Element von Metadaten.
ms.assetid: 1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4
keywords:
- Windows Media Format SDK, Attribute
- Advanced Systems Format (ASF), Attribute
- ASF (Advanced Systems Format), Attribute
- Attribute,About
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23738e20df2c6360b20b7c3da005cde6b3942d44
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262192"
---
# <a name="attributes-windows-media-format-11-sdk"></a><span data-ttu-id="82681-108">Attribute (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="82681-108">Attributes (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="82681-109">Ein Attribut ist ein einzelnes Element von Metadaten.</span><span class="sxs-lookup"><span data-stu-id="82681-109">An attribute is an individual item of metadata.</span></span> <span data-ttu-id="82681-110">Die meisten Attribute können von Ihrer Anwendung festgelegt werden und werden in den Header einer ASF-Datei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="82681-110">Most of the attributes can be set by your application and are written to the header of an ASF file.</span></span>

<span data-ttu-id="82681-111">Einige der vordefinierten Attribute sind codierte Attribute.</span><span class="sxs-lookup"><span data-stu-id="82681-111">Some of the predefined attributes are coded attributes.</span></span> <span data-ttu-id="82681-112">Diese Attribute werden nicht im Header einer ASF-Datei gespeichert, sondern von den Objekten des Windows Media Format SDK berechnet, wenn die Datei geladen wird.</span><span class="sxs-lookup"><span data-stu-id="82681-112">These attributes are not stored in the header of an ASF file, but are computed by the objects of the Windows Media Format SDK when the file is loaded.</span></span> <span data-ttu-id="82681-113">Da codierte Attribute immer berechnet werden, sind sie grundsätzlich schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="82681-113">Because coded attributes are always computed, they are inherently read-only.</span></span>

<span data-ttu-id="82681-114">Dieses SDK enthält viele Attributdefinitionen, die Sie verwenden können.</span><span class="sxs-lookup"><span data-stu-id="82681-114">This SDK includes many attribute definitions that you can use.</span></span> <span data-ttu-id="82681-115">Sie können auch eigene Attribute erstellen, um Inhalte zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="82681-115">You can also create attributes of your own to describe content.</span></span>

<span data-ttu-id="82681-116">In den folgenden Abschnitten werden die vordefinierten Attribute beschrieben.</span><span class="sxs-lookup"><span data-stu-id="82681-116">The following sections describe the predefined attributes.</span></span>



| <span data-ttu-id="82681-117">`Section`</span><span class="sxs-lookup"><span data-stu-id="82681-117">Section</span></span>                                                                | <span data-ttu-id="82681-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82681-118">Description</span></span>                                                                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82681-119">Attributliste</span><span class="sxs-lookup"><span data-stu-id="82681-119">Attribute List</span></span>](attribute-list.md)                                   | <span data-ttu-id="82681-120">Stellt eine alphabetische Liste aller vordefinierten Attribute zur</span><span class="sxs-lookup"><span data-stu-id="82681-120">Provides an alphabetical list of all of the predefined attributes.</span></span> <span data-ttu-id="82681-121">Nach der Liste wird jedes Attribut einzeln beschrieben.</span><span class="sxs-lookup"><span data-stu-id="82681-121">After the list, each attribute is described individually.</span></span>                                                                          |
| [<span data-ttu-id="82681-122">Attribute mit mehreren Werten</span><span class="sxs-lookup"><span data-stu-id="82681-122">Attributes with Multiple Values</span></span>](attributes-with-multiple-values.md) | <span data-ttu-id="82681-123">Listet die Attribute auf, die einer Datei mehr als einmal hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="82681-123">Lists the attributes that can be added to a file more than once.</span></span>                                                                                                                                      |
| [<span data-ttu-id="82681-124">Attribute nach Typ</span><span class="sxs-lookup"><span data-stu-id="82681-124">Attributes By Type</span></span>](attributes-by-type.md)                           | <span data-ttu-id="82681-125">Enthält Listen von Attributen, die nach Typ sortiert sind.</span><span class="sxs-lookup"><span data-stu-id="82681-125">Contains lists of attributes sorted by type.</span></span> <span data-ttu-id="82681-126">Dazu gehören Listen von Speziellen Attributen (z. B. solche, die sich mit der Verwaltung digitaler Rechte beschäftigen) und Listen mit vorgeschlagenen Attributen nach Inhaltstyp.</span><span class="sxs-lookup"><span data-stu-id="82681-126">These include lists of special-purpose attributes (like those dealing with digital rights management) and lists of suggested attributes by content type.</span></span> |
| [<span data-ttu-id="82681-127">UNTERSTÜTZUNG FÜR ID3-Tags</span><span class="sxs-lookup"><span data-stu-id="82681-127">ID3 Tag Support</span></span>](id3-tag-support.md)                                 | <span data-ttu-id="82681-128">Listet die Attribute auf, die mit ID3-Tags kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="82681-128">Lists the attributes that are compatible with ID3 tags.</span></span>                                                                                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="82681-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="82681-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82681-130">**IWMHeaderInfo::GetAttributeByIndex**</span><span class="sxs-lookup"><span data-stu-id="82681-130">**IWMHeaderInfo::GetAttributeByIndex**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyindex)
</dt> <dt>

[<span data-ttu-id="82681-131">**IWMHeaderInfo::GetAttributeByName**</span><span class="sxs-lookup"><span data-stu-id="82681-131">**IWMHeaderInfo::GetAttributeByName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)
</dt> <dt>

[<span data-ttu-id="82681-132">**IWMHeaderInfo::SetAttribute**</span><span class="sxs-lookup"><span data-stu-id="82681-132">**IWMHeaderInfo::SetAttribute**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute)
</dt> <dt>

[<span data-ttu-id="82681-133">**Arbeiten mit Metadaten**</span><span class="sxs-lookup"><span data-stu-id="82681-133">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




