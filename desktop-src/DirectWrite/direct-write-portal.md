---
title: DirectWrite (DWrite)
description: Heutige Anwendungen müssen qualitativ hochwertiges Textrendering, auflösungsunabhängige Konturschriftarten und vollständige Unicode-Text- und Layoutunterstützung unterstützen. DirectWrite, eine [DirectX-API,](../directx.md) bietet diese Features und vieles mehr.
ms.assetid: 62a8d723-ae1c-4cbc-a9da-3177e80d4a3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6bdc75845c2387a4fa4335fa462d0b97ec5669
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587941"
---
# <a name="directwrite-dwrite"></a><span data-ttu-id="8595a-104">DirectWrite (DWrite)</span><span class="sxs-lookup"><span data-stu-id="8595a-104">DirectWrite (DWrite)</span></span>

## <a name="purpose"></a><span data-ttu-id="8595a-105">Zweck</span><span class="sxs-lookup"><span data-stu-id="8595a-105">Purpose</span></span>

<span data-ttu-id="8595a-106">Heutige Anwendungen müssen qualitativ hochwertiges Textrendering, auflösungsunabhängige Konturschriftarten und vollständige Unicode-Text- und Layoutunterstützung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8595a-106">Today's applications must support high-quality text rendering, resolution-independent outline fonts, and full Unicode text and layout support.</span></span> <span data-ttu-id="8595a-107">DirectWrite, eine [DirectX-API,](../directx.md) bietet diese Features und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="8595a-107">DirectWrite, a [DirectX](../directx.md) API, provides these features and more.</span></span>

- <span data-ttu-id="8595a-108">Ein geräteunabhängiges Textlayoutsystem, das die Lesbarkeit von Text in Dokumenten und auf der Benutzeroberfläche verbessert.</span><span class="sxs-lookup"><span data-stu-id="8595a-108">A device-independent text layout system that improves text readability in documents and in UI.</span></span>
- <span data-ttu-id="8595a-109">Qualitativ hochwertiges, untergeordnetes Pixel, Microsoft ClearType-Textrendering, das [GDI-,](interoperating-with-gdi.md) [Direct2D-](rendering-by-using-direct2d.md)oder anwendungsspezifische Renderingtechnologie verwenden kann. [](/typography/cleartype/)</span><span class="sxs-lookup"><span data-stu-id="8595a-109">High-quality, sub-pixel, [Microsoft ClearType](/typography/cleartype/) text rendering that can use [GDI](interoperating-with-gdi.md), [Direct2D](rendering-by-using-direct2d.md), or application-specific rendering technology.</span></span>
- <span data-ttu-id="8595a-110">Hardwarebeschleunigte Text, wenn er mit [Direct2D](rendering-by-using-direct2d.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8595a-110">Hardware-accelerated text, when used with [Direct2D](rendering-by-using-direct2d.md).</span></span>
- <span data-ttu-id="8595a-111">Unterstützung für Mehrformattext.</span><span class="sxs-lookup"><span data-stu-id="8595a-111">Support for multi-format text.</span></span>
- <span data-ttu-id="8595a-112">Unterstützung für die erweiterten Typografiefeatures von OpenType-Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="8595a-112">Support for the advanced typography features of OpenType fonts.</span></span>
- <span data-ttu-id="8595a-113">Unterstützung für das Layout und Rendering von Text in allen unterstützten Sprachen.</span><span class="sxs-lookup"><span data-stu-id="8595a-113">Support for the layout and rendering of text in all supported languages.</span></span>
- <span data-ttu-id="8595a-114">[GDI-kompatibles](interoperating-with-gdi.md)Layout und Rendering.</span><span class="sxs-lookup"><span data-stu-id="8595a-114">[GDI](interoperating-with-gdi.md)-compatible layout and rendering.</span></span>

<span data-ttu-id="8595a-115">Die API unterstützt das Messen, Zeichnen und Treffertesten von Mehrformattext.</span><span class="sxs-lookup"><span data-stu-id="8595a-115">The API supports measuring, drawing, and hit-testing of multi-format text.</span></span> <span data-ttu-id="8595a-116">DirectWrite verarbeitet Text in allen unterstützten Sprachen für globale und lokalisierte Anwendungen und baut auf der schlüsselsprachlichen Infrastruktur in Windows 7 auf.</span><span class="sxs-lookup"><span data-stu-id="8595a-116">DirectWrite handles text in all supported languages for global and localized applications, building on the key language infrastructure found in Windows 7.</span></span> <span data-ttu-id="8595a-117">DirectWrite stellt außerdem eine API für Glyphenrendering auf niedriger Ebene für Entwickler zur Ausführung von eigenem Layout und eigener Unicode-zu-Glyphen-Verarbeitung bereit.</span><span class="sxs-lookup"><span data-stu-id="8595a-117">DirectWrite also provides a low-level glyph rendering API for developers who want to perform their own layout and Unicode-to-glyph processing.</span></span>

> [!NOTE]
> <span data-ttu-id="8595a-118">[Das Windows App SDK](/windows/apps/windows-app-sdk/) führt eine neue Version von DirectWrite &mdash; mit dem Namen DWriteCore &mdash; ein, die unter Windows-Versionen bis hin zu Windows 8 ausgeführt wird, und öffnet Ihnen die Möglichkeit, sie plattformübergreifend zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8595a-118">[Windows App SDK](/windows/apps/windows-app-sdk/) introduces a new version of DirectWrite&mdash;called DWriteCore&mdash;that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="8595a-119">Weitere Informationen finden Sie unter [Übersicht über DWriteCore.](dwritecore-overview.md)</span><span class="sxs-lookup"><span data-stu-id="8595a-119">For more details, see [DWriteCore overview](dwritecore-overview.md).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="8595a-120">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="8595a-120">Run-time requirements</span></span>

- <span data-ttu-id="8595a-121">Windows 7 oder Windows Vista mit Service Pack 2 (SP2) und Plattformupdate für Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8595a-121">Windows 7 or Windows Vista with Service Pack 2 (SP2) and Platform Update for Windows Vista</span></span>
- <span data-ttu-id="8595a-122">Windows Server 2008 R2 oder Windows Server 2008 mit Service Pack 2 (SP2) und Plattformupdate für Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8595a-122">Windows Server 2008 R2 or Windows Server 2008 with Service Pack 2 (SP2) and Platform Update for Windows Server 2008</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8595a-123">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="8595a-123">In this section</span></span>

| <span data-ttu-id="8595a-124">Thema</span><span class="sxs-lookup"><span data-stu-id="8595a-124">Topic</span></span> | <span data-ttu-id="8595a-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8595a-125">Description</span></span> |
|-|-|
| [<span data-ttu-id="8595a-126">Neuerungen in DirectWrite</span><span class="sxs-lookup"><span data-stu-id="8595a-126">What's new in DirectWrite</span></span>](what-s-new-in-directwrite-for-windows-8-consumer-preview.md)<br/> | <span data-ttu-id="8595a-127">Hier sind einige der neuen Ergänzungen zu DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="8595a-127">Here are some of the new additions to DirectWrite.</span></span> <br/> |
| [<span data-ttu-id="8595a-128">Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="8595a-128">Programming Guide</span></span>](programming-guide.md)<br/> | <span data-ttu-id="8595a-129">Die folgenden Themen bieten eine Übersicht über die DirectWrite-API.</span><span class="sxs-lookup"><span data-stu-id="8595a-129">The following topics provide an overview of the DirectWrite API.</span></span><br/> |
| [<span data-ttu-id="8595a-130">API-Referenz</span><span class="sxs-lookup"><span data-stu-id="8595a-130">API Reference</span></span>](reference.md)<br/> | <span data-ttu-id="8595a-131">Beschreibt die DirectWrite-API.</span><span class="sxs-lookup"><span data-stu-id="8595a-131">Describes the DirectWrite API.</span></span><br/> |
| [<span data-ttu-id="8595a-132">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="8595a-132">Sample Code</span></span>](samples.md)<br/> | <span data-ttu-id="8595a-133">Dieser Abschnitt enthält Informationen zu Beispielprogrammen für DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="8595a-133">This section contains information about sample programs for DirectWrite.</span></span><br/> |
