---
description: '\_ \_ WPD-INHALTSTYPZERTIFIKAT \_'
ms.assetid: 5fcaf17b-f583-4ba7-aec3-cdb02dbf3bbc
title: WPD_CONTENT_TYPE_CERTIFICATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bade52d6a1f066b00826d5ef79f28db19c8e24b88dd1eeafb8052855196d3b3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109860"
---
# <a name="wpd_content_type_certificate"></a>\_ \_ WPD-INHALTSTYPZERTIFIKAT \_

Ein Objekt, das seinen Typ als WPD \_ CONTENT \_ TYPE CERTIFICATE \_ beschreibt, stellt ein Zertifikat dar, das für die Authentifizierung verwendet wird.

Dieser Objekttyp unterstützt die folgenden Eigenschaften.



| Eigenschaftsname                                                                                                         | Erforderlich oder optional                                                  |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [\_WPD-OBJEKT-ID \_](object-properties.md)                                                                | Erforderlich.                                                             |
| [ÜBERGEORDNETE ID DES \_ \_ WPD-OBJEKTS \_](object-properties.md)                                                 | Erforderlich.                                                             |
| [\_WPD-OBJEKTNAME \_](object-properties.md)                                                            | Erforderlich, wenn das -Objekt eine Datei darstellt.                             |
| [PERSISTENTE EINDEUTIGE ID \_ DES WPD-OBJEKTS \_ \_ \_](object-properties.md)                          | Erforderlich.                                                             |
| [\_WPD-OBJEKTFORMAT \_](object-properties.md)                                                        | Erforderlich.                                                             |
| [\_ \_ WPD-OBJEKTINHALTSTYP \_](object-properties.md)                                           | Erforderlich.                                                             |
| [\_WPD-OBJEKT \_ ISHIDDEN](object-properties.md)                                                    | Erforderlich, wenn das Objekt ausgeblendet ist.                                     |
| [\_WPD-OBJEKT \_ ISSYSTEM](object-properties.md)                                                    | Erforderlich, wenn das -Objekt ein Systemobjekt ist (stellt eine Systemdatei dar). |
| [\_WPD-OBJEKTGRÖßE \_](object-properties.md)                                                            | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                     |
| [\_WPD-OBJEKT \_ \_ URSPRÜNGLICHER \_ DATEINAME](object-properties.md)                              | Erforderlich, wenn das -Objekt eine Datei darstellt.                             |
| [\_WPD-OBJEKT \_ NICHT \_ VERWENDBAR](object-properties.md)                                       | Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist. |
| [\_ \_ WPD-OBJEKTVERWEISE](object-properties.md)                                                | Erforderlich, wenn das -Objekt Verweise auf andere Objekte enthält.               |
| [\_WPD-OBJEKTSCHLÜSSELWÖRTER \_](object-properties.md)                                                    | Optional.                                                             |
| [\_ \_ WPD-OBJEKTSYNCHRONISIERUNGS-ID \_](object-properties.md)                                                     | Optional.                                                             |
| [\_WPD-OBJEKT \_ IST \_ \_ DRM-GESCHÜTZT](object-properties.md)                                  | Erforderlich, wenn das Objekt durch DRM-Technologie geschützt ist.                |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                           | Optional.                                                             |
| [\_WPD-OBJEKTDATUM \_ \_ GEÄNDERT](object-properties.md)                                         | Empfohlen.                                                          |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                         | Optional.                                                             |
| [WPD \_ OBJECT BACK REFERENCES (WPD-OBJEKTVERWEISE \_ \_ ZURÜCK)](object-properties.md)                                     | Wird empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.            |
| [\_ \_ WPD-OBJEKTCONTAINER \_ FUNKTIONALE \_ \_ OBJEKT-ID](object-properties.md)     | Optional.                                                             |
| [\_WPD-OBJEKT \_ GENERIERT \_ \_ MINIATURANSICHT AUS \_ RESSOURCE](object-properties.md) | Optional.                                                             |
| [\_WPD-OBJEKT \_ KANN LÖSCHEN \_](object-properties.md)                                               | Erforderlich, wenn das Objekt gelöscht werden kann.                                |
| [WPD \_ OBJECT \_ LANGUAGE \_ LOCALE](object-properties.md)                                                                | Optional.                                                             |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte enthalten in der Regel die folgenden Ressourcen.



| Ressourcenname                                          | Erforderlich oder optional | Beschreibung        |
|--------------------------------------------------------|----------------------|--------------------|
| [**WPD \_ RESOURCE \_ DEFAULT**](wpd-resource-default.md) | Erforderlich.            | Enthält die Daten. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 



