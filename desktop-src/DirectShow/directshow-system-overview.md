---
description: DirectShow-Systemübersicht
ms.assetid: aea1ab83-4c48-4b61-8a20-0ee6ad62ebe3
title: DirectShow-Systemübersicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0fb7855277029adc563cc032740d3a59b3691fcf12ed2b2595d37a1abd0d923
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966350"
---
# <a name="directshow-system-overview"></a>DirectShow-Systemübersicht

**Die Herausforderung von Multimedia**

Die Arbeit mit Multimedia stellt mehrere große Herausforderungen dar:

-   Multimediastreams enthalten große Datenmengen, die sehr schnell verarbeitet werden müssen.
-   Audio und Video müssen synchronisiert werden, damit sie gleichzeitig gestartet und beendet und mit der gleichen Rate wiedergegeben werden.
-   Daten können aus vielen Quellen stammen, einschließlich lokaler Dateien, Computernetzwerke, Fernsehsendungen und Videokameras.
-   Daten werden in einer Vielzahl von Formaten bereitgestellt, z. B. Audio-Video Interleaved (AVI), Advanced Streaming Format (ASF), Motion Picture Experts Group (MPEG) und Digital Video (DV).
-   Der Programmierer weiß nicht im Voraus, welche Hardwaregeräte auf dem System des Endbenutzers vorhanden sein werden.

**Die DirectShow-Lösung**

DirectShow wurde entwickelt, um jede dieser Herausforderungen zu bewältigen. Das Hauptentwurfsziel besteht darin, die Erstellung digitaler Medienanwendungen auf der Windows Plattform zu vereinfachen, indem Anwendungen von der Komplexität von Datentransporten, Hardwareunterschieden und Synchronisierungen abgefangen werden.

Um den zum Streamen von Video und Audio erforderlichen Durchsatz zu erzielen, verwendet DirectShow nach Möglichkeit Direct3D und DirectSound. Diese Technologien rendern Daten effizient auf den Sound- und Grafikkarten des Benutzers. DirectShow synchronisiert die Wiedergabe, indem Mediendaten in Zeitstempelbeispielen gekapselt werden. Um die Vielzahl von Quellen, Formaten und Hardwaregeräten zu verarbeiten, die möglich sind, verwendet DirectShow eine modulare Architektur, in der die Anwendung verschiedene Softwarekomponenten, die als *Filter* bezeichnet werden, kombiniert und abstreicht.

DirectShow bietet Filter, die Erfassungs- und Optimierungsgeräte basierend auf dem Windows Driver Model (WDM) unterstützen, sowie Filter, die ältere Video für Windows (VfW)-Erfassungskarten und Codecs unterstützen, die für die Schnittstellen Audio Compression Manager (ACM) und Video Compression Manager (VCM) geschrieben wurden.

Das folgende Diagramm zeigt die Beziehung zwischen einer Anwendung, den DirectShow-Komponenten und einigen der Von DirectShow unterstützten Hardware- und Softwarekomponenten.

![Architektur auf hoher Ebene](images/arch-oview2.png)

Wie hier gezeigt, kommunizieren DirectShow-Filter mit einer Vielzahl von Geräten, einschließlich des lokalen Dateisystems, TV-Tuner- und Videoerfassungskarten, VfW-Codecs, der Videoanzeige (über DirectDraw oder GDI) und der Soundkarte (über DirectSound). Daher isoliert DirectShow die Anwendung vor vielen der Komplexitäten dieser Geräte. DirectShow bietet auch native Komprimierungs- und Dekomprimierungsfilter für bestimmte Dateiformate.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu DirectShow](about-directshow.md)
</dt> </dl>

 

 



