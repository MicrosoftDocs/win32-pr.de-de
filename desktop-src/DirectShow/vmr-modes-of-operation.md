---
description: VMR-Betriebsmodi
ms.assetid: 98244af1-5934-4d1c-b9c3-7a414b065fe7
title: VMR-Betriebsmodi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43427c4119bb912d2bc2cf92b1c740b1d22e1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353170"
---
# <a name="vmr-modes-of-operation"></a><span data-ttu-id="39a44-103">VMR-Betriebsmodi</span><span class="sxs-lookup"><span data-stu-id="39a44-103">VMR Modes of Operation</span></span>

<span data-ttu-id="39a44-104">Die Komponentenarchitektur von VMR ermöglicht es Anwendungen, diese auf verschiedene Weise zu konfigurieren, je nachdem, wie das Rendering durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="39a44-104">The component architecture of the VMR enables applications to configure it in various ways, depending on how rendering is to be performed.</span></span> <span data-ttu-id="39a44-105">In der folgenden Tabelle werden die drei präsentationsmodi und die beiden-Mischungs Modi und die Komponenten aufgeführt, die für die einzelnen Konfigurationen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="39a44-105">The following table shows the three presentation modes and the two mixing modes, and the components that are present for each configuration.</span></span>



| <span data-ttu-id="39a44-106">Mode</span><span class="sxs-lookup"><span data-stu-id="39a44-106">Mode</span></span>       | <span data-ttu-id="39a44-107">Einzelner Stream</span><span class="sxs-lookup"><span data-stu-id="39a44-107">Single Stream</span></span>                                                                     | <span data-ttu-id="39a44-108">Mehrere Streams (Mischungs Modus)</span><span class="sxs-lookup"><span data-stu-id="39a44-108">Multiple Streams (Mixing Mode)</span></span>                                                                                             |
|------------|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39a44-109">Fenster</span><span class="sxs-lookup"><span data-stu-id="39a44-109">Windowed</span></span>   | <span data-ttu-id="39a44-110">Zuordnung-presentercore-Synchronisierungs Einheit</span><span class="sxs-lookup"><span data-stu-id="39a44-110">Allocator-presenterCore Synchronization Unit</span></span><br/> <span data-ttu-id="39a44-111">Fenster-Manager</span><span class="sxs-lookup"><span data-stu-id="39a44-111">Window Manager</span></span><br/> | <span data-ttu-id="39a44-112">Mixercompositor\*</span><span class="sxs-lookup"><span data-stu-id="39a44-112">MixerCompositor\*</span></span><br/> <span data-ttu-id="39a44-113">Zuordnung-Presenter</span><span class="sxs-lookup"><span data-stu-id="39a44-113">Allocator-presenter</span></span><br/> <span data-ttu-id="39a44-114">Core-Synchronisierungs Einheit</span><span class="sxs-lookup"><span data-stu-id="39a44-114">Core Synchronization Unit</span></span><br/> <span data-ttu-id="39a44-115">Fenster-Manager</span><span class="sxs-lookup"><span data-stu-id="39a44-115">Window Manager</span></span><br/> |
| <span data-ttu-id="39a44-116">Fensterlose</span><span class="sxs-lookup"><span data-stu-id="39a44-116">Windowless</span></span> | <span data-ttu-id="39a44-117">Zuordnung-presentercore-Synchronisierungs Einheit</span><span class="sxs-lookup"><span data-stu-id="39a44-117">Allocator-presenterCore Synchronization Unit</span></span><br/>                           | <span data-ttu-id="39a44-118">Mixercompositor\*</span><span class="sxs-lookup"><span data-stu-id="39a44-118">MixerCompositor\*</span></span><br/> <span data-ttu-id="39a44-119">Zuordnung-Presenter</span><span class="sxs-lookup"><span data-stu-id="39a44-119">Allocator-presenter</span></span><br/> <span data-ttu-id="39a44-120">Core-Synchronisierungs Einheit</span><span class="sxs-lookup"><span data-stu-id="39a44-120">Core Synchronization Unit</span></span><br/>                           |
| <span data-ttu-id="39a44-121">Renderlos</span><span class="sxs-lookup"><span data-stu-id="39a44-121">Renderless</span></span> | <span data-ttu-id="39a44-122">Zuordnung von "Zuweisung-Presenter" (von Anwendung bereitgestellt) Core-Synchronisierungs Einheit</span><span class="sxs-lookup"><span data-stu-id="39a44-122">Allocator-presenter (provided by application)Core Synchronization Unit</span></span><br/> | <span data-ttu-id="39a44-123">Mixercompositor\*</span><span class="sxs-lookup"><span data-stu-id="39a44-123">MixerCompositor\*</span></span><br/> <span data-ttu-id="39a44-124">Zuordnung-Presenter (von Anwendung bereitgestellt)</span><span class="sxs-lookup"><span data-stu-id="39a44-124">Allocator-presenter (provided by application)</span></span><br/> <span data-ttu-id="39a44-125">Core-Synchronisierungs Einheit</span><span class="sxs-lookup"><span data-stu-id="39a44-125">Core Synchronization Unit</span></span><br/> |



 

<span data-ttu-id="39a44-126">\* Gibt an, dass die Anwendung über die Option verfügt, eine benutzerdefinierte Komponente bereitzustellen oder die Standardkomponente zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="39a44-126">\* Indicates that the application has the option to provide a custom component or use the default component.</span></span>

<span data-ttu-id="39a44-127">Bei allen Konfigurationen sollten Sie sich beim Erstellen von Filter Diagrammen mit der VMR nicht merken, dass Sie die VMR vor dem verbinden konfigurieren müssen.</span><span class="sxs-lookup"><span data-stu-id="39a44-127">In all configurations, the main point to remember when you create filter graphs with the VMR is that you must configure the VMR before you connect it.</span></span>

<span data-ttu-id="39a44-128">Für alle Konfigurationen können Pins nicht dynamisch hinzugefügt oder entfernt werden, nachdem die VMR mit dem upstreamfilter verbunden ist, Sie können jedoch verbunden und getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="39a44-128">For all configurations, pins cannot be dynamically added or removed after the VMR is connected to the upstream filter, but they can be connected and disconnected.</span></span> <span data-ttu-id="39a44-129">Wenn die Anwendung nicht sicher ist, wie viele Pins benötigt werden, sollte die VMR für die maximal benötigte Anzahl konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="39a44-129">If the application is unsure how many pins will be needed, it should configure the VMR for the maximum number that might be needed.</span></span> <span data-ttu-id="39a44-130">Das vorhanden sein von nicht verwendeten Eingabe Pins für den Filter beeinträchtigt nicht die Renderingleistung.</span><span class="sxs-lookup"><span data-stu-id="39a44-130">The presence of unused input pins on the filter does not degrade rendering performance.</span></span> <span data-ttu-id="39a44-131">Im Gegensatz zum alten Überlagerungs-Mixer hat VMR keine Ausgabe-PIN, da es keinen separaten Filter für die Fensterverwaltung erfordert.</span><span class="sxs-lookup"><span data-stu-id="39a44-131">Unlike the old Overlay Mixer, the VMR has no output pin because it does not require a separate filter for window management.</span></span>

<span data-ttu-id="39a44-132">In den folgenden Abschnitten wird beschrieben, wie Sie den VMR für einen bestimmten Modus konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="39a44-132">The following sections describe how to configure the VMR for a given mode:</span></span>

-   [<span data-ttu-id="39a44-133">VMR-Fenstermodus (Kompatibilitätsmodus)</span><span class="sxs-lookup"><span data-stu-id="39a44-133">VMR Windowed (Compatibility) Mode</span></span>](vmr-windowed--compatibility--mode.md)
-   [<span data-ttu-id="39a44-134">Fensterloser VMR-Modus</span><span class="sxs-lookup"><span data-stu-id="39a44-134">VMR Windowless Mode</span></span>](vmr-windowless-mode.md)
-   [<span data-ttu-id="39a44-135">VMR mit mehreren Streams (Mischungs Modus)</span><span class="sxs-lookup"><span data-stu-id="39a44-135">VMR with Multiple Streams (Mixing Mode)</span></span>](vmr-with-multiple-streams--mixing-mode.md)
-   [<span data-ttu-id="39a44-136">YUV-Mischungs Modus</span><span class="sxs-lookup"><span data-stu-id="39a44-136">YUV Mixing Mode</span></span>](yuv-mixing-mode.md)
-   [<span data-ttu-id="39a44-137">Positionieren und Verschieben von Video Rechtecke im Kompositions Bereich</span><span class="sxs-lookup"><span data-stu-id="39a44-137">Positioning and Moving Video Rectangles in Composition Space</span></span>](positioning-and-moving-video-rectangles-in-composition-space.md)
-   [<span data-ttu-id="39a44-138">VMR-renderlosen Wiedergabemodus (benutzerdefinierter Zuweiser)</span><span class="sxs-lookup"><span data-stu-id="39a44-138">VMR Renderless Playback Mode (Custom Allocator-Presenters)</span></span>](vmr-renderless-playback-mode--custom-allocator-presenters.md)
-   [<span data-ttu-id="39a44-139">Exklusiver DirectDraw-Modus</span><span class="sxs-lookup"><span data-stu-id="39a44-139">DirectDraw Exclusive Mode</span></span>](directdraw-exclusive-mode.md)

 

 




