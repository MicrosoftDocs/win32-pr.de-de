---
description: Allgemeine Graph-Building Techniken
ms.assetid: 66d93305-175c-4549-b825-2f3d7fd6bf09
title: Allgemeine Graph-Building Techniken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c73a005f1fbf7af0a53f11d44d600852f88752
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213825"
---
# <a name="general-graph-building-techniques"></a>Allgemeine Graph-Building Techniken

Alle DirectShow-Anwendungen beginnen mit dem Aufbau eines Filter Diagramms. Wenn Sie die Übersichts Themen in der DirectShow-Dokumentation lesen, werden Sie zunächst feststellen, welche Art von Filter Diagramm Sie benötigen. In einigen Fällen gibt es eine Methode oder ein Hilfsobjekt, das speziell zum entwickeln dieses Diagramm Typs entworfen wurde. Beispielsweise erstellt das [DVD Graph Builder](dvd-graph-builder.md) -Objekt DVD-Wiedergabe Diagramme. In anderen Fällen muss die Anwendung das Diagramm erstellen, indem Sie Filter hinzufügen und Sie miteinander verbinden.

In diesem Abschnitt werden einige Hilfsfunktionen vorgestellt, die grundlegende Graph-Building-Vorgänge implementieren. Sie können von jeder DirectShow-Anwendung verwendet werden, die ein Filter Diagramm erstellen oder ändern muss. Dieser Abschnitt enthält die folgenden Themen:

-   [Filter nach CLSID hinzufügen](add-a-filter-by-clsid.md)
-   [Suchen einer nicht verbundenen PIN für einen Filter](find-an-unconnected-pin-on-a-filter.md)
-   [Zwei Filter verbinden](connect-two-filters.md)
-   [Suchen einer Schnittstelle in einem Filter oder einer PIN](find-an-interface-on-a-filter-or-pin.md)
-   [Suchen eines Filter-Peers](find-a-filters-peer.md)
-   [Alle Filter im Diagramm entfernen](remove-all-the-filters-in-the-graph.md)
-   [Erstellen von Diagrammen mit dem Erfassungs Diagramm-Generator](building-graphs-with-the-capture-graph-builder.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegende DirectShow-Aufgaben](basic-directshow-tasks.md)
</dt> <dt>

[Auflisten von Geräten und Filtern](enumerating-devices-and-filters.md)
</dt> <dt>

[Auflisten von Objekten in einem Filter Diagramm](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[Intelligent Connect](intelligent-connect.md)
</dt> </dl>

 

 



