---
title: Für Kachel Ressourcen verfügbarer Adressraum
description: In diesem Abschnitt wird der virtuelle Adressraum angegeben, der für Kachel Ressourcen verfügbar ist.
ms.assetid: A3D08564-3C7A-4578-BC38-EE202045580A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c774c697cf5d3bf575d01ce5751dc413c1d14b0
ms.sourcegitcommit: 4dcafeb002cbee4f6028b32a956ec22cb95cbc44
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/13/2019
ms.locfileid: "103719326"
---
# <a name="address-space-available-for-tiled-resources"></a><span data-ttu-id="6d966-103">Für Kachel Ressourcen verfügbarer Adressraum</span><span class="sxs-lookup"><span data-stu-id="6d966-103">Address space available for tiled resources</span></span>

<span data-ttu-id="6d966-104">In diesem Abschnitt wird der virtuelle Adressraum angegeben, der für Kachel Ressourcen verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6d966-104">This section specifies the virtual address space that is available for tiled resources.</span></span>

<span data-ttu-id="6d966-105">Bei 64-Bit-Betriebssystemen sind mindestens 40 Bits des virtuellen Adressraums (1 Terabyte) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6d966-105">On 64-bit operating systems, at least 40 bits of virtual address space (1 Terabyte) is available.</span></span>

<span data-ttu-id="6d966-106">Bei 32-Bit-Betriebssystemen ist der Adressraum 32 Bit (4 GB).</span><span class="sxs-lookup"><span data-stu-id="6d966-106">For 32-bit operating systems, the address space is 32 bit (4 GB).</span></span> <span data-ttu-id="6d966-107">Bei 32-Bit-ARM-Systemen kann die Erstellung einzelner kachelter Ressourcen fehlschlagen, wenn die Zuordnung mehr als 27 Bits des Adressraums (128 MB) verwenden würde.</span><span class="sxs-lookup"><span data-stu-id="6d966-107">For 32-bit ARM systems, individual tiled resource creation can fail if the allocation would use more than 27 bits of address space (128 MB).</span></span> <span data-ttu-id="6d966-108">Dies umfasst alle ausgeblendeten Auffüll Flächen im Adressraum, die die Hardware für Mipmaps, gepackte Kachel Auffüll Zeichen und ggf. das Auffüllen von Oberflächen Dimensionen auf die Potenzen von 2 verwendet.</span><span class="sxs-lookup"><span data-stu-id="6d966-108">This includes any hidden padding in the address space the hardware may use for mipmaps, packed tile padding, and possibly padding surface dimensions to powers of 2.</span></span>

<span data-ttu-id="6d966-109">Auf Grafiksystemen mit einer separaten Seiten Tabelle für die Grafikverarbeitungseinheit (Graphics Processing Unit, GPU) steht der größte Teil dieses Adressraums für GPU-Ressourcen zur Verfügung, die von der Anwendung erstellt werden, obwohl die GPU-Belegungen des Anzeige Treibers in denselben Bereich passen.</span><span class="sxs-lookup"><span data-stu-id="6d966-109">On graphics systems with a separate page table for the graphics processing unit (GPU), most of this address space will be available to GPU resources made by the application, though GPU allocations made by the display driver fit in the same space.</span></span>

<span data-ttu-id="6d966-110">In zukünftigen Systemen mit einer Seiten Tabelle, die von der CPU und GPU gemeinsam genutzt wird, wird der verfügbare Adressraum zwischen allen CPU-und GPU-Belegungen in einem Prozess gemeinsam genutzt.</span><span class="sxs-lookup"><span data-stu-id="6d966-110">On future systems with a page table shared between the CPU and GPU, the available address space is shared between all CPU and GPU allocations in a process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d966-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6d966-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d966-112">Parameter für die Kachel Ressourcen Erstellung</span><span class="sxs-lookup"><span data-stu-id="6d966-112">Tiled resource creation parameters</span></span>](tiled-resource-creation-parameters.md)
</dt> </dl>

 

 




