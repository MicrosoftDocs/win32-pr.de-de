---
description: Der Aktualisierungs Bereich identifiziert den Teil eines Fensters, der veraltet oder ungültig ist und neu gezeichnet werden muss.
ms.assetid: 21228620-9491-4e1b-8658-15e9605951f2
title: Der Aktualisierungs Bereich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e670bac065782a1e09c4d142f964aaea97d4b96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995094"
---
# <a name="the-update-region"></a><span data-ttu-id="7caa1-103">Der Aktualisierungs Bereich</span><span class="sxs-lookup"><span data-stu-id="7caa1-103">The Update Region</span></span>

<span data-ttu-id="7caa1-104">Der *Aktualisierungs Bereich* identifiziert den Teil eines Fensters, der veraltet oder ungültig ist und neu gezeichnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="7caa1-104">The *update region* identifies the portion of a window that is out-of-date or invalid and in need of redrawing.</span></span> <span data-ttu-id="7caa1-105">Das System verwendet die Update Region, um [**WM \_ Paint**](wm-paint.md) -Meldungen für Anwendungen zu generieren und die Zeit zu minimieren, in der Anwendungen die Inhalte ihrer Fenster auf den neuesten Stand bringen.</span><span class="sxs-lookup"><span data-stu-id="7caa1-105">The system uses the update region to generate [**WM\_PAINT**](wm-paint.md) messages for applications and to minimize the time applications spend bringing the contents of their windows up to date.</span></span> <span data-ttu-id="7caa1-106">Das System fügt dem Aktualisierungs Bereich nur den ungültigen Teil des Fensters hinzu. Dies erfordert, dass nur dieser Teil gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="7caa1-106">The system adds only the invalid portion of the window to the update region, requiring only that portion to be drawn.</span></span>

<span data-ttu-id="7caa1-107">Wenn das System ermittelt, dass ein Fenster aktualisiert werden muss, legt es die Abmessungen des Aktualisierungs Bereichs auf den ungültigen Teil des Fensters fest.</span><span class="sxs-lookup"><span data-stu-id="7caa1-107">When the system determines that a window needs updating, it sets the dimensions of the update region to the invalid portion of the window.</span></span> <span data-ttu-id="7caa1-108">Wenn Sie den Update Bereich festlegen, wird die Anwendung nicht sofort gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7caa1-108">Setting the update region does not immediately cause the application to draw.</span></span> <span data-ttu-id="7caa1-109">Stattdessen ruft die Anwendung weiterhin Nachrichten aus der Nachrichten Warteschlange der Anwendung ab, bis keine Nachrichten mehr vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="7caa1-109">Instead, the application continues retrieving messages from the application message queue until no messages remain.</span></span> <span data-ttu-id="7caa1-110">Das System überprüft dann den Update Bereich. wenn die Region nicht leer (nicht null) ist, sendet Sie eine [**WM \_ Paint**](wm-paint.md) -Meldung an die Fenster Prozedur.</span><span class="sxs-lookup"><span data-stu-id="7caa1-110">The system then checks the update region, and if the region is not empty (non-NULL), it sends a [**WM\_PAINT**](wm-paint.md) message to the window procedure.</span></span>

<span data-ttu-id="7caa1-111">Eine Anwendung kann den Update Bereich verwenden, um Ihre [**WM \_ Paint**](wm-paint.md) -Meldungen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="7caa1-111">An application can use the update region to generate its [**WM\_PAINT**](wm-paint.md) messages.</span></span> <span data-ttu-id="7caa1-112">Beispielsweise legt eine Anwendung, die Daten aus geöffneten Dateien lädt, in der Regel den Update Bereich beim Laden fest, sodass neue Daten während der Verarbeitung der nächsten WM-Zeichnungs Nachricht gezeichnet werden. **\_**</span><span class="sxs-lookup"><span data-stu-id="7caa1-112">For example, an application that loads data from open files typically sets the update region while loading so that new data is drawn during processing of the next **WM\_PAINT** message.</span></span> <span data-ttu-id="7caa1-113">Im Allgemeinen sollte eine Anwendung nicht zu dem Zeitpunkt gezeichnet werden, an dem sich die Daten ändern, sondern alle Zeichnungsvorgänge durch die WM-Zeichnungs Nachricht weiterleiten. **\_**</span><span class="sxs-lookup"><span data-stu-id="7caa1-113">In general, an application should not draw at the time its data changes, but route all drawing operations through the **WM\_PAINT** message.</span></span>

 

 



