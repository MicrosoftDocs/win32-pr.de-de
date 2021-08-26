---
description: Wenn eine Tabelle im Mergemodul in der Tabelle ModuleIgnoreTable aufgeführt ist, wird sie nicht mit der datei .msi zusammengeführt.
ms.assetid: 9ff87993-74f6-4436-b0a9-d7ebed6555bd
title: ModuleIgnoreTable-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46337b74f6822b374314a9248f0377ec63359c6576a6ca1398a931d27e548138
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042858"
---
# <a name="moduleignoretable-table"></a>ModuleIgnoreTable-Tabelle

Wenn eine Tabelle im Mergemodul in der Tabelle ModuleIgnoreTable aufgeführt ist, wird sie nicht mit der datei .msi zusammengeführt. Wenn die Tabelle bereits in der .msi Datei vorhanden ist, wird sie durch den Merge nicht geändert. Die Tabellen in moduleIgnoreTable können daher Daten enthalten, die nach der Zusammenführung nicht mehr benötigt werden.

Die Tabelle ModuleIgnoreTable enthält die folgenden Spalten.



| Spalte | Typ                         | Key | Nullwerte zulässig |
|--------|------------------------------|-----|----------|
| Tabelle  | [Identifier](identifier.md) | J   | Nein       |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabelle
</dt> <dd>

Der Name der Tabelle im Mergemodul, die nicht mit der datei .msi zusammengeführt werden soll.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Um die Größe der MSM-Datei zu minimieren, sollten Entwickler nicht verwendete Tabellen aus Modulen entfernen, die für die Weiterverteilung vorgesehen sind, anstatt diese Tabellen in der Tabelle ModuleIgnoreTable aufzulisten.

 

 



