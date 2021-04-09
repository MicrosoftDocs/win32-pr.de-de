---
description: 'Dieses Beispiel veranschaulicht das Layout einer CUB-Datei, die zwei ICES enthält. Der Installer führt die benutzerdefinierten Aktionen in der folgenden Reihenfolge aus: ICE01 und ICE08.'
ms.assetid: 609cd16a-4421-4082-855d-229f5ba7117b
title: Sample. CUB-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e937b779e2a620ffc17cf936e37f74867f3dfdd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958885"
---
# <a name="sample-cub-file"></a>Sample. CUB-Datei

Dieses Beispiel veranschaulicht das Layout einer CUB-Datei, die zwei [ICES](internal-consistency-evaluators-ices.md)enthält. Der Installer führt die benutzerdefinierten Aktionen in der folgenden Reihenfolge aus: ICE01 und ICE08.

Die benutzerdefinierte Aktion ICE01 ist ein [benutzerdefinierter Aktionstyp 1](custom-action-type-1.md). Es handelt sich um einen Einstiegspunkt für eine DLL, die als Stream in der CUB-Datei gespeichert ist. Dieser Stream wird in der ice.dll der binären Tabelle aufgeführt.

Die benutzerdefinierte Aktion ICE08 ist ein [benutzerdefinierter Aktionstyp 6](custom-action-type-6.md). Es handelt sich um einen Einstiegspunkt für eine Funktion in VBScript, die als Stream in der CUB-Datei gespeichert wird. Dieser Stream wird in der Binär Tabelle als ice.vbs aufgeführt.

[Binäre Tabelle](binary-table.md)



| Name    | Daten                               |
|---------|------------------------------------|
| ice.vbs | Nicht formatierte Binärdaten von ice.vbs |
| ice.dll | Nicht formatierte Binärdaten von ice.dll |



 

[Tabelle "CustomAction"](customaction-table.md)



| Aktion | type | `Source`  | Ziel |
|--------|------|---------|--------|
| ICE01  | 1    | ice.dll | ICE01  |
| ICE08  | 6    | ice.vbs | ICE02  |



 

\_Icesequence-Tabelle



| Aktion | Bedingung | Sequenz |
|--------|-----------|----------|
| ICE01  |           | 10       |
| ICE08  |           | 20       |



 

\_Spezielle Tabelle

ICE01 und ICE08 erfordern nicht die Einbindung spezieller Verarbeitungs Tabellen. Wenn die CUB-Datei spezielle Tabellen enthält, müssen Sie auch in der \_ Validierungs Tabelle enthalten sein.

[\_Validierungs Tabelle](-validation-table.md)



| Tabelle         | Spalte    | Nullwerte zulässig | MinValue | MaxValue | KeyTable | KeyColumn | Category                         | Set | BESCHREIBUNG |
|---------------|-----------|----------|----------|----------|----------|-----------|----------------------------------|-----|-------------|
| Binary        | Name      | N        |          |          |          |           | [Bezeichner](identifier.md)     |     |             |
| Binary        | Daten      | N        |          |          |          |           | [Binär (Binary)](binary.md)             |     |             |
| CustomAction  | Aktion    | N        |          |          |          |           | [Bezeichner](identifier.md)     |     |             |
| CustomAction  | type      | N        |          |          |          |           | [Integer](integer.md)           |     |             |
| CustomAction  | `Source`    | J        |          |          |          |           | [CustomSource](customsource.md) |     |             |
| CustomAction  | Ziel    | J        |          |          |          |           | [Großformatige](formatted.md)       |     |             |
| \_Icesequence | Aktion    | N        |          |          |          |           | [Bezeichner](identifier.md)     |     |             |
| \_Icesequence | Bedingung | J        |          |          |          |           | [Condition](condition.md)       |     |             |
| \_Icesequence | Sequenz  | J        |          |          |          |           | [Integer](integer.md)           |     |             |



 

 

 



