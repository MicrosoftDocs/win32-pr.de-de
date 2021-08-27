---
description: Multimedia-Streamingobjekte
ms.assetid: 4f5460db-2670-41af-a57f-20cf706827e6
title: Multimedia-Streamingobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bfefd7d16c832dc168204df771ff8f925bec3f1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471946"
---
# <a name="multimedia-streaming-objects"></a>Multimedia-Streamingobjekte

> [!Note]  
> Diese API ist veraltet. Neue Anwendungen sollten sie nicht verwenden.

 

In der folgenden Tabelle werden die Multimediastreamingobjekte beschrieben.




| CLSID | BESCHREIBUNG | Unterstützte Schnittstellen | 
|-------|-------------|----------------------|
| CLSID_AMMediaTypeStream | Kann Medienbeispiele für jeden von DirectShow unterstützten Datentyp erstellen. | <ul><li><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></li><li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li></ul> | 
| CLSID_AMAudioData | Implementierung des <a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData-Audiocontainerobjekts.</strong></a> | <ul><li><a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a></li></ul> | 
| CLSID_AMDirectDrawStream | DirectDraw-Medienstream, der einem DirectShow-Multimediastream hinzugefügt werden kann. | <ul><li><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></li><li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></li><li><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream"><strong>IDirectDrawMediaStream</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li></ul> | 
| CLSID_AMMultiMediaStream | DirectShow-Implementierung des Multimediastreams. | <ul><li><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a></li><li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream"><strong>IMultiMediaStream</strong></a></li></ul> | 
| CLSID_MediaStreamFilter | Stellt Multimediastreamingfunktionen für das CLSID_AMMultiMediaStream über die <a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream-Schnittstelle</strong></a> bereit. | <ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li></ul> | 
| – | Beispiele, die vom CLSID_AMMediaTypeStream werden. | <ul><li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample2"><strong>IMediaSample2</strong></a></li></ul> | 
| – | Vom DirectDraw-Stream erstellte Beispiele. | <ul><li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></li><li><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample"><strong>IDirectDrawStreamSample</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></li></ul> | 




 

 

 



