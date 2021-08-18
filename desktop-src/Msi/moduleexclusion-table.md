---
description: Die Tabelle ModuleExclusion enthält eine Liste mit anderen Mergemodulen, die in derselben Installer-Datenbank nicht kompatibel sind.
ms.assetid: c28d9afa-152c-43b5-9892-7a38fae8c593
title: Tabelle "ModuleExclusion"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 008d10e65d81b5668821e1a999cf08f5a10c55db3372a4b0230d560462a977c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996440"
---
# <a name="moduleexclusion-table"></a>Tabelle "ModuleExclusion"

Die Tabelle ModuleExclusion enthält eine Liste mit anderen Mergemodulen, die in derselben Installer-Datenbank nicht kompatibel sind. Diese Tabelle ermöglicht es einem Merge- oder Überprüfungstool, zu überprüfen, ob in Konflikt stehende Mergemodule nicht in der Installer-Datenbank des Benutzers zusammengeführt werden. Das Tool überprüft, indem es auf diese Tabelle mit der Tabelle ModuleSignature in der Installer-Datenbank verweist.

Die Tabelle ModuleExclusion enthält die folgenden Spalten.



| Spalte             | Typ                         | Key | Nullwerte zulässig |
|--------------------|------------------------------|-----|----------|
| ModuleID           | [Identifier](identifier.md) | J   | N        |
| ModuleLanguage     | [Integer](integer.md)       | J   | N        |
| ExcludedID         | [Identifier](identifier.md) | J   | N        |
| ExcludedLanguage   | [Integer](integer.md)       | J   | N        |
| ExcludedMinVersion | [Version](version.md)       |     | J        |
| ExcludedMaxVersion | [Version](version.md)       |     | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>Moduleid
</dt> <dd>

Bezeichner des Mergemoduls. Dies ist ein Fremdschlüssel in der [Tabelle ModuleSignature.](modulesignature-table.md)

</dd> <dt>

<span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage
</dt> <dd>

Id der Dezimalsprache des Mergemoduls in ModuleID. Dies ist ein Fremdschlüssel in der [Tabelle ModuleSignature.](modulesignature-table.md)

</dd> <dt>

<span id="ExcludedID"></span><span id="excludedid"></span><span id="EXCLUDEDID"></span>ExcludedID
</dt> <dd>

Bezeichner eines ausgeschlossenen Mergemoduls.

</dd> <dt>

<span id="ExcludedLanguage"></span><span id="excludedlanguage"></span><span id="EXCLUDEDLANGUAGE"></span>ExcludedLanguage
</dt> <dd>

Numerische Sprach-ID des Mergemoduls in ExcludedID. Die Spalte ExcludedLanguage kann die Sprach-ID für eine einzelne Sprache angeben, z.B. 1033 für Englisch in den USA oder die Sprach-ID für eine Sprachgruppe, z. B. 9 für englisch. Die Spalte ExcludedLanguage kann negative Sprach-IDs akzeptieren. Die Bedeutung des Werts in der ExcludedLanguage -Spalte lautet wie folgt.



| ExcludedLanguage | Bedeutung                                                              |
|------------------|----------------------------------------------------------------------|
| > 0           | Schließen Sie die von ExcludedLanguage angegebenen Sprach-IDs aus.              |
| = 0              | Schließen Sie keine Sprach-IDs aus.                                             |
| < 0           | Schließen Sie alle Sprach-IDs mit Ausnahme der von ExcludedLanguage angegebenen aus. |



 

</dd> <dt>

<span id="ExcludedMinVersion"></span><span id="excludedminversion"></span><span id="EXCLUDEDMINVERSION"></span>ExcludedMinVersion
</dt> <dd>

Aus einem Bereich ausgeschlossene Mindestversion. Wenn das Feld ExcludedMinVersion NULL ist, werden alle Versionen vor ExcludedMaxVersion ausgeschlossen. Wenn excludedMinVersion und ExcludedMaxVersion null sind, gibt es keinen Ausschluss basierend auf der Version.

</dd> <dt>

<span id="ExcludedMaxVersion"></span><span id="excludedmaxversion"></span><span id="EXCLUDEDMAXVERSION"></span>ExcludedMaxVersion
</dt> <dd>

Maximale Version, die aus einem Bereich ausgeschlossen ist. Wenn das Feld ExcludedMaxVersion NULL ist, werden alle Versionen nach ExcludedMinVersion ausgeschlossen. Wenn excludedMinVersion und ExcludedMaxVersion null sind, gibt es keinen Ausschluss basierend auf der Version.

</dd> </dl>

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
</dl>

 

 



