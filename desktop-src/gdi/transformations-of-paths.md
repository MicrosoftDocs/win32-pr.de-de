---
description: Pfade werden mithilfe logischer Einheiten und aktueller Transformationen definiert.
ms.assetid: a5a426ec-25e8-4fe1-985c-d078227e8aba
title: Transformationen von Pfaden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb2c033b5769a4edff29beba6cccbd80cfd26de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980296"
---
# <a name="transformations-of-paths"></a><span data-ttu-id="504b5-103">Transformationen von Pfaden</span><span class="sxs-lookup"><span data-stu-id="504b5-103">Transformations of Paths</span></span>

<span data-ttu-id="504b5-104">Pfade werden mithilfe logischer Einheiten und aktueller Transformationen definiert.</span><span class="sxs-lookup"><span data-stu-id="504b5-104">Paths are defined using logical units and current transformations.</span></span> <span data-ttu-id="504b5-105">(Wenn die [**setworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) -Funktion aufgerufen wurde, sind die logischen Einheiten Welteinheiten. andernfalls sind die logischen Einheiten Seiten Einheiten.) Eine Anwendung kann globale Transformationen verwenden, um die Linien und die Bézier-Kurven zu skalieren, zu drehen, zu scheren, zu übersetzen und wiederzugeben, die einen Pfad definieren.</span><span class="sxs-lookup"><span data-stu-id="504b5-105">(If the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function has been called, the logical units are world units; otherwise, the logical units are page units.) An application can use world transformations to scale, rotate, shear, translate, and reflect the lines and Bézier curves that define a path.</span></span>

> [!Note]  
> <span data-ttu-id="504b5-106">Eine globale Transformation innerhalb einer Pfad Klammer wirkt sich nur auf die Linien und Kurven aus, die nach dem Festlegen der Transformation gezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="504b5-106">A world transformation within a path bracket only affects those lines and curves drawn after the transformation was set.</span></span> <span data-ttu-id="504b5-107">Dies hat keine Auswirkung auf die Linien und Kurven, die gezeichnet wurden, bevor Sie festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="504b5-107">It will have no affect on those lines and curves that were drawn before it was set.</span></span> <span data-ttu-id="504b5-108">Eine Beschreibung der weltweiten Transformation finden Sie unter [Koordinaten Bereiche und Transformationen](coordinate-spaces-and-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="504b5-108">For a description of the world transformation, see [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).</span></span>

 

<span data-ttu-id="504b5-109">Eine Anwendung kann auch [**setworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) verwenden, um die Form des Stifts zu gliedern, der verwendet wird, um einen Pfad zu gliedern, wenn der Stift ein geometrischer Stift ist.</span><span class="sxs-lookup"><span data-stu-id="504b5-109">An application can also use [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) to outline the shape of the pen used to outline a path if the pen is a geometric pen.</span></span> <span data-ttu-id="504b5-110">Eine Beschreibung der geometrischen Stifte finden Sie unter [Stifte](pens.md).</span><span class="sxs-lookup"><span data-stu-id="504b5-110">For a description of geometric pens, see [Pens](pens.md).</span></span>

 

 



