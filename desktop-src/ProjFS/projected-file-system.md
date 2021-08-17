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
# <a name="windows-projected-file-system-projfs"></a>Windows Projected File System (ProjFS)

Mit dem Windows Projected File System (ProjFS) kann eine Anwendung im Benutzermodus, die als "Anbieter" bezeichnet wird, hierarchische Daten aus einem sichernden Datenspeicher in das Dateisystem projizieren, wodurch sie als Dateien und Verzeichnisse im Dateisystem angezeigt werden. Beispielsweise könnte ein einfacher Anbieter die Windows-Registrierung in das Dateisystem pro projectieren, wodurch Registrierungsschlüssel und -werte als Dateien bzw. Verzeichnisse angezeigt werden. Ein Beispiel für einen komplexeren Anbieter ist [VFS für Git,](https://github.com/Microsoft/VFSForGit)das zum Virtualisieren sehr großer Git-Repositorys verwendet wird.

> [!NOTE]
> ProjFS ist für die Verwendung mit Datenspeichern mit hoher Geschwindigkeit ausgelegt. Eines der Entwurfsziele ist es, die projizierten Daten so zu gestalten, als ob sie lokal vorhanden sind, und die Tatsache zu verbergen, dass die Daten möglicherweise remote sind. Daher bietet ProjFS keine Mechanismen zum Melden des Fortschritts der Datenrückrufe. Angabe des Online- und Offlinezustands einer Datei; und andere Features, die bei der Arbeit mit langsamen Datenspeichern wünschenswert sein können. In solchen Szenarien sollten Sie stattdessen die [Cloud Files-API verwenden.](../cfapi/cloud-files-api-portal.md)

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema                                                                                                       | Beschreibung |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [Windows Projected File System Programming Guide](projfs-programming-guide.md)                              | Konzeptionelle Informationen zum Implementieren einer ProjFS-Anbieteranwendung.
| [Windows Api-Referenz zu projizierten Dateisystemen](projfs-reference.md)                                          | Referenzinformationen für die ProjFS-Programmierschnittstelle.
| [Windows Glossar des projizierten Dateisystems](projfs-glossary.md)                                                | Spezielle Begriffe, die in ProjFS verwendet werden.

## <a name="additional-resources"></a>Weitere Ressourcen

| Thema                                                                                                             | Beschreibung                                                                                  |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [RegFS-Beispiel](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | Ein ProjFS-Beispielanbieter, der die Windows in das Dateisystem projiz. |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->