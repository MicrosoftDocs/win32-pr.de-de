---
description: '\_ \_ WPD-INHALTSTYP \_ \_ DRAHTLOSPROFIL'
ms.assetid: 229f6b65-4904-41b1-bb35-8873477a272b
title: WPD_CONTENT_TYPE_WIRELESS_PROFILE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a29b02240e6daeb98713a9a58a1332b44464cafafddab1559e07915a4acaf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119445090"
---
# <a name="wpd_content_type_wireless_profile"></a>\_ \_ WPD-INHALTSTYP \_ \_ DRAHTLOSPROFIL

Ein Objekt, das seinen Typ als WPD CONTENT TYPE WIRELESS PROFILE beschreibt, stellt Informationen dar, die für \_ den Zugriff auf ein \_ \_ \_ Drahtlosnetzwerk verwendet werden.

Dieser Objekttyp unterstützt die folgenden Eigenschaften.



| Eigenschaftsname             | Erforderlich oder optional                      |
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
| [WPD \_ OBJECT BACK REFERENCES (WPD-OBJEKTVERWEISE \_ \_ ZURÜCK)](object-properties.md)                                                                | Wird empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.            |
| [\_ \_ WPD-OBJEKTCONTAINER \_ FUNKTIONALE \_ \_ OBJEKT-ID](object-properties.md)     | Optional.                                                             |
| [\_WPD-OBJEKT \_ GENERIERT \_ \_ MINIATURANSICHT AUS \_ RESSOURCE](object-properties.md) | Optional.                                                             |
| [\_WPD-OBJEKT \_ KANN LÖSCHEN \_](object-properties.md)                                               | Erforderlich, wenn das Objekt nicht gelöscht werden kann.                             |
| [WPD \_ OBJECT \_ LANGUAGE \_ LOCALE](object-properties.md)                                                                | Optional.                                                             |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte enthalten in der Regel die folgenden Ressourcen.



| Ressourcenname                                          | Erforderlich oder optional                                  | Beschreibung               |
|--------------------------------------------------------|-------------------------------------------------------|---------------------------|
| [**WPD \_ RESOURCE \_ DEFAULT**](wpd-resource-default.md) | Erforderlich, wenn das Objekt durch Binärdaten dargestellt wird. | Enthält die Binärdaten. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 



