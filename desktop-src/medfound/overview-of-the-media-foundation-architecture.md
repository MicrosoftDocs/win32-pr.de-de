---
description: In diesem Thema wird der allgemeine Entwurf von Microsoft Media Foundation. Informationen zur Verwendung von Media Foundation für bestimmte Programmieraufgaben finden Sie im Media Foundation-Programmierhandbuch.
ms.assetid: DEA2B19A-CF15-4BF4-84C3-9A6417C942E2
title: Übersicht über die Media Foundation Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de953d05c55c96d1affa2213e1a7f11143a71aa319b4671c159f085e65268d05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118239631"
---
# <a name="overview-of-the-media-foundation-architecture"></a>Übersicht über die Media Foundation Architektur

In diesem Thema wird der allgemeine Entwurf von Microsoft Media Foundation. Informationen zur Verwendung von Media Foundation für bestimmte Programmieraufgaben finden Sie im [Media Foundation-Programmierhandbuch.](media-foundation-programming-guide.md)

Das folgende Diagramm zeigt eine übersichtsbasierte Ansicht der Media Foundation Architektur.

![Diagramm, das eine übersichtsbasierte Ansicht der Media Foundation-Architektur zeigt.](images/mfarch01.png)

Media Foundation bietet zwei unterschiedliche Programmiermodelle. Das erste Modell, das auf der linken Seite des Diagramms angezeigt wird, verwendet eine End-to-End-Pipeline für Mediendaten. Die Anwendung initialisiert die Pipeline , z. B. durch Angabe der URL einer datei, die abspielt werden soll, und ruft dann Methoden zum Steuern des Streamings auf. Im zweiten Modell, das auf der rechten Seite des Diagramms angezeigt wird, pullt die Anwendung Daten entweder aus einer Quelle oder pusht sie an ein Ziel (oder beides). Dieses Modell ist besonders nützlich, wenn Sie die Daten verarbeiten müssen, da die Anwendung direkten Zugriff auf den Datenstrom hat.

### <a name="primitives-and-platform"></a>Primitive und Plattform

Ab dem unteren Rand des *Diagramms* sind die Primitive Hilfsobjekte, die in der gesamten Media Foundation werden:

-   [Attribute sind](attributes-and-properties.md) eine allgemeine Möglichkeit, Informationen in einem Objekt als Liste von Schlüssel-Wert-Paaren zu speichern.
-   [Medientypen](media-types.md) beschreiben das Format eines Mediendatenstroms.
-   [Medienpuffer enthalten](media-buffers.md) Mediendaten, z. B. Videoframes und Audiobeispiele, und werden zum Transport von Daten zwischen Objekten verwendet.
-   [Medienbeispiele](media-samples.md) sind Container für Medienpuffer. Sie enthalten auch Metadaten zu den Puffern, z. B. Zeitstempel.

Die [Media Foundation-Plattform-APIs](media-foundation-platform-apis.md) bieten einige Kernfunktionen, die von der Media Foundation-Pipeline verwendet werden, z. B. asynchrone Rückrufe und Arbeitswarteschlangen. Bestimmte Anwendungen müssen diese APIs möglicherweise direkt aufrufen. Außerdem benötigen Sie sie, wenn Sie eine benutzerdefinierte Quelle, Transformation oder Senke für die Media Foundation.

### <a name="media-pipeline"></a>Medienpipeline

Die Medienpipeline enthält drei Objekttypen, die Mediendaten generieren oder verarbeiten:

-   [Medienquellen](media-sources.md) führen Daten in die Pipeline ein. Eine Medienquelle kann Daten aus einer lokalen Datei, z. B. einer Videodatei, erhalten. aus einem Netzwerkstream; oder von einem Hardwareerfassungsgerät.
-   [Media Foundation Transforms](media-foundation-transforms.md) (MFTs) verarbeiten Daten aus einem Stream. Encoder und Decoder werden als MFTs implementiert.
-   [Mediensenken](media-sinks.md) nutzen die Daten. z. B. durch Anzeigen von Video auf der Anzeige, Wiederwiedergabe von Audio oder Schreiben der Daten in eine Mediendatei.

Drittanbieter können ihre eigenen benutzerdefinierten Quellen, Senken und MFTs implementieren. z. B. zur Unterstützung neuer Mediendateiformate.

Die [Mediensitzung](media-session.md) steuert den Datenfluss durch die Pipeline und verarbeitet Aufgaben wie Qualitätskontrolle, Audio-/Videosynchronisierung und Reaktion auf Formatänderungen.

### <a name="source-reader-and-sink-writer"></a>Quellleser und Senkenwriter

[Quellleser und](source-reader.md) [Senkenschreiber](sink-writer.md) bieten eine alternative Möglichkeit, die grundlegenden Media Foundation (Medienquellen, Transformationen und Mediensenken) zu verwenden. Der Quellleser hostet eine Medienquelle und null oder mehr Decoder, während der Senkenwriter eine Mediensenke und null oder mehr Encoder hostet. Sie können den Quellreader verwenden, um komprimierte oder unkomprimierte Daten aus einer Medienquelle zu erhalten, und den Senkenwriter verwenden, um Daten zu codieren und die Daten an eine Mediensenke zu senden.

> [!Note]  
> Der Quellleser und senkende Writer sind in Windows 7 verfügbar.

 

Dieses Programmiermodell bietet der Anwendung mehr Kontrolle über den Datenfluss und gewährt der Anwendung auch direkten Zugriff auf die Daten aus der Quelle.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation: Grundlegende Konzepte](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[Media Foundation-Architektur](media-foundation-architecture.md)
</dt> </dl>

 

 



