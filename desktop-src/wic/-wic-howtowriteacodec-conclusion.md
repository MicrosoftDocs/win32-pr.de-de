---
description: Wenn Sie Ihren Codec auf der WIC-Plattform (Windows Imaging Component, Windows Imaging Component) erstellen, können alle auf WIC basierenden Anwendungen die gleiche Platt Form Unterstützung für Ihr Bildformat erhalten, das Sie für die allgemeinen Bildformate der Plattform erhalten.
ms.assetid: 4f25f0f4-246c-4cbd-bd11-d061dbc7de45
title: Schlussfolgerung (Schreiben eines WIC-Enabled Codecs)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de165f20ff81094c3b64d7e9667795f0bf80cef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358501"
---
# <a name="conclusion-how-to-write-a-wic-enabled-codec"></a>Schlussfolgerung (Schreiben eines WIC-Enabled Codecs)

Wenn Sie Ihren Codec auf der WIC-Plattform (Windows Imaging Component, Windows Imaging Component) erstellen, können alle auf WIC basierenden Anwendungen die gleiche Platt Form Unterstützung für Ihr Bildformat erhalten, das Sie für die allgemeinen Bildformate der Plattform erhalten. Außerdem ermöglicht es der Windows Vista-Fotogalerie, Windows-Explorer und der Photo Viewer, mit dem von Ihnen bereitgestellten Decoder Miniaturansichten und Vorschau Bilder in Ihrem Format anzuzeigen. Bei Rohdaten Formaten können anspruchsvollere Abbild Erstellungs Anwendungen die rohverarbeitungs Funktionen Ihres Decoders nutzen. Abhängig von den von Ihnen unterstützten Codierungsoptionen können Sie auch eindeutige Funktionen Ihres Encoders verfügbar machen, damit Anwendungen die erweiterten Features Ihres Bildformats voll ausschöpfen können.

Zum Entwickeln eines WIC-fähigen Codecs müssen Sie einige neue Schnittstellen implementieren. In vielen Fällen können Sie einen Wrapper für Ihren vorhandenen Codec schreiben, der diese Schnittstellen implementiert. Wenn Sie Ihren CODEC installieren, müssen Sie einige Registrierungseinträge vornehmen, damit der Codec von der WIC-Plattform erkennbar ist und den entsprechenden metadatenhandlern zugeordnet wird. Sie müssen auch eine API aufrufen, um den Miniatur Ansichts Cache aller standardmäßigen (leeren) Miniaturansichten zu löschen, die möglicherweise bereits mit Bildern in Ihrem Format verknüpft sind. Wenn Sie möchten, können Sie die Windows Vista-Fotogalerie aktivieren, um Benutzern einen Link zum Herunterladen Ihres Codecs bereitzustellen, wenn in der Fotogalerie ein Bild mit der Dateinamenerweiterung gefunden wird. Zu diesem Zweck müssen Sie Microsoft Informationen über die Dateinamenerweiterung Ihres Codecs und die URL für die Download Website bereitstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Codec-Installation und-Registrierung](-wic-codecinstallandreg.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



