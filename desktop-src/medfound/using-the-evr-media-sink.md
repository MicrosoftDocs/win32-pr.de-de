---
description: Verwenden der EVR-Medien Senke
ms.assetid: cd98266a-bc62-43da-b4d7-3561447d634f
title: Verwenden der EVR-Medien Senke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84f8c666e88b495ad2d2e53fb1de10364f91636f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106354280"
---
# <a name="using-the-evr-media-sink"></a>Verwenden der EVR-Medien Senke

Die gesteigerte Medien Senke (Enhanced Video Renderer) kann als eigenständige Komponente verwendet werden. Häufig wird jedoch eine Anwendung die EVR-Medien Senke in einer Topologie erstellen und dann die Wiedergabe mit der Medien Sitzung steuern.

Es gibt zwei Möglichkeiten, die EVR-Medien Senke zu erstellen:

-   Die [**MF**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) -Funktion erstellt die Medien Senke.

-   Die [**MF**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) -Funktion erstellt ein Aktivierungs Objekt für die Medien Senke.

Die EVR-Medien Senke verfügt anfänglich über eine streamsenke, die dem Verweis Datenstrom entspricht. Um neue streamsenken hinzuzufügen, nennen Sie [**imfmediasink:: addstreamsink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterter Videorenderer](enhanced-video-renderer.md)
</dt> <dt>

[Medien senken](media-sinks.md)
</dt> </dl>

 

 



