---
description: Die Verzeichnisse in der Verzeichnis Tabelle geben das Layout einer-Installation an.
ms.assetid: 59f6ae09-d013-46d7-a1a7-0543f31ac487
title: Verwenden einer Verzeichnis Eigenschaft in einem Pfad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2789f6442072f3db6a96c0abb7db301038673f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362735"
---
# <a name="using-a-directory-property-in-a-path"></a>Verwenden einer Verzeichnis Eigenschaft in einem Pfad

Die Verzeichnisse in der [Verzeichnis Tabelle](directory-table.md) geben das Layout einer-Installation an. Wenn das Windows Installer diese Verzeichnisse während der [costfinalize-Aktion](costfinalize-action.md)auflöst, werden die Schlüssel in der Verzeichnis Tabelle zu [Eigenschaften](properties.md) , die auf Verzeichnispfade festgelegt sind. Das Installationsprogramm legt auch immer eine Reihe von Standard [Systemordner-Eigenschaften](property-reference.md) auf Systemordner Pfade fest.

Es ist garantiert, dass die Werte der [Eigenschaften des System Ordners](property-reference.md) in einem Verzeichnis Trennzeichen enden. Die Werte aller anderen Eigenschaften, die in der [Verzeichnis Tabelle](directory-table.md) eingegeben werden, werden nur nach dem Ausführen der [Aktion "costfinalize](costfinalize-action.md)" in einem Verzeichnis Trennzeichen garantiert. Vor Abschluss der Kosten werden die in der Verzeichnis Tabelle eingegebenen Werte von Eigenschaften, die keine [System Ordnereigenschaften](property-reference.md) sind, möglicherweise nicht mit einem Verzeichnis Trennzeichen enden. Wenn bei der Installation Verzeichnis Eigenschaften mithilfe von [benutzerdefinierten Aktionen](custom-actions.md) im Paket festgelegt werden, enden die Verweis Werte möglicherweise nicht mit einem Verzeichnis Trennzeichen.

Verzeichnis Eigenschaften, die mit einem Verzeichnis Trennzeichen enden, können daher in einer Pfad Zeichenfolge ohne explizites einschließen des Verzeichnis Trennzeichens verwendet werden Wenn der Wert von Director Property beispielsweise mit einem Verzeichnis Trennzeichen endet, gibt die folgende Zeichenfolge ordnungsgemäß den Pfad zu der *Datei* im *Unterverzeichnis* an.

``` syntax
[DirectoryProperty]subdirectory\file
```

und die folgende Pfad Zeichenfolge ist falsch.

``` syntax
[DirectoryProperty]\subdirectory\file
```

 

 



