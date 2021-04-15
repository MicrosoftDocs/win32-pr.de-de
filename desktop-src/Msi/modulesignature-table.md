---
description: Die ModuleSignature-Tabelle ist eine erforderliche Tabelle.
ms.assetid: 09802282-72ad-43f1-8cce-4cdc68b01e87
title: ModuleSignature-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d75e3bb013472c49d18fa44b840ce07b11728faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529243"
---
# <a name="modulesignature-table"></a>ModuleSignature-Tabelle

Die ModuleSignature-Tabelle ist eine erforderliche Tabelle. Sie enthält alle Informationen, die zum Identifizieren eines Mergemoduls erforderlich sind. Das Mergetool fügt diese Tabelle der MSI-Datei hinzu, sofern noch keine vorhanden ist. Die ModuleSignature-Tabelle in einem Mergemodul weist nur eine Zeile auf, die die ModuleID, die Sprache und die Version enthält. Die ModuleSignature-Tabelle in einer MSI-Datei enthält jedoch eine Zeile, die diese Informationen für jede MSM-Datei enthält, die mit ihr zusammengeführt wurde.

Merge-und Überprüfungs Tools überprüfen Sie die ModuleSignature-Tabelle in MSI-Dateien, um festzustellen, ob Sie über alle vom aktuellen Mergemodul benötigten abhängigen Mergemodule verfügt (siehe [moduledependent Table](moduledependency-table.md)) und ob das Installationspaket zuvor mit zusammengesetzten Mergemodulen zusammengeführt wurde (siehe [Tabelle "moduleausschluss](moduleexclusion-table.md)").

Die ModuleSignature-Tabelle weist die folgenden Spalten auf.



| Spalte   | Typ                         | Schlüssel | Nullwerte zulässig |
|----------|------------------------------|-----|----------|
| ModuleID | [Bezeichner](identifier.md) | J   | N        |
| Sprache | [Integer](integer.md)       | J   | N        |
| Version  | [Version](version.md)       |     | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID
</dt> <dd>

Ein Bezeichner, der das Mergemodul eindeutig identifiziert. Zwei Mergemodule können nicht denselben ModuleID aufweisen, es sei denn, das Mergemodul ist vollständig abwärts kompatibel mit dem Vorgänger. Sie können eine GUID für dieses Feld mit einem Hilfsprogramm wie GUIDGEN erstellen. Die ModuleID-Spalte ist ein Primärschlüssel für die Tabelle und muss daher der Benennungs Konvention unter [Benennen von primär Schlüsseln in mergemoduldatenbanken](naming-primary-keys-in-merge-module-databases.md)entsprechen. Wenn z. b. der lesbare Name des Mergemoduls MyLibrary lautet und die GUID {880de2s0-cdd8-11d1-a849-006097abde17} lautet, wird der Eintrag in der Spalte ModuleID zu MyLibrary. 880de2s0 \_ CDD8 \_ 11d1 \_ A849 \_ 006097abde17.

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Kurse
</dt> <dd>

Der sprach Bezeichner gibt die Standardsprache für das Mergemodul an. Der sprach Bezeichner weist das Dezimal Format auf, z. b. US-Englisch ist 1033. Die vom Mergemodul verwendete Sprache kann durch Anwenden einer Transformation auf das Mergemodul vor dem Mergen geändert werden.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>Version
</dt> <dd>

Das Versions Feld enthält eine Zeichenfolge, die die Haupt-und neben Versionen des Mergemoduls beschreibt.

</dd> </dl>

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mehrere Language Merge-Module](multiple-language-merge-modules.md)
</dt> </dl>

 

 



