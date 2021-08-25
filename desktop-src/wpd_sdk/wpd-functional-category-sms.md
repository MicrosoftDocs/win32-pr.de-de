---
description: WPD \_ FUNCTIONAL \_ CATEGORY \_ SMS
ms.assetid: dbb536a6-9c12-459d-8098-ebe4fc4c8f2f
title: WPD_FUNCTIONAL_CATEGORY_SMS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273807900639f7c220bbb1828233bd717a8b814160167df3be87bda904d5a3e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838930"
---
# <a name="wpd_functional_category_sms"></a>WPD \_ FUNCTIONAL \_ CATEGORY \_ SMS

Ein \_ \_ funktionales WPD FUNCTIONAL CATEGORY \_ SMS-Objekt kapselt kurze Nachrichtendienstfunktionen (häufig als "SMS" bezeichnet) auf dem Gerät.



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
| [WPD \_ SMS \_ PROVIDER](sms-properties.md)                                                             | Erforderlich.                                                                                                                                              |
| [WPD \_ SMS \_ TIMEOUT](sms-properties.md)                                                               | Erforderlich.                                                                                                                                              |
| [WPD \_ SMS \_ MAX \_ PAYLOAD](sms-properties.md)                                                      | Erforderlich.                                                                                                                                              |
| [\_ \_ WPD-SMS-CODIERUNG](sms-properties.md)                                                             | Erforderlich.                                                                                                                                              |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte hosten in der Regel keine Ressourcen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**\_FUNKTIONALES OBJEKT DES WPD-INHALTSTYPS \_ \_ \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



