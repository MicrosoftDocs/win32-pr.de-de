---
description: Filtern Graph-Managers
ms.assetid: b1a53193-27c6-4e86-a5b9-f3c1e4401690
title: Filtern Graph-Managers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 793a261f0d7bd12058aa0dc22a448f567fea6847dca6062494f0943eee03a9b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756720"
---
# <a name="filter-graph-manager"></a>Filtern Graph-Managers

Filter Graph Manager erstellt und steuert Filterdiagramme. Dieses Objekt ist die zentrale Komponente in DirectShow. Anwendungen verwenden es zum Erstellen und Steuern von Filterdiagrammen. Der Filter Graph Manager verarbeitet auch die Synchronisierung, Ereignisbenachrichtigungen und andere Aspekte der Steuerung des Filterdiagramms. Erstellen Sie dieses Objekt, indem **Sie CoCreateInstance** aufrufen.

### <a name="clsid"></a>CLSID

Es gibt zwei CLSIDs zum Erstellen des Filter-Graph-Managers:



| CLSID                      | Beschreibung                                                 |
|----------------------------|-------------------------------------------------------------|
| CLSID \_ FilterGraph         | Erstellt den Filter Graph Manager für einen freigegebenen Arbeitsthread. |
| \_CLSID-FilterGraphNoThread | Erstellt den Filter Graph Manager im Anwendungsthread. |



 

Im Allgemeinen sollten Anwendungen CLSID \_ FilterGraph verwenden. Beide CLSIDs erstellen das gleiche Objekt, verwenden aber unterschiedliche Threadingmodelle:

-   CLSID \_ FilterGraph erstellt den Filter Graph Manager in einem Arbeitsthread, der von allen CLSID \_ FilterGraph-Instanzen innerhalb desselben Prozesses gemeinsam genutzt wird. Der Thread sendet Nachrichten, die von Filtern gesendet werden, und steuert die Lebensdauer von Fenstern, die von Filtern erstellt werden.
-   CLSID \_ FilterGraphNoThread erstellt den Filter Graph Manager im Thread der Anwendung. Wenn Sie diese CLSID verwenden, muss der Thread, der **CoCreateInstance aufruft,** über eine Nachrichtenschleife verfügen, die Nachrichten verteilt. Andernfalls können Deadlocks auftreten. Außerdem muss vor dem Beenden des Anwendungsthreads der Filter Graph Manager und alle Graphobjekte (z. B. Filter, Stecknadeln, Referenzuhren usw.) veröffentlicht werden.

### <a name="interfaces"></a>Schnittstellen

Der Filter Graph Manager macht die folgenden Schnittstellen verfügbar:

-   [**IAMGraphStreams**](/windows/desktop/api/Strmif/nn-strmif-iamgraphstreams)
-   [**IAMStats**](/windows/desktop/api/Control/nn-control-iamstats)
-   [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio)
-   [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo)
-   [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2)
-   [**IFilterChain**](/windows/desktop/api/Strmif/nn-strmif-ifilterchain)
-   [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph)
-   [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)
-   [**IFilterGraph3**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph3)
-   [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)
-   [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)
-   [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)
-   [**IGraphVersion**](/windows/desktop/api/Strmif/nn-strmif-igraphversion)
-   [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)
-   [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent)
-   [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex)
-   [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)
-   [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter)
-   [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)
-   [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)
-   [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand)
-   [**IRegisterServiceProvider**](/windows/desktop/api/Strmif/nn-strmif-iregisterserviceprovider)
-   [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager)
-   **IServiceProvider**
-   [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep)
-   [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Objekte](directshow-objects.md)
</dt> </dl>

 

 



