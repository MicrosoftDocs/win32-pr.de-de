---
description: '\_ \_ WPD-INHALTSTYP \_ \_ DRAHTLOSPROFIL'
ms.assetid: 229f6b65-4904-41b1-bb35-8873477a272b
title: WPD_CONTENT_TYPE_WIRELESS_PROFILE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 999c8aec77c6ff046690e4c3450c0643d685e1db
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423700"
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
| [\_WPD-OBJEKT \_ ISSYSTEM](object-properties.md)                                                    | Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar). |
| [\_WPD-OBJEKTGRÖßE \_](object-properties.md)                                                            | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                     |
| [\_WPD-OBJEKT \_ \_ URSPRÜNGLICHER \_ DATEINAME](object-properties.md)                              | Erforderlich, wenn das -Objekt eine Datei darstellt.                             |
| [\_WPD-OBJEKT \_ NICHT \_ VERWENDBAR](object-properties.md)                                       | Empfohlen, wenn das Objekt nicht für die Nutzung durch das Gerät vorgesehen ist. |
| [\_ \_ WPD-OBJEKTVERWEISE](object-properties.md)                                                | Erforderlich, wenn das Objekt Verweise auf andere Objekte hat.               |
| [\_ \_ WPD-OBJEKTSCHLÜSSELWÖRTER](object-properties.md)                                                    | Dies ist optional.                                                             |
| [\_ \_ WPD-OBJEKTSYNCHRONISIERUNGS-ID \_](object-properties.md)                                                     | Dies ist optional.                                                             |
| [\_WPD-OBJEKT \_ IST \_ \_ DRM-GESCHÜTZT](object-properties.md)                                  | Erforderlich, wenn das Objekt durch drm-Technologie geschützt ist.                |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                           | Dies ist optional.                                                             |
| [ÄNDERUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                         | Empfohlen.                                                          |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                         | Dies ist optional.                                                             |
| [\_ \_ WPD-OBJEKTRÜCKVERWEISE \_](object-properties.md)                                                                | Empfohlen, wenn ein anderes Objekt auf das Objekt verweist.            |
| [FUNKTIONALE \_ \_ \_ \_ OBJEKT-ID DES WPD-OBJEKTCONTAINERS \_](object-properties.md)     | Dies ist optional.                                                             |
| [\_WPD-OBJEKT \_ GENERIERT \_ \_ MINIATURANSICHTEN AUS \_ RESSOURCE](object-properties.md) | Dies ist optional.                                                             |
| [\_WPD-OBJEKT \_ KANN GELÖSCHT \_ WERDEN](object-properties.md)                                               | Erforderlich, wenn das Objekt nicht gelöscht werden kann.                             |
| [\_GEBIETSSCHEMA DER WPD-OBJEKTSPRACHE \_ \_](object-properties.md)                                                                | Dies ist optional.                                                             |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte enthalten in der Regel die folgenden Ressourcen.



| Ressourcenname                                          | Erforderlich oder optional                                  | BESCHREIBUNG               |
|--------------------------------------------------------|-------------------------------------------------------|---------------------------|
| [**WPD \_ RESOURCE \_ DEFAULT**](wpd-resource-default.md) | Erforderlich, wenn das Objekt durch Binärdaten dargestellt wird. | Enthält die Binärdaten. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 



