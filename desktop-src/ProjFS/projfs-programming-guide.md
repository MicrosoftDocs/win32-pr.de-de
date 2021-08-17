---
title: Projected File System Programming Guide
description: Konzeptionelle Informationen zum Implementieren einer ProjFS-Anbieteranwendung.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: d935c99b73e11a2110e739a4e45fdde0f7a24300a2664a2b25d6217bd2235fa9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792543"
---
# <a name="projected-file-system-projfs-programming-guide"></a>Programmierhandbuch für projected File System (ProjFS)

Mit Windows Projected File System (ProjFS) kann eine Anwendung im Benutzermodus, die als "Anbieter" bezeichnet wird, hierarchische Daten in das Dateisystem projizieren, wodurch sie als Dateien und Verzeichnisse im Dateisystem angezeigt werden.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema                                                                                                       | Beschreibung |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [Anbieterübersicht](provider-overview.md)                                                                   | Konzeptionelle Übersicht über eine Anbieteranwendung.
| [Cachezustand im Virtualisierungsstamm](cache-state.md)                                                    | Beschreibt die verschiedenen Cachezustände einer Datei oder eines Verzeichnisses, die bzw. das vom Anbieter verwaltet wird. 
| [Aktivieren Windows projizierten Dateisystems](enabling-windows-projected-file-system.md)                         | Beschreibt, wie die optionale ProjFS-Komponente aktiviert wird.
| [Lebenszyklus von Virtualisierungsinstanzen](virtualization-instance-lifecycle.md)                                   | Übersicht über den Lebenszyklus einer ProjFS-Virtualisierungsinstanz.
| [Auflisten von Dateien und Verzeichnissen](enumerating-files-and-directories.md)                                   | Beschreibt, wie ein ProjFS-Anbieter an der Verzeichnisenumeration beteiligt ist.
| [Bereitstellen von Dateidaten](providing-file-data.md)                                                               | Beschreibt, wie ein Anbieter Platzhalterinformationen und Dateidaten liefert.
| [Dateisystem-Vorgangsbenachrichtigungen](file-system-operation-notifications.md)                               | Beschreibt, wie ein Anbieter Benachrichtigungen über Dateisystemvorgänge empfangen kann.
| [Behandeln von Ansichtsänderungen](handling-view-changes.md)                                                           | Beschreibt, wie die Clientansicht des Hintergrundspeichers eines Anbieters aktualisiert wird.
| [Asynchrone Rückrufbehandlung](asynchronous-callback-handling.md)                                         | Beschreibt, wie der Anbieter Rückrufe asynchron nutzen kann.
| [Windows Api-Referenz zu projizierten Dateisystemen](/windows/desktop/api/_projfs) | Referenzinformationen für die ProjFS-Programmierschnittstelle.

## <a name="additional-resources"></a>Weitere Ressourcen

| Thema                                                                                                             | Beschreibung                                                                                  |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [RegFS-Beispiel](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | Ein ProjFS-Beispielanbieter, der die Windows in das Dateisystem projiz. |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->