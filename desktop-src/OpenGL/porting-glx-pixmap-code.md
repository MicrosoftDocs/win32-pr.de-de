---
title: Portieren von glx-pixmap-Code
description: Portieren von glx-pixmap-Code
ms.assetid: 5b87d26d-b3ea-4f90-9456-d3f7da462948
keywords:
- Pixmaps
- OpenGL unter Windows, Pixmaps
- Portieren auf OpenGL, Pixmaps
- OpenGL-Portierung, Pixmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0dbd7f94736f25346a9136d60feb4fa1bb6c68
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039529"
---
# <a name="porting-glx-pixmap-code"></a><span data-ttu-id="eeb25-107">Portieren von glx-pixmap-Code</span><span class="sxs-lookup"><span data-stu-id="eeb25-107">Porting GLX Pixmap Code</span></span>

<span data-ttu-id="eeb25-108">Das X-Fenster System verwendet *Pixmaps*, bei denen es sich um virtuelle Zeichen Flächen außerhalb des Bildschirms in Form eines dreidimensionalen Arrays von Bits handelt.</span><span class="sxs-lookup"><span data-stu-id="eeb25-108">The X Window System uses *pixmaps*, which are off-screen virtual drawing surfaces in the form of a three-dimensional array of bits.</span></span> <span data-ttu-id="eeb25-109">Sie können sich eine pixmap als Stapel von Bitmaps vorstellen: ein zweidimensionales Array von Pixeln, wobei jedes Pixel einen Wert zwischen 0 und 2N1 hat, wobei N die Tiefe der pixmap ist.</span><span class="sxs-lookup"><span data-stu-id="eeb25-109">You can think of a pixmap as a stack of bitmaps: a two-dimensional array of pixels with each pixel having a value from 0 to 2N1 where N is the depth of the pixmap.</span></span>

<span data-ttu-id="eeb25-110">Für OpenGL-Programme verwenden Sie die glx-Funktionen, **glxkreateglxpixmap** und **glxdestroyglxpixmap**, um die für das Offscreen-Rendering verwendeten glx-Pixmaps zu erstellen und zu zerstören.</span><span class="sxs-lookup"><span data-stu-id="eeb25-110">For OpenGL programs you use the GLX functions, **glXCreateGLXPixmap** and **glXDestroyGLXPixmap**, to create and destroy GLX pixmaps used for off-screen rendering.</span></span>

<span data-ttu-id="eeb25-111">Windows verwendet geräteunabhängige Bitmaps, die die gleiche Funktion wie X Window System-Pixmaps erfüllen.</span><span class="sxs-lookup"><span data-stu-id="eeb25-111">Windows uses device-independent bitmaps that serve the same function as X Window System pixmaps.</span></span> <span data-ttu-id="eeb25-112">Verwenden Sie die standardmäßigen Windows-Bitmap-Funktionen zum Erstellen und zerstören von Bitmaps.</span><span class="sxs-lookup"><span data-stu-id="eeb25-112">Use the standard Windows bitmap functions to create and destroy bitmaps.</span></span>

<span data-ttu-id="eeb25-113">In der folgenden Tabelle sind die glx-pixmap-Funktionen und ihre entsprechenden Windows-Bitmap-Funktionen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="eeb25-113">The following table lists the GLX pixmap functions and their equivalent Windows bitmap functions.</span></span>



| <span data-ttu-id="eeb25-114">Glx-pixmap und Font-Funktion</span><span class="sxs-lookup"><span data-stu-id="eeb25-114">GLX pixmap and font function</span></span>                                                          | <span data-ttu-id="eeb25-115">Windows-Bitmap und-Schriftart Funktion</span><span class="sxs-lookup"><span data-stu-id="eeb25-115">Windows bitmap and font function</span></span>                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeb25-116">Glxpixmap **glxkreateglxpixmap**(Display *\* dpy*, xvisualinfo *\* VIS*, pixmap *pixmap*)</span><span class="sxs-lookup"><span data-stu-id="eeb25-116">GLXPixmap **glXCreateGLXPixmap**( Display *\*dpy*,XVisualInfo *\*vis*,Pixmap *pixmap*)</span></span> | <span data-ttu-id="eeb25-117">HBITMAP- [Editor](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) für *hdc-HDC* lpbitmapinfoheader *lpbmih*, DWORD *fdwinit*, Konstanten Byte *\* lpbinit*, lpbitmapinfo *lpbmi*, uint \* fuusage \***)** HBITMAP [kreatedibsection](/windows/desktop/api/wingdi/nf-wingdi-createdibsection) HDC *hdc*, lpbitmapinfo *lpbmi*, DWORD *finit*, DWORD *IUsage*)</span><span class="sxs-lookup"><span data-stu-id="eeb25-117">HBITMAP [CreateDIBitmap](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) HDC *hdc*,LPBITMAPINFOHEADER *lpbmih*,DWORD *fdwInit*,CONST BYTE *\*lpbInit*,LPBITMAPINFO *lpbmi*,UINT *fuUsage\*\*\*)*\* HBITMAP [CreateDIBSection](/windows/desktop/api/wingdi/nf-wingdi-createdibsection) HDC *hdc*,LPBITMAPINFO *lpbmi*,DWORD *fInit*,DWORD *iUsage*)</span></span><br/> |
| <span data-ttu-id="eeb25-118">void **glxdestroyglxpixmap**(Display *\* dpy*, glxpixmap *pix*)</span><span class="sxs-lookup"><span data-stu-id="eeb25-118">void **glXDestroyGLXPixmap**( Display *\*dpy*,GLXPixmap *pix*)</span></span>                        | <span data-ttu-id="eeb25-119">Bool [DeleteObject](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)(hgdiobj- *hobject*)</span><span class="sxs-lookup"><span data-stu-id="eeb25-119">BOOL [DeleteObject](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)( HGDIOBJ *hObject*)</span></span>                                                                                                                                                                                                                                  |



 

 

