---
description: So kopieren Sie eine Bitmap in ein Parallelogram Verwenden Sie die plgblt-Funktion, die eine Bitblock Übertragung von einem Rechteck in einem Quell Gerätekontext in ein Parallelogramm in einem Zielgeräte Kontext ausführt.
ms.assetid: fd5b3d9f-fdce-485e-bff8-464d96b8db34
title: Bitmap-Drehung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c8711189182646c55aee414ef92409a6de20ca3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994119"
---
# <a name="bitmap-rotation"></a><span data-ttu-id="c96bc-103">Bitmap-Drehung</span><span class="sxs-lookup"><span data-stu-id="c96bc-103">Bitmap Rotation</span></span>

<span data-ttu-id="c96bc-104">So kopieren Sie eine Bitmap in ein Parallelogram Verwenden Sie die [**plgblt**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt) -Funktion, die eine Bitblock Übertragung von einem Rechteck in einem Quell Gerätekontext in ein Parallelogramm in einem Zielgeräte Kontext ausführt.</span><span class="sxs-lookup"><span data-stu-id="c96bc-104">To copy a bitmap into a parallelogram; use the [**PlgBlt**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt) function, which performs a bit-block transfer from a rectangle in a source device context into a parallelogram in a destination device context.</span></span> <span data-ttu-id="c96bc-105">Um die Bitmap zu drehen, muss eine Anwendung die Koordinaten in den Welteinheiten bereitstellen, die für die Ecken des parallelograms verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c96bc-105">To rotate the bitmap, an application must provide the coordinates, in world units, to be used for the corners of the parallelogram.</span></span> <span data-ttu-id="c96bc-106">(Weitere Informationen zu Drehung und Welteinheiten finden Sie unter [Koordinaten Bereiche und Transformationen](coordinate-spaces-and-transformations.md)).</span><span class="sxs-lookup"><span data-stu-id="c96bc-106">(For more information about rotation and world units, see [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).)</span></span>

 

 



