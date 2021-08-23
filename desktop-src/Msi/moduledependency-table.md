---
description: Die Tabelle ModuleDependency enthält eine Liste anderer Mergemodule, die für den ordnungsgemäßen Betrieb dieses Mergemoduls erforderlich sind.
ms.assetid: 36418331-bec7-40c9-8fdf-fe4b958a1443
title: ModuleDependency-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08d527ba5874c8fffb0234dbf8f041f424b7bf9aecff5e8f29005324f2a17fdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628583"
---
# <a name="moduledependency-table"></a>ModuleDependency-Tabelle

Die Tabelle ModuleDependency enthält eine Liste anderer Mergemodule, die für den ordnungsgemäßen Betrieb dieses Mergemoduls erforderlich sind. Diese Tabelle ermöglicht es einem Merge- oder Überprüfungstool, sicherzustellen, dass die erforderlichen Mergemodule tatsächlich in der Installer-Datenbank des Benutzers enthalten sind. Das Tool überprüft, indem es auf diese Tabelle mit der ModuleSignature-Tabelle in der Installer-Datenbank querge verweisen kann.

Die Tabelle ModuleDependency enthält die folgenden Spalten.



| Spalte           | Typ                         | Key | Nullwerte zulässig |
|------------------|------------------------------|-----|----------|
| ModuleID         | [Identifier](identifier.md) | J   | N        |
| ModuleLanguage   | [Integer](integer.md)       | J   | N        |
| RequiredID       | [Identifier](identifier.md) | J   | N        |
| RequiredLanguage | [Integer](integer.md)       | J   | N        |
| RequiredVersion  | [Version](version.md)       |     | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>Moduleid
</dt> <dd>

Bezeichner des Mergemoduls. Dies ist ein Fremdschlüssel in der [ModuleSignature-Tabelle.](modulesignature-table.md)

</dd> <dt>

<span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage
</dt> <dd>

Id der Dezimalsprache des Mergemoduls in ModuleID. Dies ist ein Fremdschlüssel in der [ModuleSignature-Tabelle.](modulesignature-table.md)

</dd> <dt>

<span id="RequiredID"></span><span id="requiredid"></span><span id="REQUIREDID"></span>RequiredID
</dt> <dd>

Bezeichner des Mergemoduls, das für das Mergemodul in ModuleID erforderlich ist.

</dd> <dt>

<span id="RequiredLanguage"></span><span id="requiredlanguage"></span><span id="REQUIREDLANGUAGE"></span>RequiredLanguage
</dt> <dd>

Numerische Sprach-ID des Mergemoduls in RequiredID. Die Spalte RequiredLanguage kann die Sprach-ID für eine einzelne Sprache angeben, z. B. 1033 für ENGLISCH (USA), oder die Sprach-ID für eine Sprachgruppe angeben, z. B. 9 für englisch. Wenn das Feld eine Gruppensprach-ID enthält, erfüllt jedes Mergemodul mit einem Sprachcode in dieser Gruppe die Abhängigkeit. Wenn RequiredLanguage auf 0 festgelegt ist, erfüllt jedes Mergemodul, das die anderen Anforderungen erfüllt, die Abhängigkeit.

</dd> <dt>

<span id="RequiredVersion"></span><span id="requiredversion"></span><span id="REQUIREDVERSION"></span>RequiredVersion
</dt> <dd>

Version des Mergemoduls in RequiredID. Wenn dieses Feld NULL ist, füllt jede Version die Abhängigkeit aus.

</dd> </dl>

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
</dl>

 

 



