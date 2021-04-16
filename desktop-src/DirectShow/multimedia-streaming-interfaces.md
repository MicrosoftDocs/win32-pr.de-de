---
description: Multimedia-streamingschnittstellen
ms.assetid: 53d639e2-8717-4552-b0d3-b8c500bd38a8
title: Multimedia-streamingschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d654bae73ee822f553a1494e3b374cf35b8ac4a1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530560"
---
# <a name="multimedia-streaming-interfaces"></a>Multimedia-streamingschnittstellen

> [!Note]  
> Diese APIs sind veraltet. Anwendungen sollten den [**Beispiel-Grabber**](sample-grabber-filter.md) Filter verwenden oder einen benutzerdefinierten Filter implementieren, um Daten aus einem DirectShow-Filter Diagramm zu erhalten.

 

Dieser Abschnitt enthält Referenz Einträge für alle multimediastreamingschnittstellen und ihre Methoden, einschließlich derjenigen, die von Microsoft DirectShow unterstützt werden.



| Schnittstelle                                                  | BESCHREIBUNG                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iammediastream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream)                   | Behandelt die internen Verbindungen zwischen DirectShow-Filtern und Filter Diagrammen in Anwendungen, die Multimedia-Streaming verwenden.                            |
| [**Iammediatypesample**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample)           | Enthält Methoden zum Bearbeiten von streambeispielen mit beliebigen Medientypen.                                                                            |
| [**Iammediatypeer Stream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream)           | Enthält Methoden zum Erstellen von Multimedia-Streams mit beliebigen Medientypen.                                                                            |
| [**Iammultimediastream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream)         | Macht die DirectShow-Funktionalität für multimediastreamentwickler verfügbar.                                                                                       |
| [**Iaudiodata**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata)                           | Stellt Methoden bereit, die es Anwendungen ermöglichen, die zugrunde liegenden Audiodaten, auf die Audiostreams verweisen, festzulegen und zu erhalten.                                   |
| [**Iaudiomediastream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)             | Steuert audiomedienstreams durch Bereitstellen von Methoden, die das Format des Streams festlegen und erhalten.                                                                 |
| [**Iaudiostreamsample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample)           | Ruft Informationen aus den zugrunde liegenden [**iaudiodata**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) -Datenobjekten ab.                                                                |
| [**Idirectdrawmediastream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | Steuert Mediendaten Ströme, die auf Microsoft® DirectDraw-® Oberflächen angezeigt werden.                                                                                  |
| [**Idirectdrawstreamsample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | Stellt Methoden bereit, die Zeiger auf die dem aktuellen streambeispiel zugeordnete DirectDraw-Oberfläche festlegen und abrufen.                                    |
| [**Imediastream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)                       | Bietet Zugriff auf die Merkmale eines Mediendaten Stroms, z. b. den Medientyp und die Zweck-ID des Streams. Außerdem stehen Methoden zur Erstellung von Daten Beispielen zur Anwendung. |
| [**Imediastreamfilter**](/previous-versions/windows/desktop/api/amstream/nn-amstream-imediastreamfilter)           | Wird vom Medienstrom Filter unterstützt, der intern vom multimediarestream-Objekt verwendet wird. .                                                       |
| [**Imemorydata**](/previous-versions/windows/desktop/api/austream/nn-austream-imemorydata)                         | Enthält Methoden, die Arbeitsspeicher Daten für audiodatenobjekte festlegen und abrufen.                                                                               |
| [**Imultimediastream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream)             | Stellt Methoden bereit, die einen Multimedia-Stream steuern und Zugriff auf die zugrunde liegenden Mediendaten Ströme ermöglichen.                                                   |
| [**Istreamsample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)                     | Bietet Kontrolle über das Verhalten von streambeispielen.                                                                                                   |



 

 

 



