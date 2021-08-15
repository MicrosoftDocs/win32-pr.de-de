---
description: '\_FUNKTIONALES OBJEKT DES WPD-INHALTSTYPS \_ \_ \_'
ms.assetid: 112de70b-afcc-4fba-b74f-c33bd759d517
title: WPD_CONTENT_TYPE_FUNCTIONAL_OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58121d351219c246117106d578ed3672ebf25eecf9e159f957494b5c5eae9280
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193524"
---
# <a name="wpd_content_type_functional_object"></a>\_FUNKTIONALES OBJEKT DES WPD-INHALTSTYPS \_ \_ \_

Ein Objekt, das seinen Typ als WPD \_ CONTENT \_ FUNCTIONAL OBJECT \_ beschreibt, stellt ein funktionales Objekt dar, das die Gerätefunktionalität kapselt.

Alle funktionalen Objekte unterstützen unabhängig vom Typ die folgenden Eigenschaften. (Wenn Sie ein benutzerdefiniertes funktionales Objekt definieren, muss es auch diese Eigenschaften unterstützen.)



| Eigenschaftsname                                                                                                         | Erforderlich oder optional                                                                  |
|-----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [\_ \_ WPD-OBJEKT-ID](object-properties.md)                                                                | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zur Erstellungszeit nicht festlegen.        |
| [ÜBERGEORDNETE \_ \_ \_ WPD-OBJEKT-ID](object-properties.md)                                                 | Erforderlich.                                                                             |
| [\_WPD-OBJEKTNAME \_](object-properties.md)                                                            | Erforderlich.                                                                             |
| [\_PERSISTENTE EINDEUTIGE ID DES \_ \_ \_ WPD-OBJEKTS](object-properties.md)                          | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zur Erstellungszeit nicht festlegen.        |
| [\_WPD-OBJEKTFORMAT \_](object-properties.md)                                                        | Erforderlich.                                                                             |
| [\_ \_ WPD-OBJEKTINHALTSTYP \_](object-properties.md)                                           | Erforderlich.                                                                             |
| [\_WPD-OBJEKT \_ ISHIDDEN](object-properties.md)                                                    | Erforderlich, wenn das Objekt ausgeblendet ist.                                                     |
| [WPD \_ OBJECT \_ ISSYSTEM](object-properties.md)                                                    | Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).                 |
| [\_WPD-OBJEKTGRÖßE \_](object-properties.md)                                                            | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                                     |
| [\_ \_ URSPRÜNGLICHER \_ \_ DATEINAME DES WPD-OBJEKTS](object-properties.md)                              | Erforderlich, wenn das -Objekt eine Datei darstellt.                                             |
| [\_WPD-OBJEKT \_ NICHT \_ VERWENDBAR](object-properties.md)                                       | Empfohlen, wenn das Objekt nicht für die Nutzung durch das Gerät vorgesehen ist.                 |
| [\_ \_ WPD-OBJEKTVERWEISE](object-properties.md)                                                | Erforderlich, wenn das Objekt Verweise auf andere Objekte hat.                               |
| [\_ \_ WPD-OBJEKTSCHLÜSSELWÖRTER](object-properties.md)                                                    | Optional.                                                                             |
| [\_ \_ WPD-OBJEKTSYNCHRONISIERUNGS-ID \_](object-properties.md)                                                     | Optional.                                                                             |
| [\_WPD-OBJEKT \_ IST \_ \_ DRM-GESCHÜTZT](object-properties.md)                                  | Erforderlich, wenn das Objekt durch drm-Technologie geschützt ist.                                |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                           | Optional.                                                                             |
| [ÄNDERUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                         | Empfohlen.                                                                          |
| [ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_](object-properties.md)                                         | Optional.                                                                             |
| [\_ \_ WPD-OBJEKTRÜCKVERWEISE \_](object-properties.md)                                                                | Empfohlen, wenn ein anderes Objekt auf das Objekt verweist.                            |
| [FUNKTIONALE \_ \_ \_ \_ OBJEKT-ID DES WPD-OBJEKTCONTAINERS \_](object-properties.md)     | Optional.                                                                             |
| [\_WPD-OBJEKT \_ GENERIERT \_ \_ MINIATURANSICHTEN AUS \_ RESSOURCE](object-properties.md) | Optional.                                                                             |
| [\_WPD-OBJEKT \_ KANN GELÖSCHT \_ WERDEN](object-properties.md)                                                                     | Erforderlich, wenn das Objekt nicht gelöscht werden kann.                                             |
| [\_GEBIETSSCHEMA DER WPD-OBJEKTSPRACHE \_ \_](object-properties.md)                                                                | Optional.                                                                             |
| [WPD \_ FUNCTIONAL \_ OBJECT \_ CATEGORY](miscellaneous-properties.md)                      | Erforderlich. In der folgenden Tabelle finden Sie Kategorien, die von Windows Portable Devices definiert werden. |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte hosten in der Regel keine Ressourcen.

## <a name="functional-object-categories"></a>Funktionale Objektkategorien

Funktionale Objekte können abhängig von ihren Funktionen in Kategorien gruppiert werden. Eine Kategorie wird von der WPD \_ FUNCTIONAL \_ OBJECT \_ CATEGORY-Eigenschaft (ein GUID-Wert) beschrieben. Die Kategorie bestimmt, welche zusätzlichen Eigenschaften unterstützt werden.

In der folgenden Tabelle werden die Kategorien beschrieben, die von Windows Portable Devices definiert werden. In der Beschreibung der Kategorie erfahren Sie, welche zusätzlichen Eigenschaften und Ressourcen das Objekt unterstützt.



| Funktionale Kategorie                                                                                        | BESCHREIBUNG                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WPD \_ FUNCTIONAL \_ CATEGORY \_ ALL**](wpd-functional-category-all.md)                                      | Diese Funktionskategorie ist nur als Parameter für bestimmte Abfragefunktionen gültig (um anzugeben, dass alle funktionalen Objekttypen akzeptabel sind) und ist keine vom Treiber gemeldete Funktionskategorie. |
| [**WPD \_ FUNCTIONAL \_ CATEGORY \_ AUDIO \_ CAPTURE**](wpd-functional-category-audio-capture.md)                 | Das -Objekt kapselt die Audioaufnahmefunktionen auf dem Gerät, z. B. einen Sprachaufzeichnungs- oder eine andere Audioaufzeichnungskomponente.                                                                      |
| [**WPD \_ FUNCTIONAL \_ CATEGORY \_ DEVICE**](wpd-functional-category-device.md)                                | Das -Objekt kapselt das Gerät (das oberste Objekt des Geräts).                                                                                                                          |
| [**WPD \_ FUNCTIONAL \_ CATEGORY \_ NETWORK \_ CONFIGURATION**](wpd-functional-category-network-configuration.md) | Das -Objekt kapselt die Netzwerkkonfigurationsfunktionalität für das Gerät, z. B. WLAN-Profile oder Partnerschaften.                                                                                   |
| [**\_WPD FUNCTIONAL \_ CATEGORY RENDERING INFORMATION \_ (WPD-FUNKTIONSKATEGORIERENDERINGINFORMATIONEN) \_**](wpd-functional-category-rendering-information.md) | Das -Objekt beschreibt die Typen von Mediendateien, die das Gerät wiedergeben kann.                                                                                                                            |
| [**WPD \_ FUNCTIONAL \_ CATEGORY \_ SMS**](wpd-functional-category-sms.md)                                      | Das -Objekt kapselt kurze Nachrichtendienstfunktionen (häufig als "SMS" bezeichnet) auf dem Gerät.                                                                                             |
| [**WPD \_ FUNCTIONAL \_ CATEGORY \_ STILL \_ IMAGE \_ CAPTURE**](wpd-functional-category-still-image-capture.md)    | Das -Objekt kapselt die Bildaufnahmefunktionalität auf einem Gerät, z. B. einer Kamera oder einem Kameragerät.                                                                                              |
| [**SPEICHER \_ DER WPD-FUNKTIONSKATEGORIE \_ \_**](wpd-functional-category-storage.md)                              | Das -Objekt kapselt den physischen Dateispeicher auf dem Gerät.                                                                                                                                              |
| [**WPD \_ FUNCTIONAL \_ CATEGORY \_ VIDEO \_ CAPTURE**](wpd-functional-category-video-capture.md)                 | Das -Objekt kapselt die Videoaufnahmefunktionen auf dem Gerät, z. B. eine Videoaufzeichnungskomponente. Eine Anwendung verwendet dieses Objekt, um programmgesteuerte Steuerung zu erhalten.                                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 



