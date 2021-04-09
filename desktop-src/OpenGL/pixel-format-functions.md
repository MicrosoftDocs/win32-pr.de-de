---
title: Pixel Format Funktionen
description: Die folgenden Windows-Funktionen verwalten Pixel Formate.
ms.assetid: 78a6be75-72f6-4aef-a6bc-5f052c6fe2e9
keywords:
- WGL-Funktionen, Pixel Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e219fc6a2aafecdcda43708cdb4c77553c88f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856884"
---
# <a name="pixel-format-functions"></a><span data-ttu-id="48255-104">Pixel Format Funktionen</span><span class="sxs-lookup"><span data-stu-id="48255-104">Pixel Format Functions</span></span>

<span data-ttu-id="48255-105">Die folgenden Windows-Funktionen verwalten Pixel Formate.</span><span class="sxs-lookup"><span data-stu-id="48255-105">The following Windows functions manage pixel formats.</span></span>



| <span data-ttu-id="48255-106">Windows-Funktion</span><span class="sxs-lookup"><span data-stu-id="48255-106">Windows Function</span></span>                                               | <span data-ttu-id="48255-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48255-107">Description</span></span>                                                                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48255-108">**Auswahl Pixel Format**</span><span class="sxs-lookup"><span data-stu-id="48255-108">**ChoosePixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                 | <span data-ttu-id="48255-109">Ruft das Pixel Format des Geräte Kontexts ab, das dem angegebenen Pixel Format am ehesten entspricht.</span><span class="sxs-lookup"><span data-stu-id="48255-109">Obtains the device context's pixel format that is the closest match to a specified pixel format.</span></span>                                                                      |
| [<span data-ttu-id="48255-110">**SetPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="48255-110">**SetPixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                       | <span data-ttu-id="48255-111">Legt das aktuelle Pixel Format eines Geräte Kontexts auf das durch einen Pixel Format Index angegebene Pixel Format fest.</span><span class="sxs-lookup"><span data-stu-id="48255-111">Sets a device context's current pixel format to the pixel format specified by a pixel format index.</span></span>                                                                   |
| [<span data-ttu-id="48255-112">**GetPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="48255-112">**GetPixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                       | <span data-ttu-id="48255-113">Ruft den Pixel Format Index des aktuellen Pixel Formats eines Geräte Kontexts ab.</span><span class="sxs-lookup"><span data-stu-id="48255-113">Obtains the pixel format index of a device context's current pixel format.</span></span>                                                                                            |
| [<span data-ttu-id="48255-114">**Describepixelformat**</span><span class="sxs-lookup"><span data-stu-id="48255-114">**DescribePixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)             | <span data-ttu-id="48255-115">Wenn ein Gerätekontext und ein Pixel Format Index vorliegen, füllt eine [**Pixel formatdescriptor**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) -Datenstruktur mit den Eigenschaften des Pixel Formats.</span><span class="sxs-lookup"><span data-stu-id="48255-115">Given a device context and a pixel format index, fills in a [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure with the pixel format's properties.</span></span> |
| [<span data-ttu-id="48255-116">**Getenhmetafilepixelformat**</span><span class="sxs-lookup"><span data-stu-id="48255-116">**GetEnhMetaFilePixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-getenhmetafilepixelformat) | <span data-ttu-id="48255-117">Ruft Informationen zum Pixel Format für eine erweiterte Metadatei ab.</span><span class="sxs-lookup"><span data-stu-id="48255-117">Retrieves pixel format information for an enhanced metafile.</span></span>                                                                                                          |



 

<span data-ttu-id="48255-118">Die [**chootarformat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) -Funktion gibt einen 1-basierten Pixel Format Index zurück, der die beste Entsprechung aus den unterstützten Pixel Formaten des Geräte Kontexts identifiziert.</span><span class="sxs-lookup"><span data-stu-id="48255-118">The [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) function returns a one-based pixel format index that identifies the best match from the device context's supported pixel formats.</span></span>

<span data-ttu-id="48255-119">Die Funktion [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) identifiziert das gewünschte Format mit einem 1-basierten Pixel Format Index.</span><span class="sxs-lookup"><span data-stu-id="48255-119">The [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) function identifies the desired format using a one-based pixel format index.</span></span> <span data-ttu-id="48255-120">In der Regel wird " **choosepixelformat** " aufgerufen, um ein Pixel Format mit der besten Entsprechung zu finden, und dann " **SetPixelFormat** " mit dem Ergebnis von " **choosepixelformat**" aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="48255-120">Typically, you call **ChoosePixelFormat** to find a best-match pixel format, and then call **SetPixelFormat** with the result of **ChoosePixelFormat**.</span></span>

<span data-ttu-id="48255-121">Wenn Sie **SetPixelFormat** für einen Gerätekontext aufrufen, der auf ein Fenster verweist, ändert **SetPixelFormat** auch das Pixel Format des Fensters.</span><span class="sxs-lookup"><span data-stu-id="48255-121">If you call **SetPixelFormat** for a device context that references a window, **SetPixelFormat** also changes the pixel format of the window.</span></span> <span data-ttu-id="48255-122">Wenn das Pixel Format eines Fensters mehrmals festgelegt wird, kann dies zu erheblichen Komplikationen für den Fenster Manager und für Multithreadanwendungen führen, sodass es nicht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="48255-122">Setting the pixel format of a window more than once can lead to significant complications for the Window Manager and for multithread applications, so it is not allowed.</span></span> <span data-ttu-id="48255-123">Das Pixel Format eines Fensters kann nur ein Mal festgelegt werden. Danach kann das Pixel Format des Fensters nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="48255-123">You can set the pixel format of a window only one time; after that, the window's pixel format cannot be changed.</span></span>

<span data-ttu-id="48255-124">Die [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) -Funktion gibt einen 1-basierten Pixel Format Index zurück.</span><span class="sxs-lookup"><span data-stu-id="48255-124">The [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) function returns a one-based pixel format index.</span></span>

<span data-ttu-id="48255-125">Die [**describepixelformat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) -Funktion nimmt folgende Parameter als Parameter an:</span><span class="sxs-lookup"><span data-stu-id="48255-125">The [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) function takes the following as parameters:</span></span>

-   <span data-ttu-id="48255-126">Ein Handle für einen Gerätekontext</span><span class="sxs-lookup"><span data-stu-id="48255-126">A handle to a device context</span></span>
-   <span data-ttu-id="48255-127">Ein Pixel Format Index</span><span class="sxs-lookup"><span data-stu-id="48255-127">A pixel format index</span></span>
-   <span data-ttu-id="48255-128">Ein Zeiger auf eine [**pixelformatdescriptor**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) -Datenstruktur.</span><span class="sxs-lookup"><span data-stu-id="48255-128">A pointer to a [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure</span></span>

<span data-ttu-id="48255-129">Die [**describepixelformat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) -Funktion gibt zurück, wobei die Member von **pixelformatdescriptor** entsprechend festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="48255-129">The [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) function returns with the members of **PIXELFORMATDESCRIPTOR** appropriately set.</span></span>

<span data-ttu-id="48255-130">Die **getenhmetafilepixelformat** -Funktion gibt die Größe des Pixel Formats einer Metadatei zurück und ruft die Pixel Formatinformationen der Metadatei ab.</span><span class="sxs-lookup"><span data-stu-id="48255-130">The **GetEnhMetaFilePixelFormat** function returns the size of a metafile's pixel format and retrieves the pixel format information of the metafile.</span></span>

 

 




