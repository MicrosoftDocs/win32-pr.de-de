---
description: GENERISCHE \_ \_ \_ WPD-INHALTSTYPDATEI \_
ms.assetid: e652bebc-fb3d-48cd-af59-3ad97a79711d
title: WPD_CONTENT_TYPE_GENERIC_FILE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb352d851575ab510df339915cf57b75495fc044636681e49f15f94e15288b46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083344"
---
# <a name="wpd_content_type_generic_file"></a>GENERISCHE \_ \_ \_ WPD-INHALTSTYPDATEI \_

Ein Objekt, das seinen Typ als WPD CONTENT TYPE GENERIC FILE beschreibt, \_ \_ stellt ein \_ \_ generisches Objekt mit einer zugrunde liegenden physischen Datei dar. Der Unterschied zwischen diesem Typ und WPD \_ CONTENT \_ TYPE \_ UNSPECIFIED besteht darin, dass ein UNSPECIFIED-Objekt generischer ist und keine zugrunde liegende Datei aufweisen muss. Dieser Objekttyp kann erstellt werden, um Daten eines nicht angegebenen Typs zu speichern, der vom Gerät nicht verwendet werden soll.

Dieser Objekttyp unterstützt die folgenden Eigenschaften.



| Eigenschaftsname                                                                                                         | Erforderlich oder optional                                                           |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [\_ \_ WPD-OBJEKT-ID](object-properties.md)                                                                | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zur Erstellungszeit nicht festlegen. |
| [ÜBERGEORDNETE \_ \_ \_ WPD-OBJEKT-ID](object-properties.md)                                                 | Erforderlich.                                                                      |
| [\_WPD-OBJEKTNAME \_](object-properties.md)                                                            | Erforderlich, wenn das -Objekt eine Datei darstellt.                                      |
| [\_PERSISTENTE EINDEUTIGE ID DES \_ \_ \_ WPD-OBJEKTS](object-properties.md)                          | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zur Erstellungszeit nicht festlegen. |
| [\_WPD-OBJEKTFORMAT \_](object-properties.md)                                                        | Erforderlich.                                                                      |
| [\_ \_ WPD-OBJEKTINHALTSTYP \_](object-properties.md)                                           | Erforderlich.                                                                      |
| [\_WPD-OBJEKT \_ ISHIDDEN](object-properties.md)                                                    | Erforderlich, wenn das Objekt ausgeblendet ist.                                              |
| [WPD \_ OBJECT \_ ISSYSTEM](object-properties.md)                                                    | Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).          |
| [\_WPD-OBJEKTGRÖßE \_](object-properties.md)                                                            | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                              |
| [\_ \_ URSPRÜNGLICHER \_ \_ DATEINAME DES WPD-OBJEKTS](object-properties.md)                              | Erforderlich, wenn das -Objekt eine Datei darstellt.                                      |
| [\_WPD-OBJEKT \_ NICHT \_ VERWENDBAR](object-properties.md)                                       | Empfohlen, wenn das Objekt nicht für die Nutzung durch das Gerät vorgesehen ist.          |
| [\_ \_ WPD-OBJEKTVERWEISE](object-properties.md)                                                | Erforderlich, wenn das Objekt Verweise auf andere Objekte hat.                        |
| [\_ \_ WPD-OBJEKTSCHLÜSSELWÖRTER](object-properties.md)                                                    | Optional.                                                                      |
| [\_ \_ WPD-OBJEKTSYNCHRONISIERUNGS-ID \_](object-properties.md)                                                     | Optional.                                                                      |
| [\_WPD-OBJEKT \_ IST \_ \_ DRM-GESCHÜTZT](object-properties.md)                                  | Erforderlich, wenn das Objekt durch drm-Technologie geschützt ist.                         |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                           | Optional.                                                                      |
| [ÄNDERUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                         | Empfohlen.                                                                   |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                         | Optional.                                                                      |
| [\_ \_ WPD-OBJEKTRÜCKVERWEISE \_](object-properties.md)                                                                | Empfohlen, wenn ein anderes Objekt auf das Objekt verweist.                     |
| [FUNKTIONALE \_ \_ \_ \_ OBJEKT-ID DES WPD-OBJEKTCONTAINERS \_](object-properties.md)     | Optional.                                                                      |
| [\_WPD-OBJEKT \_ GENERIERT \_ \_ MINIATURANSICHTEN AUS \_ RESSOURCE](object-properties.md) | Optional.                                                                      |
| [\_WPD-OBJEKT \_ KANN GELÖSCHT \_ WERDEN](object-properties.md)                                                                     | Erforderlich, wenn das Objekt nicht gelöscht werden kann.                                      |
| [\_GEBIETSSCHEMA DER WPD-OBJEKTSPRACHE \_ \_](object-properties.md)                                                                | Optional.                                                                      |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte enthalten in der Regel die folgenden Ressourcen.



| Ressourcenname                                          | Erforderlich oder optional | Beschreibung             |
|--------------------------------------------------------|----------------------|-------------------------|
| [**\_WPD-RESSOURCENSTANDARD \_**](wpd-resource-default.md) | Erforderlich.            | Enthält die Dateidaten. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 



