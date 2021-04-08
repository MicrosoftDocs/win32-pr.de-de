---
description: Dokument für WPD- \_ \_ Inhaltstyp \_
ms.assetid: c3859590-7674-4315-b171-3747e5d9350b
title: WPD_CONTENT_TYPE_DOCUMENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af8a0a902fb30eb0343a3846eaf3668a4a005a82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050328"
---
# <a name="wpd_content_type_document"></a>Dokument für WPD- \_ \_ Inhaltstyp \_

Ein-Objekt, das den Typ als WPD- \_ Inhaltstyp Dokument beschreibt, das \_ \_ ein Dokument darstellt. Beispiele hierfür sind Microsoft Office Word-Dateien, Microsoft Office Excel-Dateien, nur-Text-Dateien und andere proprietäre Dokumentformate.

Dieser Objekttyp kann die folgenden Eigenschaften hosten.



| Eigenschaftsname                                                                                                         | Erforderlich oder optional                                                           |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [WPD- \_ Objekt- \_ ID](object-properties.md)                                                                | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zum Zeitpunkt der Erstellung nicht festlegen. |
| [übergeordnete WPD- \_ Objekt- \_ \_ ID](object-properties.md)                                                 | Erforderlich.                                                                      |
| [WPD- \_ Objekt \_ Name](object-properties.md)                                                            | Erforderlich, wenn das-Objekt eine Datei darstellt.                                      |
| [\_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt](object-properties.md)                          | Erforderlich, schreibgeschützt. Ein Client kann diese Eigenschaft auch zum Zeitpunkt der Erstellung nicht festlegen. |
| [WPD- \_ Objekt \_ Format](object-properties.md)                                                        | Erforderlich.                                                                      |
| [Inhaltstyp für WPD- \_ Objekt \_ \_](object-properties.md)                                           | Erforderlich.                                                                      |
| [WPD- \_ Objekt \_ IsHidden](object-properties.md)                                                    | Erforderlich, wenn das Objekt ausgeblendet ist.                                              |
| [WPD- \_ Objekt \_ IsSystem](object-properties.md)                                                    | Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).          |
| [WPD- \_ Objekt \_ Größe](object-properties.md)                                                            | Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.                              |
| [\_ \_ ursprünglicher \_ Dateiname \_ des WPD-Objekts](object-properties.md)                              | Erforderlich, wenn das-Objekt eine Datei darstellt.                                      |
| [WPD- \_ Objekt \_ nicht \_ verwendbar](object-properties.md)                                       | Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist.          |
| [Verweise auf WPD- \_ Objekte \_](object-properties.md)                                                | Erforderlich, wenn das-Objekt über Verweise auf andere-Objekte verfügt.                        |
| [WPD- \_ Objekt \_ Schlüsselwörter](object-properties.md)                                                    | Dies ist optional.                                                                      |
| [WPD- \_ Objekt \_ Synchronisierungs- \_ ID](object-properties.md)                                                     | Dies ist optional.                                                                      |
| [WPD- \_ Objekt \_ ist DRM- \_ \_ geschützt](object-properties.md)                                  | Erforderlich, wenn das Objekt durch DRM-Technologie geschützt wird.                         |
| [\_ \_ Erstellungsdatum des WPD-Objekts \_](object-properties.md)                                           | Dies ist optional.                                                                      |
| [Datum des WPD- \_ Objekts \_ \_ geändert](object-properties.md)                                         | Empfohlen.                                                                   |
| [erstelltes WPD- \_ Objekt \_ Datum \_](object-properties.md)                                         | Dies ist optional.                                                                      |
| [\_ \_ zurück \_ Verweise auf WPD-Objekte](object-properties.md)                                                                | Empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.                     |
| [\_ \_ \_ Funktions \_ Objekt- \_ ID des WPD-Objekt Containers](object-properties.md)     | Dies ist optional.                                                                      |
| [WPD \_ - \_ Objekt \_ generieren \_ der Miniaturansicht aus der \_ Ressource](object-properties.md) | Dies ist optional.                                                                      |
| [WPD- \_ Objekt \_ kann \_ Löschen](object-properties.md)                                                                     | Erforderlich, wenn das Objekt nicht gelöscht werden kann.                                      |
| [Gebiets Schema der WPD- \_ Objekt \_ Sprache \_](object-properties.md)                                                                | Dies ist optional.                                                                      |
| [WPD- \_ Medien \_ Quellen- \_ URL](object-properties.md)                                                                      | Dies ist optional.                                                                      |
| [Ziel-URL für WPD- \_ Medien \_ \_](object-properties.md)                                                                 | Dies ist optional.                                                                      |
| [WPD- \_ Medien \_ Beschreibung](object-properties.md)                                                                      | Dies ist optional.                                                                      |
| [WPD- \_ Medien \_ Genre](object-properties.md)                                                                            | Dies ist optional.                                                                      |
| [WPD- \_ Medien \_ Byte- \_ Lesezeichen](object-properties.md)                                                                   | Dies ist optional.                                                                      |
| [WPD- \_ Medien- \_ GUID](object-properties.md)                                                                             | Dies ist optional.                                                                      |
| [\_ \_ unter \_ Beschreibung der WPD-Medien](object-properties.md)                                                                 | Dies ist optional.                                                                      |
| [\_Allgemeine Informationen zu WPD \_](object-properties.md)                                                                     | Empfohlen.                                                                   |
| [Text für den allgemeinen WPD- \_ \_ Informations \_ \_ Text](object-properties.md)                                                         | Empfohlen.                                                                   |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte enthalten in der Regel die folgenden Ressourcen.



| Ressourcenname                                          | Erforderlich oder optional | BESCHREIBUNG                     |
|--------------------------------------------------------|----------------------|---------------------------------|
| [**WPD- \_ Ressourcen \_ Standard**](wpd-resource-default.md) | Erforderlich             | Enthält das physische Dokument. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 



