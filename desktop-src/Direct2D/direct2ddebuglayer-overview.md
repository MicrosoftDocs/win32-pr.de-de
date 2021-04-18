---
title: Direct2D Übersicht über die Debug-Ebene
description: .
ms.assetid: 7c28e00b-ebb9-4b79-939c-64eade1351ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df560595ea0ae6c7a56c3fa568f2f94ae56652ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338372"
---
# <a name="direct2d-debug-layer-overview"></a><span data-ttu-id="80c52-103">Direct2D Übersicht über die Debug-Ebene</span><span class="sxs-lookup"><span data-stu-id="80c52-103">Direct2D Debug Layer Overview</span></span>

<span data-ttu-id="80c52-104">Die Direct2D Debug-Schicht stellt Entwurfszeit-Debugmeldungen bereit, mit denen Sie den Lauf Zeit Anwendungs Ausfall minimieren können</span><span class="sxs-lookup"><span data-stu-id="80c52-104">The Direct2D debug layer provides design-time debug messages for you to minimize runtime application failure.</span></span> <span data-ttu-id="80c52-105">In dieser Übersicht werden die Grundlagen der Direct2D Debug-Ebene beschrieben.</span><span class="sxs-lookup"><span data-stu-id="80c52-105">This overview describes the basics of the Direct2D debug layer.</span></span> <span data-ttu-id="80c52-106">Es wird vorausgesetzt, dass Sie mit dem Erstellen von Direct2D-Basisanwendungen vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="80c52-106">It assumes that you are familiar with creating basic Direct2D applications.</span></span>

<span data-ttu-id="80c52-107">Diese Übersicht enthält die folgenden Abschnitte.</span><span class="sxs-lookup"><span data-stu-id="80c52-107">This overview contains the following sections.</span></span>

-   [<span data-ttu-id="80c52-108">Was ist die Direct2D-Debug-Ebene?</span><span class="sxs-lookup"><span data-stu-id="80c52-108">What Is the Direct2D Debug Layer</span></span>](#what-is-the-direct2d-debug-layer)
-   [<span data-ttu-id="80c52-109">Installieren der Direct2D Debug-Ebene</span><span class="sxs-lookup"><span data-stu-id="80c52-109">Installing the Direct2D Debug Layer</span></span>](#installing-the-direct2d-debug-layer)
-   [<span data-ttu-id="80c52-110">Aktivieren der Debug-Ebene</span><span class="sxs-lookup"><span data-stu-id="80c52-110">Enabling the Debug Layer</span></span>](#enabling-the-debug-layer)
-   [<span data-ttu-id="80c52-111">Debugstufen</span><span class="sxs-lookup"><span data-stu-id="80c52-111">Debug Levels</span></span>](#debug-levels)
-   [<span data-ttu-id="80c52-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="80c52-112">Related topics</span></span>](#related-topics)

## <a name="what-is-the-direct2d-debug-layer"></a><span data-ttu-id="80c52-113">Was ist die Direct2D-Debug-Ebene?</span><span class="sxs-lookup"><span data-stu-id="80c52-113">What Is the Direct2D Debug Layer</span></span>

<span data-ttu-id="80c52-114">Die Direct2D-debugschicht, die separat von Direct2D in der eigenen dll mit dem Namen d2d1debug.dll implementiert wurde, stellt Debugmeldungen bereit, damit Sie Direct2D-Funktionen genau verwenden können.</span><span class="sxs-lookup"><span data-stu-id="80c52-114">The Direct2D debug layer, implemented separately from Direct2D in its own DLL named d2d1debug.dll, provides debug messages to enable you to accurately use Direct2D functions.</span></span> <span data-ttu-id="80c52-115">Die Debugmeldungen resultieren häufig aus API-Vertragsverstößen, wie z. b. ungültigen Parametern (Direct3D-bezogen), ungültigen Ressourcen, Threading Verstößen und Leistungsproblemen wie der Verwendung einer Ebene, wenn ein Clip ausreichen würde.</span><span class="sxs-lookup"><span data-stu-id="80c52-115">The debug messages often result from API contract violations such as invalid parameters (could be Direct3D-related), invalid resources, threading violations, and performance issues such as using a layer when a clip would suffice.</span></span> <span data-ttu-id="80c52-116">Um anzugeben, wie viele Informationen von der debugschicht verfolgt werden, können Sie eine der drei debugebenen angeben: Information, Warnung und Fehler. und eine Fehlermeldungs Ebene löst den Haltepunkt aus, um Sie beim Debuggen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="80c52-116">To specify how much information is traced by the debug layer, you can specify one of the three debug levels: information, warning, and error; and a message of level error triggers the breakpoint to help you debug.</span></span>

## <a name="installing-the-direct2d-debug-layer"></a><span data-ttu-id="80c52-117">Installieren der Direct2D Debug-Ebene</span><span class="sxs-lookup"><span data-stu-id="80c52-117">Installing the Direct2D Debug Layer</span></span>

<span data-ttu-id="80c52-118">Anweisungen zum Installieren der debugschicht finden Sie unter [Installieren der Direct2D-debugschicht](installing-the-direct2d-debug-layer.md).</span><span class="sxs-lookup"><span data-stu-id="80c52-118">For instructions on installing the debug layer, see [Installing the Direct2D Debug Layer](installing-the-direct2d-debug-layer.md).</span></span>

## <a name="enabling-the-debug-layer"></a><span data-ttu-id="80c52-119">Aktivieren der Debug-Ebene</span><span class="sxs-lookup"><span data-stu-id="80c52-119">Enabling the Debug Layer</span></span>

<span data-ttu-id="80c52-120">Um die Debugebene in der Anwendung zu aktivieren, geben Sie den Wert [**D2D1 \_ Debug \_ Level**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) than **D2D1 \_ Debug \_ Level \_ None** an, wenn Sie eine Factory mit der [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) -Funktion erstellen.</span><span class="sxs-lookup"><span data-stu-id="80c52-120">To enable the debug layer in your application, specify a [**D2D1\_DEBUG\_LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) value other than **D2D1\_DEBUG\_LEVEL\_NONE** when you create a factory with the [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) function.</span></span>

> [!Note]  
> <span data-ttu-id="80c52-121">Wenn die Direct2D Debug-Ebene aktiviert ist, kann der Direct2D Color Management Effect (CLSID \_ D2D1ColorManagement) beim Festlegen eines Farb Kontexts eine Zugriffsverletzung verursachen.</span><span class="sxs-lookup"><span data-stu-id="80c52-121">If the Direct2D debug layer is enabled, the Direct2D color management effect (CLSID\_D2D1ColorManagement) may cause an access violation when setting a color context.</span></span> <span data-ttu-id="80c52-122">Die Problem Umgehung besteht darin, die debugschicht bei Verwendung des Farb Verwaltungs Effekts zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="80c52-122">The workaround is to disable the debug layer when using the color management effect</span></span>

 

<span data-ttu-id="80c52-123">Wenn Sie die debugschicht für eine Factory aktivieren, werden auch Debuginformationen für jedes von dieser Factory erstellte Objekt aktiviert.</span><span class="sxs-lookup"><span data-stu-id="80c52-123">Enabling the debug layer for a factory also enables debugging information for any object created by that factory.</span></span>

<span data-ttu-id="80c52-124">Im folgenden Beispiel wird die debugschicht für eine Factory aktiviert, wenn die Anwendung für die Debug-Buildkonfiguration kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="80c52-124">The following example enables the debug layer for a factory when the application is compiled for the DEBUG build configuration.</span></span>


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
> <span data-ttu-id="80c52-125">Wenn keine Factory-Optionen angegeben werden oder die Debugebene "None" angegeben ist, wird die debugschicht nicht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="80c52-125">If no factory options are specified or a debug level of "none" is specified, the debug layer is not invoked.</span></span> <span data-ttu-id="80c52-126">Die debugschicht sollte in der Releaseversion einer Anwendung nie aktiv sein.</span><span class="sxs-lookup"><span data-stu-id="80c52-126">The debug layer should never be active in the release version of an application.</span></span>

 

<span data-ttu-id="80c52-127">Im nächsten Abschnitt werden die verschiedenen debugebenen beschrieben, die von der [**D2D1 \_ Debug \_ Level**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) -Enumeration definiert werden.</span><span class="sxs-lookup"><span data-stu-id="80c52-127">The next section describes the different debug levels defined by the [**D2D1\_DEBUG\_LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) enumeration.</span></span>

## <a name="debug-levels"></a><span data-ttu-id="80c52-128">Debugstufen</span><span class="sxs-lookup"><span data-stu-id="80c52-128">Debug Levels</span></span>

<span data-ttu-id="80c52-129">Die [**D2D1 \_ Debug \_ Level**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) -Enumeration gibt drei debugebenen an: D2D1 \_ Debug \_ Level \_ Error (Error), D2D1 \_ Debug \_ Level \_ Warning (Warning) und D2D1 \_ Debug \_ Level \_ Information (Informationen).</span><span class="sxs-lookup"><span data-stu-id="80c52-129">The [**D2D1\_DEBUG\_LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) enumeration specifies three debug levels: D2D1\_DEBUG\_LEVEL\_ERROR (error), D2D1\_DEBUG\_LEVEL\_WARNING (warning), and D2D1\_DEBUG\_LEVEL\_INFORMATION (information).</span></span> <span data-ttu-id="80c52-130">Diese Ebenen werden wie folgt interpretiert:</span><span class="sxs-lookup"><span data-stu-id="80c52-130">These levels are interpreted as follows:</span></span>

-   <span data-ttu-id="80c52-131">**Fehler:** Direct2D sendet schwerwiegende Fehlermeldungen an die debugschicht.</span><span class="sxs-lookup"><span data-stu-id="80c52-131">**Error:** Direct2D sends severe error messages to the debug layer.</span></span> <span data-ttu-id="80c52-132">Beispielsweise wird durch das Unterbrechen einer Threading Einschränkung ein schwerwiegender Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="80c52-132">For example, breaking a threading constraint will generate a severe error.</span></span>

-   <span data-ttu-id="80c52-133">**Warnung:** Direct2D sendet Fehlermeldungen und Warnungen an die debugschicht, damit Sie diese Nachrichten adressieren können.</span><span class="sxs-lookup"><span data-stu-id="80c52-133">**Warning:** Direct2D sends error messages and warnings to the debug layer so that you can address any of these messages.</span></span>

-   <span data-ttu-id="80c52-134">**Informationen:** Direct2D sendet Fehlermeldungen, Warnungen und zusätzliche Diagnoseinformationen an die debugschicht.</span><span class="sxs-lookup"><span data-stu-id="80c52-134">**Information:** Direct2D sends error messages, warnings, and additional diagnostic information to the debug layer.</span></span> <span data-ttu-id="80c52-135">Beispielsweise werden Meldungen zur Leistungsverbesserung auf dieser Debugebene gesendet.</span><span class="sxs-lookup"><span data-stu-id="80c52-135">For example, performance improvement messages will be sent at this debug level.</span></span>

<span data-ttu-id="80c52-136">Der Wert D2D1 \_ Debug \_ Level \_ None (None) gibt an, dass Direct2D keine Debugausgabe bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="80c52-136">The value D2D1\_DEBUG\_LEVEL\_NONE (none) indicates that Direct2D does not provide any debugging output.</span></span>

## <a name="related-topics"></a><span data-ttu-id="80c52-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="80c52-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80c52-138">Debugmeldungen</span><span class="sxs-lookup"><span data-stu-id="80c52-138">Debug Messages</span></span>](direct2ddebuglayer-debugmessages.md)
</dt> </dl>

 

 




