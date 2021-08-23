---
description: WPD \_ FUNCTIONAL \_ CATEGORY \_ STILL \_ IMAGE \_ CAPTURE
ms.assetid: fb434927-1548-4c6e-bfb7-3a99eef62a4a
title: WPD_FUNCTIONAL_CATEGORY_STILL_IMAGE_CAPTURE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94fb0f6f19930780784083eaeddc1156bf55c99943aae8ad5850374c04211dbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119444810"
---
# <a name="wpd_functional_category_still_image_capture"></a>WPD \_ FUNCTIONAL \_ CATEGORY \_ STILL \_ IMAGE \_ CAPTURE

Ein WPD FUNCTIONAL CATEGORY STILL IMAGE CAPTURE-Funktionsobjekt kapselt die Bildaufnahmefunktion auf einem Gerät, z. B. eine Kamera oder \_ \_ eine \_ \_ \_ Kameraanlage.



| Eigenschaftsname                                                                                                            | Erforderlich oder optional                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_WPD-OBJEKT-ID \_](object-properties.md)                                                                   | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft nicht festlegen, auch nicht zum Zeitpunkt der Erstellung.                                                                         |
| [ÜBERGEORDNETE ID DES \_ \_ WPD-OBJEKTS \_](object-properties.md)                                                    | Erforderlich.                                                                                                                                              |
| [\_WPD-OBJEKTNAME \_](object-properties.md)                                                               | Erforderlich.                                                                                                                                              |
| [PERSISTENTE EINDEUTIGE ID \_ DES WPD-OBJEKTS \_ \_ \_](object-properties.md)                             | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft nicht festlegen, auch nicht zum Zeitpunkt der Erstellung.                                                                         |
| [\_WPD-OBJEKTFORMAT \_](object-properties.md)                                                           | Erforderlich.                                                                                                                                              |
| [\_ \_ WPD-OBJEKTINHALTSTYP \_](object-properties.md)                                              | Erforderlich.                                                                                                                                              |
| [\_WPD-OBJEKT \_ ISHIDDEN](object-properties.md)                                                       | Erforderlich, wenn das Objekt ausgeblendet ist.                                                                                                                      |
| [\_WPD-OBJEKT \_ ISSYSTEM](object-properties.md)                                                       | Erforderlich, wenn das -Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).                                                                                  |
| [\_WPD-OBJEKTGRÖßE \_](object-properties.md)                                                               | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                                                                                                      |
| [\_WPD-OBJEKT \_ \_ URSPRÜNGLICHER \_ DATEINAME](object-properties.md)                                 | Erforderlich, wenn das -Objekt eine Datei darstellt.                                                                                                              |
| [\_WPD-OBJEKT \_ NICHT \_ VERWENDBAR](object-properties.md)                                          | Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist.                                                                                  |
| [\_ \_ WPD-OBJEKTVERWEISE](object-properties.md)                                                   | Erforderlich, wenn das -Objekt Verweise auf andere Objekte enthält.                                                                                                |
| [\_WPD-OBJEKTSCHLÜSSELWÖRTER \_](object-properties.md)                                                       | Optional.                                                                                                                                              |
| [\_ \_ WPD-OBJEKTSYNCHRONISIERUNGS-ID \_](object-properties.md)                                                        | Optional.                                                                                                                                              |
| [\_WPD-OBJEKT \_ IST \_ \_ DRM-GESCHÜTZT](object-properties.md)                                     | Erforderlich, wenn das Objekt durch DRM-Technologie geschützt ist.                                                                                                 |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                              | Optional.                                                                                                                                              |
| [\_WPD-OBJEKTDATUM \_ \_ GEÄNDERT](object-properties.md)                                            | Empfohlen.                                                                                                                                           |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                            | Optional.                                                                                                                                              |
| [WPD \_ OBJECT BACK REFERENCES (WPD-OBJEKTVERWEISE \_ \_ ZURÜCK)](object-properties.md)                                                                   | Wird empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.                                                                                             |
| [\_ \_ WPD-OBJEKTCONTAINER \_ FUNKTIONALE \_ \_ OBJEKT-ID](object-properties.md)        | Optional.                                                                                                                                              |
| [\_WPD-OBJEKT \_ GENERIERT \_ \_ MINIATURANSICHT AUS \_ RESSOURCE](object-properties.md)    | Optional.                                                                                                                                              |
| [\_WPD-OBJEKT \_ KANN LÖSCHEN \_](object-properties.md)                                                                        | Erforderlich, wenn das Objekt nicht gelöscht werden kann.                                                                                                              |
| [WPD \_ OBJECT \_ LANGUAGE \_ LOCALE](object-properties.md)                                                                   | Optional.                                                                                                                                              |
| [WPD \_ FUNCTIONAL \_ OBJECT \_ CATEGORY](miscellaneous-properties.md)                         | Erforderlich. Unter [**WPD \_ CONTENT TYPE FUNCTIONAL \_ \_ \_ OBJECT**](wpd-content-type-functional-object.md) finden Sie Kategorien, die von portablen Windows definiert werden. |
| [WPD \_ STILL \_ IMAGE \_ CAPTURE \_ RESOLUTION](still-image-properties.md)                  | Erforderlich.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ CAPTURE \_ FORMAT](still-image-properties.md)                          | Erforderlich.                                                                                                                                              |
| [WPD–EINSTELLUNG \_ \_ FÜR DIE \_ BILDKOMPRIMIERUNG \_](still-image-properties.md)                | Optional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ WHITE \_ BALANCE](still-image-properties.md)                            | Optional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ RGB \_ GAIN](still-image-properties.md)                                      | Optional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ FNUMBER](still-image-properties.md)                                         | Optional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ FOCAL \_ LENGTH](still-image-properties.md)                              | Optional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ FOCUS \_ DISTANCE](still-image-properties.md)                          | Optional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ FOCUS \_ MODE](still-image-properties.md)                                  | Optional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ EXPOSURE \_ METERING \_ MODE](still-image-properties.md)         | Optional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ FLASH \_ MODE](still-image-properties.md)                                  | Optional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ EXPOSURE \_ TIME](still-image-properties.md)                            | Optional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ EXPOSURE \_ PROGRAM \_ MODE](still-image-properties.md)           | Optional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ EXPOSURE \_ INDEX](still-image-properties.md)                          | Optional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ EXPOSURE \_ BIAS \_ COMPENSATION](still-image-properties.md) | Optional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ CAPTURE \_ DELAY](still-image-properties.md)                            | Optional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ CAPTURE \_ MODE](still-image-properties.md)                              | Optional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ CONTRAST](still-image-properties.md)                                       | Optional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ SHARPNESS](still-image-properties.md)                                     | Optional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ DIGITAL \_ ZOOM](still-image-properties.md)                              | Optional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ \_ EFFECT-MODUS](still-image-properties.md)                                | Optional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ BURST \_ NUMBER](still-image-properties.md)                              | Optional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ BURST \_ INTERVAL](still-image-properties.md)                          | Optional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ TIMELAPSE \_ NUMBER](still-image-properties.md)                      | Optional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ TIMELAPSE \_ INTERVAL](still-image-properties.md)                  | Optional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ FOCUS \_ METERING \_ MODE](still-image-properties.md)               | Optional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ UPLOAD \_ URL](still-image-properties.md)                                  | Optional.                                                                                                                                              |
| [WPD \_ STILL \_ IMAGE \_ INTERPRET](still-image-properties.md)                                           | Optional.                                                                                                                                              |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte hosten in der Regel keine Ressourcen.

Viele dieser Eigenschaften haben miteinander verbundene Auswirkungen. Wenn beispielsweise **WPD \_ STILL IMAGE EXPOSURE \_ \_ \_ METERING \_ MODE** auf automatic festgelegt ist, werden F-Stop, Belichtungszeit und Belichtungsmessung verknüpft. Eine unterschiedliche Messung bewirkt, dass die anderen variieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**\_FUNKTIONALES OBJEKT DES WPD-INHALTSTYPS \_ \_ \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



