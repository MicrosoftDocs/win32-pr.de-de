---
description: Renderer Filter für internen Skript Befehl
ms.assetid: 264cc7c3-987c-4832-85a2-087278a4d024
title: Renderer Filter für internen Skript Befehl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b241643d991e9348015dc51ea5b2f1c4875f079d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521595"
---
# <a name="internal-script-command-renderer-filter"></a><span data-ttu-id="5cdee-103">Renderer Filter für internen Skript Befehl</span><span class="sxs-lookup"><span data-stu-id="5cdee-103">Internal Script Command Renderer Filter</span></span>

<span data-ttu-id="5cdee-104">Empfängt Skript Befehle und sendet Sie an die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="5cdee-104">Receives script commands and dispatches them to the application.</span></span>

<span data-ttu-id="5cdee-105">Dieser Filter akzeptiert Skript Befehle in einem von zwei Formaten:</span><span class="sxs-lookup"><span data-stu-id="5cdee-105">This filter accepts script commands in one of two formats:</span></span>

-   <span data-ttu-id="5cdee-106">MediaType \_ Text: jedes Medien Beispiel enthält eine ANSI-Text Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="5cdee-106">MEDIATYPE\_Text: Each media sample contains an ANSI text string.</span></span>
-   <span data-ttu-id="5cdee-107">MediaType \_ ScriptCommand: jedes Medien Beispiel enthält zwei mit NULL endenden Unicode-Zeichen folgen, die zusammen verkettet sind.</span><span class="sxs-lookup"><span data-stu-id="5cdee-107">MEDIATYPE\_ScriptCommand: Each media sample contains two NULL-terminated Unicode strings, concatenated together.</span></span> <span data-ttu-id="5cdee-108">Die erste Zeichenfolge beschreibt den Befehlstyp, und die zweite Zeichenfolge ist der Skript Befehl.</span><span class="sxs-lookup"><span data-stu-id="5cdee-108">The first string describes the command type and the second string is the script command.</span></span>

    <span data-ttu-id="5cdee-109">Wenn der Filter ein Beispiel empfängt, sendet er eine Ereignis Benachrichtigung für das [**EC- \_ OLE- \_ Ereignis**](ec-ole-event.md) .</span><span class="sxs-lookup"><span data-stu-id="5cdee-109">When the filter receives a sample, it sends an [**EC\_OLE\_EVENT**](ec-ole-event.md) event notification.</span></span> <span data-ttu-id="5cdee-110">Der erste Ereignis Parameter ist ein **BSTR** mit dem Befehlstyp oder, `Text` Wenn das Format MediaType \_ Text ist.</span><span class="sxs-lookup"><span data-stu-id="5cdee-110">The first event parameter is a **BSTR** with the command type, or `Text` if the format is MEDIATYPE\_Text.</span></span> <span data-ttu-id="5cdee-111">Der zweite Ereignis Parameter ist ein **BSTR** mit dem Skript Befehl.</span><span class="sxs-lookup"><span data-stu-id="5cdee-111">The second event parameter is a **BSTR** with the script command.</span></span> <span data-ttu-id="5cdee-112">Die Anwendung kann das Ereignis abrufen und auf den Skript Befehl reagieren.</span><span class="sxs-lookup"><span data-stu-id="5cdee-112">The application can retrieve the event and respond to the script command.</span></span>

<span data-ttu-id="5cdee-113">Ein Beispiel für die Verwendung dieses Filters finden Sie unter [Sami (CC)-Parser](sami--cc--parser-filter.md).</span><span class="sxs-lookup"><span data-stu-id="5cdee-113">For an example of how to use this filter, see [SAMI (CC) Parser](sami--cc--parser-filter.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5cdee-114">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="5cdee-114">Filter Interfaces</span></span></td>
<td><span data-ttu-id="5cdee-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>imediaposition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>imediaseeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="5cdee-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5cdee-116">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="5cdee-116">Input Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="5cdee-117">MEDIATYPE_ScriptCommand MEDIASUBTYPE_NULL</span><span class="sxs-lookup"><span data-stu-id="5cdee-117">MEDIATYPE_ScriptCommand, MEDIASUBTYPE_NULL</span></span></li>
<li><span data-ttu-id="5cdee-118">MEDIATYPE_Text MEDIASUBTYPE_NULL</span><span class="sxs-lookup"><span data-stu-id="5cdee-118">MEDIATYPE_Text, MEDIASUBTYPE_NULL</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5cdee-119">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="5cdee-119">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="5cdee-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="5cdee-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5cdee-121">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="5cdee-121">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="5cdee-122">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="5cdee-122">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5cdee-123">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="5cdee-123">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="5cdee-124">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="5cdee-124">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5cdee-125">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="5cdee-125">Filter CLSID</span></span></td>
<td><span data-ttu-id="5cdee-126">{48025243-2d39-11CE-875d-00608cb78066}</span><span class="sxs-lookup"><span data-stu-id="5cdee-126">{48025243-2D39-11CE-875D-00608CB78066}</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5cdee-127">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="5cdee-127">Property Page CLSID</span></span></td>
<td><span data-ttu-id="5cdee-128">Keine Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="5cdee-128">No property page</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5cdee-129">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="5cdee-129">Executable</span></span></td>
<td><span data-ttu-id="5cdee-130">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="5cdee-130">Quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5cdee-131"><a href="merit.md">Verdienst</a></span><span class="sxs-lookup"><span data-stu-id="5cdee-131"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="5cdee-132">MERIT_PREFERRED + 1</span><span class="sxs-lookup"><span data-stu-id="5cdee-132">MERIT_PREFERRED + 1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5cdee-133"><a href="filter-categories.md">Filter Kategorie</a></span><span class="sxs-lookup"><span data-stu-id="5cdee-133"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="5cdee-134">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="5cdee-134">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="5cdee-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5cdee-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cdee-136">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="5cdee-136">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



