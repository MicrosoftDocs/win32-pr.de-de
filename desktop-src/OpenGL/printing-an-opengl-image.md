---
title: Drucken eines OpenGL-Bilds
description: Sie können die in erweiterten Metadateien gerenderten OpenGL-Bilder drucken.
ms.assetid: 6099cbe2-82f9-46ec-a3ca-74486c111639
keywords:
- OpenGL unter Windows, Drucken
- Drucken von OpenGL-Bildern OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ca0c5260a084796915a7564f793f0e252b5228c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338287"
---
# <a name="printing-an-opengl-image"></a><span data-ttu-id="872d8-105">Drucken eines OpenGL-Bilds</span><span class="sxs-lookup"><span data-stu-id="872d8-105">Printing an OpenGL Image</span></span>

<span data-ttu-id="872d8-106">Sie können die in erweiterten Metadateien gerenderten OpenGL-Bilder drucken.</span><span class="sxs-lookup"><span data-stu-id="872d8-106">You can print OpenGL images rendered in enhanced metafiles.</span></span> <span data-ttu-id="872d8-107">Wenn Sie zu einem Druckergerät (HDC) gerenden werden, muss es von einem metadateispooler unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="872d8-107">When you render to a printer device (HDC) it must be backed by a metafile spooler.</span></span> <span data-ttu-id="872d8-108">OpenGL verwendet Arbeitsspeicher für tiefe, Farbe und andere Puffer zum Speichern der Grafikausgabe an einen Drucker.</span><span class="sxs-lookup"><span data-stu-id="872d8-108">OpenGL uses memory for depth, color, and other buffers to store graphics output to a printer.</span></span> <span data-ttu-id="872d8-109">Da bei der normalen Drucker Auflösung eine beträchtliche Menge an Arbeitsspeicher zum Speichern der Grafikausgabe erforderlich ist, ist für das Drucken eines OpenGL-Images möglicherweise mehr Arbeitsspeicher erforderlich, als im System verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="872d8-109">Because typical printer resolution requires a significant amount of memory to store the graphics output, printing an OpenGL image might require more memory than is available in the system.</span></span> <span data-ttu-id="872d8-110">Um diese Einschränkung zu umgehen, druckt die aktuelle Implementierung von OpenGL OpenGL-Grafiken in Bändern.</span><span class="sxs-lookup"><span data-stu-id="872d8-110">To overcome this limitation, the current implementation of OpenGL prints OpenGL graphics in bands.</span></span> <span data-ttu-id="872d8-111">Dies erhöht jedoch die Zeit, die zum Drucken von OpenGL-Bildern benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="872d8-111">However, this increases the time it takes to print OpenGL images.</span></span>

<span data-ttu-id="872d8-112">Vor dem Drucken eines OpenGL-Bilds müssen Sie die [StartDoc](/windows/desktop/api/wingdi/nf-wingdi-startdoca) -Funktion aufrufen, um die Initialisierung eines Drucker Geräte Kontexts (DC) abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="872d8-112">Before you print an OpenGL image, you must call the [StartDoc](/windows/desktop/api/wingdi/nf-wingdi-startdoca) function to complete the initialization of a printer device context (DC).</span></span> <span data-ttu-id="872d8-113">Nachdem Sie **StartDoc** aufgerufen haben, können Sie renderingkontexte (hglrc) erstellen, die auf dem Druckergerät gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="872d8-113">After calling **StartDoc**, you can create rendering contexts (HGLRC) to render to the printer device.</span></span> <span data-ttu-id="872d8-114">Wenn Sie vor dem Aufrufen von **StartDoc** renderingkontexte erstellen, gibt es keine Möglichkeit, zu bestimmen, ob eine Metadatei gespoolte ist.</span><span class="sxs-lookup"><span data-stu-id="872d8-114">If you create rendering contexts before calling **StartDoc**, there is no way to determine whether a metafile is spooled.</span></span>

<span data-ttu-id="872d8-115">Im folgenden Codebeispiel wird gezeigt, wie ein OpenGL-Bild gedruckt wird:</span><span class="sxs-lookup"><span data-stu-id="872d8-115">The following code sample shows how to print an OpenGL image:</span></span>

``` syntax
HDC            hDC;
DOCINFO        di;
HGLRC          hglrc;

// Call StartDoc to start the document 
StartDoc( hDC, &di );

// Prepare the printer driver to accept data 
StartPage(hDC);

// Create a rendering context using the metafile DC 
hglrc = wglCreateContext ( hDCmetafile );

// Do OpenGL rendering operations here 
    . . .
wglMakeCurrent(NULL, NULL); // Get rid of rendering context 
    . . .
EndPage(hDC); // Finish writing to the page 
EndDoc(hDC); // End the print job
```

<span data-ttu-id="872d8-116">Weitere Informationen zur Verwendung von Metadateien finden Sie unter [erweiterte Metafile-Vorgänge](/windows/desktop/gdi/enhanced-metafile-operations).</span><span class="sxs-lookup"><span data-stu-id="872d8-116">For more information on using metafiles, see [Enhanced Metafile Operations](/windows/desktop/gdi/enhanced-metafile-operations).</span></span>

 

 