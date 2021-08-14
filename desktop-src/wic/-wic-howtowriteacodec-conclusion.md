---
description: Wenn Sie Ihren Codec auf der WIC-Plattform (Windows Imaging Component) erstellen, können alle Anwendungen, die auf WIC aufbauen, die gleiche Plattformunterstützung für Ihr Bildformat erhalten, die sie auch für die allgemeinen Bildformate erhalten, die mit der Plattform ausgeliefert werden.
ms.assetid: 4f25f0f4-246c-4cbd-bd11-d061dbc7de45
title: Schlussfolgerung (Schreiben eines WIC-Enabled Codecs)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5288438ea518e1776562b288184067df6d82c326eb6786b163f20e90c6febc05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205821"
---
# <a name="conclusion-how-to-write-a-wic-enabled-codec"></a>Schlussfolgerung (Schreiben eines WIC-Enabled Codecs)

Wenn Sie Ihren Codec auf der WIC-Plattform (Windows Imaging Component) erstellen, können alle Anwendungen, die auf WIC aufbauen, die gleiche Plattformunterstützung für Ihr Bildformat erhalten, die sie auch für die allgemeinen Bildformate erhalten, die mit der Plattform ausgeliefert werden. Außerdem können die Windows Vista Fotogalerie, Windows Explorer und Bildanzeige Miniaturansichten und Vorschauen von Bildern in Ihrem Format mithilfe des von Ihnen bereitgestellten Decoders anzeigen. Bei Rohformaten ermöglicht es anspruchsvollere Imageerstellungsanwendungen, die Rohdatenverarbeitungsfunktionen Ihres Decoders zu nutzen. Abhängig von den unterstützten Encoderoptionen können Sie auch einzigartige Funktionen Ihres Encoders verfügbar machen, damit Anwendungen die erweiterten Features Ihres Bildformats in vollem Umfang nutzen können.

Für die Entwicklung eines WIC-fähigen Codecs müssen Sie einige neue Schnittstellen implementieren. In vielen Fällen können Sie einen Wrapper für Ihren vorhandenen Codec schreiben, der diese Schnittstellen implementiert. Wenn Sie Ihren Codec installieren, müssen Sie einige Registrierungseinträge vornehmen, damit Ihr Codec von der WIC-Plattform ermittelt werden kann, und ihn den entsprechenden Metadatenhandlern zuordnen. Sie müssen auch eine API aufrufen, um den Miniaturansichtscache aller standardmäßigen (leeren) Miniaturansichten zu löschen, die möglicherweise zuvor Bildern in Ihrem Format zugeordnet waren. Wenn Sie möchten, können Sie die Windows Vista-Fotogalerie aktivieren, um Benutzern einen Link zum Herunterladen Ihres Codecs bereitzustellen, wenn die Fotogalerie auf ein Bild mit Ihrer Dateinamenerweiterung trifft. Hierzu müssen Sie Microsoft Informationen zur Dateierweiterung Ihres Codecs und die URL für Ihre Downloadwebsite bereitstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[CODEC-Installation und -Registrierung](-wic-codecinstallandreg.md)
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



