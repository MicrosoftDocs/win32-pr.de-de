---
title: Windows Projected File System
description: Übersicht über das Windows Projected File System (ProjFS)
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/14/2018
ms.topic: article
ms.openlocfilehash: 68f121162efdf75fb9226b41f9b3a1121bef6480
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120585"
---
# <a name="windows-projected-file-system-projfs"></a>Windows Projected File System (ProjFS)

Das Windows Projected File System (ProjFS) ermöglicht einer Anwendung im Benutzermodus, die als "Anbieter" bezeichnet wird, hierarchische Daten aus einem sicherungsbasierten Datenspeicher in das Dateisystem zu projizieren, sodass sie als Dateien und Verzeichnisse im Dateisystem angezeigt werden. Beispielsweise könnte ein einfacher Anbieter die Windows-Registrierung in das Dateisystem pro projektieren, sodass Registrierungsschlüssel und -werte als Dateien bzw. Verzeichnisse angezeigt werden. Ein Beispiel für einen komplexeren Anbieter ist [VFS für Git,](https://github.com/Microsoft/VFSForGit)das zum Virtualisieren sehr großer Git-Repositorys verwendet wird.

> [!NOTE]
> ProjFS ist für die Verwendung mit Datenspeichern mit hoher Geschwindigkeit konzipiert. Eines der Entwurfsziele besteht darin, dass die projizierten Daten so aussehen, als wären sie lokal vorhanden, wodurch die Tatsache ausgeblendet wird, dass es sich bei den Daten möglicherweise um Remotedaten handelt. Daher bietet ProjFS keine Mechanismen zum Melden des Fortschritts des Datenrückrufs. Angabe des Online- und Offlinezustands einer Datei oder andere Features, die bei der Arbeit mit langsamen Sicherungsdatenspeichern wünschenswert sein können. In solchen Szenarien sollten Sie stattdessen die [Clouddateien-API](../cfapi/cloud-files-api-portal.md)verwenden.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema                                                                                                       | Beschreibung |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [Programmierhandbuch für windows-projizierte Dateisysteme](projfs-programming-guide.md)                              | Konzeptionelle Informationen zum Implementieren einer ProjFS-Anbieteranwendung.
| [Windows Projected File System API Reference](projfs-reference.md)                                          | Referenzinformationen für die ProjFS-Programmierschnittstelle.
| [Windows Projected File System Glossary](projfs-glossary.md)                                                | Spezielle Begriffe, die in ProjFS verwendet werden.

## <a name="additional-resources"></a>Weitere Ressourcen

| Thema                                                                                                             | Beschreibung                                                                                  |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [RegFS-Beispiel](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | Ein ProjFS-Beispielanbieter, der die Windows-Registrierung in das Dateisystem projiziert. |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->