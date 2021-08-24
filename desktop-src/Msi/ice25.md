---
description: ICE25 überprüft, ob .msi-Datei alle internen Abhängigkeiten und Ausschlüsse des Mergemoduls erfüllt.
ms.assetid: e6e3ea44-a1d4-451a-b326-e8fb7ed4adeb
title: ICE25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2715ce629ad22b872b8d38d0c6848236b9f1af9378a0a652b702e7b72cbd7dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528950"
---
# <a name="ice25"></a>ICE25

ICE25 überprüft, ob .msi datei alle internen Mergemodulabhängigkeiten [und](merge-modules.md) -ausschlüsse erfüllt. ICE überprüft Folgendes:

-   Alle Mergemodulabhängigkeiten, die in der [ModuleDependency-Tabelle](moduledependency-table.md) der .msi angegeben sind, werden von mindestens einem Mergemodul erfüllt, das in der [ModuleSignature-Tabelle aufgeführt ist.](modulesignature-table.md)
-   Dass keines der ausgeschlossenen Mergemodule in der [ModuleExclusion-Tabelle](moduleexclusion-table.md) mit den merge-Modulen in der [ModuleSignature-Tabelle inkompatibel ist.](modulesignature-table.md)

## <a name="result"></a>Ergebnis

ICE25 gibt eine Fehlermeldung aus, wenn .msi-Datei zuvor mit einem inkompatiblen Mergemodul zusammengeführt wurde oder wenn sie nicht mit einem erforderlichen Mergemodul zusammengeführt wurde.

## <a name="example"></a>Beispiel

ICE25 veröffentlicht die folgenden Fehler für das gezeigte Beispiel.

``` syntax
Dependency failure: Need ModuleX@0 v2.0 
Module ModuleB@1033 v1.0 is excluded.
```

[ModuleSignature-Tabelle](modulesignature-table.md)



| ModuleID | Sprache | Version |
|----------|----------|---------|
| Modulea  | 0        | 1.0     |
| ModuleB  | 1033     | 1.0     |



 

[ModuleDependency-Tabelle](moduledependency-table.md)



| ModuleID | ModuleLanguage | RequiredID | RequiredLanguage | RequiredVersion |
|----------|----------------|------------|------------------|-----------------|
| Modulea  | 0              | ModuleX    | 0                | 2.0             |



 

[ModuleExclusion-Tabelle](moduleexclusion-table.md)



| ModuleID | ModuleLanguage | ExcludedID | ExcludedLanguage | ExcludedMinVersion | ExcludedMaxVersion |
|----------|----------------|------------|------------------|--------------------|--------------------|
| Modulea  | 0              | ModuleB    | 1033             |                    |                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



