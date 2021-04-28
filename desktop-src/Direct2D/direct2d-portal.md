---
title: Direct2D
description: Direct2D
ms.assetid: 03b3b91c-9751-4f8d-af24-85067f06930b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8223ec5e98db3e45b0087073b4eb68baeae81280
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089178"
---
# <a name="direct2d"></a><span data-ttu-id="0a79c-103">Direct2D</span><span class="sxs-lookup"><span data-stu-id="0a79c-103">Direct2D</span></span>

## <a name="purpose"></a><span data-ttu-id="0a79c-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="0a79c-104">Purpose</span></span>

<span data-ttu-id="0a79c-105">Direct2D ist eine hardwarebeschleunigte 2D-Grafik-API mit unmittelbarem Modus, die das Rendern mit hoher Leistung und in hoher Qualität für 2D-Geometrie, Bitmaps und Text bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="0a79c-105">Direct2D is a hardware-accelerated, immediate-mode, 2-D graphics API that provides high performance and high-quality rendering for 2-D geometry, bitmaps, and text.</span></span> <span data-ttu-id="0a79c-106">Die Direct2D-API ist für eine gute Zusammenarbeit mit GDI, GDI+ und Direct3D konzipiert.</span><span class="sxs-lookup"><span data-stu-id="0a79c-106">The Direct2D API is designed to interoperate well with GDI, GDI+, and Direct3D.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="0a79c-107">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="0a79c-107">Developer audience</span></span>

<span data-ttu-id="0a79c-108">Direct2D ist in erster Linie für die Verwendung durch die folgenden Klassen von Entwicklern konzipiert:</span><span class="sxs-lookup"><span data-stu-id="0a79c-108">Direct2D is designed primarily for use by the following classes of developers:</span></span>

-   <span data-ttu-id="0a79c-109">Entwickler von großen, nativen Anwendungen im Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="0a79c-109">Developers of large, enterprise-scale, native applications.</span></span>
-   <span data-ttu-id="0a79c-110">Entwickler, die Steuerungstoolkits und Bibliotheken für die Nutzung durch Downstreamentwickler erstellen.</span><span class="sxs-lookup"><span data-stu-id="0a79c-110">Developers who create control toolkits and libraries for consumption by downstream developers.</span></span>
-   <span data-ttu-id="0a79c-111">Entwickler, die serverseitiges Rendering von 2D-Grafiken benötigen.</span><span class="sxs-lookup"><span data-stu-id="0a79c-111">Developers who require server-side rendering of 2-D graphics.</span></span>
-   <span data-ttu-id="0a79c-112">Entwickler, die Direct3D-Grafiken verwenden und einfaches, leistungsstarkes 2D- und Textrendering für Menüs, Benutzeroberflächenelemente und Kopf-auf-Bildschirme (HUDs) benötigen.</span><span class="sxs-lookup"><span data-stu-id="0a79c-112">Developers who use Direct3D graphics and need simple, high-performance 2-D and text rendering for menus, user-interface (UI) elements, and Heads-up Displays (HUDs).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="0a79c-113">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="0a79c-113">Run-time requirements</span></span>

-   <span data-ttu-id="0a79c-114">Windows 7 oder Windows Vista mit Service Pack 2 (SP2) und Plattformupdate für Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="0a79c-114">Windows 7 or Windows Vista with Service Pack 2 (SP2) and Platform Update for Windows Vista and later.</span></span>
-   <span data-ttu-id="0a79c-115">Windows Server 2008 R2 oder Windows Server 2008 mit Service Pack 2 (SP2) und Plattformupdate für Windows Server 2008 und höher.</span><span class="sxs-lookup"><span data-stu-id="0a79c-115">Windows Server 2008 R2 or Windows Server 2008 with Service Pack 2 (SP2) and Platform Update for Windows Server 2008 and later.</span></span>

> [!Note]
>
> <span data-ttu-id="0a79c-116">Platform Update für Windows Vista und Platform Update für Windows Server 2008 sind eine Reihe von Laufzeitbibliotheken, mit denen Entwickler Anwendungen auf Windows 7, Windows Vista, Windows Server 2008 R2 und Windows Server 2008 ausrichten können.</span><span class="sxs-lookup"><span data-stu-id="0a79c-116">The Platform Update for Windows Vista and Platform Update for Windows Server 2008 are a set of run-time libraries that enables developers to target applications to Windows 7, Windows Vista, Windows Server 2008 R2, and Windows Server 2008.</span></span> <span data-ttu-id="0a79c-117">Diese Updates sind für alle Windows Vista- und Windows Server 2008-Kunden über Windows Update verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0a79c-117">These updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="0a79c-118">Drittanbieteranwendungen, die Platform Update für Windows Vista oder Platform Update für Windows Server 2008 erfordern, können Windows Update erkennen, ob das erforderliche update installiert ist. Andernfalls werden Windows Update sie im Hintergrund herunterladen und installieren.</span><span class="sxs-lookup"><span data-stu-id="0a79c-118">Third-party applications that require Platform Update for Windows Vista or Platform Update for Windows Server 2008 can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span> <span data-ttu-id="0a79c-119">Weitere Informationen zu beiden Updates finden Sie unter [Plattformupdate für Windows Vista.](https://support.microsoft.com/kb/971644)</span><span class="sxs-lookup"><span data-stu-id="0a79c-119">For more information about both updates, see [Platform Update for Windows Vista](https://support.microsoft.com/kb/971644).</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="0a79c-120">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="0a79c-120">In this section</span></span>



| <span data-ttu-id="0a79c-121">Thema</span><span class="sxs-lookup"><span data-stu-id="0a79c-121">Topic</span></span>                                                                                          | <span data-ttu-id="0a79c-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0a79c-122">Description</span></span>                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a79c-123">Neuerungen in Direct2D</span><span class="sxs-lookup"><span data-stu-id="0a79c-123">What's new in Direct2D</span></span>](what-s-new-in-direct2d-for-windows-8-consumer-preview.md)<br/> | <span data-ttu-id="0a79c-124">Hier sind einige der neuen Ergänzungen zu Direct2D.</span><span class="sxs-lookup"><span data-stu-id="0a79c-124">Here are some of the new additions to Direct2D.</span></span> <br/>                                                                                                                   |
| [<span data-ttu-id="0a79c-125">Informationen zu Direct2D</span><span class="sxs-lookup"><span data-stu-id="0a79c-125">About Direct2D</span></span>](direct2d-overview.md)<br/>                                             | <span data-ttu-id="0a79c-126">Führt Direct2D ein, eine API, die Win32-Entwicklern die Möglichkeit bietet, 2D-Grafikrenderingaufgaben mit höherer Leistung und visueller Qualität auszuführen.</span><span class="sxs-lookup"><span data-stu-id="0a79c-126">Introduces Direct2D, an API that provides Win32 developers with the ability to perform 2-D graphics rendering tasks with superior performance and visual quality.</span></span> <br/> |
| [<span data-ttu-id="0a79c-127">Direct2D-Schnellstart für Windows 8</span><span class="sxs-lookup"><span data-stu-id="0a79c-127">Direct2D Quickstart for Windows 8</span></span>](direct2d-quickstart-with-device-context.md)<br/>    | <span data-ttu-id="0a79c-128">Fasst die erforderlichen Schritte zum Zeichnen mit Direct2D zusammen und stellt Beispielcode bereit.</span><span class="sxs-lookup"><span data-stu-id="0a79c-128">Summarizes the steps required to draw with Direct2D and provides example code.</span></span><br/>                                                                                     |
| [<span data-ttu-id="0a79c-129">Erste Schritte mit Direct2D</span><span class="sxs-lookup"><span data-stu-id="0a79c-129">Getting Started with Direct2D</span></span>](getting-started-with-direct2d-nav.md)<br/>              | <span data-ttu-id="0a79c-130">Beschreibt die ersten Schritte beim Erstellen von Direct2D-Anwendungen und stellt Beispielcode bereit.</span><span class="sxs-lookup"><span data-stu-id="0a79c-130">Describes how to get started creating Direct2D applications and provides example code.</span></span><br/>                                                                             |
| [<span data-ttu-id="0a79c-131">Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="0a79c-131">Programming Guide</span></span>](programming-guide.md)<br/>                                          | <span data-ttu-id="0a79c-132">Dieser Abschnitt enthält themen zur konzeptionellen Programmierung, in denen die Verwendung der Direct2D-API beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="0a79c-132">This section contains conceptual programming topics that describe how to use the Direct2D API.</span></span> <br/>                                                                    |
| [<span data-ttu-id="0a79c-133">Direct2D-Referenz</span><span class="sxs-lookup"><span data-stu-id="0a79c-133">Direct2D reference</span></span>](reference.md)<br/>                                                      | <span data-ttu-id="0a79c-134">Beschreibt die Direct2D-API im Detail.</span><span class="sxs-lookup"><span data-stu-id="0a79c-134">Describes the Direct2D API in detail.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="0a79c-135">Tools und Hilfsprogramme</span><span class="sxs-lookup"><span data-stu-id="0a79c-135">Tools and Utilities</span></span>](tools-and-utilities.md)<br/>                                      | <span data-ttu-id="0a79c-136">Tools und Hilfsprogramme, die für Direct2D bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="0a79c-136">Tools and utilities provided for Direct2D.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="0a79c-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a79c-137">Samples</span></span>](d2d-samples.md)<br/>                                                          | <span data-ttu-id="0a79c-138">Beispielanwendungen, die die Direct2D-API veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="0a79c-138">Sample applications that demonstrate the Direct2D API.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="0a79c-139">Direct2D-Glossar</span><span class="sxs-lookup"><span data-stu-id="0a79c-139">Direct2D Glossary</span></span>](direct2d-glossary.md)<br/>                                          | <span data-ttu-id="0a79c-140">Beschreibt Begriffe, die häufig in der Direct2D-Dokumentation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0a79c-140">Describes terms commonly used by the Direct2D documentation.</span></span> <br/>                                                                                                      |



 

## <a name="additional-resources"></a><span data-ttu-id="0a79c-141">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0a79c-141">Additional resources</span></span>

-   [<span data-ttu-id="0a79c-142">**DirectX-Grafiken und -Spiele**</span><span class="sxs-lookup"><span data-stu-id="0a79c-142">**DirectX Graphics and Gaming**</span></span>](/windows/desktop/directx)
-   [<span data-ttu-id="0a79c-143">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="0a79c-143">DirectWrite</span></span>](/windows/desktop/DirectWrite/direct-write-portal)

 

