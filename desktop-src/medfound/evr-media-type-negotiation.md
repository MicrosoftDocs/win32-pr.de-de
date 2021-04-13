---
description: EVR-Medientyp Aushandlung
ms.assetid: 3a12b80d-7aac-437d-b515-aab37c1e81b2
title: EVR-Medientyp Aushandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb1f87a24db866c9e80b211b0385c12dcd6b594
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351458"
---
# <a name="evr-media-type-negotiation"></a>EVR-Medientyp Aushandlung

In diesem Thema wird beschrieben, wie der Enhanced Video Renderer (EVR) Medientypen validiert.

-   Beim DirectShow-EVR-Filter erfolgt die typaushandlung, wenn die Pins des Filters verbunden sind.

-   Für die EVR-Medien Senke werden die Medientypen über die [**IMF mediatyethandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) -Schnittstelle auf den streamsenken festgelegt. In der Regel aushandt der topologielader die Medientypen, obwohl die Anwendung auch die Medientypen direkt festlegen kann.

Der EVR meldet keine bevorzugten Medientypen. Der Client muss die Medientypen testen, bis er einen akzeptablen Typ findet. Der Medientyp für den Verweis Datenstrom muss festgelegt werden, bevor die Typen für die untergeordneten Datenströme festgelegt werden können.

Für den Verweis Datenstrom erhält der EVR-Mixer eine Liste mit kompatiblen DXVA-renderingzielformaten (DirectX Video Acceleration). Der EVR Presenter verwendet diese Liste, um das Format für die Direct3D SwapChain auszuwählen. Wenn kein kompatibles renderzielformat gefunden werden kann, lehnt der EVR den Medientyp ab.

Bei den Substreams fragt der EVR-Mixer, ob das DXVA-Gerät dieses substreamformat in Kombination mit dem renderzielformat unterstützt, das für den Verweis Datenstrom ausgewählt wurde. Folglich können sich die verfügbaren substreamformate abhängig vom Verweisstream ändern.

Im folgenden wird der Prozess ausführlicher beschrieben. Diese Details sind für die meisten Anwendungen nicht wichtig, sind aber möglicherweise hilfreich, wenn Sie einen benutzerdefinierten Mixer oder Presenter schreiben.

Für den Verweis Datenstrom erfolgt die Aushandlung wie folgt:

1.  Der EVR ruft [**IMF Transform:: abtinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) auf dem Mixer auf.

2.  Der Mixer konvertiert den Medientyp mithilfe der [**DXVA2 \_ videodesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) -Struktur in eine DXVA 2,0-Beschreibung.

3.  Der Mixer ruft [**idirectxvideoprocmeorservice:: getvideoprocess ordeviceguids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) auf, um eine Liste der Videoprozessor-GUIDs abzurufen.

4.  Für jede Videoprozessor-GUID ruft der-Mixer [**idirectxvideoprocesorservice:: getvideoprocess orrendertargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) auf, um die unterstützten renderzielformate zu erhalten.

5.  Der EVR ruft [**IMF videopresenter::P rocess Message**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) für den Presenter mit der \_ Meldung "invalidatemediatype" der MF-Nachricht auf \_ . Diese Meldung bewirkt, dass der Presenter ein neues Format auswählt.

6.  Der Presenter ruft [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) auf, um eine Liste der verfügbaren Ausgabeformate vom Mixer zu erhalten. Der Mixer generiert diese Liste aus den in Schritt 4 erhaltenen Formaten.

7.  Der Presenter wählt ein Format aus und ruft [**IMF Transform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) auf dem Mixer auf.

Für Substreams ist der Prozess einfacher:

1.  Der EVR ruft [**IMF Transform:: abtinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) auf dem Mixer auf.

2.  Der Mixer ruft [**idirectxvideoprocess orservice:: getvideoprocess orsubstreamformats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) auf, um eine Liste der verfügbaren substreamformate zu erhalten.

3.  Wenn das vorgeschlagene Format in dieser Liste enthalten ist, akzeptiert das EVR den Eingabetyp.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterter Videorenderer](enhanced-video-renderer.md)
</dt> </dl>

 

 



