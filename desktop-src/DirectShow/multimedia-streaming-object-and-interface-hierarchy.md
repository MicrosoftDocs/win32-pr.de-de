---
description: Multimediastreamingobjekt und Schnittstellen Hierarchie
ms.assetid: dbb6dc3b-b55e-4f6c-918f-068308e2dba9
title: Multimediastreamingobjekt und Schnittstellen Hierarchie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52339644730139af22fd21fa2c24b8448a1afaf3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869611"
---
# <a name="multimedia-streaming-object-and-interface-hierarchy"></a>Multimediastreamingobjekt und Schnittstellen Hierarchie

> [!Note]  
> Diese APIs sind veraltet. Anwendungen sollten den [**Beispiel-Grabber**](sample-grabber-filter.md) Filter verwenden oder einen benutzerdefinierten Filter implementieren, um Daten aus einem DirectShow-Filter Diagramm zu erhalten.

 

Das folgende Diagramm zeigt die Objekthierarchie, die beim Multimedia-Streaming verwendet wird.

![multimediastreaming-Objekthierarchie](images/mmstream02.png)

Die Multimedia-streamingarchitektur definiert drei allgemeine Objekttyp:

-   Das **ammultimediastream** -Objekt macht die [**iammultimediastream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) -Schnittstelle verfügbar. Intern umschließt dieses Objekt das DirectShow-Filter Diagramm.
-   *Media Stream* -Objekte machen die [**imediastream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) -Schnittstelle verfügbar und sind Daten spezifisch. Das ammultimediastream-Objekt enthält einen oder mehrere Mediendaten Ströme.
-   *Stream-Beispiel* Objekte enthalten die Daten für einen bestimmten Datenstrom.

Die folgenden Medienstrom Objekte werden unterstützt:

-   Audiodatenstrom. Macht die [**iaudiomediastream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream) -Schnittstelle verfügbar.
-   DirectDraw-Stream. Stellt einen Videostream dar, der auf eine DirectDraw-Oberfläche gerendert wird. Macht die [**idirectdrawmediastream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) -Schnittstelle verfügbar.
-   Medientyp-Stream. Stellt beliebige Daten dar. Macht die [**iammediatypeer Stream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream) -Schnittstelle verfügbar.

Jedes Mediendaten Strom-Objekt erstellt eine eigene Art von Datenstrom Sample-Objekt:

-   Audiodatenströme erstellen Audiobeispiele, die die [**iaudiostreamsample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) -Schnittstelle verfügbar machen.
-   DirectDraw-Streams erstellen DirectDraw-Beispiele, die die [**idirectdrawstreamsample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) -Schnittstelle verfügbar machen.
-   Medientyp-Streams erstellen Beispiele für den Medientyp, die die [**iammediatypesample**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample) -Schnittstelle verfügbar machen.

Das folgende Diagramm zeigt die Schnittstellen Hierarchie für die zuvor aufgelisteten Schnittstellen:

![multimediastreaming-Schnittstellen Hierarchie](images/mmstream01.png)

 

 



