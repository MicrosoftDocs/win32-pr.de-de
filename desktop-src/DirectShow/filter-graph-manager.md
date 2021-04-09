---
description: Diagramm-Manager Filtern
ms.assetid: b1a53193-27c6-4e86-a5b9-f3c1e4401690
title: Diagramm-Manager Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7161f15ea04e1404425d4671ca7991420e0aa993
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860003"
---
# <a name="filter-graph-manager"></a>Diagramm-Manager Filtern

Der Filter Graph-Manager erstellt und steuert Filter Diagramme. Dieses Objekt ist die zentrale Komponente in DirectShow. Anwendungen verwenden Sie, um Filter Diagramme zu erstellen und zu steuern. Der Filter Graph-Manager behandelt auch die Synchronisierung, Ereignis Benachrichtigung und andere Aspekte der Steuerung des Filter Diagramms. Erstellen Sie dieses Objekt durch Aufrufen von **CoCreateInstance**.

### <a name="clsid"></a>CLSID

Es gibt zwei CLSIDs zum Erstellen des Filter Graph-Managers:



| CLSID                      | BESCHREIBUNG                                                 |
|----------------------------|-------------------------------------------------------------|
| CLSID- \_ Filtergraph         | Erstellt den Filter Graph-Manager in einem freigegebenen Arbeits Thread. |
| CLSID- \_ filtergraphnothread | Erstellt den Filter Graph-Manager im Anwendungs Thread. |



 

Im Allgemeinen sollten Anwendungen CLSID \_ Filtergraph verwenden. Beide CLSIDs erstellen dasselbe Objekt, verwenden jedoch verschiedene Threading Modelle:

-   CLSID \_ Filtergraph erstellt den Filter Graph-Manager in einem Arbeits Thread, der von allen CLSID- \_ Filtergraph-Instanzen innerhalb desselben Prozesses gemeinsam genutzt wird. Der Thread sendet Nachrichten, die von Filtern gesendet werden, und steuert die Lebensdauer von Fenstern, die durch Filter erstellt wurden.
-   CLSID \_ filtergraphnothread erstellt den Filter Graph-Manager im Anwendungs Thread. Wenn Sie diese CLSID verwenden, muss der Thread, der **cokreateinstance** aufruft, eine Nachrichten Schleife aufweisen, die Nachrichten sendet. Andernfalls können Deadlocks auftreten. Bevor der Anwendungs Thread beendet wird, muss er außerdem den Filter Graph-Manager und alle Graph-Objekte (z. b. Filter, Pins, Referenzuhren usw.) freigeben.

### <a name="interfaces"></a>Schnittstellen

Der Filter Graph-Manager macht die folgenden Schnittstellen verfügbar:

-   [**Iamgraphstreams**](/windows/desktop/api/Strmif/nn-strmif-iamgraphstreams)
-   [**Iamstats**](/windows/desktop/api/Control/nn-control-iamstats)
-   [**Ibasicaudiodatei**](/windows/desktop/api/Control/nn-control-ibasicaudio)
-   [**Ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo)
-   [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2)
-   [**Ifilterchain**](/windows/desktop/api/Strmif/nn-strmif-ifilterchain)
-   [**Ifiltergraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph)
-   [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)
-   [**IFilterGraph3**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph3)
-   [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)
-   [**Igraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)
-   [**Igraphconfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)
-   [**Igraphversion**](/windows/desktop/api/Strmif/nn-strmif-igraphversion)
-   [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)
-   [**Imediaevent**](/windows/desktop/api/Control/nn-control-imediaevent)
-   [**Imediaeventex**](/windows/desktop/api/Control/nn-control-imediaeventex)
-   [**Imediaeventsink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)
-   [**Imediafilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter)
-   [**Imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition)
-   [**Imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)
-   [**Iqueuecommand**](/windows/desktop/api/Control/nn-control-iqueuecommand)
-   [**Iregisterserviceprovider**](/windows/desktop/api/Strmif/nn-strmif-iregisterserviceprovider)
-   [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager)
-   **IServiceProvider**
-   [**Ivideoframestep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep)
-   [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Objekte](directshow-objects.md)
</dt> </dl>

 

 



