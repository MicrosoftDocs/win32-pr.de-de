---
description: Beschreibt die Einführung von Bibliotheken für Windows 7.
ms.assetid: 83c47963-4c8e-45ee-b707-bd45cfe048cd
title: Windows Shellbibliotheken in Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28f120f1bc4e4208a7e6bbf35bbcfc4717ed05dfb7344658a80b1ea1d9a3ba50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969599"
---
# <a name="windows-shell-libraries-in-windows"></a>Windows Shellbibliotheken in Windows

In diesem Thema wird die Einführung von Bibliotheken für Windows 7 und höher beschrieben. Bibliotheken sind ein Windows Shell-Feature. Um auf Windows Shell-Funktionalität wie Bibliotheken zugreifen zu können, müssen Drittanbieter von Windows Search-Anwendungen zunächst einen Shell-Datenspeicher implementieren. Weitere Informationen finden Sie unter [Implementieren der grundlegenden Ordnerobjektschnittstellen.](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85))

Dieses Thema ist wie folgt organisiert:

- [Libraries](#libraries)
  - [Einstiegspunkte für Benutzerdaten](#user-data-entry-points)
  - [Ordnersammlungen](#collections-of-folders)
  - [Unterstützte Ordner in Bibliotheken](#supported-folders-in-libraries)
  - [Storage gesichert](#storage-backed)
  - [Nicht-Dateisystem-Shellcontainer](#non-file-system-shell-containers)
  - [Bibliotheksbeschreibungen](#library-descriptions)
- [Zugehörige Themen](#related-topics)

## <a name="libraries"></a>Bibliotheken

In Windows 7 und höher sind Bibliotheken das Standard-Repository für Benutzerdaten. Benutzer können ihre Dateien auf die gleiche Weise durchsuchen wie in einem Ordner, oder sie können ihre Dateien anzeigen, die nach Eigenschaften wie Datum, Typ und Autor angeordnet sind. Im Gegensatz zu einem Ordner speichert eine Bibliothek keine Elemente, sondern zeigt Dateien an, die gleichzeitig in mehreren Ordnern gespeichert sind. Bibliotheken stellen einen einzelnen Zugriffspunkt und umfassende Ansichtspivoten für Benutzer ihrer aggregierten Inhalte bereit. Wenn ein Benutzer beispielsweise zusätzlich zum Ordner **My Musik** Musikdateien in Ordnern auf einem externen Laufwerk enthält, kann er sofort über die Musik-Bibliothek auf alle Musikdateien zugreifen.

### <a name="user-data-entry-points"></a>Einstiegspunkte für Benutzerdaten

Standardbibliotheken (z. **B. Eigene Dokumente**, **Meine Bilder** usw.) entsprechen [known Folder](/previous-versions/windows/desktop/legacy/bb776911(v=vs.85)). Standardbibliotheken bieten Benutzern vertraute Einstiegspunkte, aber da Bibliotheksinhalte nicht auf Inhaltsbibliotheken für bekannte Ordner beschränkt sind, haben Benutzer mehr Möglichkeiten, zu bestimmen, wo Dokumente und Medien gespeichert werden sollen. Bibliotheken werden über den Shellnamespace (Shelldatenquelle) verfügbar gemacht. Ihre Anwendung kann Benutzern die gleichen vertrauten Einstiegspunkte für ihre Daten bereitstellen, indem sie Bibliotheksinformationen aktiviert und browset.

### <a name="collections-of-folders"></a>Ordnersammlungen

Bibliotheken sind benutzerdefinierte Inhaltssammlungen. Windows Durchsucht indizes unterstützte Ordner, wenn sie in Bibliotheken enthalten sind. Dies ermöglicht die sofortige Suche und eigenschaftenbasierte Stapelanordnungsansichten in Bibliotheken.

### <a name="supported-folders-in-libraries"></a>Unterstützte Ordner in Bibliotheken

Damit Ordner in Bibliotheken unterstützt werden können, müssen sie auf dem lokalen Computer indizierbar und entweder auf einem Remotecomputer Windows Computers oder auf einem Server mit Dateien indiziert sein, die von Windows Search indiziert werden.

Das Hinzufügen nicht unterstützter Ordner durch Benutzer im Dialogfeld Windows Bibliotheksverwaltung wird blockiert. Wenn nicht indizierte Remoteordner mithilfe der [IShellLibrary-API](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) zu einer Bibliothek hinzugefügt werden, wird die Bibliotheksbenutzeroberfläche **Tresor Modus** zurückgesetzt. In **Tresor Modus** werden Features wie eigenschaftenbasierte Stapelanordnungsansichten, Filtervorschläge und Die Unterstützung der **Startmenüsuche** aus der betroffenen Bibliothek entfernt.

In der folgenden Tabelle werden ordner aufgelistet, die in Bibliotheken mithilfe des Dialogfelds Windows-Explorer-Bibliotheksverwaltung enthalten sind, sowie Ordner, die im **Tresor-Modus** nicht unterstützt werden:

| Unterstützte Ordner                                                                                                                            | Nicht unterstützte Ordner                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| Feste und externe NTFS- und FAT32-Festplatten                                                                                                | Wechseldatenträger (z. B. Thumbdrives und SD-Karten)                                                     |
| Freigaben, die von Windows Search indiziert werden (z. B. Abteilungsserver und auf Computern, auf denen Windows 10 und Windows 7 Home Edition ausgeführt werden) | Wechselmedien (z. B. CDs und DVDs)                                                                  |
| Offline verfügbare Freigaben (z. **B. umgeleitete Eigene Dokumente,** **clientseitiger Cache)**                                               | Netzwerkfreigaben, die weder offline noch remote indiziert (z. B. NAS-Laufwerke) verfügbar sind             |
| –                                                                                                                                          | Andere Datenquellen (z. B. Microsoft SharePoint, Microsoft Exchange, Microsoft OneDrive usw.) |

### <a name="storage-backed"></a>Storage-Backed

Bibliotheken sind Sammlungen von Speicherordnern. Benutzer können Dateien direkt in eine Bibliothek speichern und kopieren, da jede Bibliothek über einen Standardspeicherort verfügt, an den diese Dateien gesendet werden. Bei Standardbibliotheken ist dies der benutzerverwendete ordner, der in einer Bibliothek enthalten ist (z. **B. Eigene Dokumente**), oder der erste Ordner, der einer benutzerdefinierten Bibliothek hinzugefügt wurde. Dies ist der Ordner, in den Dateien verschoben werden, wenn ein Benutzer Dateien per Drag & Drop in eine Bibliothek zieht oder mit dem allgemeinen Dateidialogfeld in einer Bibliothek speichert. Der Benutzer kann den Standardspeicherort einer Bibliothek jederzeit ändern. Wenn er jedoch den Standardspeicherort entfernt, wird der nächste Ordner in der Bibliothek als neuer Speicherort ausgewählt. Benutzer können darüber hinaus in jedem Ordner speichern, für den sie über Berechtigungen verfügen, die in einer Bibliothek enthalten sind.

### <a name="non-file-system-shell-containers"></a>Nicht-Dateisystem-Shellcontainer

Bibliotheken können Shellcontainer im Dateisystem wie **Computer** und **Systemsteuerung** enthalten, aber Dateisystemelemente enthalten. Bibliotheksordner und -inhalte können mithilfe von APIs für Dateisystemdateien und Ordner in früheren Betriebssystemen aufzählt und darauf zugegriffen werden. Wenn Ihre Anwendung stark von dateisystemspezifischen APIs abhängig ist, kann die [IShellLibrary-API](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) verwendet werden, um die Dateisystempfade von Ordnern und Dateien in Bibliotheken abzurufen. In den meisten Fällen wird empfohlen, das Shell-Programmiermodell zu verwenden, um mehrere Windows Versionen und Elementflexibilität zu unterstützen. Weitere Informationen finden Sie unter [Navigieren im Shellnamespace.](https://msdn.microsoft.com/library/dd378496(VS.85).aspx)

### <a name="library-descriptions"></a>Bibliotheksbeschreibungen

Bibliotheksbeschreibungen werden auf dem Datenträger als XML-Datei im Ordner %appdata%Microsoft \\ Windows \\ Libraries (und möglicherweise als **\_ FOLDERID-Bibliotheken)** gespeichert. Weitere Informationen zu **\_ FOLDERID-Bibliotheken** finden Sie unter [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid).

Bibliotheksbeschreibungsdateien sind XML-Dateien mit der Dateinamenerweiterung .library-ms. Auf diese Dateien sollte nie von Anwendungen zugegriffen oder sie bearbeitet werden. Der in den Bibliotheksbeschreibungsdateien beibehaltene Ordnerpfadtext ist nicht immer aktuell. Bibliotheksordner werden in der Bibliotheksbeschreibungsdatei im serialisierten binären [Shelllinkformat](/windows/desktop/shell/links) beibehalten. Weitere Informationen zu Bibliotheken und zum Bibliotheksbeschreibungsschema finden Sie unter [Bibliotheksbeschreibungsschema.](../shell/library-schema-entry.md) Weitere Informationen zu Verbundsuchconnectors und zum Search Connector Description-Schema finden Sie unter [Search Connector Description Schema](search-sconn-desc-schema-entry.md).

> [HINWEIS]  
> Anwendungen sollten immer das Shell-Programmiermodell oder die [IShellLibrary-API](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) verwenden, um Bibliotheksinhalte zu nutzen und zu bearbeiten, und nie versuchen, manuell auf die Bibliotheksbeschreibungsdatei zuzugreifen oder sie zu bearbeiten.

## <a name="related-topics"></a>Zugehörige Themen

[suche nach Windows 7](./-search-3x-wds-overview.md)

[Neu für Windows 7-Suche](new-for-windows-7-search.md)

[Indizieren von Priorisierungs- und Rowsetereignissen in Windows 7](indexing-prioritization-and-rowset-events.md)