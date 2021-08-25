---
description: Die Verzeichnisse in der Directory-Tabelle geben das Layout einer Installation an.
ms.assetid: 59f6ae09-d013-46d7-a1a7-0543f31ac487
title: Verwenden einer Verzeichniseigenschaft in einem Pfad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa00bf3953be46484d74d3a432135763d1b06d4e7daf72bbc36f284e039613f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141475"
---
# <a name="using-a-directory-property-in-a-path"></a>Verwenden einer Verzeichniseigenschaft in einem Pfad

Die Verzeichnisse in der [Directory-Tabelle geben](directory-table.md) das Layout einer Installation an. Wenn der Windows Installer diese Verzeichnisse während der [Aktion CostFinalize](costfinalize-action.md)auflöset, [](properties.md) werden die Schlüssel in der Directory-Tabelle zu Eigenschaften, die auf Verzeichnispfade festgelegt sind. Das Installationsprogramm legt auch immer eine Reihe von Standardeigenschaften für [Systemordner auf](property-reference.md) Systemordnerpfade fest.

Die Werte der [Systemordnereigenschaften](property-reference.md) enden garantiert in einem Verzeichnistrennzeichen. Die Werte aller anderen Eigenschaften, die in der [Directory-Tabelle](directory-table.md) eingegeben werden, enden garantiert nur in einem Verzeichnistrennzeichen, nachdem das Installationsprogramm die [Aktion CostFinalize ausgeführt hat.](costfinalize-action.md) Vor Abschluss der Kosten werden die Werte der in der Verzeichnistabelle eingegebenen Eigenschaften, die keine [Systemordnereigenschaften](property-reference.md) sind, möglicherweise nicht in einem Verzeichnistrennzeichen enden. Wenn ihre Installation Verzeichniseigenschaften [](custom-actions.md) mithilfe benutzerdefinierter Aktionen im Paket fest legt, enden die Werte für den Verweis daher möglicherweise nicht mit einem Verzeichnistrennzeichen.

Verzeichniseigenschaften, die mit einem Verzeichnistrennzeichen enden, können daher in einer Pfadzeichenfolge verwendet werden, ohne dass das Verzeichnistrennzeichen explizit enthalten ist. Wenn der Wert von DirectoryProperty beispielsweise mit einem Verzeichnistrennzeichen endet, gibt die folgende Zeichenfolge den Pfad zur Datei *im* *Unterverzeichnis richtig an.*

``` syntax
[DirectoryProperty]subdirectory\file
```

und die folgende Pfadzeichenfolge ist falsch.

``` syntax
[DirectoryProperty]\subdirectory\file
```

 

 



