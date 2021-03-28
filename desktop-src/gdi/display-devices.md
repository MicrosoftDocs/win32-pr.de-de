---
description: Vor dem zeichnen muss das System das Anzeigegerät für Zeichnungsvorgänge vorbereiten.
ms.assetid: a3802aa7-deec-4151-b1b1-4cd38f769864
title: Geräte anzeigen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6df9e5e1746f309f402b31e736c58092d134d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978657"
---
# <a name="display-devices"></a><span data-ttu-id="b1daf-103">Geräte anzeigen</span><span class="sxs-lookup"><span data-stu-id="b1daf-103">Display Devices</span></span>

<span data-ttu-id="b1daf-104">Vor dem zeichnen muss das System das Anzeigegerät für Zeichnungsvorgänge vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="b1daf-104">Before painting, the system must prepare the display device for drawing operations.</span></span> <span data-ttu-id="b1daf-105">Ein Anzeigegeräte Kontext definiert eine Gruppe von Grafikobjekten und deren zugeordneten Attributen sowie die Grafikmodi, die die Ausgabe beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="b1daf-105">A display device context defines a set of graphic objects and their associated attributes, and the graphic modes that affect output.</span></span> <span data-ttu-id="b1daf-106">Das System bereitet jeden Anzeigegeräte Kontext für die Ausgabe in einem Fenster vor, wobei die Zeichnungsobjekte, Farben und Modi für das Fenster anstelle des Anzeige Geräts festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b1daf-106">The system prepares each display device context for output to a window, setting the drawing objects, colors, and modes for the window instead of the display device.</span></span> <span data-ttu-id="b1daf-107">Wenn die Anwendung den Anzeigegeräte Kontext über Aufrufe an GDI-Funktionen bereitstellt, verwendet GDI die Informationen im Kontext, um die Ausgabe im angegebenen Fenster zu generieren, ohne in andere Fenster oder andere Teile des Bildschirms einzugreifen.</span><span class="sxs-lookup"><span data-stu-id="b1daf-107">When the application supplies the display device context through calls to GDI functions, GDI uses the information in the context to generate output in the specified window without intruding on other windows or other parts of the screen.</span></span>

<span data-ttu-id="b1daf-108">Das System stellt fünf Arten von Anzeigegeräte Kontexten bereit.</span><span class="sxs-lookup"><span data-stu-id="b1daf-108">The system provides five kinds of display device contexts.</span></span>



| <span data-ttu-id="b1daf-109">type</span><span class="sxs-lookup"><span data-stu-id="b1daf-109">Type</span></span>                                           | <span data-ttu-id="b1daf-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b1daf-110">Meaning</span></span>                                                                                                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1daf-111">gewöhnliche</span><span class="sxs-lookup"><span data-stu-id="b1daf-111">common</span></span>](common-display-device-contexts.md)   | <span data-ttu-id="b1daf-112">Lässt das Zeichnen im Client Bereich eines angegebenen Fensters zu.</span><span class="sxs-lookup"><span data-stu-id="b1daf-112">Permits drawing in the client area of a specified window.</span></span>                                                                                                        |
| [<span data-ttu-id="b1daf-113">class</span><span class="sxs-lookup"><span data-stu-id="b1daf-113">class</span></span>](class-display-device-contexts.md)     | <span data-ttu-id="b1daf-114">Lässt das Zeichnen im Client Bereich eines angegebenen Fensters zu.</span><span class="sxs-lookup"><span data-stu-id="b1daf-114">Permits drawing in the client area of a specified window.</span></span>                                                                                                        |
| [<span data-ttu-id="b1daf-115">parent</span><span class="sxs-lookup"><span data-stu-id="b1daf-115">parent</span></span>](parent-display-device-contexts.md)   | <span data-ttu-id="b1daf-116">Ermöglicht das Zeichnen an beliebiger Stelle im-Fenster.</span><span class="sxs-lookup"><span data-stu-id="b1daf-116">Permits drawing anywhere in the window.</span></span> <span data-ttu-id="b1daf-117">Obwohl der übergeordnete Gerätekontext auch das Zeichnen im übergeordneten Fenster zulässt, ist er nicht für die Verwendung auf diese Weise vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="b1daf-117">Although the parent device context also permits drawing in the parent window, it is not intended to be used in this way.</span></span> |
| [<span data-ttu-id="b1daf-118">private</span><span class="sxs-lookup"><span data-stu-id="b1daf-118">private</span></span>](private-display-device-contexts.md) | <span data-ttu-id="b1daf-119">Lässt das Zeichnen im Client Bereich eines angegebenen Fensters zu.</span><span class="sxs-lookup"><span data-stu-id="b1daf-119">Permits drawing in the client area of a specified window.</span></span>                                                                                                        |
| [<span data-ttu-id="b1daf-120">Fenster</span><span class="sxs-lookup"><span data-stu-id="b1daf-120">window</span></span>](window-display-device-contexts.md)   | <span data-ttu-id="b1daf-121">Ermöglicht das Zeichnen an beliebiger Stelle im-Fenster.</span><span class="sxs-lookup"><span data-stu-id="b1daf-121">Permits drawing anywhere in the window.</span></span>                                                                                                                          |



 

<span data-ttu-id="b1daf-122">Das System stellt einen allgemeinen, Klassen-, übergeordneten oder privaten Gerätekontext für ein Fenster bereit, das auf dem Typ des Anzeigegeräte Kontexts basiert, der im Klassen Stil dieses Fensters angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="b1daf-122">The system supplies a common, class, parent, or private device context to a window based on the type of display device context specified in that window's class style.</span></span> <span data-ttu-id="b1daf-123">Das System stellt einen Fenster Gerätekontext nur dann bereit, wenn die Anwendung explizit eine Anforderung anfordert, indem Sie die [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) -oder [**getdcex**](/windows/desktop/api/Winuser/nf-winuser-getdcex) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b1daf-123">The system supplies a window device context only when the application explicitly requests one for example, by calling the [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) or [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) function.</span></span> <span data-ttu-id="b1daf-124">In allen Fällen kann eine Anwendung die [**windowfromdc**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc) -Funktion verwenden, um zu bestimmen, welches Fenster ein angezeigter DC zurzeit darstellt.</span><span class="sxs-lookup"><span data-stu-id="b1daf-124">In all cases, an application can use the [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc) function to determine which window a display DC currently represents.</span></span>

<span data-ttu-id="b1daf-125">Dieser Abschnitt enthält Informationen zu den folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="b1daf-125">This section provides information on the following topics.</span></span>

-   [<span data-ttu-id="b1daf-126">Gerätekontext Cache anzeigen</span><span class="sxs-lookup"><span data-stu-id="b1daf-126">Display Device Context Cache</span></span>](display-device-context-cache.md)
-   [<span data-ttu-id="b1daf-127">Gerätekontext Standardwerte anzeigen</span><span class="sxs-lookup"><span data-stu-id="b1daf-127">Display Device Context Defaults</span></span>](display-device-context-defaults.md)
-   [<span data-ttu-id="b1daf-128">Gängige Anzeige von Geräte Kontexten</span><span class="sxs-lookup"><span data-stu-id="b1daf-128">Common Display Device Contexts</span></span>](common-display-device-contexts.md)
-   [<span data-ttu-id="b1daf-129">Private Anzeigegeräte Kontexte</span><span class="sxs-lookup"><span data-stu-id="b1daf-129">Private Display Device Contexts</span></span>](private-display-device-contexts.md)
-   [<span data-ttu-id="b1daf-130">Übergeordnete Geräte Kontexte anzeigen</span><span class="sxs-lookup"><span data-stu-id="b1daf-130">Parent Display Device Contexts</span></span>](parent-display-device-contexts.md)
-   [<span data-ttu-id="b1daf-131">Klassen Anzeige von Geräte Kontexten</span><span class="sxs-lookup"><span data-stu-id="b1daf-131">Class Display Device Contexts</span></span>](class-display-device-contexts.md)
-   [<span data-ttu-id="b1daf-132">Fenster Geräte Kontexte anzeigen</span><span class="sxs-lookup"><span data-stu-id="b1daf-132">Window Display Device Contexts</span></span>](window-display-device-contexts.md)
-   [<span data-ttu-id="b1daf-133">Übergeordnete Geräte Kontexte anzeigen</span><span class="sxs-lookup"><span data-stu-id="b1daf-133">Parent Display Device Contexts</span></span>](parent-display-device-contexts.md)

 

 



