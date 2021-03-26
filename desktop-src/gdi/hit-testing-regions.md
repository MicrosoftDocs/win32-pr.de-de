---
description: Eine Anwendung führt Treffer Tests für Regionen durch, um die Koordinaten der aktuellen Cursorposition zu bestimmen.
ms.assetid: 861a2558-0967-43f6-be3f-580992da05ff
title: Treffer Testregionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe136c3ba9ab4babfc1150ae4c3eee878cb42327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215197"
---
# <a name="hit-testing-regions"></a><span data-ttu-id="c30b0-103">Treffer Testregionen</span><span class="sxs-lookup"><span data-stu-id="c30b0-103">Hit Testing Regions</span></span>

<span data-ttu-id="c30b0-104">Eine Anwendung führt Treffer Tests für Regionen durch, um die Koordinaten der aktuellen Cursorposition zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="c30b0-104">An application performs hit testing on regions to determine the coordinates of the current cursor position.</span></span> <span data-ttu-id="c30b0-105">Anschließend übergibt Sie diese Koordinaten sowie ein Handle, das den Bereich an die [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) -Funktion identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c30b0-105">Then it passes these coordinates as well as a handle identifying the region to the [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) function.</span></span> <span data-ttu-id="c30b0-106">Die Cursor Koordinaten können abgerufen werden, indem die verschiedenen Maus Meldungen verarbeitet werden, z. b. [**WM \_ lbuttondown**](../inputdev/wm-lbuttondown.md) , [**WM \_ lbuttonup**](../inputdev/wm-lbuttonup.md) , [**WM \_ rbuttondown**](../inputdev/wm-rbuttondown.md) und [**WM \_ rbuttonup**](../inputdev/wm-rbuttonup.md).</span><span class="sxs-lookup"><span data-stu-id="c30b0-106">The cursor coordinates can be retrieved by processing the various mouse messages, such as [**WM\_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) , [**WM\_LBUTTONUP**](../inputdev/wm-lbuttonup.md) , [**WM\_RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) , and [**WM\_RBUTTONUP**](../inputdev/wm-rbuttonup.md).</span></span> <span data-ttu-id="c30b0-107">Der Rückgabewert für PtInRegion gibt an, ob die Cursorposition innerhalb des angegebenen Bereichs liegt.</span><span class="sxs-lookup"><span data-stu-id="c30b0-107">The return value for PtInRegion indicates whether the cursor position is within the given region.</span></span>

 

 
