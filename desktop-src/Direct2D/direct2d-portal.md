---
title: Direct2D
description: .
ms.assetid: 03b3b91c-9751-4f8d-af24-85067f06930b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2eae62ba2d6ff44920d6b6d4890a8c48bc3c0f8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039275"
---
# <a name="direct2d"></a><span data-ttu-id="dc1dd-103">Direct2D</span><span class="sxs-lookup"><span data-stu-id="dc1dd-103">Direct2D</span></span>

## <a name="purpose"></a><span data-ttu-id="dc1dd-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="dc1dd-104">Purpose</span></span>

<span data-ttu-id="dc1dd-105">Direct2D ist eine hardwarebeschleunigte 2D-Grafik-API mit unmittelbarem Modus, die das Rendern mit hoher Leistung und in hoher Qualität für 2D-Geometrie, Bitmaps und Text bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="dc1dd-105">Direct2D is a hardware-accelerated, immediate-mode, 2-D graphics API that provides high performance and high-quality rendering for 2-D geometry, bitmaps, and text.</span></span> <span data-ttu-id="dc1dd-106">Die Direct2D-API ist für die Zusammenarbeit mit GDI, GDI+ und Direct3D konzipiert.</span><span class="sxs-lookup"><span data-stu-id="dc1dd-106">The Direct2D API is designed to interoperate well with GDI, GDI+, and Direct3D.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="dc1dd-107">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="dc1dd-107">Developer audience</span></span>

<span data-ttu-id="dc1dd-108">Direct2D wurde hauptsächlich für die Verwendung durch die folgenden Klassen von Entwicklern entwickelt:</span><span class="sxs-lookup"><span data-stu-id="dc1dd-108">Direct2D is designed primarily for use by the following classes of developers:</span></span>

-   <span data-ttu-id="dc1dd-109">Entwickler umfangreicher, Unternehmens eigener Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="dc1dd-109">Developers of large, enterprise-scale, native applications.</span></span>
-   <span data-ttu-id="dc1dd-110">Entwickler, die Steuerelement-Toolkits und-Bibliotheken für die Nutzung durch downstreamentwickler erstellen.</span><span class="sxs-lookup"><span data-stu-id="dc1dd-110">Developers who create control toolkits and libraries for consumption by downstream developers.</span></span>
-   <span data-ttu-id="dc1dd-111">Entwickler, die ein serverseitiges Rendering von 2D-Grafiken benötigen.</span><span class="sxs-lookup"><span data-stu-id="dc1dd-111">Developers who require server-side rendering of 2-D graphics.</span></span>
-   <span data-ttu-id="dc1dd-112">Entwickler, die Direct3D-Grafiken verwenden und einfache, hochleistungsfähige 2D-und Text Rendering für Menüs, Benutzeroberflächen Elemente (UI) und Heads-up-anzeigen (HUDs) benötigen.</span><span class="sxs-lookup"><span data-stu-id="dc1dd-112">Developers who use Direct3D graphics and need simple, high-performance 2-D and text rendering for menus, user-interface (UI) elements, and Heads-up Displays (HUDs).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="dc1dd-113">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="dc1dd-113">Run-time requirements</span></span>

-   <span data-ttu-id="dc1dd-114">Windows 7 oder Windows Vista mit Service Pack 2 (SP2) und ein Platt Form Update für Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="dc1dd-114">Windows 7 or Windows Vista with Service Pack 2 (SP2) and Platform Update for Windows Vista and later.</span></span>
-   <span data-ttu-id="dc1dd-115">Windows Server 2008 R2 oder Windows Server 2008 mit Service Pack 2 (SP2) und Platt Form Update für Windows Server 2008 und höher.</span><span class="sxs-lookup"><span data-stu-id="dc1dd-115">Windows Server 2008 R2 or Windows Server 2008 with Service Pack 2 (SP2) and Platform Update for Windows Server 2008 and later.</span></span>

> [!Note]
>
> <span data-ttu-id="dc1dd-116">Das Platt Form Update für Windows Vista und das Platt Form Update für Windows Server 2008 sind eine Reihe von Laufzeitbibliotheken, mit denen Entwickler Anwendungen auf Windows 7, Windows Vista, Windows Server 2008 R2 und Windows Server 2008 ausrichten können.</span><span class="sxs-lookup"><span data-stu-id="dc1dd-116">The Platform Update for Windows Vista and Platform Update for Windows Server 2008 are a set of run-time libraries that enables developers to target applications to Windows 7, Windows Vista, Windows Server 2008 R2, and Windows Server 2008.</span></span> <span data-ttu-id="dc1dd-117">Diese Updates werden für alle Windows Vista-und Windows Server 2008-Kunden über Windows Update verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="dc1dd-117">These updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="dc1dd-118">Anwendungen von Drittanbietern, die ein Platt Form Update für Windows Vista oder ein Platt Form Update für Windows Server 2008 erfordern, können Windows Update erkennen, ob das erforderliche aktualisierte installiert ist. Wenn dies nicht der Fall ist, wird Windows Update im Hintergrund heruntergeladen und installiert.</span><span class="sxs-lookup"><span data-stu-id="dc1dd-118">Third-party applications that require Platform Update for Windows Vista or Platform Update for Windows Server 2008 can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span> <span data-ttu-id="dc1dd-119">Weitere Informationen zu beiden Updates finden Sie unter [Platt Form Update für Windows Vista](https://support.microsoft.com/kb/971644).</span><span class="sxs-lookup"><span data-stu-id="dc1dd-119">For more information about both updates, see [Platform Update for Windows Vista](https://support.microsoft.com/kb/971644).</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="dc1dd-120">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="dc1dd-120">In this section</span></span>



| <span data-ttu-id="dc1dd-121">Thema</span><span class="sxs-lookup"><span data-stu-id="dc1dd-121">Topic</span></span>                                                                                          | <span data-ttu-id="dc1dd-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc1dd-122">Description</span></span>                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc1dd-123">Neues in Direct2D</span><span class="sxs-lookup"><span data-stu-id="dc1dd-123">What's new in Direct2D</span></span>](what-s-new-in-direct2d-for-windows-8-consumer-preview.md)<br/> | <span data-ttu-id="dc1dd-124">Im folgenden finden Sie einige der neuen Ergänzungen zu Direct2D.</span><span class="sxs-lookup"><span data-stu-id="dc1dd-124">Here are some of the new additions to Direct2D.</span></span> <br/>                                                                                                                   |
| [<span data-ttu-id="dc1dd-125">Informationen zu Direct2D</span><span class="sxs-lookup"><span data-stu-id="dc1dd-125">About Direct2D</span></span>](direct2d-overview.md)<br/>                                             | <span data-ttu-id="dc1dd-126">Führt Direct2D ein, eine API, die Win32-Entwicklern die Möglichkeit bietet, 2D-Grafik Rendering-Aufgaben mit hoher Leistung und visueller Qualität auszuführen.</span><span class="sxs-lookup"><span data-stu-id="dc1dd-126">Introduces Direct2D, an API that provides Win32 developers with the ability to perform 2-D graphics rendering tasks with superior performance and visual quality.</span></span> <br/> |
| [<span data-ttu-id="dc1dd-127">Direct2D Schnellstart für Windows 8</span><span class="sxs-lookup"><span data-stu-id="dc1dd-127">Direct2D Quickstart for Windows 8</span></span>](direct2d-quickstart-with-device-context.md)<br/>    | <span data-ttu-id="dc1dd-128">Fasst die Schritte zusammen, die zum Zeichnen mit Direct2D erforderlich sind, und stellt Beispielcode bereit.</span><span class="sxs-lookup"><span data-stu-id="dc1dd-128">Summarizes the steps required to draw with Direct2D and provides example code.</span></span><br/>                                                                                     |
| [<span data-ttu-id="dc1dd-129">Ersten Einstieg in Direct2D</span><span class="sxs-lookup"><span data-stu-id="dc1dd-129">Getting Started with Direct2D</span></span>](getting-started-with-direct2d-nav.md)<br/>              | <span data-ttu-id="dc1dd-130">Beschreibt die ersten Schritte beim Erstellen von Direct2D-Anwendungen und stellt Beispielcode bereit.</span><span class="sxs-lookup"><span data-stu-id="dc1dd-130">Describes how to get started creating Direct2D applications and provides example code.</span></span><br/>                                                                             |
| [<span data-ttu-id="dc1dd-131">Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="dc1dd-131">Programming Guide</span></span>](programming-guide.md)<br/>                                          | <span data-ttu-id="dc1dd-132">Dieser Abschnitt enthält konzeptionelle Programmierthemen, in denen die Verwendung der Direct2D-API beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="dc1dd-132">This section contains conceptual programming topics that describe how to use the Direct2D API.</span></span> <br/>                                                                    |
| [<span data-ttu-id="dc1dd-133">Direct2D-Referenz</span><span class="sxs-lookup"><span data-stu-id="dc1dd-133">Direct2D reference</span></span>](reference.md)<br/>                                                      | <span data-ttu-id="dc1dd-134">Beschreibt die Direct2D-API im Detail.</span><span class="sxs-lookup"><span data-stu-id="dc1dd-134">Describes the Direct2D API in detail.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="dc1dd-135">Tools und Hilfsprogramme</span><span class="sxs-lookup"><span data-stu-id="dc1dd-135">Tools and Utilities</span></span>](tools-and-utilities.md)<br/>                                      | <span data-ttu-id="dc1dd-136">Tools und Hilfsprogramme, die für Direct2D bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="dc1dd-136">Tools and utilities provided for Direct2D.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="dc1dd-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc1dd-137">Samples</span></span>](d2d-samples.md)<br/>                                                          | <span data-ttu-id="dc1dd-138">Beispielanwendungen, die die Direct2D-API veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="dc1dd-138">Sample applications that demonstrate the Direct2D API.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="dc1dd-139">Direct2D Glossar</span><span class="sxs-lookup"><span data-stu-id="dc1dd-139">Direct2D Glossary</span></span>](direct2d-glossary.md)<br/>                                          | <span data-ttu-id="dc1dd-140">Beschreibt Begriffe, die in der Direct2D-Dokumentation häufig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dc1dd-140">Describes terms commonly used by the Direct2D documentation.</span></span> <br/>                                                                                                      |



 

## <a name="additional-resources"></a><span data-ttu-id="dc1dd-141">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="dc1dd-141">Additional resources</span></span>

-   [<span data-ttu-id="dc1dd-142">**DirectX-Grafiken und -Spiele**</span><span class="sxs-lookup"><span data-stu-id="dc1dd-142">**DirectX Graphics and Gaming**</span></span>](/windows/desktop/directx)
-   [<span data-ttu-id="dc1dd-143">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="dc1dd-143">DirectWrite</span></span>](/windows/desktop/DirectWrite/direct-write-portal)

 

