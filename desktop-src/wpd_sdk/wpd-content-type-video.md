---
description: Video zum WPD- \_ \_ Inhaltstyp \_
ms.assetid: d4a6bd98-c28e-487b-95cc-2c73cd44e3b5
title: WPD_CONTENT_TYPE_VIDEO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afde065ef233ff64a4eb72af8be5f7308050ff75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366094"
---
# <a name="wpd_content_type_video"></a>Video zum WPD- \_ \_ Inhaltstyp \_

Ein-Objekt, das den Typ des WPD- \_ \_ Inhaltstyp Videos beschreibt, \_ stellt eine Videodatei dar.

Dieser Objekttyp unterstützt die folgenden Eigenschaften.



|                                                                                                                       |                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| **Eigenschaftenname**                                                                                                     | **Erforderlich oder optional**                                                                                                     |
| [WPD- \_ Objekt- \_ ID](object-properties.md)                                                                | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zum Zeitpunkt der Erstellung nicht festlegen.                                               |
| [übergeordnete WPD- \_ Objekt- \_ \_ ID](object-properties.md)                                                 | Erforderlich.                                                                                                                    |
| [WPD- \_ Objekt \_ Name](object-properties.md)                                                            | Erforderlich, wenn das-Objekt eine Datei darstellt.                                                                                    |
| [\_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt](object-properties.md)                          | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zum Zeitpunkt der Erstellung nicht festlegen.                                               |
| [WPD- \_ Objekt \_ Format](object-properties.md)                                                        | Erforderlich.                                                                                                                    |
| [Inhaltstyp für WPD- \_ Objekt \_ \_](object-properties.md)                                           | Erforderlich.                                                                                                                    |
| [WPD- \_ Objekt \_ IsHidden](object-properties.md)                                                    | Erforderlich, wenn das Objekt ausgeblendet ist.                                                                                            |
| [WPD- \_ Objekt \_ IsSystem](object-properties.md)                                                    | Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).                                                        |
| [WPD- \_ Objekt \_ Größe](object-properties.md)                                                            | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                                                                            |
| [\_ \_ ursprünglicher \_ Dateiname \_ des WPD-Objekts](object-properties.md)                              | Erforderlich, wenn das-Objekt eine Datei darstellt.                                                                                    |
| [WPD- \_ Objekt \_ nicht \_ verwendbar](object-properties.md)                                       | Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist.                                                        |
| [Verweise auf WPD- \_ Objekte \_](object-properties.md)                                                | Erforderlich, wenn das-Objekt über Verweise auf andere-Objekte verfügt.                                                                      |
| [WPD- \_ Objekt \_ Schlüsselwörter](object-properties.md)                                                    | Dies ist optional.                                                                                                                    |
| [WPD- \_ Objekt \_ Synchronisierungs- \_ ID](object-properties.md)                                                     | Dies ist optional.                                                                                                                    |
| [WPD- \_ Objekt \_ ist DRM- \_ \_ geschützt](object-properties.md)                                  | Erforderlich, wenn das Objekt durch DRM-Technologie geschützt wird.                                                                       |
| [\_ \_ Erstellungsdatum des WPD-Objekts \_](object-properties.md)                                           | Dies ist optional.                                                                                                                    |
| [Datum des WPD- \_ Objekts \_ \_ geändert](object-properties.md)                                         | Empfohlen.                                                                                                                 |
| [erstelltes WPD- \_ Objekt \_ Datum \_](object-properties.md)                                         | Dies ist optional.                                                                                                                    |
| [\_ \_ zurück \_ Verweise auf WPD-Objekte](object-properties.md)                                                                | Empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.                                                                   |
| [\_ \_ \_ Funktions \_ Objekt- \_ ID des WPD-Objekt Containers](object-properties.md)     | Dies ist optional.                                                                                                                    |
| [WPD \_ - \_ Objekt \_ generieren \_ der Miniaturansicht aus der \_ Ressource](object-properties.md) | Dies ist optional.                                                                                                                    |
| [WPD- \_ Objekt \_ kann \_ Löschen](object-properties.md)                                                                     | Erforderlich, wenn das Objekt nicht gelöscht werden kann.                                                                                    |
| [Gebiets Schema der WPD- \_ Objekt \_ Sprache \_](object-properties.md)                                                                | Dies ist optional.                                                                                                                    |
| [WPD- \_ Medien \_ Gesamt- \_ Bitrate](media-properties.md)                                            | Empfohlen.                                                                                                                 |
| [Typ der WPD- \_ Medien \_ Bitrate \_](media-properties.md)                                              | Dies ist optional.                                                                                                                    |
| [Copyright von WPD- \_ Medien \_](media-properties.md)                                                     | Dies ist optional.                                                                                                                    |
| [Inhalts-ID des WPD- \_ Medien \_ Abonnements \_ \_](media-properties.md)                       | Empfohlen, wenn dieses Objekt Inhalt aus einem Online Abonnement Dienst darstellt.                                          |
| [Verwendung der WPD- \_ Medien \_ \_ Anzahl](media-properties.md)                                                    | Empfohlen.                                                                                                                 |
| [Anzahl der \_ Skip-Medien für WPD \_ \_](media-properties.md)                                                  | Dies ist optional.                                                                                                                    |
| [Zeitpunkt des \_ \_ letzten \_ Zugriffs \_ auf WPD-Medien](media-properties.md)                                 | Dies ist optional.                                                                                                                    |
| [\_ \_ Eltern \_ Bewertung für WPD-Medien](media-properties.md)                                        | Dies ist optional.                                                                                                                    |
| [WPD \_ - \_ medienmeta- \_ Genre](media-properties.md)                                                  | Dies ist optional.                                                                                                                    |
| [WPD \_ Media \_ Composer](media-properties.md)                                                       | Dies ist optional.                                                                                                                    |
| [\_ \_ effektive \_ Bewertung von WPD-Medien](media-properties.md)                                      | Dies ist optional.                                                                                                                    |
| [\_ \_ unter \_ Titel der WPD-Medien](media-properties.md)                                                    | Dies ist optional.                                                                                                                    |
| [\_ \_ Veröffentlichungs \_ Datum für WPD-Medien](media-properties.md)                                              | Empfohlen.                                                                                                                 |
| [WPD- \_ Medien \_ Stichproben \_ Rate](media-properties.md)                                                | Dies ist optional.                                                                                                                    |
| [Bewertung der WPD \_ \_ -Medien Sterne \_](media-properties.md)                                                | Empfohlen.                                                                                                                 |
| [effektive Bewertung der WPD- \_ Medien \_ Benutzer \_ \_](media-properties.md)                           | Empfohlen.                                                                                                                 |
| [WPD- \_ Medien \_ Titel](media-properties.md)                                                             | Erforderlich.                                                                                                                    |
| [Dauer der WPD- \_ Medien \_](media-properties.md)                                                       | Erforderlich.                                                                                                                    |
| [WPD \_ - \_ Medien \_ Jetzt kaufen](media-properties.md)                                                        | Empfohlen.                                                                                                                 |
| [WPD- \_ Medien \_ Codierungs \_ Profil](media-properties.md)                                      | Dies ist optional.                                                                                                                    |
| [WPD- \_ Medien \_ Breite](media-properties.md)                                                             | Erforderlich.                                                                                                                    |
| [WPD- \_ Medien \_ Höhe](media-properties.md)                                                           | Erforderlich.                                                                                                                    |
| [WPD- \_ Medien \_ Künstler](media-properties.md)                                                           | Empfohlen.                                                                                                                 |
| [WPD- \_ Medien \_ Quellen- \_ URL](media-properties.md)                                                  | Empfohlen.                                                                                                                 |
| [Ziel-URL für WPD- \_ Medien \_ \_](media-properties.md)                                        | Dies ist optional.                                                                                                                    |
| [WPD- \_ Medien \_ Beschreibung](media-properties.md)                                                 | Dies ist optional.                                                                                                                    |
| [WPD- \_ Medien \_ Genre](media-properties.md)                                                             | Dies ist optional.                                                                                                                    |
| [Lesezeichen für WPD- \_ Medien \_ Zeit \_](media-properties.md)                                            | Dies ist optional.                                                                                                                    |
| [WPD- \_ Medien \_ Byte- \_ Lesezeichen](media-properties.md)                                            | Dies ist optional.                                                                                                                    |
| [WPD- \_ Medien- \_ GUID](media-properties.md)                                                               | Dies ist optional.                                                                                                                    |
| [\_ \_ unter \_ Beschreibung der WPD-Medien](media-properties.md)                                        | Dies ist optional.                                                                                                                    |
| [WPD- \_ Video \_ Autor](video-properties.md)                                                           | Dies ist optional.                                                                                                                    |
| [WPD-Video recorddebug- \_ \_ \_ Stations \_ Name](video-properties.md)                       | Dies ist optional.                                                                                                                    |
| [WPD-Video recorddebug- \_ \_ \_ Kanal \_ Nummer](video-properties.md)                   | Dies ist optional.                                                                                                                    |
| [WPD- \_ Video \_ recordebug \_ Wiederholen](video-properties.md)                                    | Dies ist optional.                                                                                                                    |
| [WPD- \_ Video \_ Puffer \_ Größe](video-properties.md)                                                | Dies ist optional.                                                                                                                    |
| [WPD- \_ Video \_ Gutschriften](video-properties.md)                                                         | Dies ist optional.                                                                                                                    |
| [WPD \_ - \_ Video \_ schlüsselframe- \_ Abstand](video-properties.md)                                 | Dies ist optional.                                                                                                                    |
| [WPD- \_ Video \_ Qualitäts \_ Einstellung](video-properties.md)                                        | Dies ist optional.                                                                                                                    |
| [WPD- \_ Video \_ Überprüfungstyp \_](video-properties.md)                                                    | Erforderlich.                                                                                                                    |
| [WPD- \_ Video \_ Bitrate](video-properties.md)                                                         | Erforderlich.                                                                                                                    |
| [WPD- \_ Video- \_ FourCC- \_ Code](video-properties.md)                                                | Erforderlich, wenn der Codec von Microsoft Video für Windows (Vfw), Microsoft DirectShow und Windows Media-Format unterstützt wird. |
| [WPD- \_ Video \_ Framerate](video-properties.md)                                                     | Dies ist optional.                                                                                                                    |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte enthalten in der Regel die folgenden Ressourcen.



| Ressourcenname                                              | Erforderlich oder optional       | BESCHREIBUNG                                                          |
|------------------------------------------------------------|----------------------------|----------------------------------------------------------------------|
| [**WPD- \_ Ressourcen \_ Standard**](wpd-resource-default.md)     | Erforderlich.                  | Enthält die Videodaten (Datei).                                      |
| [**WPD- \_ Ressourcen \_ Miniaturansicht**](wpd-resource-thumbnail.md) | Empfohlen, falls verfügbar. | Enthält den Keyframe oder einen anderen nicht leeren Sample Frame für das Video. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 



