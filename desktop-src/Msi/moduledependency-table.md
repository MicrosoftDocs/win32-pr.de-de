---
description: Die moduledepen-Tabelle speichert eine Liste anderer Mergemodule, die erforderlich sind, damit dieses Mergemodul ordnungsgemäß funktioniert.
ms.assetid: 36418331-bec7-40c9-8fdf-fe4b958a1443
title: Moduledepenptabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb0c550f8c5ae480a07ca10401d1d3b67c496ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368832"
---
# <a name="moduledependency-table"></a>Moduledepenptabelle

Die moduledepen-Tabelle speichert eine Liste anderer Mergemodule, die erforderlich sind, damit dieses Mergemodul ordnungsgemäß funktioniert. Diese Tabelle ermöglicht einem Merge-oder Überprüfungs Tool, sicherzustellen, dass die erforderlichen Mergemodule tatsächlich in der Installer-Datenbank des Benutzers enthalten sind. Das Tool überprüft, ob Querverweise auf diese Tabelle mit der ModuleSignature-Tabelle in der Installer-Datenbank durchgeführt werden.

Die moduledepenptabelle weist die folgenden Spalten auf.



| Spalte           | Typ                         | Schlüssel | Nullwerte zulässig |
|------------------|------------------------------|-----|----------|
| ModuleID         | [Bezeichner](identifier.md) | J   | N        |
| Modulelanguage   | [Integer](integer.md)       | J   | N        |
| Requirements did       | [Bezeichner](identifier.md) | J   | N        |
| Requirements-Sprache | [Integer](integer.md)       | J   | N        |
| RequiredVersion  | [Version](version.md)       |     | J        |



 

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

<span id="RequiredID"></span><span id="requiredid"></span><span id="REQUIREDID"></span>Requirements did
</dt> <dd>

Der Bezeichner des Mergemoduls, das vom Mergemodul in ModuleID benötigt wird.

</dd> <dt>

<span id="RequiredLanguage"></span><span id="requiredlanguage"></span><span id="REQUIREDLANGUAGE"></span>Requirements-Sprache
</dt> <dd>

Numerische Sprach-ID des Mergemoduls in Requirements did. In der Spalte "Requirements-language" können Sie die Sprach-ID für eine einzelne Sprache angeben, z. b. 1033 für US-Englisch, oder Sie können die Sprach-ID für eine Sprachgruppe angeben, z. b. 9 für Englisch. Wenn das Feld eine Gruppen Sprachen-ID enthält, erfüllt jedes Mergemodul mit einem Sprachcode in dieser Gruppe die Abhängigkeit. Wenn für "Requirements" der Wert "0" festgelegt ist, erfüllt jedes Mergemodul, das die anderen Anforderungen erfüllt, die Abhängigkeit.

</dd> <dt>

<span id="RequiredVersion"></span><span id="requiredversion"></span><span id="REQUIREDVERSION"></span>RequiredVersion
</dt> <dd>

Version des Mergemoduls in Requirements did. Wenn dieses Feld NULL ist, füllt jede Version die Abhängigkeit aus.

</dd> </dl>

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
</dl>

 

 



