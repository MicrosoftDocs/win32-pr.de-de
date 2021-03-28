---
description: Wenn eine Anwendung eine Zeichnungs Funktion aufruft, um eine Form zu zeichnen, positioniert das System einen Pinsel am Anfang des Zeichnungs Vorgangs und ordnet ein Pixel in der Pinsel Bitmap dem Client Bereich am Fenster Ursprung zu. Dies ist die linke obere Ecke des Fensters.
ms.assetid: b951fd9a-1e87-4b17-9be8-263896c73922
title: Pinsel Ursprung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 016237b97a52da6fd7fa14a3b6ba2dc25b03b96e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104571193"
---
# <a name="brush-origin"></a><span data-ttu-id="d8c9b-103">Pinsel Ursprung</span><span class="sxs-lookup"><span data-stu-id="d8c9b-103">Brush Origin</span></span>

<span data-ttu-id="d8c9b-104">Wenn eine Anwendung eine Zeichnungs Funktion aufruft, um eine Form zu zeichnen, positioniert das System einen Pinsel am Anfang des Zeichnungs Vorgangs und ordnet ein Pixel in der Pinsel Bitmap dem Client Bereich am *Fenster Ursprung* zu. Dies ist die linke obere Ecke des Fensters.</span><span class="sxs-lookup"><span data-stu-id="d8c9b-104">When an application calls a drawing function to paint a shape, the system positions a brush at the start of the paint operation and maps a pixel in the brush bitmap to the client area at the *window origin*, which is the upper-left corner of the window.</span></span> <span data-ttu-id="d8c9b-105">Die Koordinaten des Pixels, das vom System zugeordnet wird, werden als *Pinsel Ursprung* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d8c9b-105">The coordinates of the pixel that the system maps are called the *brush origin*.</span></span> <span data-ttu-id="d8c9b-106">Der Standard Pinsel Ursprung befindet sich in der oberen linken Ecke der Pinsel Bitmap an den Koordinaten (0,0).</span><span class="sxs-lookup"><span data-stu-id="d8c9b-106">The default brush origin is located in the upper-left corner of the brush bitmap, at the coordinates (0,0).</span></span> <span data-ttu-id="d8c9b-107">Das System kopiert dann den Pinsel in den Client Bereich und bildet so ein Muster, das so groß wie die Bitmap ist.</span><span class="sxs-lookup"><span data-stu-id="d8c9b-107">The system then copies the brush across the client area, forming a pattern that is as tall as the bitmap.</span></span> <span data-ttu-id="d8c9b-108">Der Kopiervorgang wird zeilenweise fortgesetzt, bis der gesamte Client Bereich ausgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="d8c9b-108">The copy operation continues, row by row, until the entire client area is filled.</span></span> <span data-ttu-id="d8c9b-109">Allerdings ist das Pinsel Muster nur innerhalb der Grenzen der angegebenen Form sichtbar.</span><span class="sxs-lookup"><span data-stu-id="d8c9b-109">However, the brush pattern is visible only within the boundaries of the specified shape.</span></span>

<span data-ttu-id="d8c9b-110">Es gibt Instanzen, wenn der Standard Pinsel Ursprung nicht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d8c9b-110">There are instances when the default brush origin should not be used.</span></span> <span data-ttu-id="d8c9b-111">Beispielsweise kann es erforderlich sein, dass eine Anwendung denselben Pinsel verwendet, um die Hintergründe der übergeordneten und untergeordneten Fenster zu zeichnen und den Hintergrund eines untergeordneten Fensters mit dem des übergeordneten Fensters zu mischen.</span><span class="sxs-lookup"><span data-stu-id="d8c9b-111">For example, it may be necessary for an application to use the same brush to paint the backgrounds of its parent and child windows and blend a child window's background with that of the parent window.</span></span> <span data-ttu-id="d8c9b-112">Zu diesem Zweck sollte die Anwendung den Pinsel Ursprung zurücksetzen, indem Sie die Funktion [**setbrushorgex**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex) aufruft und den Ursprung um die erforderliche Anzahl von Pixeln verschiebt.</span><span class="sxs-lookup"><span data-stu-id="d8c9b-112">To do this, the application should reset the brush origin by calling the [**SetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex) function and shifting the origin the required number of pixels.</span></span> <span data-ttu-id="d8c9b-113">(Eine Anwendung kann den aktuellen Pinsel Ursprung durch Aufrufen der [**getbrushorgex**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex) -Funktion abrufen.)</span><span class="sxs-lookup"><span data-stu-id="d8c9b-113">(An application can retrieve the current brush origin by calling the [**GetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex) function.)</span></span>

<span data-ttu-id="d8c9b-114">In der folgenden Abbildung ist ein fünf zeiiger Stern dargestellt, der mit einem von der Anwendung definierten Pinsel gefüllt wurde.</span><span class="sxs-lookup"><span data-stu-id="d8c9b-114">The following illustration shows a five-pointed star filled by using an application-defined brush.</span></span> <span data-ttu-id="d8c9b-115">Die Abbildung zeigt ein Zoom Bild des Pinsels sowie den Speicherort, an dem er am Anfang des Paint-Vorgangs zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="d8c9b-115">The illustration shows a zoomed image of the brush, as well as the location to which it was mapped at the beginning of the paint operation.</span></span>

![Abbildung, die anzeigt, dass der Pinsel Ursprung dem Fenster Ursprung zugeordnet ist](images/csbru-01.png)

 

 



