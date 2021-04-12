---
description: Bietet Zugriff auf die Tablettstiftereignisse von Stift-oder Fingerabdruck-Digitalisierern.
ms.assetid: a239b53c-7fc9-4211-962a-6cfbe0be4e4c
title: RealTimeStylus-Referenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9016779c3165bc8fb6e24e5612901a7fd58435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216973"
---
# <a name="realtimestylus-reference"></a><span data-ttu-id="5ecc9-103">RealTimeStylus-Referenz</span><span class="sxs-lookup"><span data-stu-id="5ecc9-103">RealTimeStylus Reference</span></span>

<span data-ttu-id="5ecc9-104">Bietet Zugriff auf die Tablettstiftereignisse von Stift-oder Fingerabdruck-Digitalisierern.</span><span class="sxs-lookup"><span data-stu-id="5ecc9-104">Provides access to the stylus events coming from pen or touch digitizers.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5ecc9-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="5ecc9-105">In This Section</span></span>

-   [<span data-ttu-id="5ecc9-106">RealTimeStylus-Klassen und-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="5ecc9-106">RealTimeStylus Classes and Interfaces</span></span>](realtimestylus-classes-and-interfaces.md)
-   [<span data-ttu-id="5ecc9-107">RealTimeStylus-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="5ecc9-107">RealTimeStylus Enumerations</span></span>](realtimestylus-enumerations.md)
-   [<span data-ttu-id="5ecc9-108">RealTimeStylus-Strukturen</span><span class="sxs-lookup"><span data-stu-id="5ecc9-108">RealTimeStylus Structures</span></span>](realtimestylus-structures.md)

## <a name="remarks"></a><span data-ttu-id="5ecc9-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ecc9-109">Remarks</span></span>

<span data-ttu-id="5ecc9-110">Dieses Objekt implementiert die [**irealtimestylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) -com-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5ecc9-110">This object implements the [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) COM interface.</span></span>

<span data-ttu-id="5ecc9-111">Dieses Objekt kann durch Aufrufen der [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Methode in C++ instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="5ecc9-111">This object can be instantiated by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

<span data-ttu-id="5ecc9-112">Sie können Daten aus dem Paketstream in den synchronen und asynchronen Plug-ins des [**RealTimeStylus-Klassen**](realtimestylus-class.md) Objekts vollständig steuern, dynamisch rendern, ändern und sogar löschen.</span><span class="sxs-lookup"><span data-stu-id="5ecc9-112">You can fully control, dynamically render, modify, and even delete data from the packet stream within the synchronous and asynchronous plug-ins of the [**RealTimeStylus Class**](realtimestylus-class.md) object.</span></span>

<span data-ttu-id="5ecc9-113">Der Echt Zeit Stift bietet eine Möglichkeit, ein **inksammungsobjekt** zu erstellen, das Single Thread ist und im Thread der Anwendungs Benutzeroberfläche ansässig ist.</span><span class="sxs-lookup"><span data-stu-id="5ecc9-113">The real time stylus provides a way to create an **InkCollecting** object that is single-threaded and resident in the application UI thread.</span></span> <span data-ttu-id="5ecc9-114">Dieses **inksammatenobjekt** greift auf die Echt Zeit Stift Daten aus der Warteschlange zu.</span><span class="sxs-lookup"><span data-stu-id="5ecc9-114">This **InkCollecting** object accesses the real time stylus data from the queue.</span></span> <span data-ttu-id="5ecc9-115">Ein **InkCollection** -Objekt in Verbindung mit dem Echt Zeit Stift ermöglicht die echtzeitauswahl Bearbeitung und die Echtzeitbearbeitung der gesammelten frei Hand Daten.</span><span class="sxs-lookup"><span data-stu-id="5ecc9-115">An **InkCollecting** object in conjunction with real time stylus enables real-time selection editing and real-time editing of the collected ink data.</span></span> <span data-ttu-id="5ecc9-116">Weitere Informationen finden Sie unter [zugreifen auf und](accessing-and-manipulating-stylus-input.md)Bearbeiten von Tablettstifteingaben.</span><span class="sxs-lookup"><span data-stu-id="5ecc9-116">For more information, please see [Accessing and Manipulating Stylus Input](accessing-and-manipulating-stylus-input.md).</span></span>

<span data-ttu-id="5ecc9-117">Verwenden Sie das [**RealTimeStylus-Klassen**](realtimestylus-class.md) Objekt, um direkt mit dem tablettstiftdateistream zu interagieren oder Echt Zeit Eingaben zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="5ecc9-117">Use the [**RealTimeStylus Class**](realtimestylus-class.md) object to interact directly with the tablet stylus data stream or to block real-time inking.</span></span> <span data-ttu-id="5ecc9-118">Verwenden Sie das [**InkCollector-Klassen**](inkcollector-class.md) Objekt, das [**InkOverlay-Klassen**](inkoverlay-class.md) Objekt, das [InkPicture-Steuer](inkpicture-control-reference.md) Element Steuerelement oder das [InkEdit](inkedit-control-reference.md) -Steuerelement, wenn das Standardverhalten dieser Objekte das benötigte Verhalten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="5ecc9-118">Use the [**InkCollector Class**](inkcollector-class.md) object, [**InkOverlay Class**](inkoverlay-class.md) object, [InkPicture Control](inkpicture-control-reference.md) control, or [InkEdit Control](inkedit-control-reference.md) control when the default behavior of these objects provides the behavior you need.</span></span>

<span data-ttu-id="5ecc9-119">Die Echt Zeit Tablettstiftereignisse befinden sich in einem bestimmten Fenster Handle innerhalb eines bestimmten Fenster Eingabe Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="5ecc9-119">The real time stylus events are on a specific window handle within a specific window input rectangle.</span></span> <span data-ttu-id="5ecc9-120">Realtimestylusservice kann Tablettstiftdaten an mehrere [**RealTimeStylus-Klassen**](realtimestylus-class.md) Objekte senden.</span><span class="sxs-lookup"><span data-stu-id="5ecc9-120">The RealTimeStylusService can send stylus data to multiple [**RealTimeStylus Class**](realtimestylus-class.md) objects.</span></span> <span data-ttu-id="5ecc9-121">Jedes **RealTimeStylus-Klassen** Objekt empfängt Tablettstiftdaten für einen bestimmten Abschnitt eines Fensters, basierend auf der definierten [**irealtimestylus:: windowinputrechteck-Eigenschaft**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) für dieses **RealTimeStylus-Klassen** Objekt.</span><span class="sxs-lookup"><span data-stu-id="5ecc9-121">Each **RealTimeStylus Class** object receives stylus data for a specific section of a window based on the defined [**IRealTimeStylus::WindowInputRectangle Property**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) for that **RealTimeStylus Class** object.</span></span> <span data-ttu-id="5ecc9-122">Das **RealTimeStylus-Klassen** Objekt ruft die Tablettstiftdaten ab und verarbeitet diese dann über eine Liste synchroner und asynchroner Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="5ecc9-122">The **RealTimeStylus Class** object gets the stylus data and then processes this through a list of synchronous and asynchronous plug-ins.</span></span>

<span data-ttu-id="5ecc9-123">Der Unterschied zwischen den synchronen Plug-ins und den asynchronen Plug-ins liegt in dem Thread, in dem Sie ausgeführt werden, und der aufrufenden Sequenz.</span><span class="sxs-lookup"><span data-stu-id="5ecc9-123">The difference between the synchronous plug-ins and the asynchronous plug-ins lies in the thread in which they execute and the calling sequence.</span></span> <span data-ttu-id="5ecc9-124">Synchrone Plug-ins werden von dem Thread aufgerufen, in dem das [**RealTimeStylus-Klassen**](realtimestylus-class.md) Objekt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5ecc9-124">Synchronous plug-ins are called by the thread in which the [**RealTimeStylus Class**](realtimestylus-class.md) object executes.</span></span> <span data-ttu-id="5ecc9-125">Jedes Mal, wenn das **RealTimeStylus-Klassen** Objekt instanziiert wird, wird ein Ausführungs Thread instanziiert.</span><span class="sxs-lookup"><span data-stu-id="5ecc9-125">Every time **RealTimeStylus Class** object is instantiated, an execution thread is instantiated.</span></span> <span data-ttu-id="5ecc9-126">Synchrone Plug-ins werden für diesen neuen Thread ausgeführt, der für die Instanz des **RealTimeStylus-Klassen** Objekts instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="5ecc9-126">Synchronous plug-ins are executed on this new thread instantiated for the instance of the **RealTimeStylus Class** object.</span></span> <span data-ttu-id="5ecc9-127">Asynchrone Plug-ins werden über die Benutzeroberfläche oder den Anwendungs Thread aufgerufen, nachdem der Paketstream von den synchronen Plug-ins verarbeitet und in der Ausgabe Warteschlange gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="5ecc9-127">Asynchronous plug-ins are called through the UI or application thread after the packet stream has been processed by the synchronous plug-ins and stored in the output queue.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ecc9-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5ecc9-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ecc9-129">**Idynamicrenderer-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5ecc9-129">**IDynamicRenderer Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)
</dt> <dt>

[<span data-ttu-id="5ecc9-130">**IStylusSyncPlugin**</span><span class="sxs-lookup"><span data-stu-id="5ecc9-130">**IStylusSyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)
</dt> <dt>

[<span data-ttu-id="5ecc9-131">**IStylusAsyncPlugin**</span><span class="sxs-lookup"><span data-stu-id="5ecc9-131">**IStylusAsyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)
</dt> <dt>

[<span data-ttu-id="5ecc9-132">**Irealtimestylus**</span><span class="sxs-lookup"><span data-stu-id="5ecc9-132">**IRealTimeStylus**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)
</dt> </dl>

 

 
