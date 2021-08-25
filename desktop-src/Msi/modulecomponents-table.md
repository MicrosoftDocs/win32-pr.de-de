---
description: Die Tabelle ModuleComponents enthält eine Liste der Komponenten im Mergemodul.
ms.assetid: def96d52-c9fa-4fac-b575-f9de8eb82d1c
title: Tabelle "ModuleComponents"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25216833022ada7592511091c6954222d8ebf354e732c95a54e8857948963541
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926480"
---
# <a name="modulecomponents-table"></a>Tabelle "ModuleComponents"

Die Tabelle ModuleComponents enthält eine Liste der Komponenten im Mergemodul.

Die Tabelle ModuleComponents enthält die folgenden Spalten.



| Spalte    | Typ                         | Key | Nullwerte zulässig |
|-----------|------------------------------|-----|----------|
| Komponente | [Identifier](identifier.md) | J   | N        |
| ModuleID  | [Identifier](identifier.md) | J   | N        |
| Sprache  | [Integer](integer.md)       | J   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>Komponente
</dt> <dd>

Ein Bezeichner, der auf eine Komponente im Mergemodul verweist. Die Component -Spalte ist ein Fremdschlüssel für die [Component-Tabelle](component-table.md). Der Eintrag in der Spalte Komponente muss der Benennungskonvention unter [Benennen von Primärschlüsseln in Mergemoduldatenbanken](naming-primary-keys-in-merge-module-databases.md)entsprechen.

</dd> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>Moduleid
</dt> <dd>

Der Bezeichner für das Mergemodul. Dies ist ein Fremdschlüssel für die [Tabelle ModuleSignature.](modulesignature-table.md)

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Sprache
</dt> <dd>

Der Sprachbezeichner beschreibt die Standardsprache für das Mergemodul. Der Sprachbezeichner ist im Dezimalformat, z.B. ist Englisch in den USA 1033. Fremdschlüssel für die [ModuleSignature-Tabelle](modulesignature-table.md).

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sprachtransformationen müssen in der Lage sein, diese Tabelle zu aktualisieren, wenn das Mergemodul mehrere Sprachen unterstützt.

 

 



