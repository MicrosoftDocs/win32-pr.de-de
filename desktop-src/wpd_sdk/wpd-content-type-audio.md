---
description: '\_WPD-INHALTSTYP \_ \_ AUDIO'
ms.assetid: a3d84878-489b-489a-a67e-0e4d25ddd3f7
title: WPD_CONTENT_TYPE_AUDIO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd4aa78b7fa546fab9fe186265ca721e441860a2fc55c2ba0b384df377e1344b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842354"
---
# <a name="wpd_content_type_audio"></a>\_WPD-INHALTSTYP \_ \_ AUDIO

Ein Objekt, das seinen Typ als WPD \_ CONTENT \_ TYPE AUDIO \_ beschreibt, stellt eine Audiodatei dar, z. B. eine Windows Media Audio (WMA) oder MP3-Datei.

Dieser Objekttyp unterstützt die folgenden Eigenschaften.



| Eigenschaftsname                                                                                                         | Erforderlich oder optional                                                               |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [\_ \_ WPD-OBJEKT-ID](object-properties.md)                                                                | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zur Erstellungszeit nicht festlegen.     |
| [ÜBERGEORDNETE \_ \_ \_ WPD-OBJEKT-ID](object-properties.md)                                                 | Erforderlich.                                                                          |
| [\_WPD-OBJEKTNAME \_](object-properties.md)                                                            | Erforderlich, wenn das -Objekt eine Datei darstellt.                                          |
| [\_PERSISTENTE EINDEUTIGE ID DES \_ \_ \_ WPD-OBJEKTS](object-properties.md)                          | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zur Erstellungszeit nicht festlegen.     |
| [\_WPD-OBJEKTFORMAT \_](object-properties.md)                                                        | Erforderlich.                                                                          |
| [\_ \_ WPD-OBJEKTINHALTSTYP \_](object-properties.md)                                           | Erforderlich.                                                                          |
| [\_WPD-OBJEKT \_ ISHIDDEN](object-properties.md)                                                    | Erforderlich, wenn das Objekt ausgeblendet ist.                                                  |
| [WPD \_ OBJECT \_ ISSYSTEM](object-properties.md)                                                    | Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).              |
| [\_WPD-OBJEKTGRÖßE \_](object-properties.md)                                                            | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                                  |
| [\_ \_ URSPRÜNGLICHER \_ \_ DATEINAME DES WPD-OBJEKTS](object-properties.md)                              | Erforderlich, wenn das -Objekt eine Datei darstellt.                                          |
| [\_WPD-OBJEKT \_ NICHT \_ VERWENDBAR](object-properties.md)                                       | Empfohlen, wenn das Objekt nicht für die Nutzung durch das Gerät vorgesehen ist.              |
| [\_ \_ WPD-OBJEKTVERWEISE](object-properties.md)                                                | Erforderlich, wenn das Objekt Verweise auf andere Objekte hat.                            |
| [\_ \_ WPD-OBJEKTSCHLÜSSELWÖRTER](object-properties.md)                                                    | Optional.                                                                          |
| [\_ \_ WPD-OBJEKTSYNCHRONISIERUNGS-ID \_](object-properties.md)                                                     | Optional.                                                                          |
| [\_WPD-OBJEKT \_ IST \_ \_ DRM-GESCHÜTZT](object-properties.md)                                  | Erforderlich, wenn das Objekt durch drm-Technologie geschützt ist.                             |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                           | Optional.                                                                          |
| [ÄNDERUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                         | Empfohlen.                                                                       |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                         | Optional.                                                                          |
| [\_ \_ WPD-OBJEKTRÜCKVERWEISE \_](object-properties.md)                                                                | Empfohlen, wenn ein anderes Objekt auf das Objekt verweist.                         |
| [FUNKTIONALE \_ \_ \_ \_ OBJEKT-ID DES WPD-OBJEKTCONTAINERS \_](object-properties.md)     | Optional.                                                                          |
| [\_WPD-OBJEKT \_ GENERIERT \_ \_ MINIATURANSICHTEN AUS \_ RESSOURCE](object-properties.md) | Optional.                                                                          |
| [\_WPD-OBJEKT \_ KANN GELÖSCHT \_ WERDEN](object-properties.md)                                                                     | Erforderlich, wenn das Objekt gelöscht werden kann.                                             |
| [\_GEBIETSSCHEMA DER WPD-OBJEKTSPRACHE \_ \_](object-properties.md)                                                                | Optional.                                                                          |
| [WPD \_ MEDIA \_ TOTAL \_ BITRATE](media-properties.md)                                            | Empfohlen.                                                                       |
| [WPD \_ MEDIA \_ \_ BITRATE-TYP](media-properties.md)                                              | Optional.                                                                          |
| [WPD \_ MEDIA \_ COPYRIGHT](media-properties.md)                                                     | Optional.                                                                          |
| [\_INHALTS-ID DES WPD-MEDIENABONNEMENTS \_ \_ \_](media-properties.md)                       | Empfohlen, wenn dieses Objekt Inhalte aus einem Onlineabonnementdienst darstellt. |
| [ANZAHL DER \_ \_ WPD-MEDIENNUTZUNG \_](media-properties.md)                                                    | Empfohlen.                                                                       |
| [WPD \_ MEDIA \_ SKIP \_ COUNT](media-properties.md)                                                  | Optional.                                                                          |
| [ZEITPUNKT \_ \_ DES LETZTEN ZUGRIFFS \_ AUF WPD-MEDIEN \_](media-properties.md)                                 | Optional.                                                                          |
| [WPD \_ MEDIA \_ PARENTAL \_ RATING](media-properties.md)                                        | Optional.                                                                          |
| [WPD \_ MEDIA \_ META \_ GENRE](media-properties.md)                                                  | Optional.                                                                          |
| [WPD \_ MEDIA \_ COMPOSER](media-properties.md)                                                       | Optional.                                                                          |
| [EFFEKTIVE BEWERTUNG VON \_ WPD-MEDIEN \_ \_](media-properties.md)                                      | Optional.                                                                          |
| [\_ \_ WPD-MEDIENUNTERTITEL \_](media-properties.md)                                                    | Optional.                                                                          |
| [\_ \_ WPD-MEDIENVERÖFFENTLICHUNGSDATUM \_](media-properties.md)                                              | Empfohlen.                                                                       |
| [WPD \_ MEDIA \_ SAMPLE \_ RATE](media-properties.md)                                                | Optional.                                                                          |
| [WPD \_ MEDIA \_ STAR \_ RATING](media-properties.md)                                                | Empfohlen.                                                                       |
| [WPD \_ MEDIA \_ USER \_ EFFECTIVE \_ RATING](media-properties.md)                           | Empfohlen.                                                                       |
| [\_WPD-MEDIENTITEL \_](media-properties.md)                                                             | Erforderlich.                                                                          |
| [\_WPD-MEDIENDAUER \_](media-properties.md)                                                       | Erforderlich.                                                                          |
| [WPD \_ MEDIA \_ JETZT KAUFEN \_](media-properties.md)                                                        | Empfohlen.                                                                       |
| [\_ \_ WPD-MEDIENCODIERUNGSPROFIL \_](media-properties.md)                                      | Optional.                                                                          |
| [WPD \_ MEDIA \_ INTERPRET](media-properties.md)                                                                            | Empfohlen.                                                                       |
| [WPD \_ MEDIA \_ ALBUM \_ INTERPRET](media-properties.md)                                                                     | Empfohlen.                                                                       |
| [\_ \_ WPD-MEDIENQUELL-URL \_](media-properties.md)                                                                       | Optional.                                                                          |
| [ZIEL-URL FÜR \_ WPD-MEDIEN \_ \_](media-properties.md)                                                                  | Optional.                                                                          |
| [\_WPD-MEDIENBESCHREIBUNG \_](media-properties.md)                                                                       | Optional.                                                                          |
| [WPD \_ MEDIA \_ GENRE](media-properties.md)                                                                             | Optional.                                                                          |
| [\_ \_ \_ WPD-MEDIENZEITLESEZEICHEN](media-properties.md)                                                                    | Optional.                                                                          |
| [WPD \_ MEDIA \_ BYTE \_ BOOKMARK](media-properties.md)                                                                    | Optional.                                                                          |
| [WPD \_ MEDIA \_ GUID](media-properties.md)                                                                              | Optional.                                                                          |
| [\_ \_ WPD-MEDIENUNTERBESCHREIBUNG \_](media-properties.md)                                                                  | Optional.                                                                          |
| [WPD \_ MUSIC \_ ALBUM](music-properties.md)                                                             | Empfohlen.                                                                       |
| [WPD \_ MUSIC \_ TRACK](music-properties.md)                                                             | Empfohlen.                                                                       |
| [WPD \_ \_ MUSIC-GÄNGE](music-properties.md)                                                           | Optional.                                                                          |
| [WPD \_ \_ MUSIC-STIMMUNG](music-properties.md)                                                               | Optional.                                                                          |
| [WPD \_ AUDIO \_ BITRATE](audio-properties.md)                                                         | Empfohlen.                                                                       |
| [\_ \_ \_ WPD-AUDIOKANALANZAHL](audio-properties.md)                                            | Optional.                                                                          |
| [\_ \_ WPD-AUDIOFORMATCODE \_](audio-properties.md)                                                | Optional.                                                                          |
| [\_ \_ WPD-AUDIOBITTIEFE \_](audio-properties.md)                                                    | Optional.                                                                          |
| [\_ \_ WPD-AUDIOBLOCKAUSRICHTUNG \_](audio-properties.md)                                        | Optional.                                                                          |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte enthalten in der Regel die folgenden Ressourcen.



| Ressourcenname                                               | Erforderlich oder optional       | Beschreibung                                        |
|-------------------------------------------------------------|----------------------------|----------------------------------------------------|
| [**\_WPD-RESSOURCENSTANDARD \_**](wpd-resource-default.md)      | Optional.                  | Enthält die vollständige Audiodatei.                  |
| [**WPD \_ RESOURCE \_ ALBUM \_ ART**](wpd-resource-album-art.md) | Empfohlen, falls verfügbar. | Enthält das Bild für das Album.                |
| [**WPD \_ RESOURCE \_ AUDIOCLIP**](wpd-resource-audio-clip.md) | Optional.                  | Enthält einen Beispielclip der vollständigen Audiodatei. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 



