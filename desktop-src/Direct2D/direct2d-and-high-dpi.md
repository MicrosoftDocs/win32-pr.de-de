---
title: Direct2D und High-dpi
description: Beschreibt, wie Direct2D eine hohe dpi-Anzeige bietet.
ms.assetid: 1809ab0e-853f-4dac-be97-563c92b9caee
keywords:
- Direct2D, High-dpi
- High-dpi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6548849416268f31b8b0c4a4261347c818ffa24c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949060"
---
# <a name="direct2d-and-high-dpi"></a><span data-ttu-id="dfed6-105">Direct2D und High-dpi</span><span class="sxs-lookup"><span data-stu-id="dfed6-105">Direct2D and High-DPI</span></span>

<span data-ttu-id="dfed6-106">Das Schreiben einer dpi-fähigen Anwendung ist der Schlüssel, mit dem eine Benutzeroberfläche (UI) über eine Vielzahl von Anzeigeeinstellungen mit hoher dpi hinweg konsistent aussehen kann.</span><span class="sxs-lookup"><span data-stu-id="dfed6-106">Writing a DPI-aware application is the key to making a user interface (UI) look consistently good across a wide variety of high-DPI display settings.</span></span> <span data-ttu-id="dfed6-107">Eine Anwendung, die nicht dpi-fähig ist, aber in einer Einstellung mit hoher dpi-Anzeige ausgeführt wird, kann von vielen visuellen Elementen leiden, einschließlich falscher Skalierung von Benutzeroberflächen Elementen, ausgeschnittenen Text und unscharfe Bilder.</span><span class="sxs-lookup"><span data-stu-id="dfed6-107">An application that is not DPI-aware but is running on a high-DPI display setting can suffer from many visual artifacts, including incorrect scaling of UI elements, clipped text, and blurry images.</span></span> <span data-ttu-id="dfed6-108">Durch Hinzufügen von Unterstützung in Ihrer Anwendung für dpi-Bewusstsein machen Sie die Darstellung der Benutzeroberfläche Ihrer Anwendung besser vorhersagbar, sodass Sie für Benutzer visuell ansprechend und leichter lesbar ist.</span><span class="sxs-lookup"><span data-stu-id="dfed6-108">By adding support in your application for DPI-awareness, you make the presentation of your application's UI more predictable, making it more visually appealing and easier to read for users.</span></span> <span data-ttu-id="dfed6-109">Glücklicherweise erleichtert Direct2D das Schreiben von Anwendungen, die gut in High-dpi funktionieren.</span><span class="sxs-lookup"><span data-stu-id="dfed6-109">Fortunately, Direct2D makes it easier than ever to write applications that work well in high-DPI.</span></span> <span data-ttu-id="dfed6-110">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="dfed6-110">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="dfed6-111">High-dpi-Unterstützung in Direct2D</span><span class="sxs-lookup"><span data-stu-id="dfed6-111">High-DPI Support in Direct2D</span></span>](#high-dpi-support-in-direct2d)
-   [<span data-ttu-id="dfed6-112">Windows 8 und High-dpi</span><span class="sxs-lookup"><span data-stu-id="dfed6-112">Windows 8 and High-DPI</span></span>](#windows-8-and-high-dpi)
-   [<span data-ttu-id="dfed6-113">Was ist eine DIP?</span><span class="sxs-lookup"><span data-stu-id="dfed6-113">What is a DIP?</span></span>](#what-is-a-dip)
-   [<span data-ttu-id="dfed6-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dfed6-114">Related topics</span></span>](#related-topics)

## <a name="high-dpi-support-in-direct2d"></a><span data-ttu-id="dfed6-115">High-dpi-Unterstützung in Direct2D</span><span class="sxs-lookup"><span data-stu-id="dfed6-115">High-DPI Support in Direct2D</span></span>

<span data-ttu-id="dfed6-116">Direct2D bietet die folgenden Features für die Arbeit mit Szenarien mit hoher dpi-Verwendung:</span><span class="sxs-lookup"><span data-stu-id="dfed6-116">Direct2D provides the following features for working with high-DPI scenarios:</span></span>

-   <span data-ttu-id="dfed6-117">Der System-dpi wird beim Erstellen eines Renderziels automatisch berücksichtigt, solange das Anwendungs Manifest angibt, dass dpi korrekt von der Anwendung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="dfed6-117">It automatically honors the system DPI when creating a windowed render target, so long as the application manifest indicates that the application handles DPI correctly.</span></span> <span data-ttu-id="dfed6-118">(Informationen dazu, wie Sie deklarieren, dass Ihre Anwendung dpi-fähig ist, finden [Sie unter sicherstellen, dass Ihre Anwendung ordnungsgemäß auf hoch-dpi-anzeigen angezeigt](how-to--size-a-window-properly-for-high-dpi-displays.md)wird.)</span><span class="sxs-lookup"><span data-stu-id="dfed6-118">(For information on how to declare that your application is DPI-aware, see [How to Ensure That Your Application Displays Properly on High-DPI Displays](how-to--size-a-window-properly-for-high-dpi-displays.md).)</span></span>
-   <span data-ttu-id="dfed6-119">Er drückt Koordinaten in Dips (geräteunabhängige Pixel) aus, sodass die Anwendung automatisch skaliert werden kann, wenn die dpi-Einstellung geändert wird.</span><span class="sxs-lookup"><span data-stu-id="dfed6-119">It expresses coordinates in DIPs (Device Independent Pixels), which enables the application to scale automatically when the DPI setting changes.</span></span>
-   <span data-ttu-id="dfed6-120">Bitmaps können einen dpi-Wert aufweisen und diese ordnungsgemäß skalieren, indem Sie den dpi-Wert berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="dfed6-120">It enables bitmaps to have a DPI and correctly scales them by taking the DPI into account.</span></span> <span data-ttu-id="dfed6-121">Diese Funktion kann auch verwendet werden, um Symbole in unterschiedlichen Auflösungen beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="dfed6-121">This feature can also be used to maintain icons at different resolutions.</span></span>
-   <span data-ttu-id="dfed6-122">Die meisten Ressourcen werden in Dips ausgedrückt, wodurch die Ressourcen automatisch unabhängig von der Auflösung werden.</span><span class="sxs-lookup"><span data-stu-id="dfed6-122">It expresses most resources in DIPs, which makes the resources automatically independent of resolution.</span></span>
-   <span data-ttu-id="dfed6-123">Es verwendet einen Gleit Komma Koordinaten Bereich und Antialiasing, sodass jeder Inhalt auf beliebige dpi-Werte skaliert werden kann.</span><span class="sxs-lookup"><span data-stu-id="dfed6-123">It uses a floating-point coordinate space and antialiasing, so any content can be scaled to any arbitrary DPI.</span></span>

<span data-ttu-id="dfed6-124">Die Direct2D-Grafik Pipeline ist so konzipiert, dass Sie zwischen 96 dpi und 1200dpi skaliert.</span><span class="sxs-lookup"><span data-stu-id="dfed6-124">The Direct2D graphics pipeline is designed to scale from 96 DPI to 1200DPI.</span></span>

## <a name="windows-8-and-high-dpi"></a><span data-ttu-id="dfed6-125">Windows 8 und High-dpi</span><span class="sxs-lookup"><span data-stu-id="dfed6-125">Windows 8 and High-DPI</span></span>

<span data-ttu-id="dfed6-126">Ab Windows 8 gibt es zusätzliche Features für die Unterstützung von hoch dpi.</span><span class="sxs-lookup"><span data-stu-id="dfed6-126">Starting with Windows 8, there are additional features for high-DPI support.</span></span>

<span data-ttu-id="dfed6-127">Wenn der Gerätekontext dpi hoch genug ist, ändert Direct2D den Schwellenwert, der zum Aktivieren des vertikalen Antialiasing von Text verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dfed6-127">If the device context DPI is high enough, Direct2D changes the threshold it uses to enable vertical antialiasing of text.</span></span> <span data-ttu-id="dfed6-128">Dies führt zu schnellerem Text Rendering in hoch dpi-anzeigen.</span><span class="sxs-lookup"><span data-stu-id="dfed6-128">This results in faster text rendering on high-DPI displays.</span></span> <span data-ttu-id="dfed6-129">Darüber hinaus können Sie den Einheits Modus mithilfe der [**ID2D1DeviceContext::**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) \*-Methode auf Pixel anstelle von Dips umstellen.</span><span class="sxs-lookup"><span data-stu-id="dfed6-129">Additionally, you can switch the unit mode to pixels instead of DIPs using the [**ID2D1DeviceContext::SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) method.</span></span> <span data-ttu-id="dfed6-130">Wenn Sie den Einheiten Modus auf Pixel und den Gerätekontext dpi auf den Bildschirm dpi festlegen, ist die Optimierung weiterhin aktiviert.</span><span class="sxs-lookup"><span data-stu-id="dfed6-130">If you set the unit mode to pixels and the device context DPI to the screen DPI, the optimization is still enabled.</span></span>

## <a name="what-is-a-dip"></a><span data-ttu-id="dfed6-131">Was ist eine DIP?</span><span class="sxs-lookup"><span data-stu-id="dfed6-131">What is a DIP?</span></span>

<span data-ttu-id="dfed6-132">Bei einem geräteunabhängigen Pixel (DIP) handelt es sich um ein logisches Pixel, das den Pixeln des physischen Geräts über einen skalaren, den dpi-Wert zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="dfed6-132">A device independent pixel (DIP) is a logical pixel that maps to the pixels of the physical device through a scalar, the DPI.</span></span> <span data-ttu-id="dfed6-133">DPI steht für Punkte pro Zoll, wobei ein Punkt ein physisches Geräte Pixel darstellt.</span><span class="sxs-lookup"><span data-stu-id="dfed6-133">DPI stands for dots per inch, where a dot represents a physical device pixel.</span></span> <span data-ttu-id="dfed6-134">(Die Nomenklatur stammt aus dem Druck, wobei Punkte der kleinste frei Hand Punkt sind, den ein Druckprozess verursachen kann).</span><span class="sxs-lookup"><span data-stu-id="dfed6-134">(The nomenclature comes from printing, where dots are the smallest ink dot that a printing process can produce).</span></span> <span data-ttu-id="dfed6-135">Da ein Standard Monitor, der 96 Punkte pro Zoll hat, den dpi-Wert 96 bedeutete, dass ein Geräte unabhängiges Pixel (oder DIP) 1:1 mit einem physischen Pixel zugeordnet hat.</span><span class="sxs-lookup"><span data-stu-id="dfed6-135">Because a standard monitor used to have 96 dots per inch, a DPI of 96 meant that a device independent pixel (or DIP) mapped 1:1 with a physical pixel.</span></span> <span data-ttu-id="dfed6-136">Wenn z. b. der dpi-Code 96 \* 2 = 192 ist, würde eine einzelne DIP zwei physische Pixel umfassen.</span><span class="sxs-lookup"><span data-stu-id="dfed6-136">For example, if the DPI were 96\*2 = 192, then a single DIP would encompass two physical pixels.</span></span>

<span data-ttu-id="dfed6-137">Es gibt zahlreiche Gründe, warum Anwendungen diese Skalierung nicht unbedingt ordnungsgemäß verarbeiten müssen. einer der einfachsten Gründe hierfür ist, dass zusätzliche Arbeit erforderlich ist, um diesen Skalarwert beim Rendern zu ermitteln und zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="dfed6-137">There are many reasons why applications don't necessarily handle this scaling correctly; one of the simplest reasons is that it requires extra work to discover and use this scalar value when rendering.</span></span> <span data-ttu-id="dfed6-138">In Direct2D wird die Skalierung standardmäßig angewendet.</span><span class="sxs-lookup"><span data-stu-id="dfed6-138">In Direct2D, the scaling is applied by default.</span></span> <span data-ttu-id="dfed6-139">Aufgrund dieser Zuordnung kann es vorkommen, dass physische Geräte Pixel an Bruch Koordinaten in Bruchteilen stehen. Dies ist einer der Gründe, warum Direct2D einen Gleit Komma Koordinaten Bereich verwendet.</span><span class="sxs-lookup"><span data-stu-id="dfed6-139">Because of this mapping, physical device pixels might end up at fractional DIP coordinates, which is one of the reasons why Direct2D uses a floating-point coordinate space.</span></span>

<dl> <span data-ttu-id="dfed6-140">physisches Pixel = (DIP × dpi)/96</span><span class="sxs-lookup"><span data-stu-id="dfed6-140">physical pixel = (dip × DPI) / 96</span></span>  
</dl>

<span data-ttu-id="dfed6-141">Um ein physisches Pixel in eine DIP zu konvertieren, verwenden Sie die folgende Formel:</span><span class="sxs-lookup"><span data-stu-id="dfed6-141">To convert a physical pixel to a DIP, use this formula:</span></span>

<dl> <span data-ttu-id="dfed6-142">DIP = (physisches Pixel × 96)/dpi</span><span class="sxs-lookup"><span data-stu-id="dfed6-142">dip = (physical pixel × 96) / DPI</span></span>  
</dl>

> [!Note]
>
> <span data-ttu-id="dfed6-143">Ab Windows 8 können Sie den Einheits Modus mithilfe der [**ID2D1DeviceContext::**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) \*-Methode auf Pixel anstelle von Dips umstellen.</span><span class="sxs-lookup"><span data-stu-id="dfed6-143">Starting with Windows 8, you can switch the unit mode to pixels instead of DIPs using the [**ID2D1DeviceContext::SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) method.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="dfed6-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dfed6-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfed6-145">So stellen Sie sicher, dass Ihre Anwendung auf hoch-dpi-anzeigen ordnungsgemäß angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="dfed6-145">How to Ensure That Your Application Displays Properly on High-DPI Displays</span></span>](how-to--size-a-window-properly-for-high-dpi-displays.md)
</dt> </dl>

 

 