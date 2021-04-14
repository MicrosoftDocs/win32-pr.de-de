---
description: Informationen zur transcode-API
ms.assetid: 54733364-f10c-4c1d-9800-75e283ba4be4
title: Informationen zur transcode-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d2d49a33a97bbb538888173db78705061583ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565505"
---
# <a name="about-the-transcode-api"></a>Informationen zur transcode-API

Das folgende Diagramm zeigt, wie sich die transcodieren-API auf den Rest der Media Foundation Codierungs Pipeline bezieht.

![ein Diagramm, das die transcodieren-API anzeigt.](images/encoding08.png)

Die Codierungs Pipeline enthält die folgenden Datenverarbeitungs Objekte:

-   Medienquelle
-   Decoder
-   Video Resizer oder audioresampler
-   Encoder
-   Medien Senke

Die Video Resizer ist nur erforderlich, wenn die Größe des Ausgabevideos von der Quelle abweicht. Der audioresampler ist nur erforderlich, wenn die Audiodatei vor der Codierung erneut erstellt werden muss. Das Decoder-/encoderpaar ist für die Transcodierung erforderlich, aber nicht für das remuxing.

Bei der Codierungs *Topologie* handelt es sich um den Satz von Pipeline Objekten (Quelle, Decoder, Resizer, Resampler, Encoder und Medien Senke) sowie die Verbindungspunkte zwischen Ihnen. Weitere Informationen zu Topologien finden Sie unter [Topologien](topologies.md).

Verschiedene Komponenten sind für das Erstellen der verschiedenen Pipeline Objekte verantwortlich:

-   Die Anwendung verwendet in der Regel den [quellresolver](source-resolver.md) , um die Medienquelle zu erstellen.
-   Die [Medien Sitzung](media-session.md) lädt und konfiguriert den Decoder, den Video Resizer und den audioresampler. Intern wird hierfür das topologielader verwendet (siehe [**imftopoloader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)).
-   Die transcodieren-API lädt und konfiguriert den Encoder und die Medien Senke.

Erweiterte Anwendungen können den Encoder und die Medien Senke direkt konfigurieren, anstatt die transcodieren-API zu verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Transcode-API](transcode-api.md)
</dt> <dt>

[Verwenden der transcode-API](fast-transcode-objects.md)
</dt> </dl>

 

 



