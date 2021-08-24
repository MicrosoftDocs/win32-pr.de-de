---
description: SPEICHER \_ DER WPD-FUNKTIONSKATEGORIE \_ \_
ms.assetid: 92a10de6-3e50-4042-a9b7-3c1d5944791f
title: WPD_FUNCTIONAL_CATEGORY_STORAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b16d70ebff4c61643b4d5ae0f8b333f5f9a7dc02103a32e14ded7a0ac4d8189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805937"
---
# <a name="wpd_functional_category_storage"></a>SPEICHER \_ DER WPD-FUNKTIONSKATEGORIE \_ \_

Ein funktionales WPD \_ FUNCTIONAL \_ CATEGORY \_ STORAGE-Objekt kapselt physischen Dateispeicher auf dem Gerät.



| Eigenschaftsname                                                                                                         | Erforderlich oder optional                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_ \_ WPD-OBJEKT-ID](object-properties.md)                                                                | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zur Erstellungszeit nicht festlegen.                                                                         |
| [ÜBERGEORDNETE \_ \_ \_ WPD-OBJEKT-ID](object-properties.md)                                                 | Erforderlich.                                                                                                                                              |
| [\_WPD-OBJEKTNAME \_](object-properties.md)                                                            | Erforderlich.                                                                                                                                              |
| [\_PERSISTENTE EINDEUTIGE ID DES \_ \_ \_ WPD-OBJEKTS](object-properties.md)                          | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zur Erstellungszeit nicht festlegen.                                                                         |
| [\_WPD-OBJEKTFORMAT \_](object-properties.md)                                                        | Erforderlich.                                                                                                                                              |
| [\_ \_ WPD-OBJEKTINHALTSTYP \_](object-properties.md)                                           | Erforderlich.                                                                                                                                              |
| [\_WPD-OBJEKT \_ ISHIDDEN](object-properties.md)                                                    | Erforderlich, wenn das Objekt ausgeblendet ist.                                                                                                                      |
| [WPD \_ OBJECT \_ ISSYSTEM](object-properties.md)                                                    | Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).                                                                                  |
| [\_WPD-OBJEKTGRÖßE \_](object-properties.md)                                                            | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                                                                                                      |
| [\_ \_ URSPRÜNGLICHER \_ \_ DATEINAME DES WPD-OBJEKTS](object-properties.md)                              | Erforderlich, wenn das -Objekt eine Datei darstellt.                                                                                                              |
| [\_WPD-OBJEKT \_ NICHT \_ VERWENDBAR](object-properties.md)                                       | Empfohlen, wenn das Objekt nicht für die Nutzung durch das Gerät vorgesehen ist.                                                                                  |
| [\_ \_ WPD-OBJEKTVERWEISE](object-properties.md)                                                | Erforderlich, wenn das Objekt Verweise auf andere Objekte hat.                                                                                                |
| [\_ \_ WPD-OBJEKTSCHLÜSSELWÖRTER](object-properties.md)                                                    | Optional.                                                                                                                                              |
| [\_ \_ WPD-OBJEKTSYNCHRONISIERUNGS-ID \_](object-properties.md)                                                     | Optional.                                                                                                                                              |
| [\_WPD-OBJEKT \_ IST \_ \_ DRM-GESCHÜTZT](object-properties.md)                                  | Erforderlich, wenn das Objekt durch drm-Technologie geschützt ist.                                                                                                 |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                           | Optional.                                                                                                                                              |
| [ÄNDERUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                         | Empfohlen.                                                                                                                                           |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                         | Optional.                                                                                                                                              |
| [\_ \_ WPD-OBJEKTRÜCKVERWEISE \_](object-properties.md)                                                                | Empfohlen, wenn ein anderes Objekt auf das Objekt verweist.                                                                                             |
| [FUNKTIONALE \_ \_ \_ \_ OBJEKT-ID DES WPD-OBJEKTCONTAINERS \_](object-properties.md)     | Optional.                                                                                                                                              |
| [\_WPD-OBJEKT \_ GENERIERT \_ \_ MINIATURANSICHTEN AUS \_ RESSOURCE](object-properties.md) | Optional.                                                                                                                                              |
| [\_WPD-OBJEKT \_ KANN GELÖSCHT \_ WERDEN](object-properties.md)                                                                     | Erforderlich, wenn das Objekt nicht gelöscht werden kann.                                                                                                              |
| [\_GEBIETSSCHEMA DER WPD-OBJEKTSPRACHE \_ \_](object-properties.md)                                                                | Optional.                                                                                                                                              |
| [WPD \_ FUNCTIONAL \_ OBJECT \_ CATEGORY](miscellaneous-properties.md)                      | Erforderlich. Unter [**WPD \_ CONTENT TYPE FUNCTIONAL \_ \_ \_ OBJECT**](wpd-content-type-functional-object.md) finden Sie Kategorien, die von Windows Portable Devices definiert werden. |
| [\_WPD-SPEICHERTYP \_](storage-properties.md)                                                         | Erforderlich.                                                                                                                                              |
| [\_ \_ \_ WPD-SPEICHERDATEISYSTEMTYP \_](storage-properties.md)                               | Optional.                                                                                                                                              |
| [\_WPD-SPEICHERKAPAZITÄT \_](storage-properties.md)                                                 | Erforderlich.                                                                                                                                              |
| [FREIER \_ \_ WPD-SPEICHERPLATZ \_ \_ IN \_ BYTES](storage-properties.md)                        | Optional.                                                                                                                                              |
| [FREIER \_ \_ WPD-SPEICHERPLATZ \_ \_ IN \_ OBJEKTEN](storage-properties.md)                    | Optional.                                                                                                                                              |
| [\_ \_ WPD-SPEICHERBESCHREIBUNG](storage-properties.md)                                           | Optional.                                                                                                                                              |
| [\_ \_ \_ WPD-SPEICHERSERIENNUMMER](storage-properties.md)                                      | Optional.                                                                                                                                              |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte enthalten in der Regel die folgenden Ressourcen.



| Ressourcenname                                    | Erforderlich oder optional | Beschreibung                                        |
|--------------------------------------------------|----------------------|----------------------------------------------------|
| [**\_WPD-RESSOURCENSYMBOL \_**](wpd-resource-icon.md) | Optional.            | Enthält die Symboldarstellung für diesen Speicher. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**\_FUNKTIONALES OBJEKT DES WPD-INHALTSTYPS \_ \_ \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



