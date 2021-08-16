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

Ein \_ \_ funktionales WPD FUNCTIONAL CATEGORY \_ DEVICE-Objekt kapselt das Gerät (das oberste Objekt des Geräts). Wenn ein Gerät diese Funktionskategorie implementiert, sollte es diese Eigenschaften zusätzlich zu den eigenschaften unterstützen, die für das [Geräteobjekt](device-object.md)aufgeführt sind.



| Eigenschaftsname                                                                                                         | Erforderlich oder optional                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [\_ \_ WPD-OBJEKT-ID](object-properties.md)                                                                | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zur Erstellungszeit nicht festlegen.                                      |
| [ÜBERGEORDNETE \_ \_ \_ WPD-OBJEKT-ID](object-properties.md)                                                 | Erforderlich.                                                                                                           |
| [\_WPD-OBJEKTNAME \_](object-properties.md)                                                            | Erforderlich.                                                                                                           |
| [\_PERSISTENTE EINDEUTIGE ID DES \_ \_ \_ WPD-OBJEKTS](object-properties.md)                          | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zur Erstellungszeit nicht festlegen.                                      |
| [\_WPD-OBJEKTFORMAT \_](object-properties.md)                                                        | Erforderlich.                                                                                                           |
| [\_ \_ WPD-OBJEKTINHALTSTYP \_](object-properties.md)                                           | Erforderlich.                                                                                                           |
| [\_WPD-OBJEKT \_ ISHIDDEN](object-properties.md)                                                    | Erforderlich, wenn das Objekt ausgeblendet ist.                                                                                   |
| [WPD \_ OBJECT \_ ISSYSTEM](object-properties.md)                                                    | Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).                                               |
| [\_WPD-OBJEKTGRÖßE \_](object-properties.md)                                                            | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                                                                   |
| [\_ \_ URSPRÜNGLICHER \_ \_ DATEINAME DES WPD-OBJEKTS](object-properties.md)                              | Erforderlich, wenn das -Objekt eine Datei darstellt.                                                                           |
| [\_WPD-OBJEKT \_ NICHT \_ VERWENDBAR](object-properties.md)                                       | Empfohlen, wenn das Objekt nicht für die Nutzung durch das Gerät vorgesehen ist.                                               |
| [\_ \_ WPD-OBJEKTVERWEISE](object-properties.md)                                                | Erforderlich, wenn das Objekt Verweise auf andere Objekte hat.                                                             |
| [\_ \_ WPD-OBJEKTSCHLÜSSELWÖRTER](object-properties.md)                                                    | Optional.                                                                                                           |
| [\_ \_ WPD-OBJEKTSYNCHRONISIERUNGS-ID \_](object-properties.md)                                                     | Optional.                                                                                                           |
| [\_WPD-OBJEKT \_ IST \_ \_ DRM-GESCHÜTZT](object-properties.md)                                  | Erforderlich, wenn das Objekt durch drm-Technologie geschützt ist.                                                              |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                           | Optional.                                                                                                           |
| [ÄNDERUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                         | Empfohlen.                                                                                                        |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                         | Optional.                                                                                                           |
| [\_ \_ WPD-OBJEKTRÜCKVERWEISE \_](object-properties.md)                                                                | Empfohlen, wenn ein anderes Objekt auf das Objekt verweist.                                                          |
| [FUNKTIONALE \_ \_ \_ \_ OBJEKT-ID DES WPD-OBJEKTCONTAINERS \_](object-properties.md)     | Optional.                                                                                                           |
| [\_WPD-OBJEKT \_ GENERIERT \_ \_ MINIATURANSICHTEN AUS \_ RESSOURCE](object-properties.md) | Optional.                                                                                                           |
| [WPD \_ FUNCTIONAL \_ OBJECT \_ CATEGORY](miscellaneous-properties.md)                      | Erforderlich.                                                                                                           |
| [\_ \_ WPD-GERÄTESYNCHRONISIERUNGSPARTNER \_](device-properties.md)                                           | Optional.                                                                                                           |
| [\_ \_ WPD-GERÄTEFIRMWAREVERSION \_](device-properties.md)                                   | Erforderlich.                                                                                                           |
| [WPD \_ DEVICE \_ POWER \_ LEVEL](device-properties.md)                                             | Empfohlen, wenn das Gerät über einen Akku verfügt.                                                                                |
| [WPD \_ DEVICE \_ POWER \_ SOURCE](device-properties.md)                                           | Empfohlen.                                                                                                        |
| [\_WPD-GERÄTEPROTOKOLL \_](device-properties.md)                                                    | Empfohlen.                                                                                                        |
| [\_WPD-GERÄTEHERSTELLER \_](device-properties.md)                                            | Erforderlich.                                                                                                           |
| [\_WPD-GERÄTEMODELL \_](device-properties.md)                                                          | Erforderlich.                                                                                                           |
| [\_ \_ WPD-GERÄTESERIENNUMMER \_](device-properties.md)                                         | Erforderlich.                                                                                                           |
| [\_WPD-GERÄT \_ UNTERSTÜTZT NICHT \_ \_ VERWENDBAR](device-properties.md)                    | Erforderlich, wenn das Gerät nicht verwendbare Objekte unterstützt. Das heißt, wenn das Gerät für die einfache Datenspeicherung verwendet werden kann. |
| [WPD \_ DEVICE \_ DATETIME](device-properties.md)                                                    | Optional.                                                                                                           |
| [ANZEIGENAME DES \_ WPD-GERÄTS \_ \_](device-properties.md)                                         | Empfohlen.                                                                                                        |
| [VOM \_ WPD-GERÄT \_ UNTERSTÜTZTE \_ \_ DRM-SCHEMAS](device-properties.md)                        | Empfohlen, wenn das Gerät DRM-Technologie unterstützt.                                                                  |
| [VOM \_ \_ WPD-GERÄT UNTERSTÜTZTE \_ FORMATE WERDEN \_ \_ SORTIERT.](device-properties.md)       | Empfohlen, wenn das Gerät die bevorzugte Formatreihenfolge unterstützt.                                                       |
| [\_WPD-GERÄTETYP \_](device-properties.md)                                                            | Empfohlen.                                                                                                        |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte hosten in der Regel keine Ressourcen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**\_FUNKTIONALES OBJEKT DES WPD-INHALTSTYPS \_ \_ \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



