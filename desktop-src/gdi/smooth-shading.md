---
description: Smooth Schattierung ist eine Methode zum Schattieren einer Region mit einem Farbverlauf.
ms.assetid: 94f26d15-fb76-47ec-b805-f04975d41b43
title: Smooth-Schattierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5b73738c03147083099a5070e61fe21ca5cac76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217046"
---
# <a name="smooth-shading"></a><span data-ttu-id="ddd87-103">Smooth-Schattierung</span><span class="sxs-lookup"><span data-stu-id="ddd87-103">Smooth Shading</span></span>

<span data-ttu-id="ddd87-104">*Smooth Schattierung* ist eine Methode zum Schattieren einer Region mit einem Farbverlauf.</span><span class="sxs-lookup"><span data-stu-id="ddd87-104">*Smooth shading* is a method of shading a region with a color gradient.</span></span> <span data-ttu-id="ddd87-105">Durch Einschließen von Farbinformationen, zusammen mit den Begrenzungen des Zeichnungs primitiven, wird der Farbverlauf angegeben.</span><span class="sxs-lookup"><span data-stu-id="ddd87-105">Including color information, along with the bounds of drawing primitive, specifies the color gradient.</span></span> <span data-ttu-id="ddd87-106">GDI linear interpoliert die Farbe des Inneren des primitiven, das an die Farb Endpunkte weitergegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ddd87-106">GDI linearly interpolates the color of the inside of the primitive passed on the color endpoints.</span></span> <span data-ttu-id="ddd87-107">Farb-und Vertex-Informationen sind in der-Struktur der [**dreiseitigen**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) Position in Positionsinformationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="ddd87-107">Color and vertex information is included with position information in the [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) structure.</span></span>

<span data-ttu-id="ddd87-108">Verwenden Sie die [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) -Funktion, um ein Dreieck oder eine Rechteck Struktur auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="ddd87-108">Use the [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) function to fill a triangle or rectangle structure.</span></span> <span data-ttu-id="ddd87-109">Zum Auffüllen eines Dreiecks mit Smooth Schattierung aufrufen Sie **GradientFill** mit den drei Dreieck Endpunkten.</span><span class="sxs-lookup"><span data-stu-id="ddd87-109">To fill a triangle with smooth shading, call **GradientFill** with the three triangle endpoints.</span></span> <span data-ttu-id="ddd87-110">Zum Auffüllen eines Rechtecks mit Smooth Schattierung aufrufen Sie **GradientFill** mit den linken oberen und unteren rechten Rechteck Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="ddd87-110">To fill a rectangle with smooth shading, call **GradientFill** with the upper-left and lower-right rectangle coordinates.</span></span> <span data-ttu-id="ddd87-111">**GradientFill** verweist auf die [**trivertex**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex)-, [**\_ gradientenrect**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)-und [**Gradient- \_ Dreiecks**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle) Strukturen.</span><span class="sxs-lookup"><span data-stu-id="ddd87-111">**GradientFill** references the [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex), [**GRADIENT\_RECT**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect), and [**GRADIENT\_TRIANGLE**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle) structures.</span></span>

<span data-ttu-id="ddd87-112">Ein Beispiel finden Sie unter [Zeichnen eines schattierten Dreiecks](drawing-a-shaded-triangle.md).</span><span class="sxs-lookup"><span data-stu-id="ddd87-112">For an example, see [Drawing a Shaded Triangle](drawing-a-shaded-triangle.md).</span></span>

 

 



