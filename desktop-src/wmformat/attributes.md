---
title: Attribute (Windows Media-Format 11 SDK)
description: Attribute
ms.assetid: 1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4
keywords:
- Windows Media-Format-SDK, Attribute
- Advanced Systems Format (ASF), Attribute
- ASF (Advanced Systems Format), Attribute
- Attribute, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c209558ed4803fee96e9b482302af1864cbf988b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391426"
---
# <a name="attributes-windows-media-format-11-sdk"></a><span data-ttu-id="c19b1-107">Attribute (Windows Media-Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="c19b1-107">Attributes (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="c19b1-108">Bei einem Attribut handelt es sich um ein einzelnes Element von Metadaten.</span><span class="sxs-lookup"><span data-stu-id="c19b1-108">An attribute is an individual item of metadata.</span></span> <span data-ttu-id="c19b1-109">Die meisten Attribute können von der Anwendung festgelegt und in den Header einer ASF-Datei geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c19b1-109">Most of the attributes can be set by your application and are written to the header of an ASF file.</span></span>

<span data-ttu-id="c19b1-110">Einige der vordefinierten Attribute sind codierte Attribute.</span><span class="sxs-lookup"><span data-stu-id="c19b1-110">Some of the predefined attributes are coded attributes.</span></span> <span data-ttu-id="c19b1-111">Diese Attribute werden nicht im Header einer ASF-Datei gespeichert, sondern durch die Objekte des Windows Media Format SDK berechnet, wenn die Datei geladen wird.</span><span class="sxs-lookup"><span data-stu-id="c19b1-111">These attributes are not stored in the header of an ASF file, but are computed by the objects of the Windows Media Format SDK when the file is loaded.</span></span> <span data-ttu-id="c19b1-112">Da codierte Attribute immer berechnet werden, sind Sie grundsätzlich schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c19b1-112">Because coded attributes are always computed, they are inherently read-only.</span></span>

<span data-ttu-id="c19b1-113">Dieses SDK enthält viele Attribut Definitionen, die Sie verwenden können.</span><span class="sxs-lookup"><span data-stu-id="c19b1-113">This SDK includes many attribute definitions that you can use.</span></span> <span data-ttu-id="c19b1-114">Sie können auch eigene Attribute erstellen, um Inhalte zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c19b1-114">You can also create attributes of your own to describe content.</span></span>

<span data-ttu-id="c19b1-115">In den folgenden Abschnitten werden die vordefinierten Attribute beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c19b1-115">The following sections describe the predefined attributes.</span></span>



| <span data-ttu-id="c19b1-116">`Section`</span><span class="sxs-lookup"><span data-stu-id="c19b1-116">Section</span></span>                                                                | <span data-ttu-id="c19b1-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c19b1-117">Description</span></span>                                                                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c19b1-118">Attributliste</span><span class="sxs-lookup"><span data-stu-id="c19b1-118">Attribute List</span></span>](attribute-list.md)                                   | <span data-ttu-id="c19b1-119">Stellt eine alphabetische Liste aller vordefinierten Attribute bereit.</span><span class="sxs-lookup"><span data-stu-id="c19b1-119">Provides an alphabetical list of all of the predefined attributes.</span></span> <span data-ttu-id="c19b1-120">Nach der Liste wird jedes Attribut einzeln beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c19b1-120">After the list, each attribute is described individually.</span></span>                                                                          |
| [<span data-ttu-id="c19b1-121">Attribute mit mehreren Werten</span><span class="sxs-lookup"><span data-stu-id="c19b1-121">Attributes with Multiple Values</span></span>](attributes-with-multiple-values.md) | <span data-ttu-id="c19b1-122">Listet die Attribute auf, die einer Datei mehrmals hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="c19b1-122">Lists the attributes that can be added to a file more than once.</span></span>                                                                                                                                      |
| [<span data-ttu-id="c19b1-123">Attribute nach Typ</span><span class="sxs-lookup"><span data-stu-id="c19b1-123">Attributes By Type</span></span>](attributes-by-type.md)                           | <span data-ttu-id="c19b1-124">Enthält Listen von Attributen, sortiert nach Typ.</span><span class="sxs-lookup"><span data-stu-id="c19b1-124">Contains lists of attributes sorted by type.</span></span> <span data-ttu-id="c19b1-125">Hierzu zählen Listen mit speziellen Attributen (wie z. b. die, die mit Digital Rights Management arbeiten) und Listen der vorgeschlagenen Attribute nach Inhaltstyp.</span><span class="sxs-lookup"><span data-stu-id="c19b1-125">These include lists of special-purpose attributes (like those dealing with digital rights management) and lists of suggested attributes by content type.</span></span> |
| [<span data-ttu-id="c19b1-126">Unterstützung für Unterstützung</span><span class="sxs-lookup"><span data-stu-id="c19b1-126">ID3 Tag Support</span></span>](id3-tag-support.md)                                 | <span data-ttu-id="c19b1-127">Listet die Attribute auf, die mit ID3-Tags kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="c19b1-127">Lists the attributes that are compatible with ID3 tags.</span></span>                                                                                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="c19b1-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c19b1-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c19b1-129">**Iwmheaderinfo:: getattributebyindex**</span><span class="sxs-lookup"><span data-stu-id="c19b1-129">**IWMHeaderInfo::GetAttributeByIndex**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyindex)
</dt> <dt>

[<span data-ttu-id="c19b1-130">**Iwmheaderinfo:: getattributebyname**</span><span class="sxs-lookup"><span data-stu-id="c19b1-130">**IWMHeaderInfo::GetAttributeByName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)
</dt> <dt>

[<span data-ttu-id="c19b1-131">**Iwmheaderinfo:: Event Tribute**</span><span class="sxs-lookup"><span data-stu-id="c19b1-131">**IWMHeaderInfo::SetAttribute**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute)
</dt> <dt>

[<span data-ttu-id="c19b1-132">**Arbeiten mit Metadaten**</span><span class="sxs-lookup"><span data-stu-id="c19b1-132">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




