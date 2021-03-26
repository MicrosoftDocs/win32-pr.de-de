---
description: Verwenden Sie die GetDC-Funktion, um das Zeichnen auszuführen, das unmittelbar statt bei der Verarbeitung einer WM-Zeichnungs Nachricht ausgeführt werden muss \_ .
ms.assetid: 75525e26-72f5-4a58-a663-0bbdc2034759
title: Verwenden der GetDC-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c018228eccbce7b487444341481165e24214b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979376"
---
# <a name="using-the-getdc-function"></a><span data-ttu-id="790ce-103">Verwenden der GetDC-Funktion</span><span class="sxs-lookup"><span data-stu-id="790ce-103">Using the GetDC Function</span></span>

<span data-ttu-id="790ce-104">Verwenden Sie die [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) -Funktion, um das Zeichnen auszuführen, das unmittelbar statt bei der Verarbeitung einer WM-Zeichnungs Nachricht ausgeführt werden muss. [**\_**](wm-paint.md)</span><span class="sxs-lookup"><span data-stu-id="790ce-104">You use the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) function to carry out drawing that must occur instantly rather than when a [**WM\_PAINT**](wm-paint.md) message is processing.</span></span> <span data-ttu-id="790ce-105">Diese Zeichnung wird in der Regel als Reaktion auf eine Aktion durch den Benutzer ausgeführt, z. b. das Treffen einer Auswahl oder Zeichnung mit der Maus.</span><span class="sxs-lookup"><span data-stu-id="790ce-105">Such drawing is usually in response to an action by the user, such as making a selection or drawing with the mouse.</span></span> <span data-ttu-id="790ce-106">In solchen Fällen sollte der Benutzer sofortiges Feedback erhalten und darf nicht gezwungen werden, die Auswahl oder Zeichnung aufzuheben, damit die Anwendung das Ergebnis anzeigt.</span><span class="sxs-lookup"><span data-stu-id="790ce-106">In such cases, the user should receive instant feedback and must not be forced to stop selecting or drawing in order for the application to display the result.</span></span> <span data-ttu-id="790ce-107">In den folgenden Abschnitten wird gezeigt, wie Sie GetDC zum Zeichnen in einem Fenster verwenden:</span><span class="sxs-lookup"><span data-stu-id="790ce-107">The following sections show how to use GetDC to draw in a window:</span></span>

-   [<span data-ttu-id="790ce-108">Zeichnen mit der Maus</span><span class="sxs-lookup"><span data-stu-id="790ce-108">Drawing with the Mouse</span></span>](drawing-with-the-mouse.md)
-   [<span data-ttu-id="790ce-109">Zeichnen in zeitgesteuerten Intervallen</span><span class="sxs-lookup"><span data-stu-id="790ce-109">Drawing at Timed Intervals</span></span>](drawing-at-timed-intervals.md)

 

 



