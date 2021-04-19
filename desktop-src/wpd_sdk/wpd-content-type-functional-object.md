---
description: Funktions Objekt des WPD- \_ \_ Inhaltstyp \_ \_
ms.assetid: 112de70b-afcc-4fba-b74f-c33bd759d517
title: WPD_CONTENT_TYPE_FUNCTIONAL_OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8516d29bf08b4873dc80c72b9a23de19dc50d0e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362615"
---
# <a name="wpd_content_type_functional_object"></a>Funktions Objekt des WPD- \_ \_ Inhaltstyp \_ \_

Ein Objekt, das den Typ als WPD- \_ Inhalts \_ Funktions Objekt beschreibt, das \_ ein funktionales Objekt darstellt, das die Gerätefunktionalität kapselt.

Alle funktionalen Objekte, unabhängig vom Typ, unterstützen die folgenden Eigenschaften. (Wenn Sie ein benutzerdefiniertes funktionales Objekt definieren, muss es auch diese Eigenschaften unterstützen.)



| Eigenschaftsname                                                                                                         | Erforderlich oder optional                                                                  |
|-----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [WPD- \_ Objekt- \_ ID](object-properties.md)                                                                | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zum Zeitpunkt der Erstellung nicht festlegen.        |
| [übergeordnete WPD- \_ Objekt- \_ \_ ID](object-properties.md)                                                 | Erforderlich.                                                                             |
| [WPD- \_ Objekt \_ Name](object-properties.md)                                                            | Erforderlich.                                                                             |
| [\_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt](object-properties.md)                          | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zum Zeitpunkt der Erstellung nicht festlegen.        |
| [WPD- \_ Objekt \_ Format](object-properties.md)                                                        | Erforderlich.                                                                             |
| [Inhaltstyp für WPD- \_ Objekt \_ \_](object-properties.md)                                           | Erforderlich.                                                                             |
| [WPD- \_ Objekt \_ IsHidden](object-properties.md)                                                    | Erforderlich, wenn das Objekt ausgeblendet ist.                                                     |
| [WPD- \_ Objekt \_ IsSystem](object-properties.md)                                                    | Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).                 |
| [WPD- \_ Objekt \_ Größe](object-properties.md)                                                            | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                                     |
| [\_ \_ ursprünglicher \_ Dateiname \_ des WPD-Objekts](object-properties.md)                              | Erforderlich, wenn das-Objekt eine Datei darstellt.                                             |
| [WPD- \_ Objekt \_ nicht \_ verwendbar](object-properties.md)                                       | Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist.                 |
| [Verweise auf WPD- \_ Objekte \_](object-properties.md)                                                | Erforderlich, wenn das-Objekt über Verweise auf andere-Objekte verfügt.                               |
| [WPD- \_ Objekt \_ Schlüsselwörter](object-properties.md)                                                    | Dies ist optional.                                                                             |
| [WPD- \_ Objekt \_ Synchronisierungs- \_ ID](object-properties.md)                                                     | Dies ist optional.                                                                             |
| [WPD- \_ Objekt \_ ist DRM- \_ \_ geschützt](object-properties.md)                                  | Erforderlich, wenn das Objekt durch DRM-Technologie geschützt wird.                                |
| [\_ \_ Erstellungsdatum des WPD-Objekts \_](object-properties.md)                                           | Dies ist optional.                                                                             |
| [Datum des WPD- \_ Objekts \_ \_ geändert](object-properties.md)                                         | Empfohlen.                                                                          |
| [erstelltes WPD- \_ Objekt \_ Datum \_](object-properties.md)                                         | Dies ist optional.                                                                             |
| [\_ \_ zurück \_ Verweise auf WPD-Objekte](object-properties.md)                                                                | Empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.                            |
| [\_ \_ \_ Funktions \_ Objekt- \_ ID des WPD-Objekt Containers](object-properties.md)     | Dies ist optional.                                                                             |
| [WPD \_ - \_ Objekt \_ generieren \_ der Miniaturansicht aus der \_ Ressource](object-properties.md) | Dies ist optional.                                                                             |
| [WPD- \_ Objekt \_ kann \_ Löschen](object-properties.md)                                                                     | Erforderlich, wenn das Objekt nicht gelöscht werden kann.                                             |
| [Gebiets Schema der WPD- \_ Objekt \_ Sprache \_](object-properties.md)                                                                | Dies ist optional.                                                                             |
| [WPD- \_ Funktions \_ Objekt \_ Kategorie](miscellaneous-properties.md)                      | Erforderlich. In der folgenden Tabelle finden Sie die Kategorien, die von tragbaren Windows-Geräten definiert werden. |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte Hosten in der Regel keine Ressourcen.

## <a name="functional-object-categories"></a>Funktionale Objektkategorien

Funktionale Objekte können abhängig von ihren Funktionen in Kategorien gruppiert werden. Eine Kategorie wird durch die Eigenschaft "WPD \_ Functional \_ Object \_ Category" (ein GUID-Wert) beschrieben. Die Kategorie bestimmt, welche zusätzlichen Eigenschaften unterstützt werden.

In der folgenden Tabelle werden die Kategorien beschrieben, die von tragbaren Windows-Geräten definiert werden. Weitere Informationen zu den zusätzlichen Eigenschaften und Ressourcen, die das Objekt unterstützt, finden Sie in der Beschreibung der Kategorie.



| Funktionale Kategorie                                                                                        | BESCHREIBUNG                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WPD- \_ Funktions \_ Kategorie \_ alle**](wpd-functional-category-all.md)                                      | Diese funktionale Kategorie ist nur als Parameter für bestimmte Abfragefunktionen gültig (um anzugeben, dass alle funktionalen Objekttypen zulässig sind) und keine vom Treiber gemeldete funktionale Kategorie. |
| [**WPD \_ \_ -Funktions Kategorie \_ - \_ Audioerfassung**](wpd-functional-category-audio-capture.md)                 | Das-Objekt kapselt die audioerfassungs Funktionen auf dem Gerät, z. b. eine Sprachaufzeichnung oder eine andere audioaufzeichnungs Komponente.                                                                      |
| [**WPD \_ - \_ funktionskategoriegerät \_**](wpd-functional-category-device.md)                                | Das-Objekt kapselt das Gerät (d. h. das oberste Objekt des Geräts).                                                                                                                          |
| [**Netzwerkkonfiguration der WPD- \_ Funktions \_ Kategorie \_ \_**](wpd-functional-category-network-configuration.md) | Das-Objekt kapselt Netzwerk Konfigurationsfunktionen für das Gerät ein, z. b. WiFi-Profile oder Partnerschaften.                                                                                   |
| [**Informationen zur \_ Funktions \_ Kategorie \_ der WPD \_**](wpd-functional-category-rendering-information.md) | Das-Objekt beschreibt die Typen von Mediendateien, die vom Gerät wiedergegeben werden können.                                                                                                                            |
| [**WPD- \_ Funktions \_ Kategorie \_ SMS**](wpd-functional-category-sms.md)                                      | Das-Objekt kapselt die Funktion für kurze Nachrichtendienste (in der Regel als "Text Messaging" bezeichnet) auf dem Gerät.                                                                                             |
| [**WPD- \_ Funktions \_ Kategorie \_ trotzdem \_ Image \_ Erfassung**](wpd-functional-category-still-image-capture.md)    | Das-Objekt kapselt weiterhin die Funktionen der Bild Erfassung auf einem Gerät wie z. b. eine Kamera oder eine kameraanlage.                                                                                              |
| [**Speicher für WPD- \_ Funktions \_ Kategorie \_**](wpd-functional-category-storage.md)                              | Das-Objekt kapselt den physischen Dateispeicher auf dem Gerät.                                                                                                                                              |
| [**Video Erfassung der WPD- \_ Funktions \_ Kategorie \_ \_**](wpd-functional-category-video-capture.md)                 | Das-Objekt kapselt die Video Erfassungs Funktionen auf dem Gerät, z. b. eine Video Recorder-Komponente. Eine Anwendung verwendet dieses Objekt, um die programmgesteuerte Steuerung zu erhalten.                                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 



