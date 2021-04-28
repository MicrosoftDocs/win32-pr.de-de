---
title: Übersicht über direct2D-Debugebenen
description: Übersicht über direct2D-Debugebenen
ms.assetid: 7c28e00b-ebb9-4b79-939c-64eade1351ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833174e0d18b11e2384d838930d5508601cfceaf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099988"
---
# <a name="direct2d-debug-layer-overview"></a><span data-ttu-id="48cef-103">Übersicht über direct2D-Debugebenen</span><span class="sxs-lookup"><span data-stu-id="48cef-103">Direct2D Debug Layer Overview</span></span>

<span data-ttu-id="48cef-104">Die Direct2D-Debugebene stellt Debugmeldungen zur Entwurfszeit bereit, mit deren Hilfe Sie Laufzeitanwendungsfehler minimieren können.</span><span class="sxs-lookup"><span data-stu-id="48cef-104">The Direct2D debug layer provides design-time debug messages for you to minimize runtime application failure.</span></span> <span data-ttu-id="48cef-105">In dieser Übersicht werden die Grundlagen der Direct2D-Debugebene beschrieben.</span><span class="sxs-lookup"><span data-stu-id="48cef-105">This overview describes the basics of the Direct2D debug layer.</span></span> <span data-ttu-id="48cef-106">Es wird davon ausgegangen, dass Sie mit der Erstellung grundlegender Direct2D-Anwendungen vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="48cef-106">It assumes that you are familiar with creating basic Direct2D applications.</span></span>

<span data-ttu-id="48cef-107">Diese Übersicht enthält die folgenden Abschnitte.</span><span class="sxs-lookup"><span data-stu-id="48cef-107">This overview contains the following sections.</span></span>

-   [<span data-ttu-id="48cef-108">Was ist die Direct2D-Debugebene?</span><span class="sxs-lookup"><span data-stu-id="48cef-108">What Is the Direct2D Debug Layer</span></span>](#what-is-the-direct2d-debug-layer)
-   [<span data-ttu-id="48cef-109">Installieren der Direct2D-Debugebene</span><span class="sxs-lookup"><span data-stu-id="48cef-109">Installing the Direct2D Debug Layer</span></span>](#installing-the-direct2d-debug-layer)
-   [<span data-ttu-id="48cef-110">Aktivieren der Debugebene</span><span class="sxs-lookup"><span data-stu-id="48cef-110">Enabling the Debug Layer</span></span>](#enabling-the-debug-layer)
-   [<span data-ttu-id="48cef-111">Debugebenen</span><span class="sxs-lookup"><span data-stu-id="48cef-111">Debug Levels</span></span>](#debug-levels)
-   [<span data-ttu-id="48cef-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="48cef-112">Related topics</span></span>](#related-topics)

## <a name="what-is-the-direct2d-debug-layer"></a><span data-ttu-id="48cef-113">Was ist die Direct2D-Debugebene?</span><span class="sxs-lookup"><span data-stu-id="48cef-113">What Is the Direct2D Debug Layer</span></span>

<span data-ttu-id="48cef-114">Die Direct2D-Debugebene, die separat von Direct2D in einer eigenen DLL namens d2d1debug.dll implementiert wird, stellt Debugmeldungen bereit, damit Sie Direct2D-Funktionen genau verwenden können.</span><span class="sxs-lookup"><span data-stu-id="48cef-114">The Direct2D debug layer, implemented separately from Direct2D in its own DLL named d2d1debug.dll, provides debug messages to enable you to accurately use Direct2D functions.</span></span> <span data-ttu-id="48cef-115">Die Debugmeldungen resultieren häufig aus API-Vertragsverletzungen wie ungültigen Parametern (kann direct3D-bezogen sein), ungültigen Ressourcen, Threadingverletzungen und Leistungsproblemen wie der Verwendung einer Ebene, wenn ein Clip ausreichen würde.</span><span class="sxs-lookup"><span data-stu-id="48cef-115">The debug messages often result from API contract violations such as invalid parameters (could be Direct3D-related), invalid resources, threading violations, and performance issues such as using a layer when a clip would suffice.</span></span> <span data-ttu-id="48cef-116">Um anzugeben, wie viele Informationen von der Debugebene nachverfolgt werden, können Sie eine der drei Debugebenen angeben: Information, Warnung und Fehler. und eine Meldung des Ebenenfehlers löst den Haltepunkt aus, um Sie beim Debuggen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="48cef-116">To specify how much information is traced by the debug layer, you can specify one of the three debug levels: information, warning, and error; and a message of level error triggers the breakpoint to help you debug.</span></span>

## <a name="installing-the-direct2d-debug-layer"></a><span data-ttu-id="48cef-117">Installieren der Direct2D-Debugebene</span><span class="sxs-lookup"><span data-stu-id="48cef-117">Installing the Direct2D Debug Layer</span></span>

<span data-ttu-id="48cef-118">Anweisungen zum Installieren der Debugebene finden Sie unter [Installieren der Direct2D-Debugebene.](installing-the-direct2d-debug-layer.md)</span><span class="sxs-lookup"><span data-stu-id="48cef-118">For instructions on installing the debug layer, see [Installing the Direct2D Debug Layer](installing-the-direct2d-debug-layer.md).</span></span>

## <a name="enabling-the-debug-layer"></a><span data-ttu-id="48cef-119">Aktivieren der Debugebene</span><span class="sxs-lookup"><span data-stu-id="48cef-119">Enabling the Debug Layer</span></span>

<span data-ttu-id="48cef-120">Um die Debugebene in Ihrer Anwendung zu aktivieren, geben Sie einen anderen [**D2D1 \_ DEBUG \_ LEVEL-Wert**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) als **D2D1 \_ DEBUG LEVEL \_ \_ NONE** an, wenn Sie eine Factory mit der [**D2D1CreateFactory-Funktion**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) erstellen.</span><span class="sxs-lookup"><span data-stu-id="48cef-120">To enable the debug layer in your application, specify a [**D2D1\_DEBUG\_LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) value other than **D2D1\_DEBUG\_LEVEL\_NONE** when you create a factory with the [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) function.</span></span>

> [!Note]  
> <span data-ttu-id="48cef-121">Wenn die Direct2D-Debugebene aktiviert ist, kann der Direct2D-Farbverwaltungseffekt (CLSID \_ D2D1ColorManagement) beim Festlegen eines Farbkontexts eine Zugriffsverletzung verursachen.</span><span class="sxs-lookup"><span data-stu-id="48cef-121">If the Direct2D debug layer is enabled, the Direct2D color management effect (CLSID\_D2D1ColorManagement) may cause an access violation when setting a color context.</span></span> <span data-ttu-id="48cef-122">Die Problemumgehung besteht darin, die Debugebene bei Verwendung des Farbverwaltungseffekts zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="48cef-122">The workaround is to disable the debug layer when using the color management effect</span></span>

 

<span data-ttu-id="48cef-123">Wenn Sie die Debugebene für eine Factory aktivieren, werden auch Debuginformationen für jedes objekt aktiviert, das von dieser Factory erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="48cef-123">Enabling the debug layer for a factory also enables debugging information for any object created by that factory.</span></span>

<span data-ttu-id="48cef-124">Im folgenden Beispiel wird die Debugebene für eine Factory aktiviert, wenn die Anwendung für die DEBUG-Buildkonfiguration kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="48cef-124">The following example enables the debug layer for a factory when the application is compiled for the DEBUG build configuration.</span></span>


```C++
        // If you set the options.debugLevel to D2D1_DEBUG_LEVEL_NONE,
        // the debug layer is not enabled.
#if defined(DEBUG) || defined(_DEBUG)
        D2D1_FACTORY_OPTIONS options;
        options.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;

        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            options,
            &m_pD2DFactory
            );
#else
        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            &m_pD2DFactory
            );
#endif
```



> [!Note]  
> <span data-ttu-id="48cef-125">Wenn keine Factoryoptionen angegeben oder die Debugebene "none" angegeben ist, wird die Debugebene nicht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="48cef-125">If no factory options are specified or a debug level of "none" is specified, the debug layer is not invoked.</span></span> <span data-ttu-id="48cef-126">Die Debugebene sollte in der Releaseversion einer Anwendung nie aktiv sein.</span><span class="sxs-lookup"><span data-stu-id="48cef-126">The debug layer should never be active in the release version of an application.</span></span>

 

<span data-ttu-id="48cef-127">Im nächsten Abschnitt werden die verschiedenen Debugebenen beschrieben, die durch die [**D2D1 \_ DEBUG \_ LEVEL-Enumeration**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) definiert werden.</span><span class="sxs-lookup"><span data-stu-id="48cef-127">The next section describes the different debug levels defined by the [**D2D1\_DEBUG\_LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) enumeration.</span></span>

## <a name="debug-levels"></a><span data-ttu-id="48cef-128">Debugebenen</span><span class="sxs-lookup"><span data-stu-id="48cef-128">Debug Levels</span></span>

<span data-ttu-id="48cef-129">Die [**D2D1 \_ DEBUG \_ LEVEL-Enumeration**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) gibt drei Debugebenen an: D2D1 \_ DEBUG LEVEL ERROR \_ \_ (Fehler), D2D1 \_ DEBUG LEVEL WARNING \_ \_ (Warnung) und D2D1 \_ DEBUG LEVEL INFORMATION \_ \_ (Information).</span><span class="sxs-lookup"><span data-stu-id="48cef-129">The [**D2D1\_DEBUG\_LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) enumeration specifies three debug levels: D2D1\_DEBUG\_LEVEL\_ERROR (error), D2D1\_DEBUG\_LEVEL\_WARNING (warning), and D2D1\_DEBUG\_LEVEL\_INFORMATION (information).</span></span> <span data-ttu-id="48cef-130">Diese Ebenen werden wie folgt interpretiert:</span><span class="sxs-lookup"><span data-stu-id="48cef-130">These levels are interpreted as follows:</span></span>

-   <span data-ttu-id="48cef-131">**Fehler:** Direct2D sendet schwerwiegende Fehlermeldungen an die Debugebene.</span><span class="sxs-lookup"><span data-stu-id="48cef-131">**Error:** Direct2D sends severe error messages to the debug layer.</span></span> <span data-ttu-id="48cef-132">Wenn Sie z. B. eine Threadingeinschränkung durchbrechen, wird ein schwerwiegender Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="48cef-132">For example, breaking a threading constraint will generate a severe error.</span></span>

-   <span data-ttu-id="48cef-133">**Warnung:** Direct2D sendet Fehlermeldungen und Warnungen an die Debugebene, sodass Sie jede dieser Meldungen beheben können.</span><span class="sxs-lookup"><span data-stu-id="48cef-133">**Warning:** Direct2D sends error messages and warnings to the debug layer so that you can address any of these messages.</span></span>

-   <span data-ttu-id="48cef-134">**Informationen:** Direct2D sendet Fehlermeldungen, Warnungen und zusätzliche Diagnoseinformationen an die Debugebene.</span><span class="sxs-lookup"><span data-stu-id="48cef-134">**Information:** Direct2D sends error messages, warnings, and additional diagnostic information to the debug layer.</span></span> <span data-ttu-id="48cef-135">Beispielsweise werden Meldungen zur Leistungsverbesserung auf dieser Debugebene gesendet.</span><span class="sxs-lookup"><span data-stu-id="48cef-135">For example, performance improvement messages will be sent at this debug level.</span></span>

<span data-ttu-id="48cef-136">Der Wert D2D1 \_ DEBUG \_ LEVEL NONE \_ (none) gibt an, dass Direct2D keine Debugausgabe bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="48cef-136">The value D2D1\_DEBUG\_LEVEL\_NONE (none) indicates that Direct2D does not provide any debugging output.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48cef-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="48cef-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48cef-138">Debuggen von Nachrichten</span><span class="sxs-lookup"><span data-stu-id="48cef-138">Debug Messages</span></span>](direct2ddebuglayer-debugmessages.md)
</dt> </dl>

 

 




