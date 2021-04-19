---
description: Die modulecomponents-Tabelle enthält eine Liste der Komponenten, die im Mergemodul gefunden werden.
ms.assetid: def96d52-c9fa-4fac-b575-f9de8eb82d1c
title: Modulecomponents-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ea2f47418b0387c7fa9d289d156fb0369f53adf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349624"
---
# <a name="modulecomponents-table"></a>Modulecomponents-Tabelle

Die modulecomponents-Tabelle enthält eine Liste der Komponenten, die im Mergemodul gefunden werden.

Die modulecomponents-Tabelle weist die folgenden Spalten auf.



| Spalte    | Typ                         | Schlüssel | Nullwerte zulässig |
|-----------|------------------------------|-----|----------|
| Komponente | [Bezeichner](identifier.md) | J   | N        |
| ModuleID  | [Bezeichner](identifier.md) | J   | N        |
| Sprache  | [Integer](integer.md)       | J   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>Zulieferern
</dt> <dd>

Ein Bezeichner, der auf eine Komponente im Mergemodul verweist. Die Komponenten Spalte ist ein Fremdschlüssel für die [Komponenten Tabelle](component-table.md). Der Eintrag in der Component-Spalte muss der Benennungs Konvention unter [Benennen von primär Schlüsseln in mergemoduldatenbanken](naming-primary-keys-in-merge-module-databases.md)entsprechen.

</dd> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID
</dt> <dd>

Der Bezeichner für das Mergemodul. Dies ist ein Fremdschlüssel für die [ModuleSignature-Tabelle](modulesignature-table.md).

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Kurse
</dt> <dd>

Der Sprachen Bezeichner beschreibt die Standardsprache für das Mergemodul. Der sprach Bezeichner weist das Dezimal Format auf, z. b. US-Englisch ist 1033. Fremdschlüssel für die [ModuleSignature-Tabelle](modulesignature-table.md).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sprach Transformationen müssen in der Lage sein, diese Tabelle zu aktualisieren, wenn das Mergemodul mehrere Sprachen unterstützt.

 

 



