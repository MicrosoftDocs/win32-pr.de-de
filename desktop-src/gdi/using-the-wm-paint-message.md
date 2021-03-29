---
description: Sie können die WM- \_ Zeichnungs Nachricht verwenden, um die zum Anzeigen von Informationen erforderliche Zeichnung auszuführen.
ms.assetid: cc56745f-95d0-4607-a206-1e7ed7109bf0
title: Verwenden der WM_PAINT Nachricht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba77246e04effc74de8158aef9bfc4aaf27471c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215646"
---
# <a name="using-the-wm_paint-message"></a><span data-ttu-id="70c09-103">Verwenden der WM-Zeichnungs \_ Meldung</span><span class="sxs-lookup"><span data-stu-id="70c09-103">Using the WM\_PAINT Message</span></span>

<span data-ttu-id="70c09-104">Sie können die [**WM- \_**](wm-paint.md) Zeichnungs Nachricht verwenden, um die zum Anzeigen von Informationen erforderliche Zeichnung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="70c09-104">You can use the [**WM\_PAINT**](wm-paint.md) message to carry out the drawing necessary for displaying information.</span></span> <span data-ttu-id="70c09-105">Da das System WM- \_ Paint-Meldungen an Ihre Anwendung sendet, wenn Ihr Fenster aktualisiert werden muss oder wenn Sie explizit ein Update anfordern, können Sie den Code zum Zeichnen in der Fenster Prozedur Ihrer Anwendung konsolidieren.</span><span class="sxs-lookup"><span data-stu-id="70c09-105">Because the system sends WM\_PAINT messages to your application when your window must be updated or when you explicitly request an update, you can consolidate the code for drawing in your application's window procedure.</span></span> <span data-ttu-id="70c09-106">Sie können diesen Code dann immer dann verwenden, wenn Ihre Anwendung entweder neue oder vorhandene Informationen zeichnen muss.</span><span class="sxs-lookup"><span data-stu-id="70c09-106">You can then use this code whenever your application must draw either new or existing information.</span></span>

<span data-ttu-id="70c09-107">In den folgenden Abschnitten werden verschiedene Möglichkeiten zum Verwenden der WM- \_ Zeichnungs Nachricht zum Zeichnen in einem Fenster gezeigt:</span><span class="sxs-lookup"><span data-stu-id="70c09-107">The following sections show a variety of ways to use the WM\_PAINT message to draw in a window:</span></span>

-   [<span data-ttu-id="70c09-108">Zeichnen im Client Bereich</span><span class="sxs-lookup"><span data-stu-id="70c09-108">Drawing in the Client Area</span></span>](drawing-in-the-client-area.md)
-   [<span data-ttu-id="70c09-109">Neuzeichnen des gesamten Client Bereichs</span><span class="sxs-lookup"><span data-stu-id="70c09-109">Redrawing the Entire Client Area</span></span>](redrawing-the-entire-client-area.md)
-   [<span data-ttu-id="70c09-110">Neuzeichnen in der Aktualisierungs Region</span><span class="sxs-lookup"><span data-stu-id="70c09-110">Redrawing in the Update Region</span></span>](redrawing-in-the-update-region.md)
-   [<span data-ttu-id="70c09-111">Der Client Bereich wird ungültig gemacht.</span><span class="sxs-lookup"><span data-stu-id="70c09-111">Invalidating the Client Area</span></span>](invalidating-the-client-area.md)
-   [<span data-ttu-id="70c09-112">Zeichnen eines minimierten Fensters</span><span class="sxs-lookup"><span data-stu-id="70c09-112">Drawing a Minimized Window</span></span>](drawing-a-minimized-window.md)
-   [<span data-ttu-id="70c09-113">Zeichnen eines benutzerdefinierten Fenster Hintergrunds</span><span class="sxs-lookup"><span data-stu-id="70c09-113">Drawing a Custom Window Background</span></span>](drawing-a-custom-window-background.md)

 

 



