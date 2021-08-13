---
description: Informationen zur Transcodierungs-API
ms.assetid: 54733364-f10c-4c1d-9800-75e283ba4be4
title: Informationen zur Transcodierungs-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cca7a5c39ebb4527a615c4c488239a1da4b88283f66199d25f6613a8d1f9bd82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449774"
---
# <a name="about-the-transcode-api"></a>Informationen zur Transcodierungs-API

Das folgende Diagramm zeigt, wie sich die Transcodierungs-API auf den Rest der Media Foundation-Codierungspipeline bezieht.

![Ein Diagramm, das die Transcodierungs-API zeigt.](images/encoding08.png)

Die Codierungspipeline enthält die folgenden Datenverarbeitungsobjekte:

-   Medienquelle
-   Decoder
-   Video-Resizer oder Audio-Resampler
-   Encoder
-   Mediensenke

Die Videogrößeänderung ist nur erforderlich, wenn sich die Größe des Ausgabevideos von der Quelle unterscheidet. Der Audio-Resampler wird nur benötigt, wenn die Audiodaten vor der Codierung neu gesampelt werden müssen. Das Decoder-Encoder-Paar ist für die Transcodierung erforderlich, jedoch nicht für die Neucodierung.

Die *Codierungstopologie* ist der Satz von Pipelineobjekten (Quelle, Decoder, Resizer, Resampler, Encoder und Mediensenke) sowie die Verbindungspunkte zwischen ihnen. Weitere Informationen zu Topologien finden Sie unter [Topologien.](topologies.md)

Verschiedene Komponenten sind für die Erstellung der verschiedenen Pipelineobjekte verantwortlich:

-   Die Anwendung verwendet in der Regel den [Quell-Resolver,](source-resolver.md) um die Medienquelle zu erstellen.
-   Die [Mediensitzung](media-session.md) lädt und konfiguriert den Decoder, den Video-Resizer und den Audio-Resampler. Intern wird hierzu das Topologieladeprogramm verwendet (siehe [**ZULASTENTopoLoader).**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)
-   Die Transcodierungs-API lädt und konfiguriert den Encoder und die Mediensenke.

Erweiterte Anwendungen können den Encoder und die Mediensenke direkt konfigurieren, anstatt die Transcodierungs-API zu verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Transcodieren der API](transcode-api.md)
</dt> <dt>

[Verwenden der Transcode-API](fast-transcode-objects.md)
</dt> </dl>

 

 



