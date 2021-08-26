---
description: 'Dieses Beispiel veranschaulicht das Layout einer CUB-Datei, die zwei ICEs enthält. Das Installationsprogramm führt die benutzerdefinierten Aktionen in der folgenden Reihenfolge aus: ICE01 und ICE08.'
ms.assetid: 609cd16a-4421-4082-855d-229f5ba7117b
title: CUB-Beispieldatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7aadbaca8bde7091f38d5ce8ccc39926ec6c595aa33e65e488136e89cccfc81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039660"
---
# <a name="sample-cub-file"></a>CUB-Beispieldatei

Dieses Beispiel veranschaulicht das Layout einer CUB-Datei, die zwei [ICEs enthält.](internal-consistency-evaluators-ices.md) Das Installationsprogramm führt die benutzerdefinierten Aktionen in der folgenden Reihenfolge aus: ICE01 und ICE08.

Die benutzerdefinierte Aktion ICE01 ist ein [benutzerdefinierter Aktionstyp 1.](custom-action-type-1.md) Es ist ein Einstiegspunkt für eine DLL, die als Stream in der CUB-Datei gespeichert ist. Dieser Stream wird im Binärtabellen-ice.dll.

Die benutzerdefinierte Aktion ICE08 ist ein [benutzerdefinierter Aktionstyp 6.](custom-action-type-6.md) Es ist ein Einstiegspunkt für eine Funktion in VBScript, die als Stream in der CUB-Datei gespeichert wird. Dieser Stream wird in der Binärtabelle als ice.vbs.

[Binäre Tabelle](binary-table.md)



| Name    | Daten                               |
|---------|------------------------------------|
| ice.vbs | Unformatierte Binärdaten ice.vbs |
| ice.dll | Unformatierte Binärdaten ice.dll |



 

[CustomAction-Tabelle](customaction-table.md)



| Aktion | type | `Source`  | Ziel |
|--------|------|---------|--------|
| ICE01  | 1    | ice.dll | ICE01  |
| ICE08  | 6    | ice.vbs | ICE02  |



 

\_ICESequence-Tabelle



| Aktion | Bedingung | Sequenz |
|--------|-----------|----------|
| ICE01  |           | 10       |
| ICE08  |           | 20       |



 

\_Spezielle Tabelle

ICE01 und ICE08 erfordern nicht die Einbeziehung spezieller Verarbeitungstabellen. Wenn die CUB-Datei spezielle Tabellen enthält, müssen sie auch in der \_ Validierungstabelle enthalten sein.

[\_Validierungstabelle](-validation-table.md)



| Tabelle         | Spalte    | Nullwerte zulässig | Minvalue | MaxValue | KeyTable | KeyColumn | Kategorie                         | Set | BESCHREIBUNG |
|---------------|-----------|----------|----------|----------|----------|-----------|----------------------------------|-----|-------------|
| Binary        | Name      | N        |          |          |          |           | [Identifier](identifier.md)     |     |             |
| Binary        | Daten      | N        |          |          |          |           | [Binär (Binary)](binary.md)             |     |             |
| CustomAction  | Aktion    | N        |          |          |          |           | [Identifier](identifier.md)     |     |             |
| CustomAction  | type      | N        |          |          |          |           | [Integer](integer.md)           |     |             |
| CustomAction  | Quelle    | J        |          |          |          |           | [CustomSource](customsource.md) |     |             |
| CustomAction  | Ziel    | J        |          |          |          |           | [Formatiert](formatted.md)       |     |             |
| \_ICESequence | Aktion    | N        |          |          |          |           | [Identifier](identifier.md)     |     |             |
| \_ICESequence | Bedingung | J        |          |          |          |           | [Condition](condition.md)       |     |             |
| \_ICESequence | Sequenz  | J        |          |          |          |           | [Integer](integer.md)           |     |             |



 

 

 



