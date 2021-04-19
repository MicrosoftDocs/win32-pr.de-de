---
description: Der Tablet PC umfasst Technologien für die Interaktion mit Tablet Pen-Daten, während diese gesammelt werden.
ms.assetid: e026f860-be4d-40a5-b951-15b8be3cd626
title: Zugreifen auf und Bearbeiten von Tablettstifteingaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 333126f195154241333127ec585864bd9d592a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343206"
---
# <a name="accessing-and-manipulating-stylus-input"></a><span data-ttu-id="b08ef-103">Zugreifen auf und Bearbeiten von Tablettstifteingaben</span><span class="sxs-lookup"><span data-stu-id="b08ef-103">Accessing and Manipulating Stylus Input</span></span>

<span data-ttu-id="b08ef-104">Der Tablet PC umfasst Technologien für die Interaktion mit Tablet Pen-Daten, während diese gesammelt werden.</span><span class="sxs-lookup"><span data-stu-id="b08ef-104">The Tablet PC includes technology for interacting with tablet pen data as it is being gathered.</span></span> <span data-ttu-id="b08ef-105">Die [**RealTimeStylus**](realtimestylus-class.md) -Klasse ist Teil der StylusInput-API (Application Programming Interfaces), die Zugriff auf den Tablet Pen-Datenstream bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b08ef-105">The [**RealTimeStylus**](realtimestylus-class.md) class is part of the StylusInput application programming interfaces (API), which provide access to the tablet pen data stream.</span></span> <span data-ttu-id="b08ef-106">Mit diesen APIs können Sie den Stream unabhängig vom Rendern und Sammeln von frei Hand Eingaben erfassen, unterbrechen und ändern.</span><span class="sxs-lookup"><span data-stu-id="b08ef-106">These APIs allow you to capture, interrupt, and modify the stream independently from rendering and collecting ink.</span></span>

<span data-ttu-id="b08ef-107">Die StylusInput-APIs sind für Folgendes konzipiert:</span><span class="sxs-lookup"><span data-stu-id="b08ef-107">The StylusInput APIs are designed to:</span></span>

-   <span data-ttu-id="b08ef-108">Stellen Sie Echtzeitzugriff auf den Tablet Pen-Datenstrom bereit.</span><span class="sxs-lookup"><span data-stu-id="b08ef-108">Provide real-time access to the tablet pen data stream.</span></span>
-   <span data-ttu-id="b08ef-109">Sorgen Sie dafür, dass der Benutzeroberflächen Thread das dynamische frei Hand Rendering blockiert, indem die Paketdaten im UI-Thread in die Warteschlange eingereiht werden und die frei Hand Auflistung Single Thread ist.</span><span class="sxs-lookup"><span data-stu-id="b08ef-109">Keep the user interface (UI) thread from blocking dynamic ink rendering by queuing the packet data on the UI thread and making ink collection single threaded.</span></span>
-   <span data-ttu-id="b08ef-110">Erhöhen Sie die Leistung, und senken Sie die gesamt Thread Verwendung über das [**InkCollector**](inkcollector-class.md) -Objekt, das [**InkOverlay**](inkoverlay-class.md) -Objekt, das [InkPicture](inkpicture-control-reference.md) -Steuerelement oder das [InkEdit](inkedit-control-reference.md) -Steuerelement, um frei Hand Eingaben</span><span class="sxs-lookup"><span data-stu-id="b08ef-110">Increase the performance and lower the overall thread usage over using the [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, [InkPicture](inkpicture-control-reference.md) control, or [InkEdit](inkedit-control-reference.md) control to collect ink.</span></span>

<span data-ttu-id="b08ef-111">Die StylusInput-APIs sind nicht für die Arbeit mit dem [**InkCollector**](inkcollector-class.md) -Objekt, dem [**InkOverlay**](inkoverlay-class.md) -Objekt, dem [InkPicture](inkpicture-control-reference.md) -Steuerelement oder dem [InkEdit](inkedit-control-reference.md) -Steuerelement konzipiert.</span><span class="sxs-lookup"><span data-stu-id="b08ef-111">The StylusInput APIs are not designed to work with the [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, [InkPicture](inkpicture-control-reference.md) control, or [InkEdit](inkedit-control-reference.md) control.</span></span>

<span data-ttu-id="b08ef-112">Wenn Sie direkt mit dem Tablettstiftdaten-Datenstrom interagieren müssen oder wenn Ihre Anwendung das Echt Zeit Inking blockieren kann, verwenden Sie das [**RealTimeStylus**](realtimestylus-class.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="b08ef-112">When you need to interact directly with the tablet pen data stream or when your application may block real-time inking, use the [**RealTimeStylus**](realtimestylus-class.md) object.</span></span> <span data-ttu-id="b08ef-113">Verwenden Sie das [**InkCollector**](inkcollector-class.md) -Objekt, das [**InkOverlay**](inkoverlay-class.md) -Objekt, das [InkPicture](inkpicture-control-reference.md) -Steuerelement oder das [InkEdit](inkedit-control-reference.md) -Steuerelement, wenn das Standardverhalten dieser Objekte das benötigte Verhalten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="b08ef-113">Use the [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, [InkPicture](inkpicture-control-reference.md) control, or [InkEdit](inkedit-control-reference.md) control when the default behavior of these objects provides the behavior you need.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b08ef-114">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="b08ef-114">In This Section</span></span>

<span data-ttu-id="b08ef-115">In den folgenden Abschnitten werden die Elemente der StylusInput-APIs beschrieben:</span><span class="sxs-lookup"><span data-stu-id="b08ef-115">The following sections describe elements of the StylusInput APIs:</span></span>

-   [<span data-ttu-id="b08ef-116">Architektur der StylusInput-APIs</span><span class="sxs-lookup"><span data-stu-id="b08ef-116">Architecture of the StylusInput APIs</span></span>](architecture-of-the-stylusinput-apis.md)
-   [<span data-ttu-id="b08ef-117">Arbeiten mit den StylusInput-APIs</span><span class="sxs-lookup"><span data-stu-id="b08ef-117">Working with the StylusInput APIs</span></span>](working-with-the-stylusinput-apis.md)
    -   [<span data-ttu-id="b08ef-118">Arbeiten mit der RealTimeStylus-Klasse</span><span class="sxs-lookup"><span data-stu-id="b08ef-118">Working with the RealTimeStylus Class</span></span>](working-with-the-realtimestylus-class.md)
    -   [<span data-ttu-id="b08ef-119">Plug-ins und die RealTimeStylus-Klasse</span><span class="sxs-lookup"><span data-stu-id="b08ef-119">Plug-ins and the RealTimeStylus Class</span></span>](plug-ins-and-the-realtimestylus-class.md)
    -   [<span data-ttu-id="b08ef-120">Plug-In-Daten und die RealTimeStylus-Klasse</span><span class="sxs-lookup"><span data-stu-id="b08ef-120">Plug-in Data and the RealTimeStylus Class</span></span>](plug-in-data-and-the-realtimestylus-class.md)
    -   [<span data-ttu-id="b08ef-121">Implementierungs Hinweise für die StylusInput-APIs</span><span class="sxs-lookup"><span data-stu-id="b08ef-121">Implementation Notes for the StylusInput APIs</span></span>](implementation-notes-for-the-stylusinput-apis.md)
    -   [<span data-ttu-id="b08ef-122">Plug-Ins für die frei Hand Erfassung</span><span class="sxs-lookup"><span data-stu-id="b08ef-122">Ink-Collection Plug-ins</span></span>](ink-collection-plug-ins.md)
    -   [<span data-ttu-id="b08ef-123">Plug-Ins für dynamisches Renderer</span><span class="sxs-lookup"><span data-stu-id="b08ef-123">Dynamic-Renderer Plug-ins</span></span>](dynamic-renderer-plug-ins.md)
    -   [<span data-ttu-id="b08ef-124">Erkennungs-Plug-ins</span><span class="sxs-lookup"><span data-stu-id="b08ef-124">Recognizer Plug-ins</span></span>](recognizer-plug-ins.md)
-   [<span data-ttu-id="b08ef-125">Überlegungen bei der Verwendung der StylusInput-APIs</span><span class="sxs-lookup"><span data-stu-id="b08ef-125">Considerations when Using the StylusInput APIs</span></span>](considerations-when-using-the-stylusinput-apis.md)
    -   [<span data-ttu-id="b08ef-126">Entwurfs Überlegungen für die StylusInput-APIs</span><span class="sxs-lookup"><span data-stu-id="b08ef-126">Design Considerations for the StylusInput APIs</span></span>](design-considerations-for-the-stylusinput-apis.md)
    -   [<span data-ttu-id="b08ef-127">Threading Überlegungen für die StylusInput-APIs</span><span class="sxs-lookup"><span data-stu-id="b08ef-127">Threading Considerations for the StylusInput APIs</span></span>](threading-considerations-for-the-stylusinput-apis.md)

[<span data-ttu-id="b08ef-128">Das Cascaded RealTimeStylus-Modell</span><span class="sxs-lookup"><span data-stu-id="b08ef-128">The Cascaded RealTimeStylus Model</span></span>](the-cascaded-realtimestylus-model.md)

-   [<span data-ttu-id="b08ef-129">Überlegungen zur Fehlerbehandlung für die StylusInput-APIs</span><span class="sxs-lookup"><span data-stu-id="b08ef-129">Error Handling Considerations for the StylusInput APIs</span></span>](error-handling-considerations-for-the-stylusinput-apis.md)
-   [<span data-ttu-id="b08ef-130">Überlegungen zur Leistung der StylusInput-APIs</span><span class="sxs-lookup"><span data-stu-id="b08ef-130">Performance Considerations for the StylusInput APIs</span></span>](performance-considerations-for-the-stylusinput-apis.md)
-   [<span data-ttu-id="b08ef-131">Überlegungen zur teilweisen Vertrauenswürdigkeit für die StylusInput-APIs</span><span class="sxs-lookup"><span data-stu-id="b08ef-131">Partial Trust Considerations for the StylusInput APIs</span></span>](partial-trust-considerations-for-the-stylusinput-apis.md)

## <a name="related-topics"></a><span data-ttu-id="b08ef-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b08ef-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b08ef-133">Plug-in-Beispiel für RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="b08ef-133">RealTimeStylus Plug-in Sample</span></span>](realtimestylus-plug-in-sample.md)
</dt> <dt>

[<span data-ttu-id="b08ef-134">RealTimeStylus Ink Collection-Beispiel</span><span class="sxs-lookup"><span data-stu-id="b08ef-134">RealTimeStylus Ink Collection Sample</span></span>](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 



