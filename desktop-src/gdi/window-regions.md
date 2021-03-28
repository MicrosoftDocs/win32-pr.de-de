---
description: Zusätzlich zum Update Bereich verfügt jedes Fenster über einen sichtbaren Bereich, der den für den Benutzer sichtbaren Fenster Teil definiert.
ms.assetid: 9d8beba1-93c0-437d-a138-76880a40bc79
title: Fensterbereiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02555339412c604f79f69294febbab524fc92a70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042650"
---
# <a name="window-regions"></a><span data-ttu-id="9d2da-103">Fensterbereiche</span><span class="sxs-lookup"><span data-stu-id="9d2da-103">Window Regions</span></span>

<span data-ttu-id="9d2da-104">Zusätzlich zum Update Bereich verfügt jedes Fenster über einen *sichtbaren Bereich* , der den für den Benutzer sichtbaren Fenster Teil definiert.</span><span class="sxs-lookup"><span data-stu-id="9d2da-104">In addition to the update region, every window has a *visible region* that defines the window portion visible to the user.</span></span> <span data-ttu-id="9d2da-105">Das System ändert den sichtbaren Bereich für das Fenster, wenn die Größe des Fensters geändert wird oder wenn ein anderes Fenster verschoben wird, sodass es einen Teil des Fensters verdeckt oder verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="9d2da-105">The system changes the visible region for the window whenever the window changes size or whenever another window is moved such that it obscures or exposes a portion of the window.</span></span> <span data-ttu-id="9d2da-106">Anwendungen können den sichtbaren Bereich nicht direkt ändern, aber das System verwendet automatisch den sichtbaren Bereich, um den Clippingbereich für jeden für das Fenster abgerufenen Anzeigegeräte Kontext zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9d2da-106">Applications cannot change the visible region directly, but the system automatically uses the visible region to create the clipping region for any display device context retrieved for the window.</span></span>

<span data-ttu-id="9d2da-107">Der *Clippingbereich* bestimmt, wo das System das Zeichnen zulässt.</span><span class="sxs-lookup"><span data-stu-id="9d2da-107">The *clipping region* determines where the system permits drawing.</span></span> <span data-ttu-id="9d2da-108">Wenn die Anwendung einen Anzeigegeräte Kontext mithilfe der [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)-, [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)-oder [**getdcex**](/windows/desktop/api/Winuser/nf-winuser-getdcex) -Funktion abruft, legt das System den Clippingbereich für den Gerätekontext auf die Schnittmenge des sichtbaren Bereichs und des Aktualisierungs Bereichs fest.</span><span class="sxs-lookup"><span data-stu-id="9d2da-108">When the application retrieves a display device context using the [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc), or [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) function, the system sets the clipping region for the device context to the intersection of the visible region and the update region.</span></span> <span data-ttu-id="9d2da-109">Anwendungen können den Clippingbereich mithilfe von Funktionen wie " [**setwindowrgn**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn)", " [**selectclippath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) " und " [**selectcliprgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn)" ändern, um das Zeichnen auf einen bestimmten Teil des Aktualisierungs Bereichs weiter einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="9d2da-109">Applications can change the clipping region by using functions such as [**SetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn), [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) and [**SelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn), to further limit drawing to a particular portion of the update area.</span></span>

<span data-ttu-id="9d2da-110">Die \_ Stile WS clipchildren und WS Clip-untergeordnete Elemente \_ geben an, wie das System den sichtbaren Bereich für ein Fenster berechnet.</span><span class="sxs-lookup"><span data-stu-id="9d2da-110">The WS\_CLIPCHILDREN and WS\_CLIPSIBLINGS styles further specify how the system calculates the visible region for a window.</span></span> <span data-ttu-id="9d2da-111">Wenn ein Fenster einen oder beide Formate enthält, schließt der sichtbare Bereich alle untergeordneten Fenster oder neben geordneten Fenster (Fenster mit dem gleichen übergeordneten Fenster) aus.</span><span class="sxs-lookup"><span data-stu-id="9d2da-111">If a window has one or both of these styles, the visible region excludes any child window or sibling windows (windows having the same parent window).</span></span> <span data-ttu-id="9d2da-112">Daher wird das Zeichnen, das andernfalls in diesen Fenstern eingedrungen wäre, immer abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="9d2da-112">Therefore, drawing that would otherwise intrude in these windows will always be clipped.</span></span>

 

 



