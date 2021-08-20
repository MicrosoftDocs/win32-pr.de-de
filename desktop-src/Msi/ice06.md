---
description: ICE06 überprüft jede Tabelle, um zu überprüfen, ob alle in der Tabelle Überprüfung aufgeführten Spalten \_ in der Tabelle vorhanden sind. Wenn keine Tabelle vorhanden ist, werden alle \_ Validierungseinträge für diese Tabelle ignoriert.
ms.assetid: 0c3f21ae-49ea-4cfe-b465-6fdc2b19cbb9
title: ICE06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: febccd205b78e90d3dac49f88d0750f803c8cd575b6b76b46cab79a684deea90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142568"
---
# <a name="ice06"></a>ICE06

ICE06 überprüft jede Tabelle, um zu überprüfen, ob alle in der [ \_ Tabelle Überprüfung](-validation-table.md) aufgeführten Spalten in der Tabelle vorhanden sind. Wenn keine Tabelle vorhanden ist, werden alle \_ Validierungseinträge für diese Tabelle ignoriert.

Der Zweck von ICE06 besteht darin, Instanzen zu erkennen, in denen ein Autor versucht, eine neue \_ Validierungstabelle zu verwenden, die eine Schemaänderung mit einer alten Datenbank widerspiegelt, die nicht aktualisiert wurde. ICE06 erkennt auch den umgekehrten Fall einer alten \_ Validierungstabelle, die mit einer geänderten Datenbank verwendet wird.

Beachten Sie, dass die von [ICE03](ice03.md) durchgeführte interne Validierung die Instanz einer Tabellenspalte abfängt, die nicht in der \_ Validierungstabelle definiert ist, die im Spaltenkatalog aufgeführt ist. Die Verwendung von ICE03 und ICE06 stellt daher sicher, dass jede Spalte in der Datenbank getestet wird.

## <a name="result"></a>Ergebnis

ICE06 gibt einen Fehler aus, wenn in der Tabelle Validierung eine Tabellenspalte definiert \_ ist, die nicht in der Tabelle Spalten aufgeführt \_ ist.

## <a name="example"></a>Beispiel

Im folgenden Beispiel sendet ICE06 die Nachricht.

Spalte: Version der Tabelle: ModuleSignature ist in der Datenbank nicht definiert.

[ \_ Validierungstabelle](-validation-table.md) (partiell)



| Tabelle           | Spalte   |
|-----------------|----------|
| Modulesignature | ModuleID |
| Modulesignature | Version  |



 

[ \_ Spaltentabelle](-columns-table.md) (teilweise)



| Tabelle           | number | name     |
|-----------------|--------|----------|
| Modulesignature | 1      | ModuleID |



 

Die Spalte Version der Tabelle ModuleSignature ist nicht in der Datenbank enthalten oder in der \_ Tabelle Spalten aufgeführt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



