---
title: Reference-Element (veraltet)
description: Reference-Element (veraltet)
ms.assetid: 0a549750-abaa-43bf-8420-8fe00eb6feff
keywords:
- Windows Media-Metadatendateien, Reference-Element
- Metadatendateien, Reference-Element
- Reference-Element
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c521b080609bbe51470a2de960481a86e8264c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342068"
---
# <a name="reference-element-deprecated"></a><span data-ttu-id="fbab7-106">Reference-Element (veraltet)</span><span class="sxs-lookup"><span data-stu-id="fbab7-106">reference Element (deprecated)</span></span>

<span data-ttu-id="fbab7-107">In diesem Thema wird eine Funktion beschrieben, die in der aktuellen Version von Windows Media Metafiles nicht mehr verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fbab7-107">This topic documents a feature that is no longer used in the current version of Windows Media Metafiles.</span></span>

<span data-ttu-id="fbab7-108">Das **Reference** -Element enthält eine Liste mit Verweisen auf URLs.</span><span class="sxs-lookup"><span data-stu-id="fbab7-108">The **reference** element contains a list of references to URLs.</span></span> <span data-ttu-id="fbab7-109">Jedes Element in der Liste hat das Format Ref *xx*  =  *URL*, wobei *xx* eine ganze Zahl und *URL* die URL einer ASF-Datei (Advanced Systems Format) ist.</span><span class="sxs-lookup"><span data-stu-id="fbab7-109">Each item in the list has the form Ref *XX* = *URL*, where *XX* is an integer and *URL* is the URL of an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="fbab7-110">**Syntax**</span><span class="sxs-lookup"><span data-stu-id="fbab7-110">**Syntax**</span></span>


```XML
[reference]
RefXX = URL
RefXX = URL
   
<entity type="hellip"/>
```



<span data-ttu-id="fbab7-111">Die von *xx* dargestellten ganzzahligen müssen in aufsteigender Reihenfolge vorliegen.</span><span class="sxs-lookup"><span data-stu-id="fbab7-111">The integers represented by *XX* must be in ascending order.</span></span> <span data-ttu-id="fbab7-112">Das heißt, die Ganzzahl in jeder Zeile muss größer als die ganze Zahl in der vorherigen Zeile sein.</span><span class="sxs-lookup"><span data-stu-id="fbab7-112">That is, the integer in each line must be greater than the integer in the preceding line.</span></span>

<span data-ttu-id="fbab7-113">Wenn ein Client Programm ein Verweis Element liest, versucht es, eine Verbindung mit der Mediendatei herzustellen, die durch die erste URL in der Liste repräsentiert wird.</span><span class="sxs-lookup"><span data-stu-id="fbab7-113">When a client program reads a reference element, it attempts to connect to the media file represented by the first URL in the list.</span></span> <span data-ttu-id="fbab7-114">Wenn dies fehlschlägt, versucht das Client Programm, eine Verbindung mit der durch die nächste URL in der Liste dargestellten Datei herzustellen.</span><span class="sxs-lookup"><span data-stu-id="fbab7-114">If that fails, the client program attempts to connect to the file represented by the next URL in the list.</span></span> <span data-ttu-id="fbab7-115">Das Client Programm fährt fort, bis eine erfolgreiche Verbindung hergestellt wurde oder das Ende der Liste erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="fbab7-115">The client program continues down the list until it makes a successful connection or reaches the end of the list.</span></span> <span data-ttu-id="fbab7-116">Beachten Sie Folgendes: Wenn das Client Programm erfolgreich eine Verbindung herstellt, liest es keine der nachfolgenden URLs in der Liste.</span><span class="sxs-lookup"><span data-stu-id="fbab7-116">Note that if the client program makes a successful connection, it does not read any of the subsequent URLs in the list.</span></span>

<span data-ttu-id="fbab7-117">**Beispiel Code**</span><span class="sxs-lookup"><span data-stu-id="fbab7-117">**Example Code**</span></span>

<span data-ttu-id="fbab7-118">Im folgenden Beispiel versucht das Client Programm zuerst, eine Verbindung mit der durch die MMS-URL dargestellten Datei herzustellen.</span><span class="sxs-lookup"><span data-stu-id="fbab7-118">In the following example, the client program would first attempt to connect to the file represented by the mms URL.</span></span> <span data-ttu-id="fbab7-119">Wenn dies nicht der Fall ist, versucht das Client Programm, eine Verbindung mit der durch die http-URL dargestellten Datei herzustellen.</span><span class="sxs-lookup"><span data-stu-id="fbab7-119">If that failed, the client program would attempt to connect to the file represented by the http URL.</span></span>


```XML
[reference]
Ref01 = mms://example.com/MusicFile.wma
Ref02 = https://example.com/MusicFile.wma

```



## <a name="remarks"></a><span data-ttu-id="fbab7-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fbab7-120">Remarks</span></span>

<span data-ttu-id="fbab7-121">Das Format der ASF-Datei umfasst eine Vielzahl von Medientypen, einschließlich Audiodaten und Videos.</span><span class="sxs-lookup"><span data-stu-id="fbab7-121">The ASF file format encompasses a wide variety of media types including audio and video.</span></span> <span data-ttu-id="fbab7-122">Bei ASF-Dateien werden auch mehrere verschiedene Dateinamen Erweiterungen verwendet, einschließlich. WMA und. wmv.</span><span class="sxs-lookup"><span data-stu-id="fbab7-122">ASF files also use several different file name extensions, including .wma and .wmv.</span></span>

<span data-ttu-id="fbab7-123">Die von *xx* dargestellten ganzzahligen müssen in aufsteigender Reihenfolge vorliegen.</span><span class="sxs-lookup"><span data-stu-id="fbab7-123">The integers represented by *XX* must be in ascending order.</span></span> <span data-ttu-id="fbab7-124">Das heißt, die Ganzzahl in jeder Zeile muss größer als die ganze Zahl in der vorherigen Zeile sein.</span><span class="sxs-lookup"><span data-stu-id="fbab7-124">That is, the integer in each line must be greater than the integer in the preceding line.</span></span>

<span data-ttu-id="fbab7-125">Wenn ein Client Programm ein Verweis Element liest, versucht es, eine Verbindung mit der Mediendatei herzustellen, die durch die erste URL in der Liste repräsentiert wird.</span><span class="sxs-lookup"><span data-stu-id="fbab7-125">When a client program reads a reference element, it attempts to connect to the media file represented by the first URL in the list.</span></span> <span data-ttu-id="fbab7-126">Wenn dies fehlschlägt, versucht das Client Programm, eine Verbindung mit der durch die nächste URL in der Liste dargestellten Datei herzustellen.</span><span class="sxs-lookup"><span data-stu-id="fbab7-126">If that fails, the client program attempts to connect to the file represented by the next URL in the list.</span></span> <span data-ttu-id="fbab7-127">Das Client Programm fährt fort, bis eine erfolgreiche Verbindung hergestellt wurde oder das Ende der Liste erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="fbab7-127">The client program continues down the list until it makes a successful connection or reaches the end of the list.</span></span> <span data-ttu-id="fbab7-128">Beachten Sie Folgendes: Wenn das Client Programm erfolgreich eine Verbindung herstellt, liest es keine der nachfolgenden URLs in der Liste.</span><span class="sxs-lookup"><span data-stu-id="fbab7-128">Note that if the client program makes a successful connection, it does not read any of the subsequent URLs in the list.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fbab7-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fbab7-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbab7-130">**Frühere Versionen von Windows Media-Metadatendateien (veraltet)**</span><span class="sxs-lookup"><span data-stu-id="fbab7-130">**Previous Versions of Windows Media Metafiles (deprecated)**</span></span>](previous-versions-of-windows-media-metafiles--deprecated.md)
</dt> </dl>

 

 




