---
description: Filter für Datei Datenstrom-Renderer
ms.assetid: e26462bb-e67f-4522-bec2-88378c4ff442
title: Filter für Datei Datenstrom-Renderer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64c8d8a0c87dab3aa811c8246be24ded8ee04dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522315"
---
# <a name="file-stream-renderer-filter"></a><span data-ttu-id="99aec-103">Filter für Datei Datenstrom-Renderer</span><span class="sxs-lookup"><span data-stu-id="99aec-103">File Stream Renderer Filter</span></span>

<span data-ttu-id="99aec-104">Der Dateistream-rendererfilter rendert Dateinamen, die vom [MultiFile-](multi-file-parser-filter.md) Parserfilter analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="99aec-104">The File Stream Renderer filter renders file names that are parsed by the [Multi-File Parser](multi-file-parser-filter.md) filter.</span></span> <span data-ttu-id="99aec-105">Weitere Informationen finden Sie in der Dokumentation für diesen Filter.</span><span class="sxs-lookup"><span data-stu-id="99aec-105">For more information, see the documentation for that filter.</span></span>

<span data-ttu-id="99aec-106">Die Verwendung dieses Filters ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="99aec-106">The use of this filter is deprecated.</span></span> <span data-ttu-id="99aec-107">Wenn Sie mehrere Dateien innerhalb desselben Filter Diagramms **Renderen** möchten, sollte die Anwendung immer mehrmals RenderFile oder **addsourcefilter** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="99aec-107">To render multiple files within the same filter graph, the application should simply call **RenderFile** or **AddSourceFilter** multiple times.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="99aec-108">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="99aec-108">Filter interfaces</span></span></td>
<td><span data-ttu-id="99aec-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="99aec-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="99aec-110">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="99aec-110">Input pin media types</span></span></td>
<td><ul>
<li><span data-ttu-id="99aec-111">Haupttyp: MEDIATYPE_File</span><span class="sxs-lookup"><span data-stu-id="99aec-111">Major type: MEDIATYPE_File</span></span></li>
<li><span data-ttu-id="99aec-112">Untertyp: GUID_NULL</span><span class="sxs-lookup"><span data-stu-id="99aec-112">Subtype: GUID_NULL</span></span></li>
<li><span data-ttu-id="99aec-113">Formattyp: MEDIATYPE_File</span><span class="sxs-lookup"><span data-stu-id="99aec-113">Format type: MEDIATYPE_File</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="99aec-114">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="99aec-114">Input pin interfaces</span></span></td>
<td><span data-ttu-id="99aec-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="99aec-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="99aec-116">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="99aec-116">Output pin media types</span></span></td>
<td><span data-ttu-id="99aec-117">Keine</span><span class="sxs-lookup"><span data-stu-id="99aec-117">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="99aec-118">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="99aec-118">Output pin interfaces</span></span></td>
<td><span data-ttu-id="99aec-119"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>istreambuilder</strong></a></span><span class="sxs-lookup"><span data-stu-id="99aec-119"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>IStreamBuilder</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="99aec-120">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="99aec-120">Filter CLSID</span></span></td>
<td><span data-ttu-id="99aec-121">CLSID_FileRend</span><span class="sxs-lookup"><span data-stu-id="99aec-121">CLSID_FileRend</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="99aec-122">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="99aec-122">Executable</span></span></td>
<td><span data-ttu-id="99aec-123">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="99aec-123">Quartz.dll</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="99aec-124"><a href="merit.md">Verdienst</a></span><span class="sxs-lookup"><span data-stu-id="99aec-124"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="99aec-125">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="99aec-125">MERIT_UNLIKELY</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="99aec-126"><a href="filter-categories.md">Filter Kategorie</a></span><span class="sxs-lookup"><span data-stu-id="99aec-126"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="99aec-127">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="99aec-127">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="99aec-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99aec-128">Remarks</span></span>

<span data-ttu-id="99aec-129">Die CLSID des Filters ist nicht in "UUIDs. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="99aec-129">The filter's CLSID is not defined in Uuids.h.</span></span> <span data-ttu-id="99aec-130">Verwenden Sie dieses Makro in ihrer eigenen Header Datei:</span><span class="sxs-lookup"><span data-stu-id="99aec-130">Use this macro in your own header file:</span></span>


```C++
// {D51BD5A5-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_FileRend,
0xd51bd5A5, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a><span data-ttu-id="99aec-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="99aec-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99aec-132">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="99aec-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



