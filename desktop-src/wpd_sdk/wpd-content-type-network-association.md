---
description: Netzwerk Zuordnung für WPD- \_ \_ Inhaltstyp \_ \_
ms.assetid: 5c17aba1-98f7-4d6c-a5d2-2b4623a65255
title: WPD_CONTENT_TYPE_NETWORK_ASSOCIATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ab3fd2f76efef5b85991f1334977c17e34d06b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353873"
---
# <a name="wpd_content_type_network_association"></a>Netzwerk Zuordnung für WPD- \_ \_ Inhaltstyp \_ \_

Ein-Objekt, das den Typ als WPD \_ Content \_ Type \_ Network Association beschreibt, \_ stellt eine Zuordnung zwischen einem Host und einem Gerät dar.

Dieser Objekttyp unterstützt die folgenden Eigenschaften.



|                                                                                                                                              |                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| **Eigenschaftenname**                                                                                                                            | **Erforderlich oder optional**                                              |
| [WPD- \_ Objekt- \_ ID](object-properties.md)                                                                                       | Erforderlich.                                                             |
| [übergeordnete WPD- \_ Objekt- \_ \_ ID](object-properties.md)                                                                        | Erforderlich.                                                             |
| [WPD- \_ Objekt \_ Name](object-properties.md)                                                                                   | Erforderlich, wenn das-Objekt eine Datei darstellt.                             |
| [\_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt](object-properties.md)                                                 | Erforderlich.                                                             |
| [WPD- \_ Objekt \_ Format](object-properties.md)                                                                               | Erforderlich.                                                             |
| [Inhaltstyp für WPD- \_ Objekt \_ \_](object-properties.md)                                                                  | Erforderlich.                                                             |
| [WPD- \_ Objekt \_ IsHidden](object-properties.md)                                                                           | Erforderlich, wenn das Objekt ausgeblendet ist.                                     |
| [WPD- \_ Objekt \_ IsSystem](object-properties.md)                                                                           | Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar). |
| [WPD- \_ Objekt \_ Größe](object-properties.md)                                                                                   | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                     |
| [\_ \_ ursprünglicher \_ Dateiname \_ des WPD-Objekts](object-properties.md)                                                     | Erforderlich, wenn das-Objekt eine Datei darstellt.                             |
| [WPD- \_ Objekt \_ nicht \_ verwendbar](object-properties.md)                                                              | Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist. |
| [Verweise auf WPD- \_ Objekte \_](object-properties.md)                                                                       | Erforderlich, wenn das-Objekt über Verweise auf andere-Objekte verfügt.               |
| [WPD- \_ Objekt \_ Schlüsselwörter](object-properties.md)                                                                           | Dies ist optional.                                                             |
| [WPD- \_ Objekt \_ Synchronisierungs- \_ ID](object-properties.md)                                                                            | Dies ist optional.                                                             |
| [WPD- \_ Objekt \_ ist DRM- \_ \_ geschützt](object-properties.md)                                                         | Erforderlich, wenn das Objekt durch DRM-Technologie geschützt wird.                |
| [\_ \_ Erstellungsdatum des WPD-Objekts \_](object-properties.md)                                                                  | Dies ist optional.                                                             |
| [Datum des WPD- \_ Objekts \_ \_ geändert](object-properties.md)                                                                | Empfohlen.                                                          |
| [erstelltes WPD- \_ Objekt \_ Datum \_](object-properties.md)                                                                | Dies ist optional.                                                             |
| [\_ \_ zurück \_ Verweise auf WPD-Objekte](object-properties.md)                                                                                       | Empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.            |
| [\_ \_ \_ Funktions \_ Objekt- \_ ID des WPD-Objekt Containers](object-properties.md)                            | Dies ist optional.                                                             |
| [WPD \_ - \_ Objekt \_ generieren \_ der Miniaturansicht aus der \_ Ressource](object-properties.md)                        | Dies ist optional.                                                             |
| [WPD- \_ Objekt \_ kann \_ Löschen](object-properties.md)                                                                      | Erforderlich, wenn das Objekt nicht gelöscht werden kann.                             |
| [WPD- \_ Objekt \_ Sprache \_ lokal](object-properties.md)                                                                                        | Dies ist optional.                                                             |
| [WPD-Netzwerk Zuordnungs \_ \_ \_ Host \_ Netzwerk \_ -Bezeichner](network-association-properties.md) | Erforderlich.                                                             |
| [WPD- \_ Netzwerk Zuordnung \_ \_ X509V3SEQUENCE](network-association-properties.md)                       | Dies ist optional.                                                             |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte Hosten in der Regel keine Ressourcen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 



