---
description: WPD \_ \_ -Inhaltstyp \_ Audiodatei
ms.assetid: a3d84878-489b-489a-a67e-0e4d25ddd3f7
title: WPD_CONTENT_TYPE_AUDIO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b83d43fcef539579fc0a687a97ba51e52278e4da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359452"
---
# <a name="wpd_content_type_audio"></a>WPD \_ \_ -Inhaltstyp \_ Audiodatei

Ein Objekt, das den Typ als WPD \_ \_ -Inhaltstyp \_ Audiodatei beschreibt, stellt eine Audiodatei dar, z. b. eine Windows Media Audio (WMA) oder eine MP3-Datei.

Dieser Objekttyp unterstützt die folgenden Eigenschaften.



| Eigenschaftsname                                                                                                         | Erforderlich oder optional                                                               |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [WPD- \_ Objekt- \_ ID](object-properties.md)                                                                | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zum Zeitpunkt der Erstellung nicht festlegen.     |
| [übergeordnete WPD- \_ Objekt- \_ \_ ID](object-properties.md)                                                 | Erforderlich.                                                                          |
| [WPD- \_ Objekt \_ Name](object-properties.md)                                                            | Erforderlich, wenn das-Objekt eine Datei darstellt.                                          |
| [\_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt](object-properties.md)                          | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zum Zeitpunkt der Erstellung nicht festlegen.     |
| [WPD- \_ Objekt \_ Format](object-properties.md)                                                        | Erforderlich.                                                                          |
| [Inhaltstyp für WPD- \_ Objekt \_ \_](object-properties.md)                                           | Erforderlich.                                                                          |
| [WPD- \_ Objekt \_ IsHidden](object-properties.md)                                                    | Erforderlich, wenn das Objekt ausgeblendet ist.                                                  |
| [WPD- \_ Objekt \_ IsSystem](object-properties.md)                                                    | Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).              |
| [WPD- \_ Objekt \_ Größe](object-properties.md)                                                            | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                                  |
| [\_ \_ ursprünglicher \_ Dateiname \_ des WPD-Objekts](object-properties.md)                              | Erforderlich, wenn das-Objekt eine Datei darstellt.                                          |
| [WPD- \_ Objekt \_ nicht \_ verwendbar](object-properties.md)                                       | Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist.              |
| [Verweise auf WPD- \_ Objekte \_](object-properties.md)                                                | Erforderlich, wenn das-Objekt über Verweise auf andere-Objekte verfügt.                            |
| [WPD- \_ Objekt \_ Schlüsselwörter](object-properties.md)                                                    | Dies ist optional.                                                                          |
| [WPD- \_ Objekt \_ Synchronisierungs- \_ ID](object-properties.md)                                                     | Dies ist optional.                                                                          |
| [WPD- \_ Objekt \_ ist DRM- \_ \_ geschützt](object-properties.md)                                  | Erforderlich, wenn das Objekt durch DRM-Technologie geschützt wird.                             |
| [\_ \_ Erstellungsdatum des WPD-Objekts \_](object-properties.md)                                           | Dies ist optional.                                                                          |
| [Datum des WPD- \_ Objekts \_ \_ geändert](object-properties.md)                                         | Empfohlen.                                                                       |
| [erstelltes WPD- \_ Objekt \_ Datum \_](object-properties.md)                                         | Dies ist optional.                                                                          |
| [\_ \_ zurück \_ Verweise auf WPD-Objekte](object-properties.md)                                                                | Empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.                         |
| [\_ \_ \_ Funktions \_ Objekt- \_ ID des WPD-Objekt Containers](object-properties.md)     | Dies ist optional.                                                                          |
| [WPD \_ - \_ Objekt \_ generieren \_ der Miniaturansicht aus der \_ Ressource](object-properties.md) | Dies ist optional.                                                                          |
| [WPD- \_ Objekt \_ kann \_ Löschen](object-properties.md)                                                                     | Erforderlich, wenn das Objekt gelöscht werden kann.                                             |
| [Gebiets Schema der WPD- \_ Objekt \_ Sprache \_](object-properties.md)                                                                | Dies ist optional.                                                                          |
| [WPD- \_ Medien \_ Gesamt- \_ Bitrate](media-properties.md)                                            | Empfohlen.                                                                       |
| [Typ der WPD- \_ Medien \_ Bitrate \_](media-properties.md)                                              | Dies ist optional.                                                                          |
| [Copyright von WPD- \_ Medien \_](media-properties.md)                                                     | Dies ist optional.                                                                          |
| [Inhalts-ID des WPD- \_ Medien \_ Abonnements \_ \_](media-properties.md)                       | Empfohlen, wenn dieses Objekt Inhalt aus einem Online Abonnement Dienst darstellt. |
| [Verwendung der WPD- \_ Medien \_ \_ Anzahl](media-properties.md)                                                    | Empfohlen.                                                                       |
| [Anzahl der \_ Skip-Medien für WPD \_ \_](media-properties.md)                                                  | Dies ist optional.                                                                          |
| [Zeitpunkt des \_ \_ letzten \_ Zugriffs \_ auf WPD-Medien](media-properties.md)                                 | Dies ist optional.                                                                          |
| [\_ \_ Eltern \_ Bewertung für WPD-Medien](media-properties.md)                                        | Dies ist optional.                                                                          |
| [WPD \_ - \_ medienmeta- \_ Genre](media-properties.md)                                                  | Dies ist optional.                                                                          |
| [WPD \_ Media \_ Composer](media-properties.md)                                                       | Dies ist optional.                                                                          |
| [\_ \_ effektive \_ Bewertung von WPD-Medien](media-properties.md)                                      | Dies ist optional.                                                                          |
| [\_ \_ unter \_ Titel der WPD-Medien](media-properties.md)                                                    | Dies ist optional.                                                                          |
| [\_ \_ Veröffentlichungs \_ Datum für WPD-Medien](media-properties.md)                                              | Empfohlen.                                                                       |
| [WPD- \_ Medien \_ Stichproben \_ Rate](media-properties.md)                                                | Dies ist optional.                                                                          |
| [Bewertung der WPD \_ \_ -Medien Sterne \_](media-properties.md)                                                | Empfohlen.                                                                       |
| [effektive Bewertung der WPD- \_ Medien \_ Benutzer \_ \_](media-properties.md)                           | Empfohlen.                                                                       |
| [WPD- \_ Medien \_ Titel](media-properties.md)                                                             | Erforderlich.                                                                          |
| [Dauer der WPD- \_ Medien \_](media-properties.md)                                                       | Erforderlich.                                                                          |
| [WPD \_ - \_ Medien \_ Jetzt kaufen](media-properties.md)                                                        | Empfohlen.                                                                       |
| [WPD- \_ Medien \_ Codierungs \_ Profil](media-properties.md)                                      | Dies ist optional.                                                                          |
| [WPD- \_ Medien \_ Künstler](media-properties.md)                                                                            | Empfohlen.                                                                       |
| [WPD \_ Media \_ Album- \_ Künstler](media-properties.md)                                                                     | Empfohlen.                                                                       |
| [WPD- \_ Medien \_ Quellen- \_ URL](media-properties.md)                                                                       | Dies ist optional.                                                                          |
| [Ziel-URL für WPD- \_ Medien \_ \_](media-properties.md)                                                                  | Dies ist optional.                                                                          |
| [WPD- \_ Medien \_ Beschreibung](media-properties.md)                                                                       | Dies ist optional.                                                                          |
| [WPD- \_ Medien \_ Genre](media-properties.md)                                                                             | Dies ist optional.                                                                          |
| [Lesezeichen für WPD- \_ Medien \_ Zeit \_](media-properties.md)                                                                    | Dies ist optional.                                                                          |
| [WPD- \_ Medien \_ Byte- \_ Lesezeichen](media-properties.md)                                                                    | Dies ist optional.                                                                          |
| [WPD- \_ Medien- \_ GUID](media-properties.md)                                                                              | Dies ist optional.                                                                          |
| [\_ \_ unter \_ Beschreibung der WPD-Medien](media-properties.md)                                                                  | Dies ist optional.                                                                          |
| [WPD \_ Musik- \_ Album](music-properties.md)                                                             | Empfohlen.                                                                       |
| [WPD- \_ Musik \_ Titel](music-properties.md)                                                             | Empfohlen.                                                                       |
| [WPD- \_ Musik- \_ Liedtexte](music-properties.md)                                                           | Dies ist optional.                                                                          |
| [WPD \_ Musik \_ Stimmung](music-properties.md)                                                               | Dies ist optional.                                                                          |
| [WPD \_ - \_ Audiobitrate](audio-properties.md)                                                         | Empfohlen.                                                                       |
| [Anzahl von WPD \_ - \_ Audiokanälen \_](audio-properties.md)                                            | Dies ist optional.                                                                          |
| [WPD \_ - \_ \_ audioformatcode](audio-properties.md)                                                | Dies ist optional.                                                                          |
| [WPD \_ - \_ \_ audiobittiefe](audio-properties.md)                                                    | Dies ist optional.                                                                          |
| [WPD \_ - \_ Audioblock \_ Ausrichtung](audio-properties.md)                                        | Dies ist optional.                                                                          |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte enthalten in der Regel die folgenden Ressourcen.



| Ressourcenname                                               | Erforderlich oder optional       | BESCHREIBUNG                                        |
|-------------------------------------------------------------|----------------------------|----------------------------------------------------|
| [**WPD- \_ Ressourcen \_ Standard**](wpd-resource-default.md)      | Dies ist optional.                  | Enthält die gesamte Audiodatei.                  |
| [**WPD- \_ Ressourcen \_ Album- \_ Grafik**](wpd-resource-album-art.md) | Empfohlen, falls verfügbar. | Enthält das Bild für das Album.                |
| [**WPD- \_ Ressource \_ Audioclip**](wpd-resource-audio-clip.md) | Dies ist optional.                  | Enthält einen beispielclip der kompletten Audiodatei. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 



