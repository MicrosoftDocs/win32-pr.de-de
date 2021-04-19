---
title: Wahrgenommene Typen (Features der Legacy-Windows-Umgebung)
description: "\"Wahrnehmvedtype\" ist eine Eigenschaft, die ein Element im Index klassifiziert."
ms.assetid: 47a5cf55-79f6-48e7-a585-72fc3d7d53d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afaf7d8b827495a94b441e5504762dd53dbe733c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106341987"
---
# <a name="perceived-types-legacy-windows-environment-features"></a><span data-ttu-id="57765-103">Wahrgenommene Typen (Features der Legacy-Windows-Umgebung)</span><span class="sxs-lookup"><span data-stu-id="57765-103">Perceived Types (Legacy Windows Environment Features)</span></span>

> [!NOTE]
> <span data-ttu-id="57765-104">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="57765-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="57765-105">Verwenden Sie in späteren Versionen stattdessen [Windows Search](../search/-search-3x-wds-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="57765-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="57765-106">`PerceivedType` ist eine Eigenschaft, die ein Element im Index klassifiziert.</span><span class="sxs-lookup"><span data-stu-id="57765-106">`PerceivedType` is a property that classifies an item in the index.</span></span> <span data-ttu-id="57765-107">Diese Klassifizierung unterscheidet sich von der "Kind"-Klassifizierung, die von der [erweiterten Abfrage Syntax](-search-2x-wds-aqsreference.md) verwendet wird, aber auf ähnliche Weise können Benutzer Ihre Suchergebnisse verfeinern.</span><span class="sxs-lookup"><span data-stu-id="57765-107">This classification is different from the "kind" classification used by the [Advanced Query Syntax](-search-2x-wds-aqsreference.md) but similarly lets users refine their search results.</span></span> <span data-ttu-id="57765-108">Mit der AQS-Art können Benutzer Ihre Suchabfrage einschränken, während die Eigenschaft "wahrvedtype" Benutzern das Filtern des Resultsets ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="57765-108">The AQS kind lets users limit their search query while the PerceivedType property lets users filter their result set.</span></span>

## <a name="types"></a><span data-ttu-id="57765-109">Typen</span><span class="sxs-lookup"><span data-stu-id="57765-109">Types</span></span>

<span data-ttu-id="57765-110">Verwenden Sie die Eigenschaft "wahrnehmvedtype", um den Dateityp zu klassifizieren, sodass Benutzer Ihre Suchergebnisse nach Typ filtern können.</span><span class="sxs-lookup"><span data-stu-id="57765-110">Use the PerceivedType property to classify your file type so that users can filter their search results by type.</span></span> <span data-ttu-id="57765-111">Die Ausgabe muss eine der folgenden Zeichen folgen sein:</span><span class="sxs-lookup"><span data-stu-id="57765-111">The output must be one of the following strings:</span></span>

-   <span data-ttu-id="57765-112">contact</span><span class="sxs-lookup"><span data-stu-id="57765-112">contact</span></span>
-   <span data-ttu-id="57765-113">Kommunikation</span><span class="sxs-lookup"><span data-stu-id="57765-113">communications</span></span>
-   <span data-ttu-id="57765-114">Kommunikation/e-Mail</span><span class="sxs-lookup"><span data-stu-id="57765-114">communications/email</span></span>
-   <span data-ttu-id="57765-115">Kommunikation/Kalender</span><span class="sxs-lookup"><span data-stu-id="57765-115">communications/calendar</span></span>
-   <span data-ttu-id="57765-116">Kommunikation/Aufgabe</span><span class="sxs-lookup"><span data-stu-id="57765-116">communications/task</span></span>
-   <span data-ttu-id="57765-117">Kommunikation/im</span><span class="sxs-lookup"><span data-stu-id="57765-117">communications/im</span></span>
-   <span data-ttu-id="57765-118">Dokument</span><span class="sxs-lookup"><span data-stu-id="57765-118">document</span></span>
-   <span data-ttu-id="57765-119">Dokument/Hinweis</span><span class="sxs-lookup"><span data-stu-id="57765-119">document/note</span></span>
-   <span data-ttu-id="57765-120">Dokument/Text</span><span class="sxs-lookup"><span data-stu-id="57765-120">document/text</span></span>
-   <span data-ttu-id="57765-121">Dokument/Kalkulations Tabelle</span><span class="sxs-lookup"><span data-stu-id="57765-121">document/spreadsheet</span></span>
-   <span data-ttu-id="57765-122">Dokument/Präsentation</span><span class="sxs-lookup"><span data-stu-id="57765-122">document/presentation</span></span>
-   <span data-ttu-id="57765-123">music</span><span class="sxs-lookup"><span data-stu-id="57765-123">music</span></span>
-   <span data-ttu-id="57765-124">images</span><span class="sxs-lookup"><span data-stu-id="57765-124">images</span></span>
-   <span data-ttu-id="57765-125">Bilder/Bild</span><span class="sxs-lookup"><span data-stu-id="57765-125">images/picture</span></span>
-   <span data-ttu-id="57765-126">Bilder/Video</span><span class="sxs-lookup"><span data-stu-id="57765-126">images/video</span></span>
-   <span data-ttu-id="57765-127">folder</span><span class="sxs-lookup"><span data-stu-id="57765-127">folder</span></span>
-   <span data-ttu-id="57765-128">Programm</span><span class="sxs-lookup"><span data-stu-id="57765-128">program</span></span>

<span data-ttu-id="57765-129">Wenn Sie z. b. ein Filter-Add-in für einen neuen Bilddateityp erstellen möchten, müssen Sie Folgendes in Ihrer [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)-Schnittstelle implementieren:</span><span class="sxs-lookup"><span data-stu-id="57765-129">For example, when you want to create a filter add-in for a new picture file type, you need to implement the following in your [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface:</span></span>

-   <span data-ttu-id="57765-130">**GetChunk** zum Zurückgeben einer fullpropspec, die Folgendes enthält: D5CDD505-2E9C-101B-9397-08002B2CF9AE/wahrnehmvedtype</span><span class="sxs-lookup"><span data-stu-id="57765-130">**GetChunk** to return a FULLPROPSPEC that includes: D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType</span></span>
-   <span data-ttu-id="57765-131">**GetValue** zum Zurückgeben einer PROPVARIANT, die Folgendes enthält: VT \_ LPWSTR = "Images/Bild"</span><span class="sxs-lookup"><span data-stu-id="57765-131">**GetValue** to return a PROPVARIANT that includes: VT\_LPWSTR = "images/picture"</span></span>

## <a name="related-topics"></a><span data-ttu-id="57765-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="57765-132">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="57765-133">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="57765-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="57765-134">Entwickeln von IFilter-Add-ins</span><span class="sxs-lookup"><span data-stu-id="57765-134">Developing IFilter Add-ins</span></span>](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[<span data-ttu-id="57765-135">Entwickeln von Protokoll Handlern</span><span class="sxs-lookup"><span data-stu-id="57765-135">Developing Protocol Handlers</span></span>](-search-2x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="57765-136">Erweiterte Abfragesyntax</span><span class="sxs-lookup"><span data-stu-id="57765-136">Advanced Query Syntax</span></span>](-search-2x-wds-aqsreference.md)
</dt> <dt>

[<span data-ttu-id="57765-137">Schema Tabelle</span><span class="sxs-lookup"><span data-stu-id="57765-137">SchemaTable</span></span>](-search-2x-wds-schematable.md)
</dt> </dl>

 

 
