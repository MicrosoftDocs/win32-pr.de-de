---
description: Das akkumulierte umschließende Rechteck ist das kleinste Rechteck, das den Teil eines Fensters oder Client Bereichs schließt, der sich auf die letzten Zeichnungsvorgänge auswirkt.
ms.assetid: 8ae13486-a9e2-4841-ada3-c70d30450ac8
title: Akkumuliertes Rechteck
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ae3237304af68a4b8ff447b7ea2d64d3f81053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528400"
---
# <a name="accumulated-bounding-rectangle"></a><span data-ttu-id="c4d39-103">Akkumuliertes Rechteck</span><span class="sxs-lookup"><span data-stu-id="c4d39-103">Accumulated Bounding Rectangle</span></span>

<span data-ttu-id="c4d39-104">Das *akkumulierte* umschließende Rechteck ist das kleinste Rechteck, das den Teil eines Fensters oder Client Bereichs schließt, der sich auf die letzten Zeichnungsvorgänge auswirkt.</span><span class="sxs-lookup"><span data-stu-id="c4d39-104">The *accumulated bounding rectangle* is the smallest rectangle enclosing the portion of a window or client area affected by recent drawing operations.</span></span> <span data-ttu-id="c4d39-105">Mithilfe dieses Rechtecks kann eine Anwendung den Umfang der Änderungen, die durch Zeichnungsvorgänge verursacht werden, bequem ermitteln.</span><span class="sxs-lookup"><span data-stu-id="c4d39-105">An application can use this rectangle to conveniently determine the extent of changes caused by drawing operations.</span></span> <span data-ttu-id="c4d39-106">Sie wird manchmal zusammen mit [**lockwindowupdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) verwendet, um zu bestimmen, welcher Teil des Client Bereichs nach dem Löschen der Update Sperre neu gezeichnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="c4d39-106">It is sometimes used in conjunction with [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) to determine which portion of the client area must be redrawn after the update lock is cleared.</span></span>

<span data-ttu-id="c4d39-107">Eine Anwendung verwendet die [**setboundsrect**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect) -Funktion (durch Angabe \_ von DCB Enable), um mit der Anhäufung des umgebenden Rechtecks zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="c4d39-107">An application uses the [**SetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect) function (specifying DCB\_ENABLE) to begin accumulating the bounding rectangle.</span></span> <span data-ttu-id="c4d39-108">Anschließend sammelt das System Punkte für das umgebende Rechteck, wenn die Anwendung den angegebenen Anzeigegeräte Kontext verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4d39-108">The system subsequently accumulates points for the bounding rectangle as the application uses the specified display device context.</span></span> <span data-ttu-id="c4d39-109">Die Anwendung kann das aktuelle umgebende Rechteck jederzeit mithilfe der [**getboundsrect**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect) -Funktion abrufen.</span><span class="sxs-lookup"><span data-stu-id="c4d39-109">The application can retrieve the current bounding rectangle at any time by using the [**GetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect) function.</span></span> <span data-ttu-id="c4d39-110">Die Anwendung beendet die Akkumulation, indem **setboundsrect** erneut aufgerufen wird, wobei der DCB- \_ Wert deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="c4d39-110">The application stops the accumulation by calling **SetBoundsRect** again, specifying the DCB\_DISABLE value.</span></span>

 

 



