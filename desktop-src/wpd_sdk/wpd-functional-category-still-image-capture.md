---
description: WPD- \_ Funktions \_ Kategorie \_ trotzdem \_ Image \_ Erfassung
ms.assetid: fb434927-1548-4c6e-bfb7-3a99eef62a4a
title: WPD_FUNCTIONAL_CATEGORY_STILL_IMAGE_CAPTURE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88d821f1182012fbf29960fae4fc06b14ec53ecb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960493"
---
# <a name="wpd_functional_category_still_image_capture"></a>WPD- \_ Funktions \_ Kategorie \_ trotzdem \_ Image \_ Erfassung

Eine WPD \_ \_ -Funktions \_ Kategorie \_ , das immer noch \_ das funktionale Objekt der Bild Erfassung kapselt, kapselt die Bild Erfassungs Funktionalität auf einem Gerät, z. b. eine Kamera oder eine Kamera



| Eigenschaftsname                                                                                                            | Erforderlich oder optional                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [WPD- \_ Objekt- \_ ID](object-properties.md)                                                                   | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zum Zeitpunkt der Erstellung nicht festlegen.                                                                         |
| [übergeordnete WPD- \_ Objekt- \_ \_ ID](object-properties.md)                                                    | Erforderlich.                                                                                                                                              |
| [WPD- \_ Objekt \_ Name](object-properties.md)                                                               | Erforderlich.                                                                                                                                              |
| [\_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt](object-properties.md)                             | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zum Zeitpunkt der Erstellung nicht festlegen.                                                                         |
| [WPD- \_ Objekt \_ Format](object-properties.md)                                                           | Erforderlich.                                                                                                                                              |
| [Inhaltstyp für WPD- \_ Objekt \_ \_](object-properties.md)                                              | Erforderlich.                                                                                                                                              |
| [WPD- \_ Objekt \_ IsHidden](object-properties.md)                                                       | Erforderlich, wenn das Objekt ausgeblendet ist.                                                                                                                      |
| [WPD- \_ Objekt \_ IsSystem](object-properties.md)                                                       | Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).                                                                                  |
| [WPD- \_ Objekt \_ Größe](object-properties.md)                                                               | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                                                                                                      |
| [\_ \_ ursprünglicher \_ Dateiname \_ des WPD-Objekts](object-properties.md)                                 | Erforderlich, wenn das-Objekt eine Datei darstellt.                                                                                                              |
| [WPD- \_ Objekt \_ nicht \_ verwendbar](object-properties.md)                                          | Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist.                                                                                  |
| [Verweise auf WPD- \_ Objekte \_](object-properties.md)                                                   | Erforderlich, wenn das-Objekt über Verweise auf andere-Objekte verfügt.                                                                                                |
| [WPD- \_ Objekt \_ Schlüsselwörter](object-properties.md)                                                       | Dies ist optional.                                                                                                                                              |
| [WPD- \_ Objekt \_ Synchronisierungs- \_ ID](object-properties.md)                                                        | Dies ist optional.                                                                                                                                              |
| [WPD- \_ Objekt \_ ist DRM- \_ \_ geschützt](object-properties.md)                                     | Erforderlich, wenn das Objekt durch DRM-Technologie geschützt wird.                                                                                                 |
| [\_ \_ Erstellungsdatum des WPD-Objekts \_](object-properties.md)                                              | Dies ist optional.                                                                                                                                              |
| [Datum des WPD- \_ Objekts \_ \_ geändert](object-properties.md)                                            | Empfohlen.                                                                                                                                           |
| [erstelltes WPD- \_ Objekt \_ Datum \_](object-properties.md)                                            | Dies ist optional.                                                                                                                                              |
| [\_ \_ zurück \_ Verweise auf WPD-Objekte](object-properties.md)                                                                   | Empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.                                                                                             |
| [\_ \_ \_ Funktions \_ Objekt- \_ ID des WPD-Objekt Containers](object-properties.md)        | Dies ist optional.                                                                                                                                              |
| [WPD \_ - \_ Objekt \_ generieren \_ der Miniaturansicht aus der \_ Ressource](object-properties.md)    | Dies ist optional.                                                                                                                                              |
| [WPD- \_ Objekt \_ kann \_ Löschen](object-properties.md)                                                                        | Erforderlich, wenn das Objekt nicht gelöscht werden kann.                                                                                                              |
| [Gebiets Schema der WPD- \_ Objekt \_ Sprache \_](object-properties.md)                                                                   | Dies ist optional.                                                                                                                                              |
| [WPD- \_ Funktions \_ Objekt \_ Kategorie](miscellaneous-properties.md)                         | Erforderlich. Weitere [**Informationen zu \_ Kategorien \_ \_ \_**](wpd-content-type-functional-object.md) , die von tragbaren Windows-Geräten definiert werden |
| [Auflösung von WPD- \_ \_ \_ Abbild Erfassung \_](still-image-properties.md)                  | Erforderlich.                                                                                                                                              |
| [WPD \_ - \_ Image \_ Erfassungs \_ Format](still-image-properties.md)                          | Erforderlich.                                                                                                                                              |
| [WPD-Einstellung für die \_ \_ Bild \_ Komprimierung \_](still-image-properties.md)                | Dies ist optional.                                                                                                                                              |
| [WPD \_ - \_ Image- \_ weiß \_ Balance](still-image-properties.md)                            | Dies ist optional.                                                                                                                                              |
| [WPD \_ - \_ Abbild \_ RGB- \_ Gewinn](still-image-properties.md)                                      | Dies ist optional.                                                                                                                                              |
| [WPD \_ - \_ Image-Datei \_ Nummer](still-image-properties.md)                                         | Dies ist optional.                                                                                                                                              |
| [WPD \_ - \_ Image- \_ Fokus \_ Länge immer noch](still-image-properties.md)                              | Dies ist optional.                                                                                                                                              |
| [WPD \_ - \_ Bild \_ Fokus \_ Distanz immer noch](still-image-properties.md)                          | Dies ist optional.                                                                                                                                              |
| [WPD \_ - \_ Bild \_ Fokus \_ Modus immer noch](still-image-properties.md)                                  | Dies ist optional.                                                                                                                                              |
| [WPD \_ - \_ Bild zur Bild Anzeige \_ \_ \_](still-image-properties.md)         | Dies ist optional.                                                                                                                                              |
| [WPD \_ - \_ Image- \_ Flash \_ Modus immer noch](still-image-properties.md)                                  | Dies ist optional.                                                                                                                                              |
| [Zeit für \_ das \_ \_ \_ gleich zeidie Image der WPD](still-image-properties.md)                            | Dies ist optional.                                                                                                                                              |
| [WPD \_ - \_ \_ \_ Programm \_ Modus für die Bild Anzeige](still-image-properties.md)           | Dies ist optional.                                                                                                                                              |
| [WPD-Index für die \_ \_ Image-Verfüg \_ barkeit \_](still-image-properties.md)                          | Dies ist optional.                                                                                                                                              |
| [\_ \_ Kompensierung der Abbild \_ Präsenz \_ \_ für WPD weiterhin](still-image-properties.md) | Dies ist optional.                                                                                                                                              |
| [Verzögerung von WPD- \_ \_ \_ Abbild Aufzeichnung \_](still-image-properties.md)                            | Dies ist optional.                                                                                                                                              |
| [WPD \_ - \_ Image \_ Erfassungs \_ Modus](still-image-properties.md)                              | Dies ist optional.                                                                                                                                              |
| [WPD \_ immer noch \_ Bild \_ Kontrast](still-image-properties.md)                                       | Dies ist optional.                                                                                                                                              |
| [WPD \_ immer noch \_ Bild \_ Schärfe](still-image-properties.md)                                     | Dies ist optional.                                                                                                                                              |
| [WPD \_ \_ Image \_ Digital \_ Zoom](still-image-properties.md)                              | Dies ist optional.                                                                                                                                              |
| [WPD \_ - \_ Bild \_ Effekt \_ Modus immer noch](still-image-properties.md)                                | Dies ist optional.                                                                                                                                              |
| [WPD \_ - \_ Image- \_ Burst \_ Nummer](still-image-properties.md)                              | Dies ist optional.                                                                                                                                              |
| [WPD \_ - \_ \_ aufburst \_ Intervall für Images](still-image-properties.md)                          | Dies ist optional.                                                                                                                                              |
| [WPD- \_ Nummer immer noch \_ Bild Zeit \_ \_ Spanne](still-image-properties.md)                      | Dies ist optional.                                                                                                                                              |
| [WPD \_ - \_ Abbild für Zeit \_ \_ Intervall](still-image-properties.md)                  | Dies ist optional.                                                                                                                                              |
| [WPD \_ - \_ Bild \_ Fokus \_ Messungs \_ Modus immer noch](still-image-properties.md)               | Dies ist optional.                                                                                                                                              |
| [URL zum \_ \_ Hochladen von \_ Images \_ für WPD](still-image-properties.md)                                  | Dies ist optional.                                                                                                                                              |
| [WPD \_ immer noch \_ Bild- \_ Artist](still-image-properties.md)                                           | Dies ist optional.                                                                                                                                              |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte Hosten in der Regel keine Ressourcen.

Viele dieser Eigenschaften haben miteinander verbundene Auswirkungen. Wenn z. b. für **WPD weiterhin der Bild-und Leistungs \_ \_ \_ \_ Messungs \_ Modus** auf "automatisch" festgelegt ist, werden f-Pause, Anzeigezeit und Expositions Zähler verknüpft

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Funktions Objekt des WPD- \_ \_ Inhaltstyp \_ \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



