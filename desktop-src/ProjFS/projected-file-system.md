---
title: Windows-projiziertes Datei System
description: Übersicht über das projizierte Windows-Datei System (projfs)
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/14/2018
ms.topic: article
ms.openlocfilehash: 8391ec63f23c9ebae5b47e4cac862f6ab3079ceb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858295"
---
# <a name="windows-projected-file-system-projfs"></a>Windows-projiziertes Datei System (projfs)

Das von Windows projizierte Dateisystem (projfs) ermöglicht es einer Benutzermodusanwendung, die als "Anbieter" bezeichnet wird, um hierarchische Daten aus einem Sicherungsdaten Speicher in das Dateisystem zu projizieren, sodass Sie als Dateien und Verzeichnisse im Dateisystem angezeigt werden. Ein einfacher Anbieter könnte z. b. die Windows-Registrierung in das Dateisystem projizieren, sodass Registrierungsschlüssel und-Werte als Dateien bzw. Verzeichnisse angezeigt werden. Ein Beispiel für einen komplexeren Anbieter sind [VFS für git](https://github.com/Microsoft/VFSForGit), das verwendet wird, um sehr große git-Repos zu virtualisieren.

> [!NOTE]
> Projfs ist für die Verwendung mit hoch Geschwindigkeits Unterstützungs Daten speichern konzipiert. Eines der Entwurfs Ziele besteht darin, dass die projizierten Daten so angezeigt werden, als ob Sie lokal vorhanden wären, und die Tatsache ausblenden, dass die Daten Remote sein können. Projfs bietet daher keine Mechanismen zum Melden des Status des Daten Rückrufs. Angabe des Online-oder Offline Status einer Datei; ebenso wie andere Features, die bei der Arbeit mit langsamen unterstützenden Daten speichern wünschenswert sein könnten. In solchen Szenarien sollten Sie stattdessen die [Cloud Files-API](../cfapi/cloud-files-api-portal.md)verwenden.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema                                                                                                       | BESCHREIBUNG |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [Programmier Handbuch für die Programmierung von Windows projiziert](projfs-programming-guide.md)                              | Konzeptionelle Informationen zum Implementieren einer Anwendung für den projfs-Anbieter.
| [API-Referenz zu den Windows-projizierten Dateien](projfs-reference.md)                                          | Referenzinformationen für die projfs-Programmierschnittstelle.
| [Windows projiziertes Datei System Glossar](projfs-glossary.md)                                                | Besondere Begriffe, die in projfs verwendet werden.

## <a name="additional-resources"></a>Weitere Ressourcen

|                                                                                                              |                                                                                   |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Regfs-Beispiel](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | Einen projfs-Beispiel Anbieter, der die Windows-Registrierung in das Dateisystem projiziert. |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->