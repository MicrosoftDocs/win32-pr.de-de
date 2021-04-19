---
description: Beschreibt das Hinzufügen von Dateneinheiten Erweiterungen bei Verwendung von Windows Media Encoder.
ms.assetid: fdadcb85-c564-4d05-a4d7-af53a0107455
title: Verwenden von Dateneinheiten Erweiterungen (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c16053ee078f5adcd48767f53d9e6e1c0eeb02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372912"
---
# <a name="using-data-unit-extensions-microsoft-media-foundation"></a>Verwenden von Dateneinheiten Erweiterungen (Microsoft Media Foundation)

Die Windows Media Audio-und Video Codecs sind so konzipiert, dass Sie mit dem Container "Advanced Systems Format (ASF)" gut funktionieren. ASF ist das strukturierte Format, das für Windows Media Audio-Dateien (WMA) und Windows Media Video (WMV)-Dateien verwendet wird. Es ist ein erweiterbares Format, das für das Streamen von Daten konzipiert ist. Eines der ungewöhnlichen Merkmale der ASF-Struktur ist die Möglichkeit, Metadaten an einzelne Stichproben anzufügen und diese Daten mit den Beispielen im Bitstream einzubetten. Ein Element von Metadaten, das auf diese Weise gespeichert wird, wird als *dateneinheits Erweiterung* oder *Beispiel Erweiterung* bezeichnet.

Eine Erweiterung für Dateneinheiten kann Informationen enthalten, die vom Encoder, dem Decoder oder der Player Anwendung benötigt werden. Die meisten Daten-Einheiten Erweiterungs Typen, die in der Windows Media 9-Reihe von Codecs implementiert sind, enthalten Daten, die für die Anwendung vorgesehen sind, die die Medien decodiert und rendert. Beispielsweise können Sie SMPTE-Zeit Codes aus den Quelldaten verwalten, indem Sie Sie als Dateneinheiten Erweiterungen hinzufügen. Die folgenden Codec-Features erfordern jedoch Erweiterungen für Dateneinheiten:

-   [Erzwungene Keyframe-Einfügung](forcedkeyframeinsertion.md)
-   [Video Codierung mit Zeilen Sprung](interlacedvideoencoding.md)
-   Die Schwierigkeit bei der direkten Verwendung von dateneinheits Erweiterungen beim direkten Zugriff auf den Codec ist der Mechanismus, mit dem das Objekt die Erweiterungs Daten empfängt. Dies wird durch die Objekte des SDK für den Windows Media-Format erreicht, indem Puffer Objekte verwendet werden, die diese Funktion unterstützen. Es wird empfohlen, dass Sie das Windows Media-Format-SDK zum Aktivieren der Codec-Features verwenden, die Dateneinheiten Erweiterungen erfordern, aber Sie können diese Funktionen mit den eigenständigen Codec-Objekten arbeiten.

## <a name="passing-extended-samples-to-the-codec-objects"></a>Übergeben von erweiterten Beispielen an die Codec-Objekte

Das Windows Media-Format SDK verwendet Puffer Objekte, die [**inssbuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) -Schnittstellen verfügbar machen. Die neueste Schnittstelle ist [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4). Zum Übergeben von Beispielen an ein Codec-Objekt mit Dateneinheiten Erweiterungen müssen Sie ein Puffer Objekt verwenden, das die [**imediabuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) -Schnittstelle oder die [**imfmediabuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) -Schnittstelle und die **inssbuffer** -Schnittstelle implementiert. Sie können Puffer Objekte verwenden, die vom SDK für den Windows Media-Format oder Microsoft Media Foundation erstellt wurden, oder Sie können eine eigene Puffer Klasse erstellen, die die Anforderungen erfüllt. Zum Erstellen einer eigenen Puffer Klasse müssen Sie den Methoden Prototypen für die **inssbuffer** -Schnittstellen entsprechen. Diese Schnittstellendefinitionen finden Sie in der wmsbuffer. h-Header Datei, die mit dem Windows Media-Format SDK installiert wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Media-Codecs](windows-media-codecs.md)
</dt> </dl>

 

 
