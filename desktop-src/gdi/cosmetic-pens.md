---
description: Die Abmessungen eines kosmetischen Stifts werden in Geräte Einheiten angegeben.
ms.assetid: d4386681-3523-4872-b048-2a5cfbf7d039
title: Kosmetische Stifte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb312ed0b3825397ff79ebc32d363956ad04519
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754465"
---
# <a name="cosmetic-pens"></a><span data-ttu-id="ba2e9-103">Kosmetische Stifte</span><span class="sxs-lookup"><span data-stu-id="ba2e9-103">Cosmetic Pens</span></span>

<span data-ttu-id="ba2e9-104">Die Abmessungen eines kosmetischen Stifts werden in Geräte Einheiten angegeben.</span><span class="sxs-lookup"><span data-stu-id="ba2e9-104">The dimensions of a cosmetic pen are specified in device units.</span></span> <span data-ttu-id="ba2e9-105">Daher haben Zeilen, die mit einem kosmetischen Stift gezeichnet werden, immer eine festgelegte Breite.</span><span class="sxs-lookup"><span data-stu-id="ba2e9-105">Therefore, lines drawn with a cosmetic pen always have a fixed width.</span></span> <span data-ttu-id="ba2e9-106">Zeilen, die mit einem kosmetischen Stift gezeichnet werden, werden in der Regel 3 bis 10 mal schneller als mit einem geometrischen Stift gezeichnete Linien gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ba2e9-106">Lines drawn with a cosmetic pen are generally drawn 3 to 10 times faster than lines drawn with a geometric pen.</span></span> <span data-ttu-id="ba2e9-107">Kosmetische Stifte haben drei Attribute: "width", "Style" und "Color".</span><span class="sxs-lookup"><span data-stu-id="ba2e9-107">Cosmetic pens have three attributes: width, style, and color.</span></span> <span data-ttu-id="ba2e9-108">Weitere Informationen zu diesen Attributen finden Sie unter [Pen-Attribute](pen-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="ba2e9-108">For more information about these attributes, see [Pen Attributes](pen-attributes.md).</span></span>

<span data-ttu-id="ba2e9-109">Verwenden Sie zum Erstellen eines kosmetischen Stifts die Funktion " [**kreatepen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen)", " [**kreatepenindirekte**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)" oder " [**extkreatepen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) ".</span><span class="sxs-lookup"><span data-stu-id="ba2e9-109">To create a cosmetic pen, use the [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect), or [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function.</span></span> <span data-ttu-id="ba2e9-110">Verwenden Sie die [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) -Funktion, um einen der drei durch das System verwalteten, mit dem Kurs verwalteten Kosmetik Stifte abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ba2e9-110">To retrieve one of the three stock cosmetic pens managed by the system, use the [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) function.</span></span>

<span data-ttu-id="ba2e9-111">Nachdem Sie einen Stift erstellt (oder ein Handle für einen der Aktien Stifte abgerufen haben), wählen Sie den Stift mithilfe der [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) -Funktion in den Gerätekontext der Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="ba2e9-111">After you create a pen (or obtain a handle to one of the stock pens), select the pen into the application's device context (DC) using the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function.</span></span> <span data-ttu-id="ba2e9-112">Ab diesem Zeitpunkt wird dieser Stift von der Anwendung für alle Zeilen Zeichnungsvorgänge im Client Bereich verwendet.</span><span class="sxs-lookup"><span data-stu-id="ba2e9-112">From this point on, the application uses this pen for any line-drawing operations in its client area.</span></span>

 

 



