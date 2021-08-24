---
description: ICE79 überprüft die Verweise auf Komponenten und Features, die in die Datenbankfelder eingegeben wurden, mithilfe des Condition-Datentyps.
ms.assetid: f0a8ceac-084a-4693-b27d-f610eec4702a
title: ICE79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f11ab5bcf0cd538005a5188559b0426e27004cb5a6d043852be3e361d10e509
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821570"
---
# <a name="ice79"></a>ICE79

ICE79 überprüft die Verweise auf Komponenten und Features, die in die Datenbankfelder eingegeben wurden, mithilfe des [Condition-Datentyps.](condition.md)

## <a name="result"></a>Ergebnis

ICE79 gibt zwei Warnungen aus.



| ICE79-Warnung                                                                      | BESCHREIBUNG                                                      |
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| Der Datenbank fehlt die \_ Validierungstabelle. Eigenschaftennamen konnten nicht vollständig überprüft werden. | Der Datenbank fehlt [ \_ die Validierungstabelle](-validation-table.md). |
| Fehler beim Abrufen von Werten aus Spalte \[ 2 \] in Tabelle \[ \] 1. Überspringen der Spalte.         | Fehler beim Abrufen des Werts.                                          |



 

ICE79 sendet zwei Fehler.



| ICE79-Fehler                                                          | BESCHREIBUNG                               |
|----------------------------------------------------------------------|-------------------------------------------|
| Die Komponente '%ls', auf die in der '%s'-Spalte verwiesen wird. %s' der Zeile %s ist ungültig. | Ein ungültiger Komponentenverweis wurde gefunden. |
| Das Feature '%ls', auf das in spalte '%s' verwiesen wird.' %s' der Zeile %s ist ungültig.   | Ein ungültiger Funktionsverweis wurde gefunden.    |



 

## <a name="example"></a>Beispiel

ICE79 meldet die folgenden Fehler für das Beispiel:

``` syntax
Component 'NoSuchComponent' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom2 is invalid.
Feature 'NoSuchFeature' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom1 is invalid.
```

In diesem Beispiel fehlt NoSuchComponent in der [Component-Tabelle](component-table.md) und NoSuchFeature in der [Featuretabelle](feature-table.md).

[InstallExecuteSequence-Tabelle](installexecutesequence-table.md) (partiell)



| Aktion  | Bedingung                                |
|---------|------------------------------------------|
| Custom1 | TESTACTION=1046 AND &NoSuchFeature>2  |
| Custom2 | TESTACTION=146 AND $NoSuchComponent>2 |



 

Geben Sie gültige Datensätze für NoSuchFeature und NoSuchComponent in die Tabellen Feature und Component ein, um diese Fehler zu beheben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



