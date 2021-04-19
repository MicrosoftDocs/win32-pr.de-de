---
description: Bild für WPD- \_ \_ Inhaltstyp \_
ms.assetid: 87342ac7-3f4d-4ed2-99f1-843a79032c6e
title: WPD_CONTENT_TYPE_IMAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d547a6190df01f495c0a340010b4305f5c77bf5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363658"
---
# <a name="wpd_content_type_image"></a>Bild für WPD- \_ \_ Inhaltstyp \_

Ein-Objekt, das den Typ als WPD- \_ \_ Inhaltstyp Bild beschreibt, \_ stellt ein Image dar.

Dieser Objekttyp unterstützt die folgenden Eigenschaften.



| Eigenschaftsname                                                                                                         | Erforderlich oder optional                                                                             |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [WPD- \_ Objekt- \_ ID](object-properties.md)                                                                | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zum Zeitpunkt der Erstellung nicht festlegen.                   |
| [übergeordnete WPD- \_ Objekt- \_ \_ ID](object-properties.md)                                                 | Erforderlich.                                                                                        |
| [WPD- \_ Objekt \_ Name](object-properties.md)                                                            | Erforderlich, wenn das-Objekt eine Datei darstellt.                                                        |
| [\_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt](object-properties.md)                          | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zum Zeitpunkt der Erstellung nicht festlegen.                   |
| [WPD- \_ Objekt \_ Format](object-properties.md)                                                        | Erforderlich.                                                                                        |
| [Inhaltstyp für WPD- \_ Objekt \_ \_](object-properties.md)                                           | Erforderlich.                                                                                        |
| [WPD- \_ Objekt \_ IsHidden](object-properties.md)                                                    | Erforderlich, wenn das Objekt ausgeblendet ist.                                                                |
| [WPD- \_ Objekt \_ IsSystem](object-properties.md)                                                    | Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).                            |
| [WPD- \_ Objekt \_ Größe](object-properties.md)                                                            | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                                                |
| [\_ \_ ursprünglicher \_ Dateiname \_ des WPD-Objekts](object-properties.md)                              | Erforderlich, wenn das-Objekt eine Datei darstellt.                                                        |
| [WPD- \_ Objekt \_ nicht \_ verwendbar](object-properties.md)                                       | Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist.                            |
| [Verweise auf WPD- \_ Objekte \_](object-properties.md)                                                | Erforderlich, wenn das-Objekt über Verweise auf andere-Objekte verfügt.                                          |
| [WPD- \_ Objekt \_ Schlüsselwörter](object-properties.md)                                                    | Dies ist optional.                                                                                        |
| [WPD- \_ Objekt \_ Synchronisierungs- \_ ID](object-properties.md)                                                     | Dies ist optional.                                                                                        |
| [WPD- \_ Objekt \_ ist DRM- \_ \_ geschützt](object-properties.md)                                  | Erforderlich, wenn das Objekt durch DRM-Technologie geschützt wird.                                           |
| [\_ \_ Erstellungsdatum des WPD-Objekts \_](object-properties.md)                                           | Dies ist optional.                                                                                        |
| [Datum des WPD- \_ Objekts \_ \_ geändert](object-properties.md)                                         | Empfohlen.                                                                                     |
| [erstelltes WPD- \_ Objekt \_ Datum \_](object-properties.md)                                         | Dies ist optional.                                                                                        |
| [\_ \_ zurück \_ Verweise auf WPD-Objekte](object-properties.md)                                                                | Empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.                                       |
| [\_ \_ \_ Funktions \_ Objekt- \_ ID des WPD-Objekt Containers](object-properties.md)     | Dies ist optional.                                                                                        |
| [WPD \_ - \_ Objekt \_ generieren \_ der Miniaturansicht aus der \_ Ressource](object-properties.md) | Dies ist optional.                                                                                        |
| [Bittiefe des WPD- \_ Bilds \_](image-properties.md)                                                       | Empfohlen.                                                                                     |
| [ausgeschnittener WPD- \_ Image \_ \_ Status](image-properties.md)                                          | Dies ist optional.                                                                                        |
| [Status der \_ \_ \_ korrigierten WPD-Bild Farbe \_](image-properties.md)                         | Dies ist optional.                                                                                        |
| [WPD- \_ Image- \_ Nummer](image-properties.md)                                                                           | Dies ist optional.                                                                                        |
| [Anzeigezeit für WPD- \_ Image \_ \_](image-properties.md)                                                                    | Dies ist optional.                                                                                        |
| [Index für WPD- \_ Image verfügbar \_ \_](image-properties.md)                                                                   | Dies ist optional.                                                                                        |
| [horizontale Auflösung des WPD- \_ Bilds \_ \_](image-properties.md)                                                            | Dies ist optional.                                                                                        |
| [vertikale Auflösung des WPD- \_ Bilds \_ \_](image-properties.md)                                                              | Dies ist optional.                                                                                        |
| [Copyright von WPD- \_ Medien \_](media-properties.md)                                                     | Dies ist optional.                                                                                        |
| [WPD- \_ Medien \_ Breite](media-properties.md)                                                             | Erforderlich.                                                                                        |
| [WPD- \_ Medien \_ Höhe](media-properties.md)                                                           | Erforderlich.                                                                                        |
| [WPD- \_ Medien \_ Künstler](media-properties.md)                                                                            | Empfohlen.                                                                                     |
| [WPD \_ Media \_ Album- \_ Künstler](media-properties.md)                                                                     | Empfohlen. Diese Eigenschaft identifiziert die Person oder Personen, die das Objekt ursprünglich erstellt haben. |
| [WPD- \_ Medien \_ Quellen- \_ URL](media-properties.md)                                                                       | Dies ist optional.                                                                                        |
| [Ziel-URL für WPD- \_ Medien \_ \_](media-properties.md)                                                                  | Dies ist optional.                                                                                        |
| [WPD- \_ Medien \_ Beschreibung](media-properties.md)                                                                       | Dies ist optional.                                                                                        |
| [WPD- \_ Medien \_ Genre](media-properties.md)                                                                             | Dies ist optional.                                                                                        |
| [WPD- \_ Medien \_ Byte- \_ Lesezeichen](media-properties.md)                                                                    | Dies ist optional.                                                                                        |
| [WPD- \_ Medien- \_ GUID](media-properties.md)                                                                              | Dies ist optional.                                                                                        |
| [\_ \_ unter \_ Beschreibung der WPD-Medien](media-properties.md)                                                                  | Dies ist optional.                                                                                        |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte enthalten in der Regel die folgenden Ressourcen.



| Ressourcenname                                                 | Erforderlich oder optional | BESCHREIBUNG                                                                              |
|---------------------------------------------------------------|----------------------|------------------------------------------------------------------------------------------|
| [**WPD- \_ Ressourcen \_ Standard**](wpd-resource-default.md)        | Erforderlich.            | Enthält die Bilddaten.                                                                 |
| [**WPD- \_ Ressourcen \_ Miniaturansicht**](wpd-resource-thumbnail.md)    | Empfohlen.         | Enthält die Miniaturansicht für das Bild.                                                    |
| [**WPD \_ \_ - \_ ressourcenaudioclip**](wpd-resource-audio-clip.md) | Dies ist optional.            | Wenn diesem Bild eine Audioanmerkung zugeordnet ist, enthält diese Ressource die Audiodaten. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 



