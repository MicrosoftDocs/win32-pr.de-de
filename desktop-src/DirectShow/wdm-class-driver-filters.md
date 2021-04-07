---
description: WDM-Klassen Treiber Filter
ms.assetid: 864fc5ad-5aeb-4dc7-bdd2-2ad2bfb57741
title: WDM-Klassen Treiber Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338e4ec4d2aaa58bdac737b58571497cad708876
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863395"
---
# <a name="wdm-class-driver-filters"></a><span data-ttu-id="3e846-103">WDM-Klassen Treiber Filter</span><span class="sxs-lookup"><span data-stu-id="3e846-103">WDM Class Driver Filters</span></span>

<span data-ttu-id="3e846-104">Wenn ein Erfassungsgerät einen Windows-Treibermodell (WDM)-Treiber verwendet, erfordert das Diagramm möglicherweise bestimmte Filter Upstream aus dem Erfassungs Filter.</span><span class="sxs-lookup"><span data-stu-id="3e846-104">If a capture device uses a Windows Driver Model (WDM) driver, the graph might require certain filters upstream from the capture filter.</span></span> <span data-ttu-id="3e846-105">Diese Filter werden als streamklassentreiberfilter oder WDM-Filter bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3e846-105">These filters are called stream-class driver filters or WDM filters.</span></span> <span data-ttu-id="3e846-106">Sie unterstützen zusätzliche Funktionen, die von der Hardware bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3e846-106">They support additional functionality provided by the hardware.</span></span> <span data-ttu-id="3e846-107">Beispielsweise verfügt eine TV-Tuner-Karte über Funktionen zum Festlegen des Kanals.</span><span class="sxs-lookup"><span data-stu-id="3e846-107">For example, a TV tuner card has functions for setting the channel.</span></span> <span data-ttu-id="3e846-108">Der entsprechende Filter ist der [TV-Tuner-](tv-tuner-filter.md) Filter, der die [**iamtvtuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="3e846-108">The corresponding filter is the [TV Tuner](tv-tuner-filter.md) filter, which exposes the [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) interface.</span></span> <span data-ttu-id="3e846-109">Um diese Funktionalität für die Anwendung verfügbar zu machen, müssen Sie den TV-Tuner-Filter mit dem Erfassungs Filter verbinden.</span><span class="sxs-lookup"><span data-stu-id="3e846-109">To make this functionality available to the application, you must connect the TV Tuner filter to the capture filter.</span></span>

<span data-ttu-id="3e846-110">Die [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) -Schnittstelle bietet die einfachste Möglichkeit, dem Diagramm WDM-Filter hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="3e846-110">The [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface provides the easiest way to add WDM filters to the graph.</span></span> <span data-ttu-id="3e846-111">Wenn Sie das Diagramm zu einem bestimmten Zeitpunkt aufbauen, müssen Sie [**findinterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) oder [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="3e846-111">At some point while building the graph, call [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) or [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).</span></span> <span data-ttu-id="3e846-112">Bei einer der beiden Methoden werden automatisch die erforderlichen WDM-Filter gesucht und mit dem Erfassungs Filter verbunden.</span><span class="sxs-lookup"><span data-stu-id="3e846-112">Either one of these methods will automatically locate the necessary WDM filters and connect them to the capture filter.</span></span> <span data-ttu-id="3e846-113">Im restlichen Teil dieses Abschnitts wird beschrieben, wie WDM-Filter manuell hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="3e846-113">The rest of this section describes how to add WDM filters manually.</span></span> <span data-ttu-id="3e846-114">Beachten Sie jedoch, dass die empfohlene Vorgehensweise einfach ist, eine dieser **ICaptureGraphBuilder2** -Methoden aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="3e846-114">However, be aware that the recommend approach is simply to call one of these **ICaptureGraphBuilder2** methods.</span></span>

<span data-ttu-id="3e846-115">Die Pins eines WDM-Filters unterstützen mindestens ein Medium.</span><span class="sxs-lookup"><span data-stu-id="3e846-115">The pins on a WDM filter support one or more mediums.</span></span> <span data-ttu-id="3e846-116">Ein Medium definiert eine Kommunikationsmethode, z. b. einen Bus.</span><span class="sxs-lookup"><span data-stu-id="3e846-116">A medium defines a method of communication, such as a bus.</span></span> <span data-ttu-id="3e846-117">Sie müssen eine Verbindung mit Pins herstellen, die das gleiche Medium unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3e846-117">You must connect pins that support the same medium.</span></span> <span data-ttu-id="3e846-118">Die [**regpinmedium**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) -Struktur, die der für Kernel Streaming-Treiber verwendeten **kspin- \_ Mittel** Struktur entspricht, definiert ein Medium in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="3e846-118">The [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) structure, which is equivalent to the **KSPIN\_MEDIUM** structure used for kernel streaming drivers, defines a medium in DirectShow.</span></span> <span data-ttu-id="3e846-119">Der **clsmedium** -Member der **regpinmedium** -Struktur gibt den Klassen Bezeichner (CLSID) für das Medium an.</span><span class="sxs-lookup"><span data-stu-id="3e846-119">The **clsMedium** member of the **REGPINMEDIUM** structure specifies the class identifier (CLSID) for the medium.</span></span> <span data-ttu-id="3e846-120">Um das Mittel der PIN abzurufen, rufen Sie die Methode " [**ikspin:: ksquerymediums**](ikspin-ksquerymediums.md) " auf.</span><span class="sxs-lookup"><span data-stu-id="3e846-120">To retrieve a pin's medium, call the [**IKsPin::KsQueryMediums**](ikspin-ksquerymediums.md) method.</span></span> <span data-ttu-id="3e846-121">Diese Methode gibt einen Zeiger auf einen Speicherblock zurück, der eine [**ksmultiple- \_ Element**](ksmultiple-item.md) Struktur, gefolgt von NULL oder mehr **regpinmedium** -Strukturen enthält.</span><span class="sxs-lookup"><span data-stu-id="3e846-121">This method returns a pointer to a block of memory that contains a [**KSMULTIPLE\_ITEM**](ksmultiple-item.md) structure, followed by zero or more **REGPINMEDIUM** structures.</span></span> <span data-ttu-id="3e846-122">Jede **regpinmedium** -Struktur identifiziert ein Medium, das von der PIN unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="3e846-122">Each **REGPINMEDIUM** structure identifies a medium the pin supports.</span></span>

<span data-ttu-id="3e846-123">Verbinden Sie eine PIN nicht, wenn das Medium eine CLSID mit der GUID \_ null oder dem ksmediumgtid- \_ Standard aufweist.</span><span class="sxs-lookup"><span data-stu-id="3e846-123">Do not connect a pin if the medium has a CLSID of GUID\_NULL or KSMEDIUMSETID\_Standard.</span></span> <span data-ttu-id="3e846-124">Dies sind die Standardwerte, die angeben, dass die PIN keine Medien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3e846-124">These are default values indicating that the pin does not support mediums.</span></span>

<span data-ttu-id="3e846-125">Verbinden Sie außerdem keine PIN, es sei denn, der Filter erfordert genau eine verbundene Instanz dieser Pin.</span><span class="sxs-lookup"><span data-stu-id="3e846-125">Also, do not connect a pin unless the filter requires exactly one connected instance of that pin.</span></span> <span data-ttu-id="3e846-126">Andernfalls versucht die Anwendung möglicherweise, verschiedene Pins zu verbinden, die keine Verbindungen aufweisen dürfen, was dazu führen kann, dass das Programm nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="3e846-126">Otherwise, your application might try to connect various pins that shouldn't have connections, which can cause the program to stop responding.</span></span> <span data-ttu-id="3e846-127">Um die Anzahl der erforderlichen Instanzen zu ermitteln, rufen Sie die Eigenschaft ksproperty \_ Pin \_ requiaryinstance ab, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="3e846-127">To find out the number of required instances, retrieve the KSPROPERTY\_PIN\_NECESSARYINSTANCES property set, as shown in the following code example.</span></span> <span data-ttu-id="3e846-128">(Aus Gründen der Kürze werden in diesem Beispiel keine Rückgabecodes getestet, oder es werden keine Schnittstellen freigegeben.</span><span class="sxs-lookup"><span data-stu-id="3e846-128">(For brevity, this example does not test any return codes or release any interfaces.</span></span> <span data-ttu-id="3e846-129">Ihre Anwendung sollte natürlich beides tun.)</span><span class="sxs-lookup"><span data-stu-id="3e846-129">Your application should do both, of course.)</span></span>


```C++
// Obtain the pin factory identifier.
IKsPinFactory *pPinFactory;
hr = pPin->QueryInterface(IID_IKsPinFactory, (void **)&pPinFactory);

ULONG ulFactoryId;
hr = pPinFactory->KsPinFactory(&ulFactoryId);

// Get the "instance" property from the filter.
IKsControl *pKsControl;
hr = pFilter->QueryInterface(IID_IKsControl, (void **)&pKsControl);

KSP_PIN ksPin;
ksPin.Property.Set = KSPROPSETID_Pin;
ksPin.Property.Id = KSPROPERTY_PIN_NECESSARYINSTANCES;
ksPin.Property.Flags = KSPROPERTY_TYPE_GET;
ksPin.PinId = ulFactoryId;
ksPin.Reserved = 0; 

KSPROPERTY ksProp;
ULONG ulInstances, bytes;
pKsControl->KsProperty((PKSPROPERTY)&ksPin, sizeof(ksPin), 
    &ulInstances, sizeof(ULONG), &bytes);

if (hr == S_OK && bytes == sizeof(ULONG)) 
{
    if (ulInstances == 1) 
    {
        // Filter requires one instance of this pin.
        // This pin is OK.
    } 
}
```



<span data-ttu-id="3e846-130">Der folgende Pseudo Code ist eine sehr kurze Gliederung, die zeigt, wie Sie die WDM-Filter suchen und verbinden können.</span><span class="sxs-lookup"><span data-stu-id="3e846-130">The following pseudocode is an extremely brief outline showing how to find and connect the WDM filters.</span></span> <span data-ttu-id="3e846-131">Es lässt viele Details aus und soll lediglich die allgemeinen Schritte anzeigen, die Ihre Anwendung durchführen muss.</span><span class="sxs-lookup"><span data-stu-id="3e846-131">It omits many details, and is only meant to show the general steps your application would need to take.</span></span>


```C++
Add supporting filters:
{
    foreach input pin:
        skip if (pin is connected)
    
        Get pin medium
        skip if (medium is GUID_NULL or KSMEDIUMSETID_Standard)
    
        Query filter for KSPROPERTY_PIN_NECESSARYINSTANCES property
        skip if (necessary instances != 1)

        Match an existing pin || Find a matching filter
}    

Match an existing pin:
{
    foreach filter in the graph
        foreach unconnected pin
            Get pin medium
            if (mediums match)
                connect the pins    
}

Find a matching filter:
{    
    Query the filter graph manager for IFilterMapper2.
    Find a filter with an output pin that matches the medium.
    Add the filter to the graph.
    Connect the pins.
    Add supporting filters. (Recursive call.)
}
```



## <a name="related-topics"></a><span data-ttu-id="3e846-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3e846-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e846-133">Erweiterte Erfassungs Themen</span><span class="sxs-lookup"><span data-stu-id="3e846-133">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> </dl>

 

 



