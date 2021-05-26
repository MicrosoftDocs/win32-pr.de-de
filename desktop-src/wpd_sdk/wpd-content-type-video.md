---
description: WPD \_ CONTENT \_ TYPE \_ VIDEO
ms.assetid: d4a6bd98-c28e-487b-95cc-2c73cd44e3b5
title: WPD_CONTENT_TYPE_VIDEO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aacf30a9e646a6089058104bd39577fad832e31
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424121"
---
# <a name="wpd_content_type_video"></a>WPD \_ CONTENT \_ TYPE \_ VIDEO

Ein Objekt, das seinen Typ als WPD \_ CONTENT \_ TYPE VIDEO \_ beschreibt, stellt eine Videodatei dar.

Dieser Objekttyp unterstützt die folgenden Eigenschaften.



|  Eigenschaftsname                             | Erforderlich oder optional              |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [\_WPD-OBJEKT-ID \_](object-properties.md)                                                                | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft nicht festlegen, auch nicht zum Zeitpunkt der Erstellung.                                               |
| [ÜBERGEORDNETE ID DES \_ \_ WPD-OBJEKTS \_](object-properties.md)                                                 | Erforderlich.                                                                                                                    |
| [\_WPD-OBJEKTNAME \_](object-properties.md)                                                            | Erforderlich, wenn das -Objekt eine Datei darstellt.                                                                                    |
| [PERSISTENTE EINDEUTIGE ID \_ DES WPD-OBJEKTS \_ \_ \_](object-properties.md)                          | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft nicht festlegen, auch nicht zum Zeitpunkt der Erstellung.                                               |
| [\_WPD-OBJEKTFORMAT \_](object-properties.md)                                                        | Erforderlich.                                                                                                                    |
| [\_ \_ WPD-OBJEKTINHALTSTYP \_](object-properties.md)                                           | Erforderlich.                                                                                                                    |
| [\_WPD-OBJEKT \_ ISHIDDEN](object-properties.md)                                                    | Erforderlich, wenn das Objekt ausgeblendet ist.                                                                                            |
| [\_WPD-OBJEKT \_ ISSYSTEM](object-properties.md)                                                    | Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).                                                        |
| [\_WPD-OBJEKTGRÖßE \_](object-properties.md)                                                            | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                                                                            |
| [\_ \_ URSPRÜNGLICHER \_ \_ DATEINAME DES WPD-OBJEKTS](object-properties.md)                              | Erforderlich, wenn das -Objekt eine Datei darstellt.                                                                                    |
| [\_WPD-OBJEKT \_ NICHT \_ VERWENDBAR](object-properties.md)                                       | Empfohlen, wenn das Objekt nicht für die Nutzung durch das Gerät vorgesehen ist.                                                        |
| [\_ \_ WPD-OBJEKTVERWEISE](object-properties.md)                                                | Erforderlich, wenn das Objekt Verweise auf andere Objekte hat.                                                                      |
| [\_ \_ WPD-OBJEKTSCHLÜSSELWÖRTER](object-properties.md)                                                    | Dies ist optional.                                                                                                                    |
| [\_ \_ WPD-OBJEKTSYNCHRONISIERUNGS-ID \_](object-properties.md)                                                     | Dies ist optional.                                                                                                                    |
| [\_WPD-OBJEKT \_ IST \_ \_ DRM-GESCHÜTZT](object-properties.md)                                  | Erforderlich, wenn das Objekt durch drm-Technologie geschützt ist.                                                                       |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                           | Dies ist optional.                                                                                                                    |
| [ÄNDERUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                         | Empfohlen.                                                                                                                 |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                         | Dies ist optional.                                                                                                                    |
| [\_ \_ WPD-OBJEKTRÜCKVERWEISE \_](object-properties.md)                                                                | Empfohlen, wenn ein anderes Objekt auf das Objekt verweist.                                                                   |
| [FUNKTIONALE \_ \_ \_ \_ OBJEKT-ID DES WPD-OBJEKTCONTAINERS \_](object-properties.md)     | Dies ist optional.                                                                                                                    |
| [\_WPD-OBJEKT \_ GENERIERT \_ \_ MINIATURANSICHTEN AUS \_ RESSOURCE](object-properties.md) | Dies ist optional.                                                                                                                    |
| [\_WPD-OBJEKT \_ KANN LÖSCHEN \_](object-properties.md)                                                                     | Erforderlich, wenn das Objekt nicht gelöscht werden kann.                                                                                    |
| [WPD \_ OBJECT \_ LANGUAGE \_ LOCALE](object-properties.md)                                                                | Dies ist optional.                                                                                                                    |
| [WPD \_ MEDIA \_ TOTAL \_ BITRATE](media-properties.md)                                            | Empfohlen.                                                                                                                 |
| [WPD \_ MEDIA \_ \_ BITRATE-TYP](media-properties.md)                                              | Dies ist optional.                                                                                                                    |
| [\_WPD-MEDIEN \_ COPYRIGHT](media-properties.md)                                                     | Dies ist optional.                                                                                                                    |
| [WPD \_ MEDIA SUBSCRIPTION CONTENT ID \_ \_ (INHALTS-ID DES WPD-MEDIENABONNEMENTS) \_](media-properties.md)                       | Empfohlen, wenn dieses Objekt Inhalte eines Onlineabonnementdiensts darstellt.                                          |
| [ANZAHL DER \_ \_ WPD-MEDIENNUTZUNGEN \_](media-properties.md)                                                    | Empfohlen.                                                                                                                 |
| [ANZAHL DER \_ ÜBERSPRUNGENEN WPD-MEDIEN \_ \_](media-properties.md)                                                  | Dies ist optional.                                                                                                                    |
| [ZEITPUNKT DES \_ LETZTEN \_ ZUGRIFFES AUF WPD-MEDIEN \_ \_](media-properties.md)                                 | Dies ist optional.                                                                                                                    |
| [WPD \_ \_ MEDIA-JUGENDBEWERTUNG \_](media-properties.md)                                        | Dies ist optional.                                                                                                                    |
| [WPD \_ MEDIA \_ META \_ GENRE](media-properties.md)                                                  | Dies ist optional.                                                                                                                    |
| [WPD \_ MEDIA \_ COMPOSER](media-properties.md)                                                       | Dies ist optional.                                                                                                                    |
| [WPD \_ MEDIA \_ EFFECTIVE \_ RATING](media-properties.md)                                      | Dies ist optional.                                                                                                                    |
| [WPD \_ MEDIA \_ SUB \_ TITLE](media-properties.md)                                                    | Dies ist optional.                                                                                                                    |
| [\_ \_ WPD-MEDIENVERÖFFENTLICHUNGSDATUM \_](media-properties.md)                                              | Empfohlen.                                                                                                                 |
| [WPD \_ MEDIA \_ SAMPLE \_ RATE](media-properties.md)                                                | Dies ist optional.                                                                                                                    |
| [WPD \_ MEDIA \_ STAR \_ RATING](media-properties.md)                                                | Empfohlen.                                                                                                                 |
| [WPD MEDIA USER EFFECTIVE RATING (EFFEKTIVE BEWERTUNG \_ DES WPD-MEDIENBENUTZERS) \_ \_ \_](media-properties.md)                           | Empfohlen.                                                                                                                 |
| [\_WPD-MEDIENTITEL \_](media-properties.md)                                                             | Erforderlich.                                                                                                                    |
| [\_WPD-MEDIENDAUER \_](media-properties.md)                                                       | Erforderlich.                                                                                                                    |
| [WPD \_ MEDIA \_ JETZT KAUFEN \_](media-properties.md)                                                        | Empfohlen.                                                                                                                 |
| [\_ \_ WPD-MEDIENCODIERUNGSPROFIL \_](media-properties.md)                                      | Dies ist optional.                                                                                                                    |
| [\_WPD-MEDIENBREITE \_](media-properties.md)                                                             | Erforderlich.                                                                                                                    |
| [\_WPD-MEDIENHÖHE \_](media-properties.md)                                                           | Erforderlich.                                                                                                                    |
| [WPD \_ MEDIA \_ INTERPRET](media-properties.md)                                                           | Empfohlen.                                                                                                                 |
| [\_ \_ WPD-MEDIENQUELL-URL \_](media-properties.md)                                                  | Empfohlen.                                                                                                                 |
| [ZIEL-URL FÜR \_ WPD-MEDIEN \_ \_](media-properties.md)                                        | Dies ist optional.                                                                                                                    |
| [\_WPD-MEDIENBESCHREIBUNG \_](media-properties.md)                                                 | Dies ist optional.                                                                                                                    |
| [WPD \_ MEDIA \_ GENRE](media-properties.md)                                                             | Dies ist optional.                                                                                                                    |
| [\_ \_ \_ WPD-MEDIENZEITLESEZEICHEN](media-properties.md)                                            | Dies ist optional.                                                                                                                    |
| [WPD \_ MEDIA \_ BYTE \_ BOOKMARK](media-properties.md)                                            | Dies ist optional.                                                                                                                    |
| [WPD \_ MEDIA \_ GUID](media-properties.md)                                                               | Dies ist optional.                                                                                                                    |
| [\_ \_ WPD-MEDIENUNTERBESCHREIBUNG \_](media-properties.md)                                        | Dies ist optional.                                                                                                                    |
| [WPD \_ VIDEO \_ AUTHOR](video-properties.md)                                                           | Dies ist optional.                                                                                                                    |
| [WPD \_ VIDEO \_ RECORDEDTV \_ STATION \_ NAME](video-properties.md)                       | Dies ist optional.                                                                                                                    |
| [\_WPD-VIDEO \_ \_ AUFGEZEICHNETTV-KANALNUMMER \_](video-properties.md)                   | Dies ist optional.                                                                                                                    |
| [WPD \_ VIDEO \_ RECORDEDTV \_ REPEAT](video-properties.md)                                    | Dies ist optional.                                                                                                                    |
| [\_ \_ WPD-VIDEOPUFFERGRÖßE \_](video-properties.md)                                                | Dies ist optional.                                                                                                                    |
| [\_WPD-VIDEOGUTHABEN \_](video-properties.md)                                                         | Dies ist optional.                                                                                                                    |
| [WPD \_ VIDEO \_ KEY \_ FRAME \_ DISTANCE](video-properties.md)                                 | Dies ist optional.                                                                                                                    |
| [\_ \_ WPD-VIDEOQUALITÄTSEINSTELLUNG \_](video-properties.md)                                        | Dies ist optional.                                                                                                                    |
| [\_ \_ WPD-VIDEOSCANTYP \_](video-properties.md)                                                    | Erforderlich.                                                                                                                    |
| [WPD \_ VIDEO \_ BITRATE](video-properties.md)                                                         | Erforderlich.                                                                                                                    |
| [WPD \_ VIDEO \_ FOURCC \_ CODE](video-properties.md)                                                | Erforderlich, wenn der Codec von Microsoft Video für Windows (VFW), Microsoft DirectShow und Windows Media Format unterstützt wird. |
| [WPD \_ VIDEO \_ FRAMERATE](video-properties.md)                                                     | Dies ist optional.                                                                                                                    |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte enthalten in der Regel die folgenden Ressourcen.



| Ressourcenname                                              | Erforderlich oder optional       | BESCHREIBUNG                                                          |
|------------------------------------------------------------|----------------------------|----------------------------------------------------------------------|
| [**WPD \_ RESOURCE \_ DEFAULT**](wpd-resource-default.md)     | Erforderlich.                  | Enthält die Videodaten (Datei).                                      |
| [**\_WPD-RESSOURCENMINIATURANSICHT \_**](wpd-resource-thumbnail.md) | Empfohlen, falls verfügbar. | Enthält den Keyframe oder einen anderen nicht verfügbaren Beispielrahmen für das Video. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 



