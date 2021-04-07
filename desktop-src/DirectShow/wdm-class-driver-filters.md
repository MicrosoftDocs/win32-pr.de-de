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
# <a name="wdm-class-driver-filters"></a>WDM-Klassen Treiber Filter

Wenn ein Erfassungsgerät einen Windows-Treibermodell (WDM)-Treiber verwendet, erfordert das Diagramm möglicherweise bestimmte Filter Upstream aus dem Erfassungs Filter. Diese Filter werden als streamklassentreiberfilter oder WDM-Filter bezeichnet. Sie unterstützen zusätzliche Funktionen, die von der Hardware bereitgestellt werden. Beispielsweise verfügt eine TV-Tuner-Karte über Funktionen zum Festlegen des Kanals. Der entsprechende Filter ist der [TV-Tuner-](tv-tuner-filter.md) Filter, der die [**iamtvtuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) -Schnittstelle verfügbar macht. Um diese Funktionalität für die Anwendung verfügbar zu machen, müssen Sie den TV-Tuner-Filter mit dem Erfassungs Filter verbinden.

Die [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) -Schnittstelle bietet die einfachste Möglichkeit, dem Diagramm WDM-Filter hinzuzufügen. Wenn Sie das Diagramm zu einem bestimmten Zeitpunkt aufbauen, müssen Sie [**findinterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) oder [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)aufzurufen. Bei einer der beiden Methoden werden automatisch die erforderlichen WDM-Filter gesucht und mit dem Erfassungs Filter verbunden. Im restlichen Teil dieses Abschnitts wird beschrieben, wie WDM-Filter manuell hinzugefügt werden. Beachten Sie jedoch, dass die empfohlene Vorgehensweise einfach ist, eine dieser **ICaptureGraphBuilder2** -Methoden aufzurufen.

Die Pins eines WDM-Filters unterstützen mindestens ein Medium. Ein Medium definiert eine Kommunikationsmethode, z. b. einen Bus. Sie müssen eine Verbindung mit Pins herstellen, die das gleiche Medium unterstützen. Die [**regpinmedium**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) -Struktur, die der für Kernel Streaming-Treiber verwendeten **kspin- \_ Mittel** Struktur entspricht, definiert ein Medium in DirectShow. Der **clsmedium** -Member der **regpinmedium** -Struktur gibt den Klassen Bezeichner (CLSID) für das Medium an. Um das Mittel der PIN abzurufen, rufen Sie die Methode " [**ikspin:: ksquerymediums**](ikspin-ksquerymediums.md) " auf. Diese Methode gibt einen Zeiger auf einen Speicherblock zurück, der eine [**ksmultiple- \_ Element**](ksmultiple-item.md) Struktur, gefolgt von NULL oder mehr **regpinmedium** -Strukturen enthält. Jede **regpinmedium** -Struktur identifiziert ein Medium, das von der PIN unterstützt wird.

Verbinden Sie eine PIN nicht, wenn das Medium eine CLSID mit der GUID \_ null oder dem ksmediumgtid- \_ Standard aufweist. Dies sind die Standardwerte, die angeben, dass die PIN keine Medien unterstützt.

Verbinden Sie außerdem keine PIN, es sei denn, der Filter erfordert genau eine verbundene Instanz dieser Pin. Andernfalls versucht die Anwendung möglicherweise, verschiedene Pins zu verbinden, die keine Verbindungen aufweisen dürfen, was dazu führen kann, dass das Programm nicht mehr reagiert. Um die Anzahl der erforderlichen Instanzen zu ermitteln, rufen Sie die Eigenschaft ksproperty \_ Pin \_ requiaryinstance ab, wie im folgenden Codebeispiel gezeigt. (Aus Gründen der Kürze werden in diesem Beispiel keine Rückgabecodes getestet, oder es werden keine Schnittstellen freigegeben. Ihre Anwendung sollte natürlich beides tun.)


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



Der folgende Pseudo Code ist eine sehr kurze Gliederung, die zeigt, wie Sie die WDM-Filter suchen und verbinden können. Es lässt viele Details aus und soll lediglich die allgemeinen Schritte anzeigen, die Ihre Anwendung durchführen muss.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterte Erfassungs Themen](advanced-capture-topics.md)
</dt> </dl>

 

 



