---
description: Windows unterstützt fünf Grafikmodi, die es einer Anwendung ermöglichen, anzugeben, wie Farben gemischt werden, wo die Ausgabe angezeigt wird, wie die Ausgabe skaliert wird usw. Diese Modi, die auf einem DC gespeichert werden, werden in der folgenden Tabelle beschrieben.
ms.assetid: 061af47e-fd49-4eb4-9b1b-03eb9c841622
title: Grafikmodi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 823c7e25024eafb3b111b96b97907bc9b772006a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528343"
---
# <a name="graphic-modes"></a><span data-ttu-id="72e16-104">Grafikmodi</span><span class="sxs-lookup"><span data-stu-id="72e16-104">Graphic Modes</span></span>

<span data-ttu-id="72e16-105">Windows unterstützt fünf Grafikmodi, die es einer Anwendung ermöglichen, anzugeben, wie Farben gemischt werden, wo die Ausgabe angezeigt wird, wie die Ausgabe skaliert wird usw.</span><span class="sxs-lookup"><span data-stu-id="72e16-105">Windows supports five graphic modes that allow an application to specify how colors are mixed, where output appears, how the output is scaled, and so on.</span></span> <span data-ttu-id="72e16-106">Diese Modi, die auf einem DC gespeichert werden, werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="72e16-106">These modes, which are stored in a DC, are described in the following table.</span></span>



| <span data-ttu-id="72e16-107">Grafikmodus</span><span class="sxs-lookup"><span data-stu-id="72e16-107">Graphics mode</span></span> | <span data-ttu-id="72e16-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72e16-108">Description</span></span>                                                                                                                |
|---------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72e16-109">Hintergrund</span><span class="sxs-lookup"><span data-stu-id="72e16-109">Background</span></span>    | <span data-ttu-id="72e16-110">Definiert, wie Hintergrundfarben mit vorhandenen Fenstern oder Bildschirmfarben für Bitmap-und Text Vorgänge gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="72e16-110">Defines how background colors are mixed with existing window or screen colors for bitmap and text operations.</span></span>              |
| <span data-ttu-id="72e16-111">Zeichnung</span><span class="sxs-lookup"><span data-stu-id="72e16-111">Drawing</span></span>       | <span data-ttu-id="72e16-112">Definiert, wie Vorder Grundfarben mit vorhandenen Fenstern oder Bildschirmfarben für Stift-, Pinsel-, Bitmap-und Text Vorgänge gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="72e16-112">Defines how foreground colors are mixed with existing window or screen colors for pen, brush, bitmap, and text operations.</span></span> |
| <span data-ttu-id="72e16-113">Zuordnung</span><span class="sxs-lookup"><span data-stu-id="72e16-113">Mapping</span></span>       | <span data-ttu-id="72e16-114">Definiert, wie die Grafikausgabe aus dem logischen (oder weltweiten) Raum auf dem Fenster, dem Bildschirm oder dem Drucker Papier zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="72e16-114">Defines how graphics output is mapped from logical (or world) space onto the window, screen, or printer paper.</span></span>             |
| <span data-ttu-id="72e16-115">Polygon-Füllung</span><span class="sxs-lookup"><span data-stu-id="72e16-115">Polygon-fill</span></span>  | <span data-ttu-id="72e16-116">Definiert, wie das Pinsel Muster verwendet wird, um das innere komplexer Regionen auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="72e16-116">Defines how the brush pattern is used to fill the interior of complex regions.</span></span>                                             |
| <span data-ttu-id="72e16-117">Dehnung</span><span class="sxs-lookup"><span data-stu-id="72e16-117">Stretching</span></span>    | <span data-ttu-id="72e16-118">Definiert, wie Bitmapfarben mit vorhandenen Fenstern oder Bildschirmfarben gemischt werden, wenn die Bitmap komprimiert (oder zentral herunterskaliert) wird.</span><span class="sxs-lookup"><span data-stu-id="72e16-118">Defines how bitmap colors are mixed with existing window or screen colors when the bitmap is compressed (or scaled down).</span></span>  |



 

<span data-ttu-id="72e16-119">Wie bei grafischen Objekten initialisiert das System einen DC mit Standard Grafikmodi.</span><span class="sxs-lookup"><span data-stu-id="72e16-119">As it does with graphic objects, the system initializes a DC with default graphic modes.</span></span> <span data-ttu-id="72e16-120">Eine Anwendung kann diese Standard Modi abrufen und überprüfen, indem Sie die folgenden Funktionen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="72e16-120">An application can retrieve and examine these default modes by calling the following functions.</span></span>



| <span data-ttu-id="72e16-121">Grafikmodus</span><span class="sxs-lookup"><span data-stu-id="72e16-121">Graphics mode</span></span> | <span data-ttu-id="72e16-122">Funktion</span><span class="sxs-lookup"><span data-stu-id="72e16-122">Function</span></span>                                       |
|---------------|------------------------------------------------|
| <span data-ttu-id="72e16-123">Hintergrund</span><span class="sxs-lookup"><span data-stu-id="72e16-123">Background</span></span>    | [<span data-ttu-id="72e16-124">**Getbkmode**</span><span class="sxs-lookup"><span data-stu-id="72e16-124">**GetBkMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode)                 |
| <span data-ttu-id="72e16-125">Zeichnung</span><span class="sxs-lookup"><span data-stu-id="72e16-125">Drawing</span></span>       | [<span data-ttu-id="72e16-126">**GetROP2**</span><span class="sxs-lookup"><span data-stu-id="72e16-126">**GetROP2**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getrop2)                     |
| <span data-ttu-id="72e16-127">Zuordnung</span><span class="sxs-lookup"><span data-stu-id="72e16-127">Mapping</span></span>       | [<span data-ttu-id="72e16-128">**Getmapmode**</span><span class="sxs-lookup"><span data-stu-id="72e16-128">**GetMapMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode)               |
| <span data-ttu-id="72e16-129">Polygon-Füllung</span><span class="sxs-lookup"><span data-stu-id="72e16-129">Polygon-fill</span></span>  | [<span data-ttu-id="72e16-130">**Getpolyfillmode**</span><span class="sxs-lookup"><span data-stu-id="72e16-130">**GetPolyFillMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode)     |
| <span data-ttu-id="72e16-131">Dehnung</span><span class="sxs-lookup"><span data-stu-id="72e16-131">Stretching</span></span>    | [<span data-ttu-id="72e16-132">**Getstretchbltmode**</span><span class="sxs-lookup"><span data-stu-id="72e16-132">**GetStretchBltMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getstretchbltmode) |



 

<span data-ttu-id="72e16-133">Eine Anwendung kann die Standard Modi ändern, indem Sie eine der folgenden Funktionen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="72e16-133">An application can change the default modes by calling one of the following functions.</span></span>



| <span data-ttu-id="72e16-134">Grafikmodus</span><span class="sxs-lookup"><span data-stu-id="72e16-134">Graphics mode</span></span> | <span data-ttu-id="72e16-135">Funktion</span><span class="sxs-lookup"><span data-stu-id="72e16-135">Function</span></span>                                       |
|---------------|------------------------------------------------|
| <span data-ttu-id="72e16-136">Hintergrund</span><span class="sxs-lookup"><span data-stu-id="72e16-136">Background</span></span>    | [<span data-ttu-id="72e16-137">**Setbkmode**</span><span class="sxs-lookup"><span data-stu-id="72e16-137">**SetBkMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode)                 |
| <span data-ttu-id="72e16-138">Zeichnung</span><span class="sxs-lookup"><span data-stu-id="72e16-138">Drawing</span></span>       | [<span data-ttu-id="72e16-139">**SetROP2**</span><span class="sxs-lookup"><span data-stu-id="72e16-139">**SetROP2**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setrop2)                     |
| <span data-ttu-id="72e16-140">Zuordnung</span><span class="sxs-lookup"><span data-stu-id="72e16-140">Mapping</span></span>       | [<span data-ttu-id="72e16-141">**Setmapmode**</span><span class="sxs-lookup"><span data-stu-id="72e16-141">**SetMapMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)               |
| <span data-ttu-id="72e16-142">Polygon-Füllung</span><span class="sxs-lookup"><span data-stu-id="72e16-142">Polygon-fill</span></span>  | [<span data-ttu-id="72e16-143">**Setpolyfillmode**</span><span class="sxs-lookup"><span data-stu-id="72e16-143">**SetPolyFillMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode)     |
| <span data-ttu-id="72e16-144">Dehnung</span><span class="sxs-lookup"><span data-stu-id="72e16-144">Stretching</span></span>    | [<span data-ttu-id="72e16-145">**Setstretchbltmode**</span><span class="sxs-lookup"><span data-stu-id="72e16-145">**SetStretchBltMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) |



 

 

 



