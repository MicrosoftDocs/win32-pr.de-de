---
description: '\_WPD-INHALTSTYP \_ \_ NICHT ANGEGEBEN'
ms.assetid: 0175940e-2de2-4e2b-a98e-8dcc59e7020f
title: WPD_CONTENT_TYPE_UNSPECIFIED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd955ee5ebf31b2348efd3f70c85ae9c004edb83
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423680"
---
# <a name="wpd_content_type_unspecified"></a>\_WPD-INHALTSTYP \_ \_ NICHT ANGEGEBEN

Ein Objekt, das seinen Typ als WPD \_ CONTENT \_ TYPE \_ UNSPECIFIED beschreibt, stellt ein generisches Objekt dar, das möglicherweise über eine zugrunde liegende physische Datei verfügt. Der Unterschied zwischen diesem Typ und DER GENERISCHEN DATEI DES \_ \_ \_ \_ WPD-INHALTSTYPs besteht darin, dass GENERISCHE DATEIobjekte des \_ WPD-INHALTSTYPs \_ über eine zugrunde liegende physische \_ \_ Datei verfügen müssen.

Dieser Objekttyp unterstützt die folgenden Eigenschaften.



| Eigenschaftsname       | Erforderlich oder optional         |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [\_ \_ WPD-OBJEKT-ID](object-properties.md)                                                                | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft nicht einmal zur Erstellungszeit festlegen. |
| [ÜBERGEORDNETE \_ \_ \_ WPD-OBJEKT-ID](object-properties.md)                                                 | Erforderlich.                                                                     |
| [\_WPD-OBJEKTNAME \_](object-properties.md)                                                            | Erforderlich, wenn das -Objekt eine Datei darstellt.                                     |
| [\_PERSISTENTE EINDEUTIGE ID DES \_ \_ \_ WPD-OBJEKTS](object-properties.md)                          | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft nicht einmal zur Erstellungszeit festlegen. |
| [\_WPD-OBJEKTFORMAT \_](object-properties.md)                                                        | Erforderlich.                                                                     |
| [\_ \_ WPD-OBJEKTINHALTSTYP \_](object-properties.md)                                           | Erforderlich.                                                                     |
| [\_WPD-OBJEKT \_ ISHIDDEN](object-properties.md)                                                    | Erforderlich, wenn das Objekt ausgeblendet ist.                                             |
| [\_WPD-OBJEKT \_ ISSYSTEM](object-properties.md)                                                    | Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).         |
| [\_WPD-OBJEKTGRÖßE \_](object-properties.md)                                                            | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                             |
| [\_WPD-OBJEKT \_ \_ URSPRÜNGLICHER \_ DATEINAME](object-properties.md)                              | Erforderlich, wenn das -Objekt eine Datei darstellt.                                     |
| [\_WPD-OBJEKT \_ NICHT \_ VERWENDBAR](object-properties.md)                                       | Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist.         |
| [\_ \_ WPD-OBJEKTVERWEISE](object-properties.md)                                                | Erforderlich, wenn das -Objekt Verweise auf andere Objekte enthält.                       |
| [\_WPD-OBJEKTSCHLÜSSELWÖRTER \_](object-properties.md)                                                    | Dies ist optional.                                                                     |
| [\_ \_ WPD-OBJEKTSYNCHRONISIERUNGS-ID \_](object-properties.md)                                                     | Dies ist optional.                                                                     |
| [\_WPD-OBJEKT \_ IST \_ \_ DRM-GESCHÜTZT](object-properties.md)                                  | Erforderlich, wenn das Objekt durch DRM-Technologie geschützt ist.                        |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                           | Dies ist optional.                                                                     |
| [\_WPD-OBJEKTDATUM \_ \_ GEÄNDERT](object-properties.md)                                         | Empfohlen.                                                                  |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                         | Dies ist optional.                                                                     |
| [WPD \_ OBJECT BACK REFERENCES (WPD-OBJEKTVERWEISE \_ \_ ZURÜCK)](object-properties.md)                                                                | Wird empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.                    |
| [\_ \_ WPD-OBJEKTCONTAINER \_ FUNKTIONALE \_ \_ OBJEKT-ID](object-properties.md)     | Dies ist optional.                                                                     |
| [\_WPD-OBJEKT \_ GENERIERT \_ \_ MINIATURANSICHTEN AUS \_ RESSOURCE](object-properties.md) | Dies ist optional.                                                                     |
| [\_WPD-OBJEKT \_ KANN GELÖSCHT \_ WERDEN](object-properties.md)                                                                     | Erforderlich, wenn das Objekt nicht gelöscht werden kann.                                     |
| [\_GEBIETSSCHEMA DER WPD-OBJEKTSPRACHE \_ \_](object-properties.md)                                                                | Dies ist optional.                                                                     |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte enthalten in der Regel die folgenden Ressourcen.



| Ressourcenname                                          | Erforderlich oder optional                             | BESCHREIBUNG               |
|--------------------------------------------------------|--------------------------------------------------|---------------------------|
| [**\_WPD-RESSOURCENSTANDARD \_**](wpd-resource-default.md) | Erforderlich, wenn das Objekt durch Binärdaten gesichert wird. | Enthält die Binärdaten. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 



