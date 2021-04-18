---
title: Portieren von Geräte Kontexten und Pixel Formaten
description: Portieren von Geräte Kontexten und Pixel Formaten
ms.assetid: b60cac27-1e2e-4da5-81c4-69446b92f820
keywords:
- Portieren auf OpenGL, Pixel
- OpenGL-portieren, Pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d793c139c6d7a0a0fc85b2e2c36f30176ce9ab6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338977"
---
# <a name="porting-device-contexts-and-pixel-formats"></a><span data-ttu-id="3fc0a-105">Portieren von Geräte Kontexten und Pixel Formaten</span><span class="sxs-lookup"><span data-stu-id="3fc0a-105">Porting Device Contexts and Pixel Formats</span></span>

<span data-ttu-id="3fc0a-106">Jedes Fenster in der Microsoft-Implementierung von OpenGL für Windows verfügt über ein eigenes Aktuelles Pixel Format.</span><span class="sxs-lookup"><span data-stu-id="3fc0a-106">Each window in the Microsoft implementation of OpenGL for Windows has its own current pixel format.</span></span> <span data-ttu-id="3fc0a-107">Ein Pixel Format wird durch eine [**pixelformatdescriptor**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) -Datenstruktur definiert.</span><span class="sxs-lookup"><span data-stu-id="3fc0a-107">A pixel format is defined by a [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure.</span></span> <span data-ttu-id="3fc0a-108">Da jedes Fenster über ein eigenes Pixel Format verfügt, erhalten Sie einen Gerätekontext, legen Sie das Pixel Format des Geräte Kontexts fest, und erstellen Sie dann einen OpenGL-renderingkontext für den Gerätekontext.</span><span class="sxs-lookup"><span data-stu-id="3fc0a-108">Because each window has its own pixel format, you obtain a device context, set the pixel format of the device context, and then create an OpenGL rendering context for the device context.</span></span> <span data-ttu-id="3fc0a-109">Der renderingkontext verwendet automatisch das Pixel Format des Geräte Kontexts.</span><span class="sxs-lookup"><span data-stu-id="3fc0a-109">The rendering context automatically uses the pixel format of its device context.</span></span>

<span data-ttu-id="3fc0a-110">Das X-Fenster System verwendet auch eine Datenstruktur, **xvisualinfo**, um die Eigenschaften der Pixel in einem Fenster anzugeben.</span><span class="sxs-lookup"><span data-stu-id="3fc0a-110">The X Window System also uses a data structure, **XVisualInfo**, to specify the properties of pixels in a window.</span></span> <span data-ttu-id="3fc0a-111">**Xvisualinfo** -Strukturen enthalten eine **visuelle** Datenstruktur, die beschreibt, wie Farb Ressourcen in einem bestimmten Bildschirm verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3fc0a-111">**XVisualInfo** structures contain a **Visual** data structure that describes how color resources are used in a specific screen.</span></span>

<span data-ttu-id="3fc0a-112">Im X-Fenster System wird **xvisualinfo** zum Erstellen eines Fensters verwendet, indem das Fenster auf das gewünschte Pixel Format festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="3fc0a-112">In the X Window System, **XVisualInfo** is used to create a window by setting the window to the pixel format you want.</span></span> <span data-ttu-id="3fc0a-113">Die zurückgegebene-Struktur wird verwendet, um das Fenster und einen renderingkontext zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3fc0a-113">The returned structure is used to create the window and a rendering context.</span></span> <span data-ttu-id="3fc0a-114">In Windows erstellen Sie zunächst ein Fenster und erhalten ein Handle für einen Gerätekontext (HDC) des Fensters.</span><span class="sxs-lookup"><span data-stu-id="3fc0a-114">In Windows, you first create a window and get a handle to a device context (HDC) of the window.</span></span> <span data-ttu-id="3fc0a-115">Der HDC wird dann verwendet, um das Pixel Format für das Fenster festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3fc0a-115">The HDC is then used to set the pixel format for the window.</span></span> <span data-ttu-id="3fc0a-116">Der renderingkontext verwendet das Pixel Format des Fensters.</span><span class="sxs-lookup"><span data-stu-id="3fc0a-116">The rendering context uses the pixel format of the window.</span></span>

<span data-ttu-id="3fc0a-117">In der folgenden Tabelle werden die X-Fenster System-und glx-visuellen Funktionen mit ihren entsprechenden Windows-Pixel Formatfunktionen verglichen.</span><span class="sxs-lookup"><span data-stu-id="3fc0a-117">The following table compares the X Window System and GLX visual functions with their equivalent Windows pixel format functions.</span></span>



| <span data-ttu-id="3fc0a-118">X Fenster/glx-Funktion</span><span class="sxs-lookup"><span data-stu-id="3fc0a-118">X window/GLX visual function</span></span>                                                                                     | <span data-ttu-id="3fc0a-119">Windows-Pixel Format-Funktion</span><span class="sxs-lookup"><span data-stu-id="3fc0a-119">Windows pixel format function</span></span>                                                                                                      |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fc0a-120">Xvisualinfo \* **glxchoosevisual**(Display *\* dpy*, int *Screen*, int *\* atzst*)</span><span class="sxs-lookup"><span data-stu-id="3fc0a-120">XVisualInfo\***glXChooseVisual**( Display *\*dpy*,int *screen*,int *\*attribList*)</span></span>                               | <span data-ttu-id="3fc0a-121">int [**Choice Pixel Format**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)(HDC *hdc*, pixelformatdescriptor *\* ppfd*)</span><span class="sxs-lookup"><span data-stu-id="3fc0a-121">int [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)( HDC *hdc*,PIXELFORMATDESCRIPTOR *\*ppfd*)</span></span>                                      |
| <span data-ttu-id="3fc0a-122">int **glxgetconfig**(Display *\* dpy*, xvisualinfo *\* VIS*, int *\* atzst*, int *\* Wert*)</span><span class="sxs-lookup"><span data-stu-id="3fc0a-122">int **glXGetConfig**( Display *\*dpy*,XVisualInfo *\*vis*,int *\*attribList*,int *\*value*)</span></span>                      | <span data-ttu-id="3fc0a-123">int [**describepixelformat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)(HDC *hdc*, int *ipixelformat*, uint *nbytes*, lppixelformatdescriptor *ppfd*)</span><span class="sxs-lookup"><span data-stu-id="3fc0a-123">int [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)( HDC *hdc*,int *iPixelFormat*,UINT *nBytes*,LPPIXELFORMATDESCRIPTOR *ppfd*)</span></span> |
| <span data-ttu-id="3fc0a-124">Xvisualinfo \* **xgetvisualinfo**(Display *\* dpy*, Long *vinfo \_ Mask*, xvisualinfo *\* vinfo \_ Templ*, int *\* nitems*)</span><span class="sxs-lookup"><span data-stu-id="3fc0a-124">XVisualInfo\***XGetVisualInfo**( Display *\*dpy*,long *vinfo\_mask*,XVisualInfo *\*vinfo\_templ*,int *\*nitems*)</span></span> | <span data-ttu-id="3fc0a-125">int [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)(HDC *hdc*)</span><span class="sxs-lookup"><span data-stu-id="3fc0a-125">int [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)( HDC *hdc*)</span></span>                                                                           |
| <span data-ttu-id="3fc0a-126">Die von **glxchoosevisual** zurückgegebene *Visualisierung* wird verwendet, wenn ein Fenster erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3fc0a-126">The *visual* returned by **glxChooseVisual** is used when a window is created.</span></span>                                   | <span data-ttu-id="3fc0a-127">Bool [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)(HDC *hdc*, int *ipixelformat*, pixelformatdescriptor *\* ppfd*)</span><span class="sxs-lookup"><span data-stu-id="3fc0a-127">BOOL [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)( HDC *hdc*,int *iPixelFormat*,PIXELFORMATDESCRIPTOR *\*ppfd*)</span></span>                        |



 

<span data-ttu-id="3fc0a-128">In den folgenden Abschnitten finden Sie Beispiele für Pixel Format-Code Fragmente für ein X-Fenster System Programm und denselben Code, nachdem er zu Windows portiert wurde.</span><span class="sxs-lookup"><span data-stu-id="3fc0a-128">The following sections give examples of pixel format code fragments for an X Window System program, and the same code after it has been ported to Windows.</span></span>

-   [<span data-ttu-id="3fc0a-129">Code Beispiel für das glx-Pixel Format</span><span class="sxs-lookup"><span data-stu-id="3fc0a-129">GLX Pixel Format Code Sample</span></span>](glx-pixel-format-code-sample.md)
-   [<span data-ttu-id="3fc0a-130">Code Beispiel für Windows-Pixel Format</span><span class="sxs-lookup"><span data-stu-id="3fc0a-130">Windows Pixel Format Code Sample</span></span>](win32-pixel-format-code-sample.md)

<span data-ttu-id="3fc0a-131">Weitere Informationen zu Pixel Formaten finden Sie unter [Pixel Formate](pixel-formats.md).</span><span class="sxs-lookup"><span data-stu-id="3fc0a-131">For more information on pixel formats, see [Pixel Formats](pixel-formats.md).</span></span>

 

 




