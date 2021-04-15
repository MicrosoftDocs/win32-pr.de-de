---
description: Übersicht über das DirectShow-System
ms.assetid: aea1ab83-4c48-4b61-8a20-0ee6ad62ebe3
title: Übersicht über das DirectShow-System
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833fed4031c95ddb4ecbf91e7bb27c27741acc18
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520587"
---
# <a name="directshow-system-overview"></a>Übersicht über das DirectShow-System

**Die Herausforderung von Multimedia**

Das Arbeiten mit Multimedia stellt verschiedene Hauptprobleme dar:

-   Multimediarestreams enthalten große Datenmengen, die sehr schnell verarbeitet werden müssen.
-   Audiodaten und Videos müssen synchronisiert werden, sodass Sie gleichzeitig gestartet und angehalten werden und mit derselben Rate abgespielt werden.
-   Daten können aus vielen Quellen stammen, einschließlich lokaler Dateien, Computernetzwerken, Fernsehübertragungen und Videokameras.
-   Die Daten sind in einer Vielzahl von Formaten verfügbar, z. b. Audio-Video Interleaved (AVI), Advanced Streaming Format (ASF), Motion Picture Experts Group (MPEG) und Digital Video (DV).
-   Der Programmierer weiß im Voraus nicht, welche Hardware Geräte auf dem System des Endbenutzers vorhanden sein werden.

**Die DirectShow-Lösung**

DirectShow ist darauf ausgelegt, jede dieser Herausforderungen zu erfüllen. Das Hauptziel des Entwurfs Ziels besteht darin, die Aufgabe der Erstellung digitaler Medienanwendungen auf der Windows-Plattform zu vereinfachen, indem Anwendungen von den komplexen Daten Transporten, Hardware unterschieden und der Synchronisierung isoliert werden.

Um den Durchsatz zu erzielen, der zum Streamen von Video-und Audiodaten erforderlich ist, verwendet DirectShow nach Möglichkeit Direct3D und DirectSound. Diese Technologien Renderingdaten effizient in den Sound-und Grafikkarten des Benutzers. In DirectShow wird die Wiedergabe synchronisiert, indem Mediendaten in Zeitstempel Beispielen gekapselt werden. Für die unterschiedlichsten Quellen, Formate und Hardware Geräte, die möglich sind, verwendet DirectShow eine modulare Architektur, in der die Anwendung verschiedene Softwarekomponenten mit dem Namen " *Filter*" kombiniert und mit diesen übereinstimmt.

DirectShow stellt Filter bereit, die das erfassen und Optimieren von Geräten basierend auf dem Windows-Treibermodell (WDM) unterstützen, sowie Filter, die ältere Video für Windows (Vfw)-Erfassungs Karten unterstützen, und Codecs, die für die Schnittstellen von Audiokomprimierungs-Manager (ACM) und Video Compression Manager (VCM) geschrieben wurden.

Das folgende Diagramm zeigt die Beziehung zwischen einer Anwendung, den DirectShow-Komponenten und einigen der Hardware-und Softwarekomponenten, die von DirectShow unterstützt werden.

![allgemeine Architektur](images/arch-oview2.png)

Wie hier gezeigt, kommunizieren DirectShow-Filter mit einer großen Bandbreite von Geräten, darunter das lokale Dateisystem, TV-Tuner und Video Erfassungs Karten, VFW-Codecs, die Videoanzeige (über DirectDraw oder GDI) und die Soundkarte (über DirectSound). Daher isoliert DirectShow die Anwendung von vielen Komplexitäten dieser Geräte. DirectShow bietet auch systemeigene Komprimierungs-und Dekomprimierungs Filter für bestimmte Dateiformate.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu DirectShow](about-directshow.md)
</dt> </dl>

 

 



