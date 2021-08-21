---
description: Multimediastreamingschnittstellen
ms.assetid: 53d639e2-8717-4552-b0d3-b8c500bd38a8
title: Multimediastreamingschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b38200d98b0f01b7260508cbf7bd19c6e65efdfb3af78f2efff77be38294e8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118152956"
---
# <a name="multimedia-streaming-interfaces"></a>Multimediastreamingschnittstellen

> [!Note]  
> Diese APIs sind veraltet. Anwendungen sollten den [**Beispielgrabberfilter**](sample-grabber-filter.md) verwenden oder einen benutzerdefinierten Filter implementieren, um Daten aus einem DirectShow-Filterdiagramm abzurufen.

 

Dieser Abschnitt enthält Referenzeinträge für alle Multimediastreamingschnittstellen und deren Methoden, einschließlich der von Microsoft DirectShow unterstützten Schnittstellen.



| Schnittstelle                                                  | BESCHREIBUNG                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAMMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream)                   | Verarbeitet die internen Verbindungen zwischen DirectShow-Filtern und Filterdiagrammen in Anwendungen, die Multimediastreaming verwenden.                            |
| [**IAMMediaTypeSample**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample)           | Enthält Methoden zum Bearbeiten von Streambeispielen mit beliebigen Medientypen.                                                                            |
| [**IAMMediaTypeStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream)           | Enthält Methoden zum Erstellen von Multimediastreams mit beliebigen Medientypen.                                                                            |
| [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream)         | Macht DirectShow-Funktionen für Entwickler von Multimediastreams verfügbar.                                                                                       |
| [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata)                           | Stellt Methoden bereit, mit denen Anwendungen die zugrunde liegenden Audiodaten festlegen und abrufen können, auf die Audiostreams verweisen.                                   |
| [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)             | Steuert Audiomedienstreams, indem Methoden zum Festlegen und Abrufen des Streamsformats zur Verfügung gestellt werden.                                                                 |
| [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample)           | Ruft Informationen aus den zugrunde liegenden [**IAudioData-Datenobjekten**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) ab.                                                                |
| [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | Steuert Medienstreams, die auf Microsoft® DirectDraw®-Oberflächen angezeigt werden.                                                                                  |
| [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | Stellt Methoden bereit, die Zeiger auf die DirectDraw-Oberfläche festlegen und abrufen, die dem aktuellen Streambeispiel zugeordnet ist.                                    |
| [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)                       | Ermöglicht den Zugriff auf die Merkmale eines Medienstreams, z. B. den Medientyp und die Zweck-ID des Streams. Es verfügt auch über Methoden, die Datenbeispiele erstellen. |
| [**IMediaStreamFilter**](/previous-versions/windows/desktop/api/amstream/nn-amstream-imediastreamfilter)           | Wird vom Media Stream-Filter unterstützt, der intern vom Multimediastreamobjekt verwendet wird. .                                                       |
| [**IMemoryData**](/previous-versions/windows/desktop/api/austream/nn-austream-imemorydata)                         | Enthält Methoden, die Speicherdaten für Audiodatenobjekte festlegen und abrufen.                                                                               |
| [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream)             | Stellt Methoden bereit, die einen Multimediastream steuern und Zugriff auf die zugrunde liegenden Medienstreams bereitstellen.                                                   |
| [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)                     | Ermöglicht die Steuerung des Verhaltens von Streambeispielen.                                                                                                   |



 

 

 



