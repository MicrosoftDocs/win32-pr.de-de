---
description: ICE79 überprüft die Verweise auf Komponenten und Funktionen, die in den Datenbankfeldern eingegeben wurden, mithilfe des Bedingungs Datentyps.
ms.assetid: f0a8ceac-084a-4693-b27d-f610eec4702a
title: ICE79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9081297f2bf2f11283380c0f057bd0fbec417975
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129965"
---
# <a name="ice79"></a>ICE79

ICE79 überprüft die Verweise auf Komponenten und Funktionen, die in den Datenbankfeldern eingegeben wurden, [mithilfe des Bedingungs](condition.md) Datentyps.

## <a name="result"></a>Ergebnis

ICE79 gibt zwei Warnungen aus.



| ICE79-Warnung                                                                      | BESCHREIBUNG                                                      |
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| Die Validierungs Tabelle der Datenbank fehlt \_ . Eigenschaftsnamen konnten nicht vollständig überprüft werden. | Die [ \_ Validierungs Tabelle](-validation-table.md)der Datenbank fehlt. |
| Fehler beim Abrufen von Werten aus Spalte \[ 2 \] in Tabelle \[ 1 \] . Die Spalte wird übersprungen.         | Fehler beim Abrufen des Werts.                                          |



 

ICE79 gibt zwei Fehler aus.



| ICE79-Fehler                                                          | BESCHREIBUNG                               |
|----------------------------------------------------------------------|-------------------------------------------|
| Auf die '% ls '-Komponente wurde in der '% s '-Spalte verwiesen. ' '% s ' der Zeile '% s ' ist ungültig. | Es wurde ein ungültiger Komponenten Verweis gefunden. |
| Auf das Feature "% ls" wurde in der Spalte "% s" verwiesen. '% s ' der Zeile '% s ' ist ungültig.   | Es wurde ein ungültiger Funktions Verweis gefunden.    |



 

## <a name="example"></a>Beispiel

ICE79 meldet die folgenden Fehler für das Beispiel:

``` syntax
Component 'NoSuchComponent' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom2 is invalid.
Feature 'NoSuchFeature' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom1 is invalid.
```

In diesem Beispiel fehlt nosuchcomponent in der Component- [Tabelle](component-table.md) , und nosuchfeature ist in der Featuretabelle nicht vorhanden. [](feature-table.md)

[InstallExecuteSequence-Tabelle](installexecutesequence-table.md) (partiell)



| Aktion  | Bedingung                                |
|---------|------------------------------------------|
| Custom1 | TestAction = 1046 und &nosuchfeature>2  |
| Custom2 | TestAction = 146 und $NoSuchComponent>2 |



 

Um diese Fehler zu beheben, geben Sie in den Funktions-und Komponenten Tabellen gültige Datensätze für nosuchfeature und nosuchcomponent ein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



