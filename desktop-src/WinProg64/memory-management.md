---
title: Speicherverwaltung unter WOW64
description: Die Speicherverwaltung unter WOW64 hängt von der Prozessorarchitektur ab.
ms.assetid: a3fa6e51-2895-4941-9304-5939208e8102
keywords:
- WOW64 64-Bit-Windows-Programmierung, Speicherverwaltung
- Windows-Programmierung mit der Speicherverwaltung 64-Bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8602bf6e7e7d9e55894215938932559cfadc6848
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390876"
---
# <a name="memory-management-under-wow64"></a><span data-ttu-id="cf154-105">Speicherverwaltung unter WOW64</span><span class="sxs-lookup"><span data-stu-id="cf154-105">Memory Management Under WOW64</span></span>

<span data-ttu-id="cf154-106">Die Speicherverwaltung unter WOW64 hängt von der Prozessorarchitektur ab.</span><span class="sxs-lookup"><span data-stu-id="cf154-106">Memory management under WOW64 depends on the processor architecture.</span></span>

## <a name="itanium-support"></a><span data-ttu-id="cf154-107">Itanium-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="cf154-107">Itanium Support</span></span>

<span data-ttu-id="cf154-108">WOW64 simuliert 4-KB-Seiten oberhalb der nativen 8-KB-Seiten, die der Itanium-Prozessor verwendet.</span><span class="sxs-lookup"><span data-stu-id="cf154-108">WOW64 simulates 4 KB pages on top of the native 8 KB pages that the Itanium processor uses.</span></span> <span data-ttu-id="cf154-109">Der Prozessor unterstützt durch eine ausgezeichnete Simulation mit geringem mehr Aufwand.</span><span class="sxs-lookup"><span data-stu-id="cf154-109">The processor assists by providing excellent simulation with low overhead.</span></span> <span data-ttu-id="cf154-110">Im Simulations Code können folgende Fälle nicht behandelt werden:</span><span class="sxs-lookup"><span data-stu-id="cf154-110">The simulation code cannot handle the following cases:</span></span>

-   <span data-ttu-id="cf154-111">Schreib Nachverfolgung.</span><span class="sxs-lookup"><span data-stu-id="cf154-111">Write tracking.</span></span> <span data-ttu-id="cf154-112">Die Funktionen " [**getwrite**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) " und " [**resetschreitewatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) " werden im Kernel mithilfe der systemeigenen Granularität der Seitengröße implementiert. Dies bedeutet, dass die Seite "WOW64 4 KB" nicht ermitteln kann, welche simulierten 4-KB-Seiten auf der zugrunde liegenden Seite mit 8 KB geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="cf154-112">The [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) and [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) functions are implemented in the kernel using native page-size granularity, which means the WOW64 4 KB page simulation cannot determine which simulated 4 KB pages are written within the underlying 8 KB page.</span></span>
-   <span data-ttu-id="cf154-113">[Address windowingextensions (AWE)](/windows/desktop/Memory/address-windowing-extensions).</span><span class="sxs-lookup"><span data-stu-id="cf154-113">[Address Windowing Extensions (AWE)](/windows/desktop/Memory/address-windowing-extensions).</span></span> <span data-ttu-id="cf154-114">Die AWE-Funktionen arbeiten mit Seitenzahlen, und es gibt keine Möglichkeit, 64-Bit-Seitennummern zu 32-Bit-Seitenzahlen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="cf154-114">The AWE functions operate on page numbers, and there is no way to map 64-bit page numbers to 32-bit page numbers.</span></span>
-   <span data-ttu-id="cf154-115">Abschnitts Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="cf154-115">Section alignment.</span></span> <span data-ttu-id="cf154-116">Bei ausführbaren Images mit einer Abschnitts Ausrichtung, die kleiner als 8 KB ist (der Standardwert ist 4 KB für x86-Images), muss WOW64 alle Bildseiten geändert werden.</span><span class="sxs-lookup"><span data-stu-id="cf154-116">For executable images with section alignment smaller than 8 KB (the default is 4 KB for x86 images), WOW64 must dirty all image pages.</span></span> <span data-ttu-id="cf154-117">Dadurch wird jede Seite in die Auslagerungs Datei kopiert, und es wird verhindert, dass schreibgeschützte Bildseiten zwischen Prozessen freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cf154-117">This effectively copies each page to the page file, and prevents read-only image pages from being shared between processes.</span></span>
-   <span data-ttu-id="cf154-118">Die Funktionen "read [**filescatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) " und " [**Write filegather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) " werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cf154-118">The [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) and [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) functions are not supported.</span></span>

## <a name="x64-and-arm64-support"></a><span data-ttu-id="cf154-119">x64-und ARM64-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="cf154-119">x64 and ARM64 Support</span></span>

<span data-ttu-id="cf154-120">Die systemeigene Seitengröße beträgt 4 KB.</span><span class="sxs-lookup"><span data-stu-id="cf154-120">The native page size is 4 KB.</span></span> <span data-ttu-id="cf154-121">Daher wird Folgendes unterstützt:</span><span class="sxs-lookup"><span data-stu-id="cf154-121">Therefore, the following are supported:</span></span>

-   <span data-ttu-id="cf154-122">Die Funktionen " [**getwrite**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) " und " [**resetschreitewatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) " werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cf154-122">The [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) and [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) functions are supported.</span></span>
-   <span data-ttu-id="cf154-123">Die Funktionen "read [**filescatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) " und " [**Write filegather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) " werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cf154-123">The [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) and [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) functions are supported.</span></span>
-   <span data-ttu-id="cf154-124">Es gibt Vorteile bei der Verwendung großer Adressen, da x64 WOW64 einen virtuellen Adressraum von 4 GB unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cf154-124">There are advantages to using large addresses because x64 WOW64 supports a 4 GB virtual address space.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf154-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cf154-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf154-126">Arbeitsspeicher Grenzwerte für Windows-Releases</span><span class="sxs-lookup"><span data-stu-id="cf154-126">Memory Limits for Windows Releases</span></span>](/windows/desktop/Memory/memory-limits-for-windows-releases)
</dt> <dt>

[<span data-ttu-id="cf154-127">4GT RAM-Optimierung</span><span class="sxs-lookup"><span data-stu-id="cf154-127">4GT RAM Tuning</span></span>](/windows/desktop/Memory/4-gigabyte-tuning)
</dt> </dl>

 

 