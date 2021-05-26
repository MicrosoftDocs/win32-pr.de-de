---
description: WPD \_ CONTENT \_ TYPE \_ NETWORK \_ ASSOCIATION
ms.assetid: 5c17aba1-98f7-4d6c-a5d2-2b4623a65255
title: WPD_CONTENT_TYPE_NETWORK_ASSOCIATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c92f76080db4167a12578c58e9d85c9506c28b
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423718"
---
# <a name="wpd_content_type_network_association"></a>WPD \_ CONTENT \_ TYPE \_ NETWORK \_ ASSOCIATION

Ein Objekt, das seinen Typ als WPD CONTENT TYPE NETWORK ASSOCIATION beschreibt, stellt \_ eine Zuordnung zwischen einem Host und einem Gerät \_ \_ \_ dar.

Dieser Objekttyp unterstützt die folgenden Eigenschaften.



| Eigenschaftsname         | Erforderlich oder optional        |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [\_WPD-OBJEKT-ID \_](object-properties.md)                                                                                       | Erforderlich.                                                             |
| [ÜBERGEORDNETE ID DES \_ \_ WPD-OBJEKTS \_](object-properties.md)                                                                        | Erforderlich.                                                             |
| [\_WPD-OBJEKTNAME \_](object-properties.md)                                                                                   | Erforderlich, wenn das -Objekt eine Datei darstellt.                             |
| [PERSISTENTE EINDEUTIGE ID \_ DES WPD-OBJEKTS \_ \_ \_](object-properties.md)                                                 | Erforderlich.                                                             |
| [\_WPD-OBJEKTFORMAT \_](object-properties.md)                                                                               | Erforderlich.                                                             |
| [\_ \_ WPD-OBJEKTINHALTSTYP \_](object-properties.md)                                                                  | Erforderlich.                                                             |
| [\_WPD-OBJEKT \_ ISHIDDEN](object-properties.md)                                                                           | Erforderlich, wenn das Objekt ausgeblendet ist.                                     |
| [\_WPD-OBJEKT \_ ISSYSTEM](object-properties.md)                                                                           | Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar). |
| [\_WPD-OBJEKTGRÖßE \_](object-properties.md)                                                                                   | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                     |
| [\_WPD-OBJEKT \_ \_ URSPRÜNGLICHER \_ DATEINAME](object-properties.md)                                                     | Erforderlich, wenn das -Objekt eine Datei darstellt.                             |
| [\_WPD-OBJEKT \_ NICHT \_ VERWENDBAR](object-properties.md)                                                              | Empfohlen, wenn das Objekt nicht für die Nutzung durch das Gerät vorgesehen ist. |
| [\_ \_ WPD-OBJEKTVERWEISE](object-properties.md)                                                                       | Erforderlich, wenn das Objekt Verweise auf andere Objekte hat.               |
| [\_ \_ WPD-OBJEKTSCHLÜSSELWÖRTER](object-properties.md)                                                                           | Dies ist optional.                                                             |
| [\_ \_ WPD-OBJEKTSYNCHRONISIERUNGS-ID \_](object-properties.md)                                                                            | Dies ist optional.                                                             |
| [\_WPD-OBJEKT \_ IST \_ \_ DRM-GESCHÜTZT](object-properties.md)                                                         | Erforderlich, wenn das Objekt durch drm-Technologie geschützt ist.                |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                                                  | Dies ist optional.                                                             |
| [ÄNDERUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                                                | Empfohlen.                                                          |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                                                | Dies ist optional.                                                             |
| [\_ \_ WPD-OBJEKTRÜCKVERWEISE \_](object-properties.md)                                                                                       | Empfohlen, wenn ein anderes Objekt auf das Objekt verweist.            |
| [FUNKTIONALE \_ \_ \_ \_ OBJEKT-ID DES WPD-OBJEKTCONTAINERS \_](object-properties.md)                            | Dies ist optional.                                                             |
| [\_WPD-OBJEKT \_ GENERIERT \_ \_ MINIATURANSICHTEN AUS \_ RESSOURCE](object-properties.md)                        | Dies ist optional.                                                             |
| [\_WPD-OBJEKT \_ KANN GELÖSCHT \_ WERDEN](object-properties.md)                                                                      | Erforderlich, wenn das Objekt nicht gelöscht werden kann.                             |
| [WPD \_ OBJECT \_ LANGUAGE \_ LOCAL](object-properties.md)                                                                                        | Dies ist optional.                                                             |
| [\_ \_ \_ \_ WPD-NETZWERKZUORDNUNGSHOST-NETZWERKBEZEICHNER \_](network-association-properties.md) | Erforderlich.                                                             |
| [\_WPD-NETZWERK \_ ASSOCIATION \_ X509V3SEQUENCE](network-association-properties.md)                       | Dies ist optional.                                                             |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte hosten in der Regel keine Ressourcen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 



