---
description: Schnittstellen zum Entwickeln von Filter Diagrammen
ms.assetid: 18d5217a-7f4e-49e9-ac14-2f4ba229e065
title: Schnittstellen zum Entwickeln von Filter Diagrammen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862d581f44a711cc6f2aa094210571995b15005b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746009"
---
# <a name="interfaces-for-building-filter-graphs"></a>Schnittstellen zum Entwickeln von Filter Diagrammen

Anwendungen verwenden diese Schnittstellen, um verschiedene Arten von Filter Diagrammen zu erstellen.



| Schnittstelle                                                  | BESCHREIBUNG                                                 |
|------------------------------------------------------------|-------------------------------------------------------------|
| [**Iamfiltergraphcallback**](/windows/desktop/api/Strmif/nn-strmif-iamfiltergraphcallback)   | Empfangen von Rückruf Benachrichtigungen, wenn eine PIN nicht gerendert werden kann. |
| [**Iamgraphbuildercallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) | Stellt während der Diagramm Bildung einen Rückrufmechanismus bereit.        |
| [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)     | Buildfilterdiagramme für die Video Erfassung.                      |
| [**Ikreatedevenum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum)                   | Auflisten von System Geräten, z. b. Geräte Erfassung          |
| [**Idvdgraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder)               | Buildfilterdiagramme für DVD-Navigation und-Wiedergabe.        |
| [**Ienumfilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters)                       | Listet die Filter im Diagramm auf.                         |
| [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)                     | Hinzufügen, entfernen oder Verbinden von Filtern.                            |
| [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)                   | Listet die auf dem System des Benutzers registrierten Filter auf.      |
| [**Igraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)                     | Buildfilterdiagramme für die Dateiwiedergabe oder für benutzerdefinierte Verwendungen.   |
| [**Igraphconfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)                       | Dynamisches Neukonfigurieren eines Filter Diagramms.                     |
| [**Igraphversion**](/windows/desktop/api/Strmif/nn-strmif-igraphversion)                     | Bestimmen Sie, wann das Diagramm geändert wird.                           |



 

 

 



