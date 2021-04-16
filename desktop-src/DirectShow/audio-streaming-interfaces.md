---
description: Audiostreamingschnittstellen
ms.assetid: eaf510ef-a6a3-45e0-8f0a-281a44b0ff6f
title: Audiostreamingschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68210beef0b05fcfc89ae5005c485fbc4b74d40f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522483"
---
# <a name="audio-streaming-interfaces"></a>Audiostreamingschnittstellen

> [!Note]  
> Diese APIs sind veraltet. Anwendungen sollten den [**Beispiel-Grabber**](sample-grabber-filter.md) Filter verwenden oder einen benutzerdefinierten Filter implementieren, um Daten aus einem DirectShow-Filter Diagramm zu erhalten.

 



| Schnittstelle                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iaudiomediastream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)   | Steuert audiomedienstreams. Diese Schnittstelle erbt von der [**imediastream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) -Schnittstelle und wird zum Erstellen eines oder mehrerer [**iaudiostreamsample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) -Objekte verwendet. Außerdem wird es verwendet, um das aktuelle Format der Streamdaten festzulegen und abzurufen.                                                                                                            |
| [**Iaudiostreamsample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) | Ruft Informationen aus den zugrunde liegenden [**iaudiodata**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) -Datenobjekten ab.                                                                                                                                                                                                                                                                                                        |
| [**Imemorydata**](/previous-versions/windows/desktop/api/austream/nn-austream-imemorydata)               | Enthält Methoden, die Arbeitsspeicher Daten für audiodatenobjekte festlegen und abrufen. Mit audiodatenobjekten werden die zugrunde liegenden Daten bereitgestellt, auf die der Zugriff von Beispielen Diese Schnittstelle bietet eine Möglichkeit zum Initialisieren von Speicher Puffern und zum Festlegen tatsächlicher Mengen an Audiodaten in den Objekten. Darüber hinaus kann die [**imemorydata:: GetInfo**](/previous-versions/windows/desktop/api/austream/nf-austream-imemorydata-getinfo) -Methode zum Abrufen von audiospeicherdaten verwendet werden. |
| [**Iaudiodata**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata)                 | Stellt Methoden bereit, die es Anwendungen ermöglichen, die zugrunde liegenden Audiodaten, auf die Audiostreams verweisen, festzulegen und zu erhalten. Das Audiodatenformat wird in der [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur festgelegt.                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Liste der Multimedia-streamingschnittstellen](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 
