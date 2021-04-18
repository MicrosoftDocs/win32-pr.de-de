---
description: Wenn Sie einen Codec installieren, müssen Sie ihn in der Registrierung registrieren. Sie müssen auch sicherstellen, dass der Miniatur Ansichts Cache aktualisiert wird, falls bereits Bilder in Ihrem Format auf dem Computer vorhanden sind.
ms.assetid: 7aec54cb-40ac-495c-99d9-9c397b740b21
title: Codec-Installation und-Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83616071bebdbab14bfdc7dd0f879df3d49789d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368814"
---
# <a name="codec-installation-and-registration"></a>Codec-Installation und-Registrierung

Wenn Sie einen Codec installieren, müssen Sie ihn in der Registrierung registrieren. Sie müssen auch sicherstellen, dass der Miniatur Ansichts Cache aktualisiert wird, falls bereits Bilder in Ihrem Format auf dem Computer vorhanden sind.

Dieses Thema enthält folgende Abschnitte:

-   [Registrieren eines Codecs](#registering-a-codec)
-   [Aktualisieren des Miniatur Ansichts Caches bei der Installation Ihres Codecs](#updating-the-thumbnail-cache-when-installing-your-codec)
-   [Verfügbar machung Ihres WIC-Enabled Codecs für Benutzer](#making-your-wic-enabled-codec-available-to-users)
-   [Zugehörige Themen](#related-topics)

## <a name="registering-a-codec"></a>Registrieren eines Codecs

Wenn Sie einen Codec registrieren, registrieren Sie tatsächlich zwei Komponenten: den Encoder und den Decoder. Sie müssen auch Registrierungseinträge erstellen, um Ihr Containerformat bei den metadatenhandlern für die Metadatenformate zu registrieren, die von Ihrem Bildformat unterstützt werden.

In den folgenden Themen werden die Registrierungseinträge beschrieben, die Sie benötigen, um Ihren Codec zu registrieren:

[Allgemeine Registrierungseinträge](-wic-generalregentries.md)

[Codierungs spezifische Registrierungseinträge](-wic-encoderregentries.md)

[Decoderspezifische Registrierungseinträge](-wic-decoderregentries.md)

[Integration in Windows Photo Gallery und Windows-Explorer](-wic-integrationregentries.md)

## <a name="updating-the-thumbnail-cache-when-installing-your-codec"></a>Aktualisieren des Miniatur Ansichts Caches bei der Installation Ihres Codecs

Wenn ein Codec installiert ist, muss das Installationsprogramm die folgende Funktion nach dem Schreiben der zugehörigen Registrierungseinträge aufruft.


```C++
SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_IDLIST, NULL, NULL)
```



Dieser Befehl benachrichtigt Windows, dass neue Datei Zuordnungs Informationen verfügbar sind. Wenn bereits Bilder im Bildformat auf dem Computer vorhanden sind, enthält der Miniatur Ansichts Cache standardmäßige Miniaturansichten für diese, da kein Decoder zum Extrahieren der Miniaturansichten verfügbar war, als die Bilder zum ersten mal abgerufen wurden. Wenn Sie Windows Benachrichtigen, dass eine neue Datei Zuordnung verfügbar ist, verwirft der Miniatur Ansichts Cache alle leeren Miniaturansichten und extrahiert die eigentlichen Miniaturansichten aus den Dateien, die nun decodiert werden können.

## <a name="making-your-wic-enabled-codec-available-to-users"></a>Verfügbar machung Ihres WIC-Enabled Codecs für Benutzer

Wenn Sie ein Kamerahersteller sind, können Sie Ihre unformatierten Codecs in der Box mit ihren Kameras versenden. Sie können Ihre Codecs auch auf der Download Seite Ihrer Website veröffentlichen. Wenn ein Benutzer jedoch eine Bilddatei in Ihrem Format aus einer anderen Quelle, z. b. einem Friend, einem Geschäftspartner oder einer anderen Website, erhält, wissen Sie möglicherweise nicht, wo der Codec zum Decodieren des Codecs zu finden ist.

Aufgrund dieses Problems bietet Windows eine einfachere Möglichkeit für Benutzer Ihres Bildformats, ihren Codec zu finden und auf Ihren Computer herunterzuladen, beginnend mit Windows Vista. Wenn die Windows-Fotogalerie eine Dateinamenerweiterung als Bildformat erkennt und der Codec für dieses Format nicht installiert ist, wird dem Benutzer in einem Dialogfeld mitgeteilt, dass das Foto nicht angezeigt werden kann, und es wird gefragt, ob der Benutzer die für die Anzeige erforderliche Software herunterladen möchte. Wenn der Benutzer akzeptiert, wird eine von Microsoft gehostete Website mit einem Link zur Download Site des Codec-Herstellers angezeigt. (Optional können Sie anfordern, dass Benutzer direkt zu Ihrer Download Site gelangen.)

Wenn Sie möchten, dass die Dateinamen Erweiterungen Ihres Bildformats von der Windows-Fotogalerie erkannt werden, damit Benutzer zu Ihrer Download Website weitergeleitet werden können, müssen Sie die folgenden Schritte ausführen:

1.  Stellen Sie eine Download Site für Ihren Codec bereit. (Sie können für jeden von Ihnen bereitgestellten CODEC eine separate Seite oder eine Seite mit Downloads für alle Ihre Codecs bereitstellen.)

    Die Download Site sollte lokalisiert und problemlos nach Kameramodell durchsuchbar sein.

2.  Geben Sie Microsoft eine Liste mit Erweiterungen für Ihre Bildformate und die URLs für die Download Websites.

Sie müssen Microsoft über die Erweiterungen für alle neuen Codecs informieren, die Sie in Zukunft entwickeln, und über alle Änderungen an den URLs Ihrer Download Websites, damit die neuen Informationen der Windows-Fotogalerie hinzugefügt werden können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Implementieren von IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[Schlussfolgerung (Schreiben eines WIC-Enabled Codecs)](-wic-howtowriteacodec-conclusion.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



