---
description: ICE02 überprüft, ob bestimmte Verweise zwischen der Komponente, der Datei und den Registrierungs Tabellen einander unterliegen. Diese Verweise müssen einander gegenseitig sein, damit das Installationsprogramm den Installationsstatus von Komponenten ordnungsgemäß bestimmen konnte.
ms.assetid: 864404f1-439d-49a2-973d-4e6e1618863e
title: ICE02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1975203825d079d5eeb1ec5e4183767dd68625bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750136"
---
# <a name="ice02"></a>ICE02

ICE02 überprüft, ob bestimmte Verweise zwischen der [Komponente](component-table.md), der [Datei](file-table.md)und den [Registrierungs](registry-table.md) Tabellen einander unterliegen. Diese Verweise müssen einander gegenseitig sein, damit das Installationsprogramm den Installationsstatus von Komponenten ordnungsgemäß bestimmen konnte.

Das Installationsprogramm verwendet die KEYPATH-Spalte der Component-Tabelle, um zu erkennen, ob die in der Component-Spalte aufgeführte Komponente vorhanden ist. Die KEYPATH-Spalte enthält einen Schlüssel in die Registrierungs-oder Datei Tabellen. Beide Tabellen haben eine Komponenten \_ Spalte, die einen Schlüssel zurück in die Komponenten Tabelle enthält, der auf die Komponente verweist, die den Registrierungs Eintrag bzw. die Registrierungsdatei steuert. Diese Verweise müssen einander gegenseitig sein.

## <a name="result"></a>Ergebnis

ICE02 gibt eine Fehlermeldung aus, wenn ein Verweis gefunden wird, der gegenseitig sein soll und nicht ist.

## <a name="example"></a>Beispiel

ICE02 würde die folgende Fehlermeldung für eine MSI-Datei mit den angezeigten Datenbankeinträgen veröffentlichen.

``` syntax
File: 'Red_File' cannot be the key file for Component: 'Blue'. The file belongs to Component: 'Red'
```

[Komponenten Tabelle](component-table.md) (partiell)



| Komponente | KEYPATH   |
|-----------|-----------|
| Red       | Rote \_ Datei |
| Blau      | Rote \_ Datei |



 

[Dateitabelle](file-table.md) (partiell)



| Datei Spalte | Komponente\_ |
|-------------|-------------|
| Rote \_ Datei   | Red         |
| Blaue \_ Datei  | Blau        |



 

Die Komponente blau verweist \_ auf die rote Datei, aber \_ die rote Datei wird nicht von der Komponente blau gesteuert und kann daher nicht die KEYPATH-Datei sein. Wenn das Installationsprogramm aufgerufen wurde, um den Installationsstatus blau zu erhalten, würde fälschlicherweise überprüft, ob die rote \_ Datei installiert wurde. Wenn Sie das Feld "KEYPATH" für Blau in der Komponenten Tabelle in die blaue Datei ändern, wird \_ der Fehler behoben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



