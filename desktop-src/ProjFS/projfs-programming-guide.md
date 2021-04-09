---
title: Programmier Handbuch für das projizierte Datei System
description: Konzeptionelle Informationen zum Implementieren einer Anwendung für den projfs-Anbieter.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: a6b2d186ac3e674c3fa68e17ecd523b2c94f2401
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039307"
---
# <a name="projected-file-system-projfs-programming-guide"></a>Programmier Handbuch für das projizierte Datei System (projfs)

Das geplante Dateisystem von Windows (projfs) ermöglicht es einer Benutzermodusanwendung, die als "Anbieter" bezeichnet wird, um hierarchische Daten in das Dateisystem zu projizieren, sodass Sie als Dateien und Verzeichnisse im Dateisystem angezeigt werden.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema                                                                                                       | BESCHREIBUNG |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [Übersicht über den Anbieter](provider-overview.md)                                                                   | Konzeptionelle Übersicht über eine Anbieter Anwendung.
| [Cache Status im virtualisierungsstamm](cache-state.md)                                                    | Beschreibt die verschiedenen Cache Zustände, die eine vom Anbieter verwaltete Datei oder ein Verzeichnis aufweisen kann. 
| [Aktivieren des in Windows projizierten Dateisystems](enabling-windows-projected-file-system.md)                         | Beschreibt das Aktivieren der optionalen projfs-Komponente.
| [Lebenszyklus der virtualisierungsinstanz](virtualization-instance-lifecycle.md)                                   | Übersicht über den Lebenszyklus einer projfs-virtualisierungsinstanz.
| [Auflisten von Dateien und Verzeichnissen](enumerating-files-and-directories.md)                                   | Beschreibt, wie ein projfs-Anbieter an der verzeichnisenumeration teilnimmt.
| [Bereitstellen von Dateidaten](providing-file-data.md)                                                               | Beschreibt, wie ein Anbieter Platzhalter Informationen und Datei Daten bereitstellt.
| [Datei System-Vorgangs Benachrichtigungen](file-system-operation-notifications.md)                               | Beschreibt, wie ein Anbieter Benachrichtigungen von Dateisystem Vorgängen empfangen kann.
| [Behandeln von Änderungen der Ansicht](handling-view-changes.md)                                                           | Beschreibt, wie die Client Ansicht des Sicherungs Speicher eines Anbieters aktualisiert wird.
| [Asynchrone Rückruf Behandlung](asynchronous-callback-handling.md)                                         | Beschreibt, wie der Anbieter asynchron Dienst Rückrufe bedienen kann.
| [API-Referenz zu den Windows-projizierten Dateien](/windows/desktop/api/_projfs) | Referenzinformationen für die projfs-Programmierschnittstelle.

## <a name="additional-resources"></a>Weitere Ressourcen

|                                                                                                              |                                                                                   |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Regfs-Beispiel](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | Einen projfs-Beispiel Anbieter, der die Windows-Registrierung in das Dateisystem projiziert. |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->