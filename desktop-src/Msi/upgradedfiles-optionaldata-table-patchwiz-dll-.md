---
description: Die Tabelle "upgradedfile \_ OptionalData" enthält Informationen zu bestimmten Dateien in einem aktualisierten Image. Diese Tabelle ist in der Datenbank für die Patcherstellung (PCP-Datei) optional und wird von der uikreatepatchpackageex-Funktion verwendet.
ms.assetid: 8b96a83a-2bfa-47b7-bde0-896bdcc97d29
title: UpgradedFiles_OptionalData Tabelle (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2a648623e2a0cde11af34a3b948b4f2ac6fba59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218202"
---
# <a name="upgradedfiles_optionaldata-table-patchwizdll"></a>Tabelle "upgradedfiles" \_ (OptionalData) (Patchwiz.dll)

Die Tabelle "upgradedfile \_ OptionalData" enthält Informationen zu bestimmten Dateien in einem aktualisierten Image. Diese Tabelle ist in der Datenbank für die Patcherstellung (PCP-Datei) optional und wird von der [uikreatepatchpackageex](uicreatepatchpackageex--patchwiz-dll-.md) -Funktion verwendet.

Die Tabelle "upgradedfile" \_ enthält die folgenden Spalten.



| Spalte                  | Typ    | Schlüssel | Nullwerte zulässig |
|-------------------------|---------|-----|----------|
| Upgraded                | text    | J   | N        |
| FTK                     | text    | J   | N        |
| SymbolPath             | text    |     | J        |
| Zuordnung von "Zuweisung | integer |     | J        |
| Includewholefile        | integer |     | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Aktualisiert
</dt> <dd>

Fremdschlüssel für die aktualisierte Spalte der [Tabelle "UpgradedImages" (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Datei Tabellenschlüssel. Fremdschlüssel in die [Dateitabelle](file-table.md) der MSI-Datei des aktualisierten Abbilds. Wenn mindestens zwei aktualisierte Images innerhalb einer Familie denselben FTK-Wert aufweisen, muss der Wert auf dieselbe Datei verweisen. Dateien, die von mehreren upgradeimages gemeinsam genutzt werden, sollten dieselbe FTK aufweisen, um die Größe der CAB-Datei

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPath
</dt> <dd>

Der Wert in diesem Feld wird der durch Semikolons getrennten Liste der Ordner in der SymbolPath-Spalte der [UpgradedImages-Tabelle (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md) hinzugefügt, wenn der Patch generiert wird, und kann zum Hinzufügen von Symbol Dateien für eine bestimmte Datei verwendet werden.

</dd> <dt>

<span id="AllowIgnoreOnPatchError"></span><span id="allowignoreonpatcherror"></span><span id="ALLOWIGNOREONPATCHERROR"></span>Zuordnung von "Zuweisung
</dt> <dd>

Legen Sie den Wert auf 1 fest, um anzugeben, dass der Patch nicht von Bedeutung ist. Legen Sie auf 0 fest, um anzugeben, dass der Patch wichtig ist. Wenn beim Anwenden dieses Patches auf die in der Spalte FTK angegebene Datei Windows Installer ein Problem auftritt, bestimmt der Wert in diesem Feld, ob das Fehlermeldungs Feld die Schaltfläche **ignorieren** enthält, damit der Benutzer den Patchvorgang fortsetzen kann.

</dd> <dt>

<span id="IncludeWholeFile"></span><span id="includewholefile"></span><span id="INCLUDEWHOLEFILE"></span>Includewholefile
</dt> <dd>

Legen Sie auf einen Wert ungleich 0 (null) fest, wenn die gesamte in der FTK-Spalte angegebene Datei installiert werden soll, anstatt einen binären Patch zu erstellen.

</dd> </dl>

 

 



