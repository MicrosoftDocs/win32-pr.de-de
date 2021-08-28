---
description: Multimedia-Streamingobjekt und Schnittstellenhierarchie
ms.assetid: dbb6dc3b-b55e-4f6c-918f-068308e2dba9
title: Multimedia-Streamingobjekt und Schnittstellenhierarchie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b73da4777c2d05ff6455758ebde6e64a9a4c8277e8445ed59dca7f17088baea0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075768"
---
# <a name="multimedia-streaming-object-and-interface-hierarchy"></a>Multimedia-Streamingobjekt und Schnittstellenhierarchie

> [!Note]  
> Diese APIs sind veraltet. Anwendungen sollten den [**Sample Grabber-Filter**](sample-grabber-filter.md) verwenden oder einen benutzerdefinierten Filter implementieren, um Daten aus einem DirectShow-Filterdiagramm zu erhalten.

 

Das folgende Diagramm zeigt die Objekthierarchie, die beim Multimediastreaming verwendet wird.

![multimediastreaming-Objekthierarchie](images/mmstream02.png)

Die Multimediastreamingarchitektur definiert drei allgemeine Objekttypen:

-   Das **AMMultimediaStream-Objekt** macht die [**IAMMultiMediaStream-Schnittstelle**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) verfügbar. Intern umschließt dieses Objekt das DirectShow-Filterdiagramm.
-   *Medienstreamobjekte* machen die [**IMediaStream-Schnittstelle**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) verfügbar und sind datenspezifisch. Das AMMultimediaStream-Objekt enthält mindestens einen Medienstream.
-   *Streambeispielobjekte* enthalten die Daten für einen bestimmten Stream.

Die folgenden Medienstreamobjekte werden unterstützt:

-   Audiostream. Macht die [**IAudioMediaStream-Schnittstelle**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream) verfügbar.
-   DirectDraw-Stream. Stellt einen Videostream dar, der auf einer DirectDraw-Oberfläche gerendert wird. Macht die [**IDirectDrawMediaStream-Schnittstelle**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) verfügbar.
-   Medientypstream. Stellt beliebige Daten dar. Macht die [**IAMMediaTypeStream-Schnittstelle**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream) verfügbar.

Jedes Medienstreamobjekt erstellt eine eigene Art von Streambeispielobjekt:

-   Audiostreams erstellen Audiobeispiele, die die [**IAudioStreamSample-Schnittstelle**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) verfügbar machen.
-   DirectDraw-Streams erstellen DirectDraw-Beispiele, die die [**IDirectDrawStreamSample-Schnittstelle**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) verfügbar machen.
-   Medientypstreams erstellen Medientypbeispiele, die die [**IAMMediaTypeSample-Schnittstelle**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample) verfügbar machen.

Das folgende Diagramm zeigt die Schnittstellenhierarchie für die zuvor aufgeführten Schnittstellen:

![Multimediastreaming-Schnittstellenhierarchie](images/mmstream01.png)

 

 



