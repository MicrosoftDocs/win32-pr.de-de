---
description: Die ModuleSignature-Tabelle ist eine erforderliche Tabelle.
ms.assetid: 09802282-72ad-43f1-8cce-4cdc68b01e87
title: ModuleSignature-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92f269215fef06af5eeacc80f1356c2ad2226c20075c1d09f1e128c062438508
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945338"
---
# <a name="modulesignature-table"></a>ModuleSignature-Tabelle

Die ModuleSignature-Tabelle ist eine erforderliche Tabelle. Es enthält alle Informationen, die zum Identifizieren eines Mergemoduls erforderlich sind. Das Mergetool fügt diese Tabelle der .msi hinzu, sofern noch keine vorhanden ist. Die ModuleSignature-Tabelle in einem Mergemodul enthält nur eine Zeile mit moduleID, Language und Version. Die ModuleSignature-Tabelle in einer .msi-Datei enthält jedoch eine Zeile, die diese Informationen für jede MSM-Datei enthält, die mit ihr zusammengeführt wurde.

Merge- und Überprüfungstools überprüfen die Tabelle ModuleSignature in .msi-Dateien, um festzustellen, ob sie über alle abhängigen Mergemodule verfügt, die für das aktuelle Mergemodul erforderlich sind (siehe [ModuleDependency Table](moduledependency-table.md)) und ob das Installationspaket zuvor mit in Konflikt stehenden Mergemodulen zusammengeführt wurde (siehe [ModuleExclusion Table](moduleexclusion-table.md)).

Die Tabelle ModuleSignature enthält die folgenden Spalten.



| Spalte   | Typ                         | Key | Nullwerte zulässig |
|----------|------------------------------|-----|----------|
| ModuleID | [Identifier](identifier.md) | J   | N        |
| Sprache | [Integer](integer.md)       | J   | N        |
| Version  | [Version](version.md)       |     | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>Moduleid
</dt> <dd>

Ein Bezeichner, der das Mergemodul eindeutig identifiziert. Zwei Mergemodule können nur dann dieselbe ModuleID haben, wenn das Mergemodul vollständig abwärtskompatibel mit seinem Vorgänger ist. Sie können eine GUID für dieses Feld mithilfe eines Hilfsprogramms wie GUIDGEN erstellen. Die Spalte ModuleID ist ein Primärschlüssel für die Tabelle und muss daher der Namenskonvention unter Naming Primary Keys in Merge Module Databases (Benennen von Primärschlüsseln [in Mergemoduldatenbanken) folgen.](naming-primary-keys-in-merge-module-databases.md) Wenn der lesbare Name des Mergemoduls beispielsweise MyLibrary und die GUID {880DE2F0-CDD8-11D1-A849-006097ABDE17} lautet, wird der Eintrag in der Spalte ModuleID zu MyLibrary.880DE2F0 \_ CDD8 \_ 11D1 \_ A849 \_ 006097ABDE17.

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Sprache
</dt> <dd>

Der Sprachbezeichner gibt die Standardsprache für das Mergemodul an. Der Sprachbezeichner hat das Dezimalformat, z. B. "US-Englisch" ist 1033. Die vom Mergemodul verwendete Sprache kann geändert werden, indem vor dem Zusammenführen eine Transformation auf das Mergemodul angewendet wird.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>Version
</dt> <dd>

Das Feld Version enthält eine Zeichenfolge, die die Haupt- und Nebenversionen des Mergemoduls beschreibt.

</dd> </dl>

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mehrere Sprachzusammenführungsmodule](multiple-language-merge-modules.md)
</dt> </dl>

 

 



