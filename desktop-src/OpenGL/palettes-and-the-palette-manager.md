---
title: Paletten und der Palette-Manager
description: Der Windows-palettenmanager, der Teil des GDI ist, zielt speziell auf 8-Bit-Anzeige Adapter mit einer Hardware Palette von 256-Farb Einträgen ab.
ms.assetid: 3bfa5077-37ac-4597-98da-f26ad1c107a1
keywords:
- OpenGL unter Windows, Palette Manager
- OpenGL unter Windows, Hardware Paletten
- Palette-Manager OpenGL
- Hardware Paletten OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dac7d122ec36201e0156a141efc3291a87c7150
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341855"
---
# <a name="palettes-and-the-palette-manager"></a><span data-ttu-id="bef6b-107">Paletten und der Palette-Manager</span><span class="sxs-lookup"><span data-stu-id="bef6b-107">Palettes and the Palette Manager</span></span>

<span data-ttu-id="bef6b-108">Der Windows-palettenmanager, der Teil des GDI ist, zielt speziell auf 8-Bit-Anzeige Adapter mit einer *Hardware Palette* von 256-Farb Einträgen ab.</span><span class="sxs-lookup"><span data-stu-id="bef6b-108">The Windows Palette Manager, which is part of the GDI, specifically targets 8-bit display adapters with a *hardware palette* of 256 color entries.</span></span> <span data-ttu-id="bef6b-109">Pixel auf dem Bildschirm werden als 8-Bit-Index in der Hardware Palette gespeichert.</span><span class="sxs-lookup"><span data-stu-id="bef6b-109">Pixels on the screen are stored as an 8-bit index into the hardware palette.</span></span> <span data-ttu-id="bef6b-110">Jeder Eintrag in der Hardware Palette definiert in der Regel eine 24-Bit-Farbe (8 von rot, grün und blau).</span><span class="sxs-lookup"><span data-stu-id="bef6b-110">Each entry in the hardware palette usually defines a 24-bit color (8 each of red, green, and blue).</span></span>

<span data-ttu-id="bef6b-111">Der Palette-Manager verwaltet eine *Systempalette* , bei der es sich um eine Kopie der Hardware Palette handelt.</span><span class="sxs-lookup"><span data-stu-id="bef6b-111">The Palette Manager maintains a *system palette* that is a copy of the hardware palette.</span></span> <span data-ttu-id="bef6b-112">Die Systempalette ist in zwei Abschnitte unterteilt: 20 reservierte Farben und die restlichen 236-Farben, die Sie mit dem palettenmanager festlegen können.</span><span class="sxs-lookup"><span data-stu-id="bef6b-112">The system palette is divided into two sections: 20 reserved colors and the remaining 236 colors, which you can set using the Palette Manager.</span></span>

<span data-ttu-id="bef6b-113">Eine standardmäßige, 20-farbige, *logische Palette* wird ausgewählt und in einem Gerätekontext realisiert.</span><span class="sxs-lookup"><span data-stu-id="bef6b-113">A default 20-color *logical palette* is selected and realized into a device context.</span></span> <span data-ttu-id="bef6b-114">Sie können eine neue logische Palette erstellen und verwenden.</span><span class="sxs-lookup"><span data-stu-id="bef6b-114">You can create and use a new logical palette.</span></span> <span data-ttu-id="bef6b-115">Wählen Sie die logische Palette aus, die Sie erstellt haben, um die Systempalette zu ändern.</span><span class="sxs-lookup"><span data-stu-id="bef6b-115">To change the system palette, select and realize the logical palette you created.</span></span>

<span data-ttu-id="bef6b-116">Wahrscheinlich erstellen Sie eine logische Palette, um die Farben anzugeben, die Sie in ihrer OpenGL-Anwendung anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="bef6b-116">You'll probably create a logical palette to specify the colors you want displayed in your OpenGL application.</span></span> <span data-ttu-id="bef6b-117">Mit bestimmten GDI-aufrufen können Sie den größten Teil der Systempalette temporär durch eine logische Palette ersetzen.</span><span class="sxs-lookup"><span data-stu-id="bef6b-117">Using certain GDI calls, you can temporarily replace most of the system palette with a logical palette.</span></span> <span data-ttu-id="bef6b-118">Mithilfe einer logischen Palette können Sie Pixel Farben für das GDI mithilfe des RGBA-oder des Farb Index Modus definieren.</span><span class="sxs-lookup"><span data-stu-id="bef6b-118">Using a logical palette, you can define pixel colors for the GDI using either the RGBA or the color-index mode.</span></span> <span data-ttu-id="bef6b-119">Die maximale Größe einer logischen Palette beträgt 256 Farben für 8-Bit-Geräte und 4.096-Farben auf einem echten Farbgerät (16, 24 und 32 Bits).</span><span class="sxs-lookup"><span data-stu-id="bef6b-119">The maximum size of a logical palette is 256 colors for 8-bit devices and 4,096 colors on a true-color device (16, 24, and 32 bits).</span></span>

<span data-ttu-id="bef6b-120">Weitere Informationen zu den Modi RGBA und Color-Index finden Sie unter [RGBA-Modus und Windows-Palettenverwaltung](rgba-mode-and-windows-palette-management.md) und [OpenGL-Farbmodi und Windows-Palettenverwaltung](opengl-color-modes-and-windows-palette-management.md).</span><span class="sxs-lookup"><span data-stu-id="bef6b-120">For more information on the RGBA and color-index modes, see [RGBA Mode and Windows Palette Management](rgba-mode-and-windows-palette-management.md) and [OpenGL Color Modes and Windows Palette Management](opengl-color-modes-and-windows-palette-management.md).</span></span>

 

 




