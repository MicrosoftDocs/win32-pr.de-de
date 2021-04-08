---
description: ICE06 prüft jede Tabelle, um zu überprüfen, ob alle in der \_ Validierungs Tabelle aufgeführten Spalten in der Tabelle vorhanden sind. Wenn keine Tabelle vorhanden ist, werden alle \_ Validierungs Einträge für diese Tabelle ignoriert.
ms.assetid: 0c3f21ae-49ea-4cfe-b465-6fdc2b19cbb9
title: ICE06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9442d9b2c4089b88299106de875074bd7b0625
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960044"
---
# <a name="ice06"></a>ICE06

ICE06 prüft jede Tabelle, um zu überprüfen, ob alle in der [ \_ Validierungs Tabelle](-validation-table.md) aufgeführten Spalten in der Tabelle vorhanden sind. Wenn keine Tabelle vorhanden ist, werden alle \_ Validierungs Einträge für diese Tabelle ignoriert.

Der Zweck von ICE06 besteht darin, Instanzen zu erkennen, in denen ein Autor versucht, eine neue \_ Validierungs Tabelle zu verwenden, die eine Schema Änderung mit einer alten Datenbank widerspiegelt, die noch nicht aktualisiert wurde. ICE06 erkennt auch den umgekehrten Fall einer alten \_ Validierungs Tabelle, die mit einer geänderten Datenbank verwendet wird.

Beachten Sie, dass die von [ICE03](ice03.md) durchgeführte interne Validierung die Instanz einer Tabellenspalte abfängt, die in der \_ im Columns-Katalog aufgelisteten Überprüfungs Tabelle nicht definiert ist. Durch die Verwendung von "ICE03" und "ICE06" wird sichergestellt, dass jede Spalte in der Datenbank getestet wird.

## <a name="result"></a>Ergebnis

ICE06 gibt einen Fehler aus, wenn eine Tabellenspalte in der \_ Validierungs Tabelle definiert ist, die nicht in der \_ Spalten Tabelle aufgeführt ist.

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird die Nachricht von ICE06 gepostet.

Column: Version der Tabelle: ModuleSignature ist nicht in der Datenbank definiert.

[ \_ Validierungs Tabelle](-validation-table.md) (partiell)



| Tabelle           | Spalte   |
|-----------------|----------|
| ModuleSignature | ModuleID |
| ModuleSignature | Version  |



 

[ \_ Columns-Tabelle](-columns-table.md) (partiell)



| Tabelle           | number | name     |
|-----------------|--------|----------|
| ModuleSignature | 1      | ModuleID |



 

Die Spalte Version der Tabelle ModuleSignature ist nicht in der Datenbank oder in der \_ Tabelle Columns aufgeführt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



