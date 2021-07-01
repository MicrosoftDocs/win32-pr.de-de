---
title: Programmierhandbuch für projizierte Dateisysteme
description: Konzeptionelle Informationen zum Implementieren einer ProjFS-Anbieteranwendung.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 86c6f49eaf9da578226031eaf84abff7ebb059c0
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120565"
---
# <a name="projected-file-system-projfs-programming-guide"></a>ProjFS-Programmierhandbuch (Projected File System)

Das Windows Projected File System (ProjFS) ermöglicht einer Anwendung im Benutzermodus, die als "Anbieter" bezeichnet wird, hierarchische Daten in das Dateisystem zu projizieren, sodass sie als Dateien und Verzeichnisse im Dateisystem angezeigt werden.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema                                                                                                       | Beschreibung |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [Anbieterübersicht](provider-overview.md)                                                                   | Konzeptionelle Übersicht über eine Anbieteranwendung.
| [Cachestatus im Virtualisierungsstamm](cache-state.md)                                                    | Beschreibt die verschiedenen Cachezustände, die eine vom Anbieter verwaltete Datei oder ein Verzeichnis aufweisen kann. 
| [Aktivieren des windows-projizierten Dateisystems](enabling-windows-projected-file-system.md)                         | Beschreibt, wie die optionale ProjFS-Komponente aktiviert wird.
| [Virtualisierungsinstanzlebenszyklus](virtualization-instance-lifecycle.md)                                   | Übersicht über den Lebenszyklus einer ProjFS-Virtualisierungsinstanz.
| [Auflisten von Dateien und Verzeichnissen](enumerating-files-and-directories.md)                                   | Beschreibt, wie ein ProjFS-Anbieter an der Verzeichnisenumeration teilnimmt.
| [Bereitstellen von Dateidaten](providing-file-data.md)                                                               | Beschreibt, wie ein Anbieter Platzhalterinformationen und Dateidaten liefert.
| [Dateisystem-Vorgangsbenachrichtigungen](file-system-operation-notifications.md)                               | Beschreibt, wie ein Anbieter Benachrichtigungen über Dateisystemvorgänge empfangen kann.
| [Behandeln von Ansichtsänderungen](handling-view-changes.md)                                                           | Beschreibt, wie die Clientansicht des Sicherungsspeichers eines Anbieters aktualisiert wird.
| [Asynchrone Rückrufbehandlung](asynchronous-callback-handling.md)                                         | Beschreibt, wie der Anbieter Rückrufe asynchron bedienen kann.
| [Windows Projected File System API Reference](/windows/desktop/api/_projfs) | Referenzinformationen für die ProjFS-Programmierschnittstelle.

## <a name="additional-resources"></a>Weitere Ressourcen

| Thema                                                                                                             | Beschreibung                                                                                  |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [RegFS-Beispiel](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | Ein ProjFS-Beispielanbieter, der die Windows-Registrierung in das Dateisystem projiziert. |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->