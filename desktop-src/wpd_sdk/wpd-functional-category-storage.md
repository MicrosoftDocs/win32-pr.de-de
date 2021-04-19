---
description: Speicher für WPD- \_ Funktions \_ Kategorie \_
ms.assetid: 92a10de6-3e50-4042-a9b7-3c1d5944791f
title: WPD_FUNCTIONAL_CATEGORY_STORAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f3000c63207286bc1dae153e3f930231909e92f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359471"
---
# <a name="wpd_functional_category_storage"></a>Speicher für WPD- \_ Funktions \_ Kategorie \_

Ein Funktions Objekt der WPD- \_ Funktions \_ Kategorie \_ Speicher kapselt den physischen Dateispeicher auf dem Gerät.



| Eigenschaftsname                                                                                                         | Erforderlich oder optional                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [WPD- \_ Objekt- \_ ID](object-properties.md)                                                                | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zum Zeitpunkt der Erstellung nicht festlegen.                                                                         |
| [übergeordnete WPD- \_ Objekt- \_ \_ ID](object-properties.md)                                                 | Erforderlich.                                                                                                                                              |
| [WPD- \_ Objekt \_ Name](object-properties.md)                                                            | Erforderlich.                                                                                                                                              |
| [\_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt](object-properties.md)                          | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zum Zeitpunkt der Erstellung nicht festlegen.                                                                         |
| [WPD- \_ Objekt \_ Format](object-properties.md)                                                        | Erforderlich.                                                                                                                                              |
| [Inhaltstyp für WPD- \_ Objekt \_ \_](object-properties.md)                                           | Erforderlich.                                                                                                                                              |
| [WPD- \_ Objekt \_ IsHidden](object-properties.md)                                                    | Erforderlich, wenn das Objekt ausgeblendet ist.                                                                                                                      |
| [WPD- \_ Objekt \_ IsSystem](object-properties.md)                                                    | Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).                                                                                  |
| [WPD- \_ Objekt \_ Größe](object-properties.md)                                                            | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                                                                                                      |
| [\_ \_ ursprünglicher \_ Dateiname \_ des WPD-Objekts](object-properties.md)                              | Erforderlich, wenn das-Objekt eine Datei darstellt.                                                                                                              |
| [WPD- \_ Objekt \_ nicht \_ verwendbar](object-properties.md)                                       | Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist.                                                                                  |
| [Verweise auf WPD- \_ Objekte \_](object-properties.md)                                                | Erforderlich, wenn das-Objekt über Verweise auf andere-Objekte verfügt.                                                                                                |
| [WPD- \_ Objekt \_ Schlüsselwörter](object-properties.md)                                                    | Dies ist optional.                                                                                                                                              |
| [WPD- \_ Objekt \_ Synchronisierungs- \_ ID](object-properties.md)                                                     | Dies ist optional.                                                                                                                                              |
| [WPD- \_ Objekt \_ ist DRM- \_ \_ geschützt](object-properties.md)                                  | Erforderlich, wenn das Objekt durch DRM-Technologie geschützt wird.                                                                                                 |
| [\_ \_ Erstellungsdatum des WPD-Objekts \_](object-properties.md)                                           | Dies ist optional.                                                                                                                                              |
| [Datum des WPD- \_ Objekts \_ \_ geändert](object-properties.md)                                         | Empfohlen.                                                                                                                                           |
| [erstelltes WPD- \_ Objekt \_ Datum \_](object-properties.md)                                         | Dies ist optional.                                                                                                                                              |
| [\_ \_ zurück \_ Verweise auf WPD-Objekte](object-properties.md)                                                                | Empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.                                                                                             |
| [\_ \_ \_ Funktions \_ Objekt- \_ ID des WPD-Objekt Containers](object-properties.md)     | Dies ist optional.                                                                                                                                              |
| [WPD \_ - \_ Objekt \_ generieren \_ der Miniaturansicht aus der \_ Ressource](object-properties.md) | Dies ist optional.                                                                                                                                              |
| [WPD- \_ Objekt \_ kann \_ Löschen](object-properties.md)                                                                     | Erforderlich, wenn das Objekt nicht gelöscht werden kann.                                                                                                              |
| [Gebiets Schema der WPD- \_ Objekt \_ Sprache \_](object-properties.md)                                                                | Dies ist optional.                                                                                                                                              |
| [WPD- \_ Funktions \_ Objekt \_ Kategorie](miscellaneous-properties.md)                      | Erforderlich. Weitere [**Informationen zu \_ Kategorien \_ \_ \_**](wpd-content-type-functional-object.md) , die von tragbaren Windows-Geräten definiert werden |
| [WPD \_ - \_ Speichertyp](storage-properties.md)                                                         | Erforderlich.                                                                                                                                              |
| [WPD \_ - \_ Speicher \_ Datei \_ Systemtyp](storage-properties.md)                               | Dies ist optional.                                                                                                                                              |
| [WPD- \_ Speicher \_ Kapazität](storage-properties.md)                                                 | Erforderlich.                                                                                                                                              |
| [\_freier Speicherplatz auf WPD-Speicher \_ \_ \_ in \_ Bytes](storage-properties.md)                        | Dies ist optional.                                                                                                                                              |
| [\_freier Speicherplatz in WPD-Speicher \_ \_ \_ in \_ Objekten](storage-properties.md)                    | Dies ist optional.                                                                                                                                              |
| [WPD- \_ Speicher \_ Beschreibung](storage-properties.md)                                           | Dies ist optional.                                                                                                                                              |
| [WPD- \_ Speicher \_ Serien \_ Nummer](storage-properties.md)                                      | Dies ist optional.                                                                                                                                              |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte enthalten in der Regel die folgenden Ressourcen.



| Ressourcenname                                    | Erforderlich oder optional | BESCHREIBUNG                                        |
|--------------------------------------------------|----------------------|----------------------------------------------------|
| [**Symbol für WPD- \_ Ressource \_**](wpd-resource-icon.md) | Dies ist optional.            | Enthält die Symboldarstellung für diesen Speicher. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Funktions Objekt des WPD- \_ \_ Inhaltstyp \_ \_**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



