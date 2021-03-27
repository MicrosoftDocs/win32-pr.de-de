---
description: Das Registrieren eines Dateityps ist der erste Schritt beim Erstellen einer Datei Zuordnung, bei der der Dateityp \# 0034&&\# . Ohne Dateityp Handler kann die Shell dem Benutzer jedoch keine Informationen aus der Datei und der Datei verfügbar machen.
ms.assetid: c0c5c3ef-35ff-4ab6-bb8a-1f0640109d50
title: Dateityp Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cba365b6eb704def7644002b8a87c3842b62aa77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862367"
---
# <a name="file-type-handlers"></a>Dateityp Handler

Das [Registrieren eines Dateityps](fa-how-work.md) ist der erste Schritt beim Erstellen einer Datei Zuordnung, die den Dateityp "bekannt" für die Shell macht. Ohne Dateityp Handler kann die Shell dem Benutzer jedoch keine Informationen aus der Datei und der Datei verfügbar machen.

Dieses Thema ist wie folgt organisiert:

-   [Erstellen eines Dateityps, der Shell bekannt ist](#make-a-file-type-known-to-shell)
-   [Dateityp Handler-Beschreibungen](#file-type-handler-descriptions)
-   [Zugehörige Themen](#related-topics)

## <a name="make-a-file-type-known-to-shell"></a>Erstellen eines Dateityps, der Shell bekannt ist

Im folgenden Screenshot von Windows-Explorer wird die Bilddatei "Desert. Known" in der **shellbilder** -Bibliothek angezeigt und nur mit der Paint-Anwendung verknüpft.

![Screenshot, der zeigt, wie der Explorer ein Bild ohne Dateityp öffnet](images/file-assoc/fileassoc-filetypehandler.png)

In der Datei "Desert. Known" im vorherigen Screenshot fehlen die folgenden Funktionen, die von einem Dateityp Handler aktiviert werden:

-   Miniaturansicht oder Vorschau
-   Bild spezifische Verben im Kontextmenü, z. b.:
    -   Vorschau drehen
    -   Als Desktop Hintergrund festlegen
    -   Drucken
-   Bild spezifische Eigenschaften im **Detail** Bereich, z. b.:
    -   Datum der Erstellung
    -   `Tags`
    -   Rating
-   Indizierung von Datei Text

Im folgenden Screenshot weist die gleiche Datei (Wüsten. Known) die Erweiterung. jpg auf, bei der es sich um einen registrierten Dateityp mit zugeordneten Dateityp Handlern handelt, sodass ein Miniaturbild und weitere Eigenschaften angezeigt werden.

![Bild mit einem registrierten Dateityp und zugeordneten Dateityp Handlern](images/file-assoc/fileassoc-filetypehandler-2ndex.png)

## <a name="file-type-handler-descriptions"></a>Dateityp Handler-Beschreibungen

Die Funktionen, die von jedem Dateityp Handler bereitgestellt werden, sind in der folgenden Tabelle aufgeführt:



| Handler                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Kontextmenü](context-menu-handlers.md)                   | Ein Kontextmenü Handler, der manchmal auch als Kontextmenü Handler bezeichnet wird, ist ein Dateityp Handler, der einem vorhandenen Kontextmenü Befehle hinzufügt. Diese Handler sind einem bestimmten Dateityp zugeordnet und werden jedes Mal aufgerufen, wenn ein Kontextmenü für einen Member des Dateityps angezeigt wird.                                                                                                                                                                                                                                                                           |
| [Miniaturansicht](thumbnail-providers.md)                         | Ein Handler, der ein Bild bereitstellt, das ein shellelement darstellen soll.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Eigenschaft](../properties/building-property-handlers-properties.md) | Ein Eigenschaften Handler, der den Zugriff auf Element Eigenschaften für Windows Search, den Windows-Explorer und andere Anwendungen ermöglicht, die auf Eigenschaften zugreifen müssen.                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Vorschau](preview-handlers.md)                              | Ein Handler, der schnell eine schreibgeschützte, vereinfachte Ansicht des Elements erstellt, das im Vorschaubereich von Windows-Explorer angezeigt werden soll.                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [Filter](../search/-search-3x-wds-extidx-filters.md)              | Ein Filter, eine Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle, die Dokumente für Text und Eigenschaften (auch als Attribute bezeichnet) scannt. Es extrahiert Textabschnitte aus diesen Dokumenten, filtert eingebettete Formatierungen heraus und behält Informationen über die Position des Texts bei. Außerdem werden Werte Blöcke extrahiert, bei denen es sich um Eigenschaften eines gesamten Dokuments oder um klar definierte Teile eines Dokuments handelt. **IFilter** ist die Grundlage für das Entwickeln von Anwendungen höherer Ebene, z. b. dokumentindexer und Anwendungs unabhängige Viewer. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungs Registrierung](app-registration.md)
</dt> <dt>

[Dateitypen](fa-file-types.md)
</dt> <dt>

[Funktionsweise von Dateizuordnungen](fa-how-work.md)
</dt> <dt>

[Inhaltsansicht nach Dateityp oder-Art](prophand-content-view.md)
</dt> <dt>

[Dateityp Überprüfung](file-type-verifier.md)
</dt> <dt>

[Programmgesteuerte Bezeichner](fa-progids.md)
</dt> <dt>

[Wahrgenommene Typen](fa-perceivedtypes.md)
</dt> <dt>

[Zuordnungs Arrays](fa-associationarray.md)
</dt> </dl>

 

 
