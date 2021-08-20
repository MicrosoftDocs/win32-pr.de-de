---
description: Schnittstellen zum Steuern eines Filter-Graph
ms.assetid: f7de0165-e356-45d5-baed-d127caeebaf6
title: Schnittstellen zum Steuern eines Filter-Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8170b8d2da80272a5620abe163f938e53105cc5b471593a3799d4c36069fe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154091"
---
# <a name="interfaces-for-controlling-a-filter-graph"></a>Schnittstellen zum Steuern eines Filter-Graph

Diese Schnittstellen stellen Methoden zum Steuern eines Filterdiagramms bereit.



| Schnittstelle                                  | BESCHREIBUNG                                                                                               |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust)   | Passen Sie die Graphuhr an.                                                                                   |
| [**IAMGraphStreams**](/windows/desktop/api/Strmif/nn-strmif-iamgraphstreams) | Synchronisieren von Livestreams in einem Filterdiagramm.                                                               |
| [**IFilterChain**](/windows/desktop/api/Strmif/nn-strmif-ifilterchain)       | Steuerketten von Filtern.                                                                                |
| [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)     | Führen Sie das Filterdiagramm aus, halten Sie es an, und beenden Sie es. (Stellt auch automatisierungskompatible Methoden zum Erstellen von Diagrammen bereit.) |
| [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex)     | Reagieren auf Ereignisse im Diagramm.                                                                           |
| [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)     | Suchen innerhalb einer Datei.                                                                                       |
| [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand)     | Warteschlangenbefehle, die zu einem späteren Zeitpunkt ausgeführt werden sollen.                                                                    |
| [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) | Einzelschritt durch einen Videostream.                                                                        |



 

 

 



