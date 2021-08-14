---
description: Das Registrieren eines Dateityps ist der erste Schritt beim Erstellen einer Dateiassoz, wodurch dieser Dateityp &\# 0034;&\# 0034; zur Shell wird. Ohne Dateityphandler kann die Shell dem Benutzer jedoch keine Informationen aus und über die Datei verfügbar machen.
ms.assetid: c0c5c3ef-35ff-4ab6-bb8a-1f0640109d50
title: Dateityphandler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 404cfd3be4c3e8a600b2f943bda1243ca243b70af411e104000245edd13d94c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459725"
---
# <a name="file-type-handlers"></a>Dateityphandler

[Das Registrieren eines Dateityps](fa-how-work.md) ist der erste Schritt beim Erstellen einer Dateiassoz, die diesen Dateityp der Shell "bekannt" macht. Ohne Dateityphandler kann die Shell dem Benutzer jedoch keine Informationen aus und über die Datei verfügbar machen.

Dieses Thema ist wie folgt organisiert:

-   [Shell einen Dateityp bekannt machen](#make-a-file-type-known-to-shell)
-   [Beschreibungen des Dateityphandlers](#file-type-handler-descriptions)
-   [Zugehörige Themen](#related-topics)

## <a name="make-a-file-type-known-to-shell"></a>Shell einen Dateityp bekannt machen

Im folgenden Screenshot des Windows-Explorers wird die Bilddatei "Dateityp.known" in der **Shellbildbibliothek** angezeigt und nur der Paint zugeordnet.

![Screenshot, der zeigt, wie der Explorer ein Bild ohne Dateityp öffnet](images/file-assoc/fileassoc-filetypehandler.png)

In der Datei "Soll.known&quot; im vorherigen Screenshot fehlt die folgende Funktionalität, die von einem Dateityphandler aktiviert wird:

-   Miniaturansicht oder Vorschau
-   Bildspezifische Verben im Kontextmenü, z. B.:
    -   Vorschau rotieren
    -   Als Desktophintergrund festlegen
    -   Drucken
-   Bildspezifische Eigenschaften im **Detailbereich,** z. B.:
    -   Datum der Erstellung
    -   `Tags`
    -   Rating
-   Indizierung von Dateitext

Im folgenden Screenshot hat dieselbe Datei (Datei &quot;Bekannter") die Erweiterung .jpg. Dabei handelt es sich um einen registrierten Dateityp, dem Dateityphandler zugeordnet sind, sodass ein Miniaturbild und weitere Eigenschaften angezeigt werden.

![Image mit einem registrierten Dateityp und zugeordneten Dateityphandlern](images/file-assoc/fileassoc-filetypehandler-2ndex.png)

## <a name="file-type-handler-descriptions"></a>Beschreibungen des Dateityphandlers

Die von den einzelnen Dateityphandlern bereitgestellten Funktionen sind in der folgenden Tabelle aufgeführt:



| Handler                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Kontextmenü](context-menu-handlers.md)                   | Ein Kontextmenühandler, der manchmal auch als Kontextmenühandler bezeichnet wird, ist ein Dateityphandler, der einem vorhandenen Kontextmenü Befehle hinzufügt. Diese Handler sind einem bestimmten Dateityp zugeordnet und werden jedes Mal aufgerufen, wenn ein Kontextmenü für einen Member des Dateityps angezeigt wird.                                                                                                                                                                                                                                                                           |
| [Miniaturansicht](thumbnail-providers.md)                         | Ein Handler, der ein Bild zur Darstellung eines Shellelements bietet.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Eigenschaft](../properties/building-property-handlers-properties.md) | Ein Eigenschaftenhandler, der Zugriff auf Elementeigenschaften für Windows Search, den Windows-Explorer und andere Anwendungen bietet, die auf Eigenschaften zugreifen müssen.                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Vorschau](preview-handlers.md)                              | Ein Handler, der schnell eine schreibgeschützte, vereinfachte Ansicht des Elements erzeugt, das im Vorschaubereich Windows Explorer angezeigt werden soll.                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [Filter](../search/-search-3x-wds-extidx-filters.md)              | Ein Filter, eine Implementierung der [**IFilter-Schnittstelle,**](/windows/win32/api/filter/nn-filter-ifilter) der Dokumente nach Text und Eigenschaften (auch als Attribute bezeichnet) durchsucht. Es extrahiert Textbrocken aus diesen Dokumenten, filtert eingebettete Formatierungen heraus und behält Informationen zur Position des Texts bei. Außerdem werden Werteteile extrahiert, bei denen es sich um Eigenschaften eines gesamten Dokuments oder klar definierter Teile eines Dokuments handelt. **IFilter** bildet die Grundlage für die Entwicklung von Anwendungen auf höherer Ebene, z. B. Dokumentindexer und anwendungsunabhängige Viewer. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungsregistrierung](app-registration.md)
</dt> <dt>

[Dateitypen](fa-file-types.md)
</dt> <dt>

[Funktionsweise von Dateizuordnungen](fa-how-work.md)
</dt> <dt>

[Inhaltsansicht nach Dateityp oder Art](prophand-content-view.md)
</dt> <dt>

[Dateitypverifizierer](file-type-verifier.md)
</dt> <dt>

[Programmgesteuerte Bezeichner](fa-progids.md)
</dt> <dt>

[Wahrgenommene Typen](fa-perceivedtypes.md)
</dt> <dt>

[Zuordnungsarrays](fa-associationarray.md)
</dt> </dl>

 

 
