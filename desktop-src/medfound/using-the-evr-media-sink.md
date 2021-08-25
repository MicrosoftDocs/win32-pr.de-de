---
description: Verwenden der EVR-Mediensenke
ms.assetid: cd98266a-bc62-43da-b4d7-3561447d634f
title: Verwenden der EVR-Mediensenke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ced80b4f9ee17093a00436a26f3f142281907597191791712fd6900520926ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826290"
---
# <a name="using-the-evr-media-sink"></a>Verwenden der EVR-Mediensenke

Die EVR-Mediensenke (Enhanced Video Renderer) kann als eigenständige Komponente verwendet werden. Häufiger erstellt eine Anwendung jedoch die EVR-Mediensenke in einer Topologie und verwendet dann die Mediensitzung, um die Wiedergabe zu steuern.

Es gibt zwei Möglichkeiten, die EVR-Mediensenke zu erstellen:

-   Die [**MFCreateVideoRenderer-Funktion**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) erstellt die Mediensenke.

-   Die [**MFCreateVideoRendererActivate-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) erstellt ein Aktivierungsobjekt für die Mediensenke.

Die EVR-Mediensenke verfügt anfänglich über eine Streamsenke, die dem Verweisstream entspricht. Um neue Streamsenken hinzuzufügen, rufen [**SieGEMEDIASink::AddStreamSink auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterter Videorenderer](enhanced-video-renderer.md)
</dt> <dt>

[Mediensenken](media-sinks.md)
</dt> </dl>

 

 



