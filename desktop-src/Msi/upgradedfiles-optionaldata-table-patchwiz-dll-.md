---
description: Die Tabelle UpgradedFile \_ OptionalData enthält Informationen zu bestimmten Dateien in einem aktualisierten Image. Diese Tabelle ist in der Patcherstellungsdatenbank (PCP-Datei) optional und wird von der UiCreatePatchPackageEx-Funktion verwendet.
ms.assetid: 8b96a83a-2bfa-47b7-bde0-896bdcc97d29
title: UpgradedFiles_OptionalData Tabelle (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08eb766f8db9d295546670c80627284991da1ff8dccb5a0c2900be74bd785dab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012838"
---
# <a name="upgradedfiles_optionaldata-table-patchwizdll"></a>UpgradedFiles \_ OptionalData Table (Patchwiz.dll)

Die Tabelle UpgradedFile \_ OptionalData enthält Informationen zu bestimmten Dateien in einem aktualisierten Image. Diese Tabelle ist in der Patcherstellungsdatenbank (PCP-Datei) optional und wird von der [UiCreatePatchPackageEx-Funktion](uicreatepatchpackageex--patchwiz-dll-.md) verwendet.

Die Tabelle UpgradedFile \_ OptionalData weist die folgenden Spalten auf.



| Spalte                  | Typ    | Key | Nullwerte zulässig |
|-------------------------|---------|-----|----------|
| Upgraded                | text    | J   | N        |
| FTK                     | text    | J   | N        |
| SymbolPaths             | text    |     | J        |
| AllowIgnoreOnPatchError | integer |     | J        |
| IncludeWholeFile        | integer |     | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Aktualisiert
</dt> <dd>

Fremdschlüssel für die Spalte "Upgraded" der [Tabelle "UpgradedImages" (Patchwiz.dll).](upgradedimages-table-patchwiz-dll-.md)

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Dateitabellenschlüssel. Fremdschlüssel in die [Dateitabelle](file-table.md) der .msi Datei des aktualisierten Images. Wenn zwei oder mehr aktualisierte Images innerhalb einer Familie den gleichen FTK-Wert aufweisen, muss der Wert auf dieselbe Datei verweisen. Dateien, die von mehreren Upgradeimages gemeinsam genutzt werden, sollten den gleichen FTK aufweisen, um die Größe der Cab-Datei zu minimieren.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

Der Wert in diesem Feld wird der durch Semikolons getrennten Liste von Ordnern in der SymbolPaths-Spalte der [Tabelle UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md) hinzugefügt, wenn der Patch generiert wird, und kann verwendet werden, um Symboldateien für eine bestimmte Datei hinzuzufügen.

</dd> <dt>

<span id="AllowIgnoreOnPatchError"></span><span id="allowignoreonpatcherror"></span><span id="ALLOWIGNOREONPATCHERROR"></span>AllowIgnoreOnPatchError
</dt> <dd>

Legen Sie diese Einstellung auf 1 fest, um anzugeben, dass der Patch nicht wichtig ist. Legen Sie auf 0 fest, um anzugeben, dass der Patch wichtig ist. Wenn Windows Installer beim Anwenden dieses Patches auf die in der FTK-Spalte angegebene Datei auf ein Problem stößt, bestimmt der Wert in diesem Feld, ob das Fehlermeldungsfeld eine Schaltfläche **Ignorieren** enthält, damit der Benutzer den Patchvorgang fortsetzen kann.

</dd> <dt>

<span id="IncludeWholeFile"></span><span id="includewholefile"></span><span id="INCLUDEWHOLEFILE"></span>IncludeWholeFile
</dt> <dd>

Legen Sie auf einen Wert ungleich 0 (null) fest, wenn die gesamte in der FTK-Spalte angegebene Datei installiert werden soll, anstatt einen binären Patch zu erstellen.

</dd> </dl>

 

 



