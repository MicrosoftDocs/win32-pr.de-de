---
description: '\_ \_ WPD-INHALTSTYPPROGRAMM \_'
ms.assetid: 81eaf8cf-0f4f-4587-911a-063630af1c8e
title: WPD_CONTENT_TYPE_PROGRAM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ddf3c5d406c16891c692e84fb37c4d21757f702
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423770"
---
# <a name="wpd_content_type_program"></a>\_ \_ WPD-INHALTSTYPPROGRAMM \_

Ein Objekt, das seinen Typ als WPD CONTENT TYPE PROGRAM beschreibt, \_ \_ stellt ein \_ ausführbares Programm dar.

Dieser Objekttyp unterstützt die folgenden Eigenschaften.



| Eigenschaftsname     | Erforderlich oder optional      |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [\_ \_ WPD-OBJEKT-ID](object-properties.md)                                                                | Erforderlich, aber schreibgeschützt. Ein Client kann diese Eigenschaft auch zur Erstellungszeit nicht festlegen. |
| [ÜBERGEORDNETE \_ \_ \_ WPD-OBJEKT-ID](object-properties.md)                                                 | Erforderlich.                                                                          |
| [\_WPD-OBJEKTNAME \_](object-properties.md)                                                            | Erforderlich, wenn das -Objekt eine Datei darstellt.                                          |
| [\_PERSISTENTE EINDEUTIGE ID DES \_ \_ \_ WPD-OBJEKTS](object-properties.md)                          | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft nicht einmal zur Erstellungszeit festlegen.      |
| [\_WPD-OBJEKTFORMAT \_](object-properties.md)                                                        | Erforderlich.                                                                          |
| [\_ \_ WPD-OBJEKTINHALTSTYP \_](object-properties.md)                                           | Erforderlich.                                                                          |
| [\_WPD-OBJEKT \_ ISHIDDEN](object-properties.md)                                                    | Erforderlich, wenn das Objekt ausgeblendet ist.                                                  |
| [WPD \_ OBJECT \_ ISSYSTEM](object-properties.md)                                                    | Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).              |
| [\_WPD-OBJEKTGRÖßE \_](object-properties.md)                                                            | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                                  |
| [\_WPD-OBJEKT \_ \_ URSPRÜNGLICHER \_ DATEINAME](object-properties.md)                              | Erforderlich, wenn das -Objekt eine Datei darstellt.                                          |
| [\_WPD-OBJEKT \_ NICHT \_ VERWENDBAR](object-properties.md)                                       | Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist.              |
| [\_ \_ WPD-OBJEKTVERWEISE](object-properties.md)                                                | Erforderlich, wenn das -Objekt Verweise auf andere Objekte enthält.                            |
| [\_WPD-OBJEKTSCHLÜSSELWÖRTER \_](object-properties.md)                                                    | Dies ist optional.                                                                          |
| [\_ \_ WPD-OBJEKTSYNCHRONISIERUNGS-ID \_](object-properties.md)                                                     | Dies ist optional.                                                                          |
| [\_WPD-OBJEKT \_ IST \_ \_ DRM-GESCHÜTZT](object-properties.md)                                  | Erforderlich, wenn das Objekt durch DRM-Technologie geschützt ist.                             |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                           | Dies ist optional.                                                                          |
| [\_WPD-OBJEKTDATUM \_ \_ GEÄNDERT](object-properties.md)                                         | Empfohlen.                                                                       |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                         | Dies ist optional.                                                                          |
| [WPD \_ OBJECT BACK REFERENCES (WPD-OBJEKTVERWEISE \_ \_ ZURÜCK)](object-properties.md)                                                                | Wird empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.                         |
| [\_ \_ WPD-OBJEKTCONTAINER \_ FUNKTIONALE \_ \_ OBJEKT-ID](object-properties.md)     | Dies ist optional.                                                                          |
| [\_WPD-OBJEKT \_ GENERIERT \_ \_ MINIATURANSICHT AUS \_ RESSOURCE](object-properties.md) | Dies ist optional.                                                                          |
| [\_WPD-OBJEKT \_ KANN GELÖSCHT \_ WERDEN](object-properties.md)                                                                     | Erforderlich, wenn das Objekt nicht gelöscht werden kann.                                          |
| [\_GEBIETSSCHEMA DER WPD-OBJEKTSPRACHE \_ \_](object-properties.md)                                                                | Dies ist optional.                                                                          |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte enthalten in der Regel die folgenden Ressourcen.



| Ressourcenname                                          | Erforderlich oder optional | BESCHREIBUNG                |
|--------------------------------------------------------|----------------------|----------------------------|
| [**\_WPD-RESSOURCENSTANDARD \_**](wpd-resource-default.md) | Erforderlich.            | Enthält die Programmdatei. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 



