---
description: Audiostreamingschnittstellen
ms.assetid: eaf510ef-a6a3-45e0-8f0a-281a44b0ff6f
title: Audiostreamingschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1087ab127258fcd4f587cdd029d4604c35524689b5f0877476e1137e2ed924eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824470"
---
# <a name="audio-streaming-interfaces"></a>Audiostreamingschnittstellen

> [!Note]  
> Diese APIs sind veraltet. Anwendungen sollten den [**Sample Grabber-Filter**](sample-grabber-filter.md) verwenden oder einen benutzerdefinierten Filter implementieren, um Daten aus einem DirectShow-Filterdiagramm zu erhalten.

 



| Schnittstelle                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)   | Steuert Audiomedienstreams. Diese Schnittstelle erbt von der [**IMediaStream-Schnittstelle**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) und wird verwendet, um ein oder mehrere [**IAudioStreamSample-Objekte zu**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) erstellen. Sie wird auch verwendet, um das aktuelle Format der Datenstromdaten zu festlegen und abzurufen.                                                                                                            |
| [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) | Ruft Informationen aus den zugrunde liegenden [**IAudioData-Datenobjekten**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) ab.                                                                                                                                                                                                                                                                                                        |
| [**IMemoryData**](/previous-versions/windows/desktop/api/austream/nn-austream-imemorydata)               | Enthält Methoden, die Speicherdaten für Audiodatenobjekte festlegen und abrufen. Audiodatenobjekte stellen die zugrunde liegenden Daten zur Verfügung, auf die Streambeispiele zugreifen. Diese Schnittstelle bietet eine Möglichkeit, Speicherpuffer zu initialisieren und tatsächliche Mengen von Audiodaten in den -Objekten fest zu legen. Darüber hinaus kann die [**IMemoryData::GetInfo-Methode**](/previous-versions/windows/desktop/api/austream/nf-austream-imemorydata-getinfo) verwendet werden, um Audiospeicherdaten abzurufen. |
| [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata)                 | Stellt Methoden zur Verfügung, mit denen Anwendungen die zugrunde liegenden Audiodaten festlegen und erhalten können, auf die Audiostreams verweisen. Das Audiodatenformat wird in der [**WAVEFORMATEX-Struktur**](/previous-versions/dd757713(v=vs.85)) festgelegt.                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Liste der Multimedia-Streamingschnittstellen](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 
