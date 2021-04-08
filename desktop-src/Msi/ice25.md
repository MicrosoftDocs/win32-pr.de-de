---
description: ICE25 überprüft, ob eine MSI-Datei alle internen Zusammenschluss-Modul Abhängigkeiten und-Ausschlüsse erfüllt.
ms.assetid: e6e3ea44-a1d4-451a-b326-e8fb7ed4adeb
title: ICE25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d966c4c374d6e61e30b44a41ad88bed8bf907f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866295"
---
# <a name="ice25"></a>ICE25

ICE25 überprüft, ob eine MSI-Datei alle internen [Zusammenschluss-Modul](merge-modules.md) Abhängigkeiten und-Ausschlüsse erfüllt. Ice überprüft Folgendes:

-   Alle mergemodulabhängigkeiten, die in der [Tabelle "moduledependen"](moduledependency-table.md) der MSI-Datei angegeben sind, werden von mindestens einem in der [Tabelle "ModuleSignature](modulesignature-table.md)" aufgelisteten Mergemodul erfüllt.
-   Keines der ausgeschlossenen Mergemodule in der [Tabelle "moduleausschluss](moduleexclusion-table.md) " ist mit den in der Tabelle " [ModuleSignature](modulesignature-table.md)" aufgelisteten Mergemodulen nicht kompatibel.

## <a name="result"></a>Ergebnis

ICE25 gibt eine Fehlermeldung aus, wenn die MSI-Datei bereits mit einem inkompatiblen Mergemodul zusammengeführt wurde, oder wenn Sie nicht mit einem erforderlichen Mergemodul zusammengeführt wurde.

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
| Moduleb  | 1033     | 1.0     |



 

[Moduledepenptabelle](moduledependency-table.md)



| ModuleID | Modulelanguage | Requirements did | Requirements-Sprache | RequiredVersion |
|----------|----------------|------------|------------------|-----------------|
| Modulea  | 0              | Modulex    | 0                | 2.0             |



 

[Moduleausschluss-Tabelle](moduleexclusion-table.md)



| ModuleID | Modulelanguage | Excludädid | Excludecodlanguage | Excludedminversion | Excludedmaxversion |
|----------|----------------|------------|------------------|--------------------|--------------------|
| Modulea  | 0              | Moduleb    | 1033             |                    |                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



