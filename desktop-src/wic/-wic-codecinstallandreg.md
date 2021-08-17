---
description: Wenn Sie einen Codec installieren, müssen Sie ihn in der Registrierung registrieren. Sie müssen auch sicherstellen, dass der Miniaturansichtscache aktualisiert wird, falls bilder in Ihrem Format bereits auf dem Computer vorhanden sind.
ms.assetid: 7aec54cb-40ac-495c-99d9-9c397b740b21
title: Codecinstallation und -registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc13a2d937e82eae3517b9b20440f4acbb10b16af3fa0b872eb0ddd6c2a8d6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965179"
---
# <a name="codec-installation-and-registration"></a>Codecinstallation und -registrierung

Wenn Sie einen Codec installieren, müssen Sie ihn in der Registrierung registrieren. Sie müssen auch sicherstellen, dass der Miniaturansichtscache aktualisiert wird, falls bilder in Ihrem Format bereits auf dem Computer vorhanden sind.

Dieses Thema enthält folgende Abschnitte:

-   [Registrieren eines Codecs](#registering-a-codec)
-   [Aktualisieren des Miniaturansichtscaches bei der Installation des Codecs](#updating-the-thumbnail-cache-when-installing-your-codec)
-   [Verfügbarmachen ihres WIC-Enabled-Codecs für Benutzer](#making-your-wic-enabled-codec-available-to-users)
-   [Zugehörige Themen](#related-topics)

## <a name="registering-a-codec"></a>Registrieren eines Codecs

Wenn Sie einen Codec registrieren, registrieren Sie tatsächlich zwei Komponenten: den Encoder und den Decoder. Sie müssen auch Registrierungseinträge erstellen, um Ihr Containerformat bei den Metadatenhandlern für die Metadatenformate zu registrieren, die ihr Imageformat unterstützt.

In den folgenden Themen werden die Registrierungseinträge beschrieben, die Sie zum Registrieren Ihres Codecs benötigen:

[Allgemeine Registrierungseinträge](-wic-generalregentries.md)

[Encoderspezifische Registrierungseinträge](-wic-encoderregentries.md)

[Decoderspezifische Registrierungseinträge](-wic-decoderregentries.md)

[Integration in Windows Fotogalerie und Windows Explorer](-wic-integrationregentries.md)

## <a name="updating-the-thumbnail-cache-when-installing-your-codec"></a>Aktualisieren des Miniaturansichtscaches bei der Installation des Codecs

Wenn ein Codec installiert ist, muss das Installationsprogramm die folgende Funktion aufrufen, nachdem die zugehörigen Registrierungseinträge geschrieben wurden.


```C++
SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_IDLIST, NULL, NULL)
```



Dieser Aufruf benachrichtigt Windows, dass neue Dateizuordnungsinformationen verfügbar sind. Wenn Bilder im Bildformat bereits auf dem Computer vorhanden sind, enthält der Miniaturansichtscache Standardminiaturansichten für sie, da kein Decoder zum Extrahieren der Miniaturansichten verfügbar war, als die Bilder zum ersten Mal abgerufen wurden. Wenn Sie Windows benachrichtigen, dass eine neue Dateizuordnung verfügbar ist, verwirft der Miniaturansichtscache alle leeren Miniaturansichten und extrahiert die eigentlichen Miniaturansichten aus den Dateien, die jetzt decodiert werden können.

## <a name="making-your-wic-enabled-codec-available-to-users"></a>Verfügbarmachen ihres WIC-Enabled-Codecs für Benutzer

Wenn Sie ein Kamerahersteller sind, können Sie Ihre unformatierten Codecs im Feld mit Ihren Kameras versenden. Sie können Ihre Codecs auch auf der Downloadseite Ihrer Website veröffentlichen. Wenn ein Benutzer jedoch eine Bilddatei in Ihrem Format von einer anderen Quelle wie einem Freund, einem Geschäftspartner oder einer anderen Website erhält, weiß er möglicherweise nicht, wo der Codec zum Decodieren verwendet werden soll.

Aufgrund dieses Problems bietet Windows Benutzern Ihres Bildformats eine einfachere Möglichkeit, Ihren Codec zu finden und auf ihren Computer herunterzuladen, beginnend mit Windows Vista. Wenn der Windows Fotogalerie eine Dateinamenerweiterung als Bildformat erkennt und der Codec für dieses Format nicht installiert ist, weist ein Dialogfeld den Benutzer an, dass das Foto nicht angezeigt werden kann, und fragt, ob der Benutzer die erforderliche Software herunterladen möchte, um es anzuzeigen. Wenn der Benutzer akzeptiert, wird eine von Microsoft gehostete Website mit einem Link zur Downloadwebsite des Codecherstellers angezeigt. (Optional können Sie anfordern, dass Benutzer direkt zu Ihrer Downloadwebsite gelangen.)

Wenn Sie möchten, dass die Dateinamenerweiterungen Ihres Bildformats vom Windows Fotogalerie erkannt werden, damit Benutzer zu Ihrer Downloadwebsite weitergeleitet werden können, müssen Sie folgende Schritte ausführen:

1.  Stellen Sie eine Downloadwebsite für Ihren Codec bereit. (Sie können für jeden von Ihnen angegebenen Codec eine separate Seite oder eine Seite mit Downloads für alle Codecs verwenden.)

    Die Downloadwebsite sollte lokalisiert und nach Kameramodell leicht durchsuchbar sein.

2.  Stellen Sie Microsoft eine Liste der Erweiterungen für Ihre Imageformate und die URLs für Ihre Downloadwebsites bereit.

Sie müssen Microsoft über die Erweiterungen für neue Codecs informieren, die Sie in Zukunft entwickeln, sowie über änderungen an den URLs Ihrer Downloadwebsites, damit die neuen Informationen dem Windows Fotogalerie hinzugefügt werden können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Implementieren von IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[Schlussfolgerung (Schreiben eines WIC-Enabled CODEC)](-wic-howtowriteacodec-conclusion.md)
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



