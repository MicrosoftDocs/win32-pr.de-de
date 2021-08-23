---
description: WDM-Klassentreiberfilter
ms.assetid: 864fc5ad-5aeb-4dc7-bdd2-2ad2bfb57741
title: WDM-Klassentreiberfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd93db09c638ed7a8a217bec28a565086dcbfcae2b5702c9e1d07778c338646
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071894"
---
# <a name="wdm-class-driver-filters"></a>WDM-Klassentreiberfilter

Wenn ein Erfassungsgerät einen WDM-Treiber (Windows Driver Model) verwendet, erfordert das Diagramm möglicherweise bestimmte Filter, die dem Erfassungsfilter vorgelagert sind. Diese Filter werden als Streamklassentreiberfilter oder WDM-Filter bezeichnet. Sie unterstützen zusätzliche Funktionen, die von der Hardware bereitgestellt werden. Beispielsweise verfügt eine TV-Tunerkarte über Funktionen zum Festlegen des Kanals. Der entsprechende Filter ist der [TV-Tuner-Filter,](tv-tuner-filter.md) der die [**IAMTVTuner-Schnittstelle verfügbar**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) macht. Um diese Funktionalität für die Anwendung verfügbar zu machen, müssen Sie den TV-Tuner-Filter mit dem Erfassungsfilter verbinden.

Die [**ICaptureGraphBuilder2-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) bietet die einfachste Möglichkeit, WDM-Filter zum Diagramm hinzuzufügen. Rufen Sie zu einem bestimmten Zeitpunkt beim Erstellen des Diagramms [**FindInterface oder**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) [**RenderStream auf.**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) Eine dieser Methoden sucht automatisch nach den erforderlichen WDM-Filtern und verbindet sie mit dem Erfassungsfilter. Im restlichen Teil dieses Abschnitts wird beschrieben, wie WDM-Filter manuell hinzugefügt werden. Beachten Sie jedoch, dass der empfohlene Ansatz einfach das Aufrufen einer dieser **ICaptureGraphBuilder2-Methoden** ist.

Die Pins auf einem WDM-Filter unterstützen mindestens ein Medium. Ein Medium definiert eine Kommunikationsmethode, z. B. einen Bus. Sie müssen Pins verbinden, die dasselbe Medium unterstützen. Die [**REGPINMEDIUM-Struktur,**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) die der für Kernelstreamingtreiber verwendeten **KSPIN \_ MEDIUM-Struktur** entspricht, definiert ein Medium in DirectShow. Der **clsMedium-Member** der **REGPINMEDIUM-Struktur** gibt den Klassenbezeichner (CLSID) für das Medium an. Um das Medium eines Pins abzurufen, rufen Sie die [**IKsPin::KsQueryMediums-Methode**](ikspin-ksquerymediums.md) auf. Diese Methode gibt einen Zeiger auf einen Speicherblock zurück, der eine [**KSMULTIPLE \_ ITEM-Struktur**](ksmultiple-item.md) enthält, gefolgt von null oder mehr **REGPINMEDIUM-Strukturen.** Jede **REGPINMEDIUM-Struktur** identifiziert ein Medium, das vom Pin unterstützt wird.

Verbinden Sie einen Pin nicht, wenn das Medium über eine CLSID von GUID \_ NULL oder KSMEDIUMSETID \_ Standard verfügt. Dies sind Standardwerte, die angeben, dass die Stecknadel keine Medien unterstützt.

Verbinden Sie außerdem nur dann eine Stecknadel, wenn der Filter genau eine verbundene Instanz dieses Pins erfordert. Andernfalls versucht Ihre Anwendung möglicherweise, verschiedene Stecknadeln zu verbinden, die keine Verbindungen haben sollten, was dazu führen kann, dass das Programm nicht mehr reagiert. Um die Anzahl der erforderlichen Instanzen zu finden, rufen Sie den KSPROPERTY \_ PIN \_ NECESSARYINSTANCES-Eigenschaftensatz ab, wie im folgenden Codebeispiel gezeigt. (Aus Kürze werden in diesem Beispiel keine Rückgabecodes oder Schnittstellen veröffentlicht. Ihre Anwendung sollte natürlich beides tun.)


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



Der folgende Pseudocode ist eine äußerst kurze Gliederung, die zeigt, wie sie die WDM-Filter finden und verbinden. Es werden viele Details ausgelassen, und es sollen nur die allgemeinen Schritte gezeigt werden, die Ihre Anwendung ausführen müsste.


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

[Erweiterte Erfassungsthemen](advanced-capture-topics.md)
</dt> </dl>

 

 



