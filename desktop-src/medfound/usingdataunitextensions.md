---
description: Beschreibt, wie Dateneinheiterweiterungen hinzugefügt werden, wenn Windows Media Encoder verwendet werden.
ms.assetid: fdadcb85-c564-4d05-a4d7-af53a0107455
title: Verwenden von Dateneinheitenerweiterungen (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4680626f06c93e63f293699360d98ac995eedc3b3351fe617c182dbc176165ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972719"
---
# <a name="using-data-unit-extensions-microsoft-media-foundation"></a>Verwenden von Dateneinheitenerweiterungen (Microsoft Media Foundation)

Die Windows Medienaudio- und Videocodecs sind so konzipiert, dass sie gut mit dem ASF-Container (Advanced Systems Format) funktionieren. ASF ist das strukturierte Format, das für Windows WMA-Dateien (Media Audio) und Windows Media Video-Dateien (WMV) verwendet wird. Es handelt sich um ein erweiterbares Format, das für das Streamen von Daten konzipiert ist. Eines der ungewöhnlichen Merkmale der ASF-Struktur ist die Fähigkeit, Metadaten an einzelne Stichproben anzufügen und diese Daten mit den Stichproben in den Bitstream einzubetten. Ein Element von Metadaten, das auf diese Weise gespeichert wird, wird als *Dateneinheiterweiterung* oder *Beispielerweiterung* bezeichnet.

Eine Dateneinheitenerweiterung kann Informationen enthalten, die vom Encoder, dem Decoder oder der Playeranwendung benötigt werden. Die meisten Dateneinheitserweiterungstypen, die in der Windows Media 9-Serie von Codecs implementiert sind, enthalten Daten, die für die Anwendung bestimmt sind, die die Medien decodiert und rendert. Beispielsweise können Sie SMPTE-Zeitcodes aus Quelldaten verwalten, indem Sie sie als Dateneinheitenerweiterungen hinzufügen. Die folgenden Codecfeatures erfordern jedoch Dateneinheitenerweiterungen:

-   [Erzwungene Einfügung von Keyframes](forcedkeyframeinsertion.md)
-   [Interlaced Video Encoding](interlacedvideoencoding.md)
-   Die Schwierigkeit bei der Verwendung von Dateneinheiterweiterungen beim direkten Zugriff auf den Codec ist der Mechanismus, mit dem das Objekt die Erweiterungsdaten empfängt. Dies wird durch die Objekte des Windows Media Format SDK erreicht, indem Pufferobjekte verwendet werden, die zur Unterstützung dieses Features entwickelt wurden. Es wird empfohlen, das Windows Media Format SDK zu verwenden, um die Codecfunktionen zu aktivieren, die Dateneinheitserweiterungen erfordern. Sie können diese Features jedoch mit den eigenständigen Codecobjekten verwenden.

## <a name="passing-extended-samples-to-the-codec-objects"></a>Übergeben erweiterter Beispiele an codec-Objekte

Das Windows Media Format SDK verwendet Pufferobjekte, die [**INSSBuffer-Schnittstellen**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) verfügbar machen. Die neueste Schnittstelle ist [**INSSBuffer4.**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) Um Beispiele an ein Codecobjekt mit Dateneinheiterweiterungen zu übergeben, müssen Sie ein Pufferobjekt verwenden, das die [**IMediaBuffer-**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) oder [**DIENMEDIABUFFER-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) und die **INSSBuffer-Schnittstelle** implementiert. Hierfür können Sie Pufferobjekte verwenden, die vom Windows Media Format SDK oder Microsoft Media Foundation erstellt wurden, oder Sie können eine eigene Pufferklasse erstellen, die die Anforderungen erfüllt. Um eine eigene Pufferklasse zu erstellen, müssen Sie den Methodenprototypen für die **INSSBuffer-Schnittstellen** entsprechen. Diese Schnittstellendefinitionen finden Sie in der Headerdatei wmsbuffer.h, die mit dem Windows Media Format SDK installiert wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Media-Codecs](windows-media-codecs.md)
</dt> </dl>

 

 
