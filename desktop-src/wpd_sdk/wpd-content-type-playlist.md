---
description: '\_WIEDERGABELISTE DES WPD-INHALTSTYPS \_ \_'
ms.assetid: 4223970d-8c37-4326-a2df-bec558f8ac5e
title: WPD_CONTENT_TYPE_PLAYLIST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de97169b4858b48b9bf8e8a0dc7fc365961cc519
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423760"
---
# <a name="wpd_content_type_playlist"></a>\_WIEDERGABELISTE DES WPD-INHALTSTYPS \_ \_

Ein Objekt, das seinen Typ als WPD CONTENT TYPE PLAYLIST beschreibt, \_ \_ stellt eine \_ Wiedergabeliste dar. Eine Wiedergabeliste kann durch eine physische Datei dargestellt werden, oder sie kann aus Verweisen bestehen, die als Metadaten gespeichert sind.

Dieser Objekttyp unterstützt die folgenden Eigenschaften.



| Eigenschaftsname           | Erforderlich oder optional                 |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_ \_ WPD-OBJEKT-ID](object-properties.md)                                                                | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft nicht einmal zur Erstellungszeit festlegen.                                                                  |
| [ÜBERGEORDNETE \_ \_ \_ WPD-OBJEKT-ID](object-properties.md)                                                 | Erforderlich.                                                                                                                                      |
| [\_WPD-OBJEKTNAME \_](object-properties.md)                                                            | Erforderlich, wenn das -Objekt eine Datei darstellt.                                                                                                      |
| [\_PERSISTENTE EINDEUTIGE ID DES \_ \_ \_ WPD-OBJEKTS](object-properties.md)                          | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zur Erstellungszeit nicht festlegen.                                                                 |
| [\_WPD-OBJEKTFORMAT \_](object-properties.md)                                                        | Erforderlich.                                                                                                                                      |
| [\_ \_ WPD-OBJEKTINHALTSTYP \_](object-properties.md)                                           | Erforderlich.                                                                                                                                      |
| [\_WPD-OBJEKT \_ ISHIDDEN](object-properties.md)                                                    | Erforderlich, wenn das Objekt ausgeblendet ist.                                                                                                              |
| [\_WPD-OBJEKT \_ ISSYSTEM](object-properties.md)                                                    | Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).                                                                          |
| [\_WPD-OBJEKTGRÖßE \_](object-properties.md)                                                            | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                                                                                              |
| [\_WPD-OBJEKT \_ \_ URSPRÜNGLICHER \_ DATEINAME](object-properties.md)                              | Erforderlich, wenn das -Objekt eine Datei darstellt.                                                                                                      |
| [\_WPD-OBJEKT \_ NICHT \_ VERWENDBAR](object-properties.md)                                       | Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist.                                                                          |
| [\_ \_ WPD-OBJEKTVERWEISE](object-properties.md)                                                | Erforderlich, wenn das Objekt Verweise auf andere Objekte enthält. Das heißt, wenn die Verweise als Metadaten und nicht als physische Daten in einer Datei gespeichert werden. |
| [\_WPD-OBJEKTSCHLÜSSELWÖRTER \_](object-properties.md)                                                    | Dies ist optional.                                                                                                                                      |
| [\_ \_ WPD-OBJEKTSYNCHRONISIERUNGS-ID \_](object-properties.md)                                                     | Dies ist optional.                                                                                                                                      |
| [\_WPD-OBJEKT \_ IST \_ \_ DRM-GESCHÜTZT](object-properties.md)                                  | Erforderlich, wenn das Objekt durch DRM-Technologie geschützt ist.                                                                                         |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                           | Dies ist optional.                                                                                                                                      |
| [\_WPD-OBJEKTDATUM \_ \_ GEÄNDERT](object-properties.md)                                         | Empfohlen.                                                                                                                                   |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                         | Dies ist optional.                                                                                                                                      |
| [WPD \_ OBJECT BACK REFERENCES (WPD-OBJEKTVERWEISE \_ \_ ZURÜCK)](object-properties.md)                                                                | Wird empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.                                                                                     |
| [\_ \_ WPD-OBJEKTCONTAINER \_ FUNKTIONALE \_ \_ OBJEKT-ID](object-properties.md)     | Dies ist optional.                                                                                                                                      |
| [\_WPD-OBJEKT \_ GENERIERT \_ \_ MINIATURANSICHTEN AUS \_ RESSOURCE](object-properties.md) | Dies ist optional.                                                                                                                                      |
| [\_WPD-OBJEKT \_ KANN GELÖSCHT \_ WERDEN](object-properties.md)                                                                     | Erforderlich, wenn das Objekt nicht gelöscht werden kann.                                                                                                      |
| [\_GEBIETSSCHEMA DER WPD-OBJEKTSPRACHE \_ \_](object-properties.md)                                                                | Dies ist optional.                                                                                                                                      |
| [\_ \_ \_ WPD-MEDIENOBJEKTLESEZEICHEN](object-properties.md)                                                                 | Empfohlen.                                                                                                                                   |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte enthalten in der Regel die folgenden Ressourcen.



| Ressourcenname                                          | Erforderlich oder optional | BESCHREIBUNG                                                                                                                  |
|--------------------------------------------------------|----------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**\_WPD-RESSOURCENSTANDARD \_**](wpd-resource-default.md) | Dies ist optional.            | Wenn es sich bei der Wiedergabeliste um eine physische Datei handelt, z. B. eine XML-Datei, die die wiederzuspielende Mediendatei auflistet, handelt es sich um die tatsächlichen Dateibytes. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 



