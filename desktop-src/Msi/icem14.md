---
description: ICEM14 überprüft die Value-Spalte der ModuleSubstitution-Tabelle.
ms.assetid: e07ba63a-e748-4835-ae1b-9f7d30e46d39
title: ICEM14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72223f27338fb08efe4ea95b817acebd6234063f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130448"
---
# <a name="icem14"></a>ICEM14

ICEM14 überprüft die Value-Spalte der [ModuleSubstitution-Tabelle](modulesubstitution-table.md).

## <a name="result"></a>Ergebnis

ICEM14 gibt die folgenden Fehler aus.



| Fehler                                                                                                                                                         | Bedeutung                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Die Ersetzungs Zeichenfolge in der ModuleSubstitution. Value-Spalte in Zeile \[ 1 \] . \[ 2 \] . \[ 3 wurde \] in der Tabelle "ModuleConfiguration" nicht gefunden.                                 | \[1 \] . \[ 2 \] . \[ 3 \] bezieht sich auf einen *Table. Row. Column* -Primärschlüssel für eine Zeile in der ModuleSubstitution-Tabelle. Die Formatierungs Vorlage im Wertfeld dieser Zeile entspricht nicht einer Zeile mit konfigurierbaren Attributen in der [ModuleConfiguration-Tabelle](moduleconfiguration-table.md).                                                            |
| In der Tabelle ModuleSubstitution in Zeile \[ 1 \] . \[ 2 \] . \[ 3 \] , in der Tabelle "% s" ist ein konfigurierbares Element angegeben. Die '% s '-Tabelle darf keine konfigurierbaren Elemente enthalten. | Eine der folgenden Tabellen ist in der Tabellenspalte der Tabelle ModuleSubstitution aufgeführt: [ModuleSubstitution](modulesubstitution-table.md), [ModuleConfiguration](moduleconfiguration-table.md), [moduleausschluss](moduleexclusion-table.md)oder [ModuleSignature](modulesignature-table.md). Diese Tabellen können keine konfigurierbaren Felder enthalten. |
| In der Tabelle ModuleSubstitution in Zeile \[ 1 \] . \[ 2 \] . \[ 3 \] , eine leere Ersetzungs Zeichenfolge wird angegeben.                                                               | Die Formatierungs Vorlage im Wertfeld dieser Zeile entspricht nicht einer Zeile mit konfigurierbaren Attributen in der [ModuleConfiguration-Tabelle](moduleconfiguration-table.md).                                                                                                                                                                    |



 

ICEM14 gibt die folgende Warnung aus.



| Warnung                                                                  | Bedeutung                                  |
|--------------------------------------------------------------------------|------------------------------------------|
| Die ModuleSubstitution-Tabelle ist vorhanden, aber die ModuleConfiguration-Tabelle fehlt. | Die ModuleConfiguration-Tabelle ist nicht vorhanden. |



 

## <a name="table-used-during-execution"></a>Während der Ausführung verwendete Tabelle

[ModuleSubstitution-Tabelle](modulesubstitution-table.md)

[ModuleConfiguration-Tabelle](moduleconfiguration-table.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eisverweis für Mergemodul](merge-module-ice-reference.md)
</dt> </dl>

 

 



