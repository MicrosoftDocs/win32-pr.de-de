---
title: Windows Projiziertes Dateisystem
description: Übersicht über das Windows Projected File System (ProjFS)
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/14/2018
ms.topic: article
ms.openlocfilehash: d5cb20b123e72ec8e031036019a16ef1bbe2b8dc4b9bb53446c8faaced4d796b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792657"
---
# <a name="windows-projected-file-system-projfs"></a>Windows Projiziertes Dateisystem (ProjFS)

Das Windows Projected File System (ProjFS) ermöglicht einer Anwendung im Benutzermodus, die als "Anbieter" bezeichnet wird, hierarchische Daten aus einem sicherungsbasierten Datenspeicher in das Dateisystem zu projizieren, sodass sie als Dateien und Verzeichnisse im Dateisystem angezeigt werden. Beispielsweise könnte ein einfacher Anbieter die Windows Registrierung in das Dateisystem pro projektieren, sodass Registrierungsschlüssel und -werte als Dateien bzw. Verzeichnisse angezeigt werden. Ein Beispiel für einen komplexeren Anbieter ist [VFS für Git,](https://github.com/Microsoft/VFSForGit)das zum Virtualisieren sehr großer Git-Repositorys verwendet wird.

> [!NOTE]
> ProjFS ist für die Verwendung mit Datenspeichern mit hoher Geschwindigkeit konzipiert. Eines der Entwurfsziele besteht darin, dass die projizierten Daten so aussehen, als wären sie lokal vorhanden, wodurch die Tatsache ausgeblendet wird, dass es sich bei den Daten möglicherweise um Remotedaten handelt. Daher bietet ProjFS keine Mechanismen zum Melden des Fortschritts des Datenrückrufs. Angabe des Online- und Offlinezustands einer Datei oder andere Features, die bei der Arbeit mit langsamen Sicherungsdatenspeichern wünschenswert sein können. In solchen Szenarien sollten Sie stattdessen die [Clouddateien-API](../cfapi/cloud-files-api-portal.md)verwenden.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema                                                                                                       | BESCHREIBUNG |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [Windows Programmierhandbuch für projizierte Dateisysteme](projfs-programming-guide.md)                              | Konzeptionelle Informationen zum Implementieren einer ProjFS-Anbieteranwendung.
| [Windows Api-Referenz für projizierte Dateisysteme](projfs-reference.md)                                          | Referenzinformationen für die ProjFS-Programmierschnittstelle.
| [Windows Projected File System glossary (Glossar des projizierten Dateisystems)](projfs-glossary.md)                                                | Spezielle Begriffe, die in ProjFS verwendet werden.

## <a name="additional-resources"></a>Weitere Ressourcen

| Thema                                                                                                             | BESCHREIBUNG                                                                                  |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [RegFS-Beispiel](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | Ein ProjFS-Beispielanbieter, der die Windows Registrierung in das Dateisystem projiziert. |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->