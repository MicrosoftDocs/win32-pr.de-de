---
title: DirectWrite (DWrite)
description: Die heutigen Anwendungen müssen ein qualitativ hochwertiges Text Rendering, auflösungsunabhängige Gliederungs Schriftarten und vollständige Unterstützung für Unicode-Text und-Layouts unterstützen. DirectWrite, eine [DirectX](../directx.md) -API, bietet diese Features und vieles mehr.
ms.assetid: 62a8d723-ae1c-4cbc-a9da-3177e80d4a3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b1e2ff44083a56a7202847fc07ad9daaa67b7ba
ms.sourcegitcommit: dd4a3716477b1363be58ecc0d439029f81467104
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/11/2020
ms.locfileid: "104475015"
---
# <a name="directwrite-dwrite"></a><span data-ttu-id="d9e0e-104">DirectWrite (DWrite)</span><span class="sxs-lookup"><span data-stu-id="d9e0e-104">DirectWrite (DWrite)</span></span>

## <a name="purpose"></a><span data-ttu-id="d9e0e-105">Zweck</span><span class="sxs-lookup"><span data-stu-id="d9e0e-105">Purpose</span></span>

<span data-ttu-id="d9e0e-106">Die heutigen Anwendungen müssen ein qualitativ hochwertiges Text Rendering, auflösungsunabhängige Gliederungs Schriftarten und vollständige Unterstützung für Unicode-Text und-Layouts unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d9e0e-106">Today's applications must support high-quality text rendering, resolution-independent outline fonts, and full Unicode text and layout support.</span></span> <span data-ttu-id="d9e0e-107">DirectWrite, eine [DirectX](../directx.md) -API, bietet diese Features und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="d9e0e-107">DirectWrite, a [DirectX](../directx.md) API, provides these features and more.</span></span>

- <span data-ttu-id="d9e0e-108">Ein Geräte unabhängiges textlayoutsystem zur Verbesserung der Lesbarkeit von Text in Dokumenten und in der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="d9e0e-108">A device-independent text layout system that improves text readability in documents and in UI.</span></span>
- <span data-ttu-id="d9e0e-109">Hochwertiges, unter Pixel, [Microsoft ClearType](/typography/cleartype/) -Text Rendering, das [GDI](interoperating-with-gdi.md), [Direct2D](rendering-by-using-direct2d.md)oder anwendungsspezifische renderingtechnologie verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="d9e0e-109">High-quality, sub-pixel, [Microsoft ClearType](/typography/cleartype/) text rendering that can use [GDI](interoperating-with-gdi.md), [Direct2D](rendering-by-using-direct2d.md), or application-specific rendering technology.</span></span>
- <span data-ttu-id="d9e0e-110">Hardware beschleunigter Text, bei Verwendung mit [Direct2D](rendering-by-using-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="d9e0e-110">Hardware-accelerated text, when used with [Direct2D](rendering-by-using-direct2d.md).</span></span>
- <span data-ttu-id="d9e0e-111">Unterstützung für mehr formatieren Text.</span><span class="sxs-lookup"><span data-stu-id="d9e0e-111">Support for multi-format text.</span></span>
- <span data-ttu-id="d9e0e-112">Unterstützung für die erweiterten Typografiefunktionen von OpenType-Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="d9e0e-112">Support for the advanced typography features of OpenType fonts.</span></span>
- <span data-ttu-id="d9e0e-113">Unterstützung für Layout und Rendering von Text in allen unterstützten Sprachen.</span><span class="sxs-lookup"><span data-stu-id="d9e0e-113">Support for the layout and rendering of text in all supported languages.</span></span>
- <span data-ttu-id="d9e0e-114">[GDI](interoperating-with-gdi.md)-kompatibles Layout und Rendering.</span><span class="sxs-lookup"><span data-stu-id="d9e0e-114">[GDI](interoperating-with-gdi.md)-compatible layout and rendering.</span></span>

<span data-ttu-id="d9e0e-115">Die API unterstützt das Messen, zeichnen und Treffer Tests von Text mit mehreren Formaten.</span><span class="sxs-lookup"><span data-stu-id="d9e0e-115">The API supports measuring, drawing, and hit-testing of multi-format text.</span></span> <span data-ttu-id="d9e0e-116">DirectWrite verarbeitet Text in allen unterstützten Sprachen für globale und lokalisierte Anwendungen, die auf der Schlüssel sprach Infrastruktur von Windows 7 aufbauen.</span><span class="sxs-lookup"><span data-stu-id="d9e0e-116">DirectWrite handles text in all supported languages for global and localized applications, building on the key language infrastructure found in Windows 7.</span></span> <span data-ttu-id="d9e0e-117">DirectWrite stellt außerdem eine API für Glyphenrendering auf niedriger Ebene für Entwickler zur Ausführung von eigenem Layout und eigener Unicode-zu-Glyphen-Verarbeitung bereit.</span><span class="sxs-lookup"><span data-stu-id="d9e0e-117">DirectWrite also provides a low-level glyph rendering API for developers who want to perform their own layout and Unicode-to-glyph processing.</span></span>

> [!NOTE]
> <span data-ttu-id="d9e0e-118">Mit [Project Reunion](/windows/apps/project-reunion/) wird eine neue Version von DirectWrite mit dem &mdash; Namen "dwrite tecore" eingeführt, &mdash; die unter Windows-Versionen von Windows 8 bis Windows 8 ausgeführt wird. Sie öffnet die Tür, in der Sie Sie plattformübergreifend verwenden können.</span><span class="sxs-lookup"><span data-stu-id="d9e0e-118">[Project Reunion](/windows/apps/project-reunion/) introduces a new version of DirectWrite&mdash;called DWriteCore&mdash;that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="d9e0e-119">Weitere Informationen finden Sie unter [Übersicht über dbeschreib tecore](dwritecore-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d9e0e-119">For more details, see [DWriteCore overview](dwritecore-overview.md).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="d9e0e-120">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="d9e0e-120">Run-time requirements</span></span>

- <span data-ttu-id="d9e0e-121">Windows 7 oder Windows Vista mit Service Pack 2 (SP2) und Platt Form Update für Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d9e0e-121">Windows 7 or Windows Vista with Service Pack 2 (SP2) and Platform Update for Windows Vista</span></span>
- <span data-ttu-id="d9e0e-122">Windows Server 2008 R2 oder Windows Server 2008 mit Service Pack 2 (SP2) und Platt Form Update für Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9e0e-122">Windows Server 2008 R2 or Windows Server 2008 with Service Pack 2 (SP2) and Platform Update for Windows Server 2008</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d9e0e-123">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="d9e0e-123">In this section</span></span>

| <span data-ttu-id="d9e0e-124">Thema</span><span class="sxs-lookup"><span data-stu-id="d9e0e-124">Topic</span></span> | <span data-ttu-id="d9e0e-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d9e0e-125">Description</span></span> |
|-|-|
| [<span data-ttu-id="d9e0e-126">Neues in DirectWrite</span><span class="sxs-lookup"><span data-stu-id="d9e0e-126">What's new in DirectWrite</span></span>](what-s-new-in-directwrite-for-windows-8-consumer-preview.md)<br/> | <span data-ttu-id="d9e0e-127">Im folgenden finden Sie einige der neuen Ergänzungen zu DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="d9e0e-127">Here are some of the new additions to DirectWrite.</span></span> <br/> |
| [<span data-ttu-id="d9e0e-128">Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="d9e0e-128">Programming Guide</span></span>](programming-guide.md)<br/> | <span data-ttu-id="d9e0e-129">Die folgenden Themen bieten eine Übersicht über die DirectWrite-API.</span><span class="sxs-lookup"><span data-stu-id="d9e0e-129">The following topics provide an overview of the DirectWrite API.</span></span><br/> |
| [<span data-ttu-id="d9e0e-130">API-Referenz</span><span class="sxs-lookup"><span data-stu-id="d9e0e-130">API Reference</span></span>](reference.md)<br/> | <span data-ttu-id="d9e0e-131">Beschreibt die DirectWrite-API.</span><span class="sxs-lookup"><span data-stu-id="d9e0e-131">Describes the DirectWrite API.</span></span><br/> |
| [<span data-ttu-id="d9e0e-132">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="d9e0e-132">Sample Code</span></span>](samples.md)<br/> | <span data-ttu-id="d9e0e-133">Dieser Abschnitt enthält Informationen zu Beispielprogrammen für DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="d9e0e-133">This section contains information about sample programs for DirectWrite.</span></span><br/> |
