---
description: Die Tabelle "moduleausschluss" speichert eine Liste anderer Mergemodule, die in derselben Installerdatenbank nicht kompatibel sind.
ms.assetid: c28d9afa-152c-43b5-9892-7a38fae8c593
title: Moduleausschluss-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8fb4cc136937d5a01bd16a42c138532dd524ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393741"
---
# <a name="moduleexclusion-table"></a>Moduleausschluss-Tabelle

Die Tabelle "moduleausschluss" speichert eine Liste anderer Mergemodule, die in derselben Installerdatenbank nicht kompatibel sind. Diese Tabelle ermöglicht einem Merge-oder Überprüfungs Tool, zu überprüfen, ob in Konflikt stehende Mergemodule nicht in der Installer-Datenbank des Benutzers zusammengeführt werden. Das Tool überprüft, ob diese Tabelle mit der ModuleSignature-Tabelle in der Installer-Datenbank quer referenziert wird.

Die moduleausschluss-Tabelle weist die folgenden Spalten auf.



| Spalte             | Typ                         | Schlüssel | Nullwerte zulässig |
|--------------------|------------------------------|-----|----------|
| ModuleID           | [Bezeichner](identifier.md) | J   | N        |
| Modulelanguage     | [Integer](integer.md)       | J   | N        |
| Excludädid         | [Bezeichner](identifier.md) | J   | N        |
| Excludecodlanguage   | [Integer](integer.md)       | J   | N        |
| Excludedminversion | [Version](version.md)       |     | J        |
| Excludedmaxversion | [Version](version.md)       |     | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID
</dt> <dd>

Der Bezeichner des Mergemoduls. Dabei handelt es sich um einen Fremdschlüssel in der [Tabelle ModuleSignature](modulesignature-table.md).

</dd> <dt>

<span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>Modulelanguage
</dt> <dd>

Die dezimale Sprach-ID des Mergemoduls in ModuleID. Dabei handelt es sich um einen Fremdschlüssel in der [Tabelle ModuleSignature](modulesignature-table.md).

</dd> <dt>

<span id="ExcludedID"></span><span id="excludedid"></span><span id="EXCLUDEDID"></span>Excludädid
</dt> <dd>

Der Bezeichner eines ausgeschlossenen Mergemoduls.

</dd> <dt>

<span id="ExcludedLanguage"></span><span id="excludedlanguage"></span><span id="EXCLUDEDLANGUAGE"></span>Excludecodlanguage
</dt> <dd>

Numerische Sprach-ID des Mergemoduls in excluabdid. In der Spalte excludecodlanguage kann die Sprach-ID für eine einzelne Sprache angegeben werden, z. b. 1033 für US-Englisch, oder die Sprach-ID für eine Sprachgruppe, z. b. 9 für Englisch. Die excludebug Language-Spalte kann negative Sprach-IDs annehmen. Die Bedeutung des Werts in der Spalte excludlanguage lautet wie folgt.



| Excludecodlanguage | Bedeutung                                                              |
|------------------|----------------------------------------------------------------------|
| > 0           | Schließen Sie die Sprach-IDs aus, die von excludlanguage angegeben werden.              |
| = 0              | Schließen Sie keine Sprach-IDs aus.                                             |
| < 0           | Schließen Sie alle Sprach-IDs außer den von excludlanguage angegebenen aus. |



 

</dd> <dt>

<span id="ExcludedMinVersion"></span><span id="excludedminversion"></span><span id="EXCLUDEDMINVERSION"></span>Excludedminversion
</dt> <dd>

Mindestens von einem Bereich ausgeschlossener Version. Wenn das Feld excludedminversion NULL ist, werden alle Versionen vor excludedmaxversion ausgeschlossen. Wenn sowohl excludedminversion als auch excludedmaxversion NULL sind, gibt es keinen Ausschluss, der auf der Version basiert.

</dd> <dt>

<span id="ExcludedMaxVersion"></span><span id="excludedmaxversion"></span><span id="EXCLUDEDMAXVERSION"></span>Excludedmaxversion
</dt> <dd>

Die maximale Version, die von einem Bereich ausgeschlossen wird. Wenn das Feld excludedmaxversion NULL ist, werden alle Versionen nach excludedminversion ausgeschlossen. Wenn sowohl excludedminversion als auch excludedmaxversion NULL sind, gibt es keinen Ausschluss, der auf der Version basiert.

</dd> </dl>

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
</dl>

 

 



