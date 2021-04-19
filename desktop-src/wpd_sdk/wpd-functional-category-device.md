---
description: WPD \_ - \_ funktionskategoriegerät \_
ms.assetid: 64b34490-1cb5-4915-ae1c-77bd4ab79ad7
title: WPD_FUNCTIONAL_CATEGORY_DEVICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb179311af5fb3c3eef063157e3615b21eeb66a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356964"
---
# <a name="wpd_functional_category_device"></a>WPD \_ - \_ funktionskategoriegerät \_

Ein \_ Geräte funktionales Objekt der WPD-Funktions \_ Kategorie \_ kapselt das Gerät (d. h. das oberste Objekt des Geräts). Wenn ein Gerät diese funktionale Kategorie implementiert, sollte es zusätzlich zu den Eigenschaften, die für das [Geräte Objekt](device-object.md)aufgelistet werden, auch diese Eigenschaften unterstützen.



| Eigenschaftsname                                                                                                         | Erforderlich oder optional                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [WPD- \_ Objekt- \_ ID](object-properties.md)                                                                | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zum Zeitpunkt der Erstellung nicht festlegen.                                      |
| [übergeordnete WPD- \_ Objekt- \_ \_ ID](object-properties.md)                                                 | Erforderlich.                                                                                                           |
| [WPD- \_ Objekt \_ Name](object-properties.md)                                                            | Erforderlich.                                                                                                           |
| [\_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt](object-properties.md)                          | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zum Zeitpunkt der Erstellung nicht festlegen.                                      |
| [WPD- \_ Objekt \_ Format](object-properties.md)                                                        | Erforderlich.                                                                                                           |
| [Inhaltstyp für WPD- \_ Objekt \_ \_](object-properties.md)                                           | Erforderlich.                                                                                                           |
| [WPD- \_ Objekt \_ IsHidden](object-properties.md)                                                    | Erforderlich, wenn das Objekt ausgeblendet ist.                                                                                   |
| [WPD- \_ Objekt \_ IsSystem](object-properties.md)                                                    | Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).                                               |
| [WPD- \_ Objekt \_ Größe](object-properties.md)                                                            | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                                                                   |
| [\_ \_ ursprünglicher \_ Dateiname \_ des WPD-Objekts](object-properties.md)                              | Erforderlich, wenn das-Objekt eine Datei darstellt.                                                                           |
| [WPD- \_ Objekt \_ nicht \_ verwendbar](object-properties.md)                                       | Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist.                                               |
| [Verweise auf WPD- \_ Objekte \_](object-properties.md)                                                | Erforderlich, wenn das-Objekt über Verweise auf andere-Objekte verfügt.                                                             |
| [WPD- \_ Objekt \_ Schlüsselwörter](object-properties.md)                                                    | Dies ist optional.                                                                                                           |
| [WPD- \_ Objekt \_ Synchronisierungs- \_ ID](object-properties.md)                                                     | Dies ist optional.                                                                                                           |
| [WPD- \_ Objekt \_ ist DRM- \_ \_ geschützt](object-properties.md)                                  | Erforderlich, wenn das Objekt durch DRM-Technologie geschützt wird.                                                              |
| [\_ \_ Erstellungsdatum des WPD-Objekts \_](object-properties.md)                                           | Dies ist optional.                                                                                                           |
| [Datum des WPD- \_ Objekts \_ \_ geändert](object-properties.md)                                         | Empfohlen.                                                                                                        |
| [erstelltes WPD- \_ Objekt \_ Datum \_](object-properties.md)                                         | Dies ist optional.                                                                                                           |
| [\_ \_ zurück \_ Verweise auf WPD-Objekte](object-properties.md)                                                                | Empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.                                                          |
| [\_ \_ \_ Funktions \_ Objekt- \_ ID des WPD-Objekt Containers](object-properties.md)     | Dies ist optional.                                                                                                           |
| [WPD \_ - \_ Objekt \_ generieren \_ der Miniaturansicht aus der \_ Ressource](object-properties.md) | Dies ist optional.                                                                                                           |
| [WPD- \_ Funktions \_ Objekt \_ Kategorie](miscellaneous-properties.md)                      | Erforderlich.                                                                                                           |
| [WPD- \_ Geräte \_ Synchronisierungs \_ Partner](device-properties.md)                                           | Dies ist optional.                                                                                                           |
| [Version der WPD- \_ Geräte \_ Firmware \_](device-properties.md)                                   | Erforderlich.                                                                                                           |
| [\_ \_ Energie \_ Pegel des WPD-Geräts](device-properties.md)                                             | Empfohlen, wenn das Gerät über einen Akku verfügt.                                                                                |
| [WPD \_ - \_ Geräte \_ Stromquelle](device-properties.md)                                           | Empfohlen.                                                                                                        |
| [WPD- \_ Geräte \_ Protokoll](device-properties.md)                                                    | Empfohlen.                                                                                                        |
| [WPD- \_ Geräte \_ Hersteller](device-properties.md)                                            | Erforderlich.                                                                                                           |
| [WPD- \_ Geräte \_ Modell](device-properties.md)                                                          | Erforderlich.                                                                                                           |
| [\_ \_ Serien \_ Nummer des WPD-Geräts](device-properties.md)                                         | Erforderlich.                                                                                                           |
| [WPD- \_ Gerät \_ unterstützt \_ nicht \_ verwendbar](device-properties.md)                    | Erforderlich, wenn das Gerät nicht verwendbare Objekte unterstützt. Das heißt, wenn das Gerät für die einfache Datenspeicherung verwendet werden kann. |
| [DateTime für WPD- \_ Gerät \_](device-properties.md)                                                    | Dies ist optional.                                                                                                           |
| [Anzeige Name des WPD- \_ Geräts \_ \_](device-properties.md)                                         | Empfohlen.                                                                                                        |
| [vom WPD- \_ Gerät \_ unterstützte \_ DRM- \_ Schemata](device-properties.md)                        | Empfohlen, wenn das Gerät DRM-Technologie unterstützt.                                                                  |
| [vom WPD- \_ Gerät \_ unterstützte \_ Formate \_ sind \_ geordnet](device-properties.md)       | Empfohlen, wenn das Gerät eine bevorzugte Format Anordnung unterstützt.                                                       |
| [WPD \_ - \_ Gerätetyp](device-properties.md)                                                            | Empfohlen.                                                                                                        |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte Hosten in der Regel keine Ressourcen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Funktions Objekt des WPD- \_ \_ Inhaltstyp \_ \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



