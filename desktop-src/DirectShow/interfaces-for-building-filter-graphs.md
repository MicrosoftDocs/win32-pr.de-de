---
description: Schnittstellen zum Erstellen von Filterdiagrammen
ms.assetid: 18d5217a-7f4e-49e9-ac14-2f4ba229e065
title: Schnittstellen zum Erstellen von Filterdiagrammen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ca539672f39e855d891a5a3c534a8ac3cfcec35bb933034bad2621fa5339d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154128"
---
# <a name="interfaces-for-building-filter-graphs"></a>Schnittstellen zum Erstellen von Filterdiagrammen

Anwendungen verwenden diese Schnittstellen, um verschiedene Arten von Filterdiagrammen zu erstellen.



| Schnittstelle                                                  | BESCHREIBUNG                                                 |
|------------------------------------------------------------|-------------------------------------------------------------|
| [**IAMFilterGraphCallback**](/windows/desktop/api/Strmif/nn-strmif-iamfiltergraphcallback)   | Empfangen sie Rückrufbenachrichtigungen, wenn eine Stecknadel nicht gerendert werden kann. |
| [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) | Stellt einen Rückrufmechanismus während der Graphen-Entwicklung dar.        |
| [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)     | Erstellen Sie Filterdiagramme für die Videoaufnahme.                      |
| [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum)                   | Aufzählen von Systemgeräten, z. B. Erfassungsgeräten          |
| [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder)               | Erstellen Sie Filterdiagramme für die DVD-Navigation und -Wiedergabe.        |
| [**IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters)                       | Enumerieren Sie die Filter im Diagramm.                         |
| [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)                     | Hinzufügen, Entfernen oder Verbinden von Filtern.                            |
| [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)                   | Listet die im System des Benutzers registrierten Filter auf.      |
| [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)                     | Erstellen Sie Filterdiagramme für die Dateiwiedergabe oder für benutzerdefinierte Zwecke.   |
| [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)                       | Dynamisches Neukonfigurieren eines Filterdiagramms.                     |
| [**IGraphVersion**](/windows/desktop/api/Strmif/nn-strmif-igraphversion)                     | Bestimmen Sie, wann sich das Diagramm ändert.                           |



 

 

 



