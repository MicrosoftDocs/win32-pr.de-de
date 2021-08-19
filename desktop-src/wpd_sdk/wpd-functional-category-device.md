---
description: WPD \_ FUNCTIONAL \_ CATEGORY \_ DEVICE
ms.assetid: 64b34490-1cb5-4915-ae1c-77bd4ab79ad7
title: WPD_FUNCTIONAL_CATEGORY_DEVICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499f39cf60e247c0abbbcc66f7fad52099a2a83a93f348b1ac9636bb790b9354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842216"
---
# <a name="wpd_functional_category_device"></a>WPD \_ FUNCTIONAL \_ CATEGORY \_ DEVICE

Ein WPD \_ FUNCTIONAL \_ CATEGORY DEVICE-Funktionsobjekt kapselt das Gerät (d. h. das oberste \_ Objekt des Geräts). Wenn ein Gerät diese Funktionale Kategorie implementiert, sollte es diese Eigenschaften zusätzlich zu den eigenschaften unterstützen, die für das [Geräteobjekt aufgelistet sind.](device-object.md)



| Eigenschaftsname                                                                                                         | Erforderlich oder optional                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [\_WPD-OBJEKT-ID \_](object-properties.md)                                                                | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft nicht festlegen, auch nicht zum Zeitpunkt der Erstellung.                                      |
| [ÜBERGEORDNETE ID DES \_ \_ WPD-OBJEKTS \_](object-properties.md)                                                 | Erforderlich.                                                                                                           |
| [\_WPD-OBJEKTNAME \_](object-properties.md)                                                            | Erforderlich.                                                                                                           |
| [PERSISTENTE EINDEUTIGE ID \_ DES WPD-OBJEKTS \_ \_ \_](object-properties.md)                          | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft nicht festlegen, auch nicht zum Zeitpunkt der Erstellung.                                      |
| [\_WPD-OBJEKTFORMAT \_](object-properties.md)                                                        | Erforderlich.                                                                                                           |
| [\_ \_ WPD-OBJEKTINHALTSTYP \_](object-properties.md)                                           | Erforderlich.                                                                                                           |
| [\_WPD-OBJEKT \_ ISHIDDEN](object-properties.md)                                                    | Erforderlich, wenn das Objekt ausgeblendet ist.                                                                                   |
| [\_WPD-OBJEKT \_ ISSYSTEM](object-properties.md)                                                    | Erforderlich, wenn das -Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).                                               |
| [\_WPD-OBJEKTGRÖßE \_](object-properties.md)                                                            | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                                                                   |
| [\_WPD-OBJEKT \_ \_ URSPRÜNGLICHER \_ DATEINAME](object-properties.md)                              | Erforderlich, wenn das -Objekt eine Datei darstellt.                                                                           |
| [\_WPD-OBJEKT \_ NICHT \_ VERWENDBAR](object-properties.md)                                       | Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist.                                               |
| [\_ \_ WPD-OBJEKTVERWEISE](object-properties.md)                                                | Erforderlich, wenn das -Objekt Verweise auf andere Objekte enthält.                                                             |
| [\_WPD-OBJEKTSCHLÜSSELWÖRTER \_](object-properties.md)                                                    | Optional.                                                                                                           |
| [\_ \_ WPD-OBJEKTSYNCHRONISIERUNGS-ID \_](object-properties.md)                                                     | Optional.                                                                                                           |
| [\_WPD-OBJEKT \_ IST \_ \_ DRM-GESCHÜTZT](object-properties.md)                                  | Erforderlich, wenn das Objekt durch DRM-Technologie geschützt ist.                                                              |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                           | Optional.                                                                                                           |
| [\_WPD-OBJEKTDATUM \_ \_ GEÄNDERT](object-properties.md)                                         | Empfohlen.                                                                                                        |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                         | Optional.                                                                                                           |
| [WPD \_ OBJECT BACK REFERENCES (WPD-OBJEKTVERWEISE \_ \_ ZURÜCK)](object-properties.md)                                                                | Wird empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.                                                          |
| [\_ \_ WPD-OBJEKTCONTAINER \_ FUNKTIONALE \_ \_ OBJEKT-ID](object-properties.md)     | Optional.                                                                                                           |
| [\_WPD-OBJEKT \_ GENERIERT \_ \_ MINIATURANSICHT AUS \_ RESSOURCE](object-properties.md) | Optional.                                                                                                           |
| [WPD \_ FUNCTIONAL \_ OBJECT \_ CATEGORY](miscellaneous-properties.md)                      | Erforderlich.                                                                                                           |
| [\_ \_ WPD-GERÄTESYNCHRONISIERUNGSPARTNER \_](device-properties.md)                                           | Optional.                                                                                                           |
| [\_ \_ WPD-GERÄTEFIRMWAREVERSION \_](device-properties.md)                                   | Erforderlich.                                                                                                           |
| [\_ \_ \_ WPD-GERÄTELEISTUNGSSTUFE](device-properties.md)                                             | Empfohlen, wenn das Gerät über einen Akku verfügt.                                                                                |
| [\_ \_ WPD-GERÄTESTROMQUELLE \_](device-properties.md)                                           | Empfohlen.                                                                                                        |
| [\_WPD-GERÄTEPROTOKOLL \_](device-properties.md)                                                    | Empfohlen.                                                                                                        |
| [\_WPD-GERÄTEHERSTELLER \_](device-properties.md)                                            | Erforderlich.                                                                                                           |
| [\_WPD-GERÄTEMODELL \_](device-properties.md)                                                          | Erforderlich.                                                                                                           |
| [\_ \_ WPD-GERÄTESERIENNUMMER \_](device-properties.md)                                         | Erforderlich.                                                                                                           |
| [\_WPD-GERÄT \_ UNTERSTÜTZT NICHT \_ VERWENDBARE \_ GERÄTE](device-properties.md)                    | Erforderlich, wenn das Gerät nicht gebrauchsbare Objekte unterstützt. Das heißt, wenn das Gerät für die einfache Datenspeicherung verwendet werden kann. |
| [WPD \_ DEVICE \_ DATETIME](device-properties.md)                                                    | Optional.                                                                                                           |
| [\_WPD-GERÄTE-FRIENDLY \_ \_ NAME](device-properties.md)                                         | Empfohlen.                                                                                                        |
| [VOM \_ WPD-GERÄT \_ UNTERSTÜTZTE \_ DRM-SCHEMAS \_](device-properties.md)                        | Empfohlen, wenn das Gerät DRM-Technologie unterstützt.                                                                  |
| [VOM \_ \_ WPD-GERÄT \_ UNTERSTÜTZTE FORMATE \_ WERDEN \_ GEORDNET.](device-properties.md)       | Empfohlen, wenn das Gerät die bevorzugte Formatbestellung unterstützt.                                                       |
| [\_WPD-GERÄTETYP \_](device-properties.md)                                                            | Empfohlen.                                                                                                        |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte hosten in der Regel keine Ressourcen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**FUNKTIONSOBJEKT DES \_ \_ WPD-INHALTSTYPS \_ \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



