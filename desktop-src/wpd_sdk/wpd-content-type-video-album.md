---
description: WPD \_ CONTENT \_ TYPE \_ VIDEO \_ ALBUM
ms.assetid: 0445a7de-1a2d-4369-b1f6-588fd6f2c999
title: WPD_CONTENT_TYPE_VIDEO_ALBUM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4f358ebf9b3a1dad14cc4354e8bd53e86b159be
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423910"
---
# <a name="wpd_content_type_video_album"></a>WPD \_ CONTENT \_ TYPE \_ VIDEO \_ ALBUM

Ein Objekt, das seinen Typ als WPD \_ CONTENT TYPE VIDEO ALBUM \_ \_ \_ beschreibt, stellt eine Sammlung von Videodateien dar. Ein Videoalb entspricht funktional einer Wiedergabeliste von Videodateien, wird jedoch verwendet, um dem Endbenutzer ein physisches Objekt zu zeigen.

Dieser Objekttyp unterstützt die folgenden Eigenschaften.



|  Eigenschaftsname                             | Erforderlich oder optional              |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [\_WPD-OBJEKT-ID \_](object-properties.md)                                                                | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft nicht festlegen, auch nicht zum Zeitpunkt der Erstellung. |
| [ÜBERGEORDNETE ID DES \_ \_ WPD-OBJEKTS \_](object-properties.md)                                                 | Erforderlich.                                                                      |
| [\_WPD-OBJEKTNAME \_](object-properties.md)                                                            | Erforderlich, wenn das -Objekt eine Datei darstellt.                                      |
| [PERSISTENTE EINDEUTIGE ID \_ DES WPD-OBJEKTS \_ \_ \_](object-properties.md)                          | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft nicht festlegen, auch nicht zum Zeitpunkt der Erstellung. |
| [\_WPD-OBJEKTFORMAT \_](object-properties.md)                                                        | Erforderlich.                                                                      |
| [\_ \_ WPD-OBJEKTINHALTSTYP \_](object-properties.md)                                           | Erforderlich.                                                                      |
| [\_WPD-OBJEKT \_ ISHIDDEN](object-properties.md)                                                    | Erforderlich, wenn das Objekt ausgeblendet ist.                                              |
| [WPD \_ OBJECT \_ ISSYSTEM](object-properties.md)                                                    | Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).          |
| [\_WPD-OBJEKTGRÖßE \_](object-properties.md)                                                            | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                              |
| [\_ \_ URSPRÜNGLICHER \_ \_ DATEINAME DES WPD-OBJEKTS](object-properties.md)                              | Erforderlich, wenn das -Objekt eine Datei darstellt.                                      |
| [\_WPD-OBJEKT \_ NICHT \_ VERWENDBAR](object-properties.md)                                       | Empfohlen, wenn das Objekt nicht für die Nutzung durch das Gerät vorgesehen ist.          |
| [\_ \_ WPD-OBJEKTVERWEISE](object-properties.md)                                                | Erforderlich, wenn das Objekt Verweise auf andere Objekte hat.                        |
| [\_ \_ WPD-OBJEKTSCHLÜSSELWÖRTER](object-properties.md)                                                    | Dies ist optional.                                                                      |
| [\_ \_ WPD-OBJEKTSYNCHRONISIERUNGS-ID \_](object-properties.md)                                                     | Dies ist optional.                                                                      |
| [\_WPD-OBJEKT \_ IST \_ \_ DRM-GESCHÜTZT](object-properties.md)                                  | Erforderlich, wenn das Objekt durch drm-Technologie geschützt ist.                         |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                           | Dies ist optional.                                                                      |
| [ÄNDERUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                         | Empfohlen.                                                                   |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                         | Dies ist optional.                                                                      |
| [\_ \_ WPD-OBJEKTRÜCKVERWEISE \_](object-properties.md)                                                                | Empfohlen, wenn ein anderes Objekt auf das Objekt verweist.                     |
| [FUNKTIONALE \_ \_ \_ \_ OBJEKT-ID DES WPD-OBJEKTCONTAINERS \_](object-properties.md)     | Dies ist optional.                                                                      |
| [\_WPD-OBJEKT \_ GENERIERT \_ \_ MINIATURANSICHT AUS \_ RESSOURCE](object-properties.md) | Dies ist optional.                                                                      |
| [\_WPD-OBJEKT \_ KANN LÖSCHEN \_](object-properties.md)                                                                     | Erforderlich, wenn das Objekt nicht gelöscht werden kann.                                      |
| [WPD \_ OBJECT \_ LANGUAGE \_ LOCALE](object-properties.md)                                                                | Dies ist optional.                                                                      |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte hosten in der Regel keine Ressourcen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 



