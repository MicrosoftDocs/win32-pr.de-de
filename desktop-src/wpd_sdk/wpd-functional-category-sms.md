---
description: WPD- \_ Funktions \_ Kategorie \_ SMS
ms.assetid: dbb536a6-9c12-459d-8098-ebe4fc4c8f2f
title: WPD_FUNCTIONAL_CATEGORY_SMS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af3a08cb3df6bd74de843efaa3d0feed88ad86fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217486"
---
# <a name="wpd_functional_category_sms"></a>WPD- \_ Funktions \_ Kategorie \_ SMS

Ein SMS- \_ \_ \_ Funktionsobjekt für die WPD-Funktions Kategorie kapselt eine kurze Nachrichtendienst Funktionalität (in der Regel als "SMS" bezeichnet) auf dem Gerät.



| Eigenschaftsname                                                                                                         | Erforderlich oder optional                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [WPD- \_ Objekt- \_ ID](object-properties.md)                                                                | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zum Zeitpunkt der Erstellung nicht festlegen.                                                                         |
| [übergeordnete WPD- \_ Objekt- \_ \_ ID](object-properties.md)                                                 | Erforderlich.                                                                                                                                              |
| [WPD- \_ Objekt \_ Name](object-properties.md)                                                            | Erforderlich.                                                                                                                                              |
| [\_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt](object-properties.md)                          | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zum Zeitpunkt der Erstellung nicht festlegen.                                                                         |
| [WPD- \_ Objekt \_ Format](object-properties.md)                                                        | Erforderlich.                                                                                                                                              |
| [Inhaltstyp für WPD- \_ Objekt \_ \_](object-properties.md)                                           | Erforderlich.                                                                                                                                              |
| [WPD- \_ Objekt \_ IsHidden](object-properties.md)                                                    | Erforderlich, wenn das Objekt ausgeblendet ist.                                                                                                                      |
| [WPD- \_ Objekt \_ IsSystem](object-properties.md)                                                    | Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).                                                                                  |
| [WPD- \_ Objekt \_ Größe](object-properties.md)                                                            | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                                                                                                      |
| [\_ \_ ursprünglicher \_ Dateiname \_ des WPD-Objekts](object-properties.md)                              | Erforderlich, wenn das-Objekt eine Datei darstellt.                                                                                                              |
| [WPD- \_ Objekt \_ nicht \_ verwendbar](object-properties.md)                                       | Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist.                                                                                  |
| [Verweise auf WPD- \_ Objekte \_](object-properties.md)                                                | Erforderlich, wenn das-Objekt über Verweise auf andere-Objekte verfügt.                                                                                                |
| [WPD- \_ Objekt \_ Schlüsselwörter](object-properties.md)                                                    | Dies ist optional.                                                                                                                                              |
| [WPD- \_ Objekt \_ Synchronisierungs- \_ ID](object-properties.md)                                                     | Dies ist optional.                                                                                                                                              |
| [WPD- \_ Objekt \_ ist DRM- \_ \_ geschützt](object-properties.md)                                  | Erforderlich, wenn das Objekt durch DRM-Technologie geschützt wird.                                                                                                 |
| [\_ \_ Erstellungsdatum des WPD-Objekts \_](object-properties.md)                                           | Dies ist optional.                                                                                                                                              |
| [Datum des WPD- \_ Objekts \_ \_ geändert](object-properties.md)                                         | Empfohlen.                                                                                                                                           |
| [erstelltes WPD- \_ Objekt \_ Datum \_](object-properties.md)                                         | Dies ist optional.                                                                                                                                              |
| [\_ \_ zurück \_ Verweise auf WPD-Objekte](object-properties.md)                                                                | Empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.                                                                                             |
| [\_ \_ \_ Funktions \_ Objekt- \_ ID des WPD-Objekt Containers](object-properties.md)     | Dies ist optional.                                                                                                                                              |
| [WPD \_ - \_ Objekt \_ generieren \_ der Miniaturansicht aus der \_ Ressource](object-properties.md) | Dies ist optional.                                                                                                                                              |
| [WPD- \_ Objekt \_ kann \_ Löschen](object-properties.md)                                                                     | Erforderlich, wenn das Objekt nicht gelöscht werden kann.                                                                                                              |
| [Gebiets Schema der WPD- \_ Objekt \_ Sprache \_](object-properties.md)                                                                | Dies ist optional.                                                                                                                                              |
| [WPD- \_ Funktions \_ Objekt \_ Kategorie](miscellaneous-properties.md)                      | Erforderlich. Weitere [**Informationen zu \_ Kategorien \_ \_ \_**](wpd-content-type-functional-object.md) , die von tragbaren Windows-Geräten definiert werden |
| [WPD- \_ SMS- \_ Anbieter](sms-properties.md)                                                             | Erforderlich.                                                                                                                                              |
| [WPD- \_ SMS- \_ Timeout](sms-properties.md)                                                               | Erforderlich.                                                                                                                                              |
| [\_ \_ Maximale Nutzlast für WPD SMS \_](sms-properties.md)                                                      | Erforderlich.                                                                                                                                              |
| [WPD- \_ SMS- \_ Codierung](sms-properties.md)                                                             | Erforderlich.                                                                                                                                              |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte Hosten in der Regel keine Ressourcen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Funktions Objekt des WPD- \_ \_ Inhaltstyp \_ \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



