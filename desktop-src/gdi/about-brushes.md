---
description: 'Es gibt zwei Arten von Pinseln: logisch und physisch.'
ms.assetid: 2e15376d-6b4c-41c5-aef8-0dbb91b81505
title: Informationen zu Pinseln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c825892748b317807377bff12675ea04d2d2535
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130365"
---
# <a name="about-brushes"></a><span data-ttu-id="46246-103">Informationen zu Pinseln</span><span class="sxs-lookup"><span data-stu-id="46246-103">About Brushes</span></span>

<span data-ttu-id="46246-104">Es gibt zwei Arten von Pinseln: logisch und physisch.</span><span class="sxs-lookup"><span data-stu-id="46246-104">There are two types of brushes: logical and physical.</span></span> <span data-ttu-id="46246-105">Ein *logischer Pinsel* ist eine Beschreibung der idealen Bitmap, die eine Anwendung zum Zeichnen von Formen verwendet.</span><span class="sxs-lookup"><span data-stu-id="46246-105">A *logical brush* is a description of the ideal bitmap that an application uses to paint shapes.</span></span> <span data-ttu-id="46246-106">Ein *physischer Pinsel* ist die tatsächliche Bitmap, die ein Gerätetreiber basierend auf der logischen Pinsel Definition einer Anwendung erstellt.</span><span class="sxs-lookup"><span data-stu-id="46246-106">A *physical brush* is the actual bitmap that a device driver creates based on an application's logical-brush definition.</span></span> <span data-ttu-id="46246-107">Weitere Informationen zu Bitmaps finden Sie unter [Bitmaps](bitmaps.md).</span><span class="sxs-lookup"><span data-stu-id="46246-107">For more information about bitmaps, see [Bitmaps](bitmaps.md).</span></span>

<span data-ttu-id="46246-108">Wenn eine Anwendung eine der Funktionen aufruft, die einen Pinsel erstellt, ruft Sie ein Handle ab, das einen logischen Pinsel identifiziert.</span><span class="sxs-lookup"><span data-stu-id="46246-108">When an application calls one of the functions that creates a brush, it retrieves a handle that identifies a logical brush.</span></span> <span data-ttu-id="46246-109">Wenn die Anwendung dieses Handle an die [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) -Funktion übergibt, erstellt der Gerätetreiber für die entsprechende Anzeige bzw. den entsprechenden Drucker den physischen Pinsel.</span><span class="sxs-lookup"><span data-stu-id="46246-109">When the application passes this handle to the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function, the device driver for the corresponding display or printer creates the physical brush.</span></span>

<span data-ttu-id="46246-110">In den folgenden Themen werden Pinsel beschrieben:</span><span class="sxs-lookup"><span data-stu-id="46246-110">The following topics describe brushes:</span></span>

-   [<span data-ttu-id="46246-111">Pinsel Ursprung</span><span class="sxs-lookup"><span data-stu-id="46246-111">Brush Origin</span></span>](brush-origin.md)
-   [<span data-ttu-id="46246-112">Logische Pinseltypen</span><span class="sxs-lookup"><span data-stu-id="46246-112">Logical Brush Types</span></span>](logical-brush-types.md)
-   [<span data-ttu-id="46246-113">Muster Block Übertragung</span><span class="sxs-lookup"><span data-stu-id="46246-113">Pattern Block Transfer</span></span>](pattern-block-transfer.md)
-   [<span data-ttu-id="46246-114">ICM-aktivierte Pinsel Funktionen</span><span class="sxs-lookup"><span data-stu-id="46246-114">ICM-Enabled Brush Functions</span></span>](icm-enabled-brush-functions.md)

 

 



