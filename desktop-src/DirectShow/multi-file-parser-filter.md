---
description: Multifile-Parserfilter
ms.assetid: 8ef06f49-fda4-49e2-9b07-70453a2e897c
title: Multifile-Parserfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44fc83a56bb12c307b85be875a3a2e7e73b744d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106338873"
---
# <a name="multi-file-parser-filter"></a><span data-ttu-id="21e93-103">Multifile-Parserfilter</span><span class="sxs-lookup"><span data-stu-id="21e93-103">Multi-File Parser Filter</span></span>

<span data-ttu-id="21e93-104">Der MultiFile-Parserfilter analysiert ein einfaches Dateiformat, das ermöglicht, mehrere Dateinamen anzugeben, als ob es sich um eine Datei handelt.</span><span class="sxs-lookup"><span data-stu-id="21e93-104">The Multi-File Parser filter parses a simple file format that enables multiple file names to be specified as though they were one file.</span></span> <span data-ttu-id="21e93-105">Diese Dateien weisen das Format auf, das im folgenden Beispiel gezeigt wird:</span><span class="sxs-lookup"><span data-stu-id="21e93-105">These files have the format shown in the following example:</span></span>


```C++
;MULTI
https://server/share/video.mpg
https://server/share/captions.smi
```



<span data-ttu-id="21e93-106">Die Verwendung dieses Filters ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="21e93-106">The use of this filter is deprecated.</span></span> <span data-ttu-id="21e93-107">Wenn Sie mehrere Dateien innerhalb desselben Filter Diagramms **Renderen** möchten, sollte die Anwendung immer mehrmals RenderFile oder **addsourcefilter** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="21e93-107">To render multiple files within the same filter graph, the application should simply call **RenderFile** or **AddSourceFilter** multiple times.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="21e93-108">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="21e93-108">Filter interfaces</span></span></td>
<td><span data-ttu-id="21e93-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="21e93-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21e93-110">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="21e93-110">Input pin media types</span></span></td>
<td><ul>
<li><span data-ttu-id="21e93-111">Haupttyp: MEDIATYPE_Stream</span><span class="sxs-lookup"><span data-stu-id="21e93-111">Major type: MEDIATYPE_Stream</span></span></li>
<li><span data-ttu-id="21e93-112">Untertyp: CLSID_MultFile</span><span class="sxs-lookup"><span data-stu-id="21e93-112">Subtype: CLSID_MultFile</span></span></li>
<li><span data-ttu-id="21e93-113">Formattyp: GUID_NULL</span><span class="sxs-lookup"><span data-stu-id="21e93-113">Format type: GUID_NULL</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21e93-114">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="21e93-114">Input pin interfaces</span></span></td>
<td><span data-ttu-id="21e93-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="21e93-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21e93-116">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="21e93-116">Output pin media types</span></span></td>
<td><ul>
<li><span data-ttu-id="21e93-117">Haupttyp: MEDIATYPE_File</span><span class="sxs-lookup"><span data-stu-id="21e93-117">Major type: MEDIATYPE_File</span></span></li>
<li><span data-ttu-id="21e93-118">Untertyp: GUID_NULL</span><span class="sxs-lookup"><span data-stu-id="21e93-118">Subtype: GUID_NULL</span></span></li>
<li><span data-ttu-id="21e93-119">Formattyp: MEDIATYPE_File</span><span class="sxs-lookup"><span data-stu-id="21e93-119">Format type: MEDIATYPE_File</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21e93-120">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="21e93-120">Output pin interfaces</span></span></td>
<td><span data-ttu-id="21e93-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="21e93-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21e93-122">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="21e93-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="21e93-123">CLSID_MultFile</span><span class="sxs-lookup"><span data-stu-id="21e93-123">CLSID_MultFile</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21e93-124">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="21e93-124">Executable</span></span></td>
<td><span data-ttu-id="21e93-125">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="21e93-125">Quartz.dll</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21e93-126"><a href="merit.md">Verdienst</a></span><span class="sxs-lookup"><span data-stu-id="21e93-126"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="21e93-127">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="21e93-127">MERIT_UNLIKELY</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21e93-128"><a href="filter-categories.md">Filter Kategorie</a></span><span class="sxs-lookup"><span data-stu-id="21e93-128"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="21e93-129">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="21e93-129">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="21e93-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21e93-130">Remarks</span></span>

<span data-ttu-id="21e93-131">Der Filter erstellt eine Ausgabe-PIN für jede Datei, die in der Quelldatei aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="21e93-131">The filter creates one output pin for each file listed in the source file.</span></span> <span data-ttu-id="21e93-132">Der Ausgabetyp ist "MediaType \_ file", und der Format Block für den Ausgabetyp ist eine breit Zeichen-Zeichenfolge, die den Dateinamen enthält.</span><span class="sxs-lookup"><span data-stu-id="21e93-132">The output type is MEDIATYPE\_File, and the format block for the output type is a wide-character string that contains the file name.</span></span> <span data-ttu-id="21e93-133">Jede Pin stellt eine Verbindung mit einer Instanz des [Datei Datenstrom](file-stream-renderer-filter.md) -rendererfilters her.</span><span class="sxs-lookup"><span data-stu-id="21e93-133">Each pin connects to an instance of the [File Stream Renderer](file-stream-renderer-filter.md) filter.</span></span> <span data-ttu-id="21e93-134">Der Filter für den Datei Datenstrom-Renderer erstellt eine Ausgabe-PIN, die die [**istreambuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="21e93-134">The File Stream Renderer filter creates one output pin, which exposes the [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) interface.</span></span> <span data-ttu-id="21e93-135">Die Ausgabe-PIN rendert die angegebene Datei.</span><span class="sxs-lookup"><span data-stu-id="21e93-135">The output pin renders the specified file.</span></span> <span data-ttu-id="21e93-136">Zwischen dem MultiFile-Parser und dem Datei Datenstrom-Renderer werden keine Mediendaten übertragen.</span><span class="sxs-lookup"><span data-stu-id="21e93-136">No media data travels between the Multi-File Parser and the File Stream Renderer.</span></span>

<span data-ttu-id="21e93-137">Die CLSID des Filters ist nicht in "UUIDs. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="21e93-137">The filter's CLSID is not defined in Uuids.h.</span></span> <span data-ttu-id="21e93-138">Verwenden Sie dieses Makro in ihrer eigenen Header Datei:</span><span class="sxs-lookup"><span data-stu-id="21e93-138">Use this macro in your own header file:</span></span>


```C++
// {D51BD5A3-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_MultFile,
0xd51bd5a3, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a><span data-ttu-id="21e93-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="21e93-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21e93-140">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="21e93-140">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



