---
description: Die Reihenfolge der Aktionsausführung wird durch die Sequenz von Aktionen bestimmt, die in den Sequenztabellen erstellt wurden, und durch die Reihenfolge, in der das Installationsprogramm die Sequenztabellen ausgeführt.
ms.assetid: f4666f49-4ea1-42fb-b32d-ce77de79b212
title: Reihenfolge der Aktionsausführung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf28244d46ae5556d1b68cc3b7258297c69e11a8d526f3e7ca31a184e64c424e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381840"
---
# <a name="action-execution-order"></a>Reihenfolge der Aktionsausführung

Die Reihenfolge der Aktionsausführung wird durch die Sequenz von [](s-gly.md) Aktionen bestimmt, die in den Sequenztabellen erstellt wurden, und durch die Reihenfolge, in der das Installationsprogramm die Sequenztabellen ausgeführt. Weitere Informationen finden Sie in den vorgeschlagenen Aktionssequenzen unter [Verwenden einer Sequenztabelle.](using-a-sequence-table.md)

Das Installationsprogramm führt Sequenztabellen als Reaktion auf eine Anforderung für eine Installation, [Ankündigung](advertisement.md)oder eine [administrative Installation aus.](administrative-installation.md) Beispielsweise werden als Reaktion auf die Verwendung der Befehlszeilenoptionen /I, /J oder [/A](command-line-options.md)die [Aktionen INSTALL,](install-action.md) [ADVERTISE](advertise-action.md)und [ADMIN](admin-action.md) nicht innerhalb der Aktionssequenz aufgerufen. Diese aktionen auf hoher Ebene werden stattdessen an das Installationsprogramm übergeben, wenn das Installationsprogramm initialisiert wird.

Wenn dem Installationsprogramm die Install-Aktion übergeben wird und das Installationspaket mit einer Benutzeroberfläche erstellt wurde, führt das Installationsprogramm zuerst die Aktionen in der [Tabelle InstallUISequence](installuisequence-table.md) aus und führt dann die Aktionen in der [Tabelle InstallExecuteSequence](installexecutesequence-table.md) in der Reihenfolge aus. Wenn das Paket über keine Benutzeroberfläche verfügt, führt das Installationsprogramm die Aktionen in der Tabelle InstallExecuteSequence in der Reihenfolge aus.

Wenn dem Installationsprogramm die Admin-Aktion übergeben wird und das Installationspaket mit einer Benutzeroberfläche erstellt wurde, führt das Installationsprogramm zuerst die [Tabelle AdminUISequence](adminuisequence-table.md) und dann die [AdminExecuteSequence-Tabelle aus.](adminexecutesequence-table.md) Wenn das Paket über keine Benutzeroberfläche verfügt, führt das Installationsprogramm die Tabelle AdminExecute aus.

Wenn dem Installationsprogramm die AKTION ADVERTISE übergeben wird, führt das Installationsprogramm die [Tabelle AdvtExecuteSequence](advtexecutesequence-table.md) aus.

> [!Note]  
> Das Installationsprogramm verwendet nicht die [AdvtUISequence-Tabelle.](advtuisequence-table.md) Die AdvtUISequence-Tabelle sollte nicht in der Installationsdatenbank vorhanden sein, oder sie sollte leer bleiben.

 

Wenn das Installationsprogramm eine Sequenztabelle ausgeführt, führt es Aktionen in der Reihenfolge der Sequenznummern aus, die in der Spalte Sequenz aufgeführt sind. Die Aktions reihenfolge ist immer linear ohne Verzweigung oder Schleifen. Paketentwickler können bedingt verhindern, dass eine bestimmte Aktion ausgeführt wird, indem sie einen logischen Ausdruck in der Spalte Bedingung erstellen. Das Installationsprogramm überspringt die Aktion, wenn die Bedingung als False ausgewertet wird. Weitere Informationen finden Sie unter Using a Sequence Table and Conditional Statement Syntax (Verwenden [einer Sequenztabelle](using-a-sequence-table.md) und [der Syntax für bedingte Anweisungen).](conditional-statement-syntax.md)

Alle Sequenztabellen verfügen über die folgenden Spalten.



| Column    | BESCHREIBUNG                                                                                                                                                                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aktion    | Der Primärschlüssel für die Tabelle; der Aktionsname muss eindeutig sein.                                                                                                                                                                                |
| Bedingung | Ein boolescher Ausdruck, der verwendet wird, um zu bestimmen, ob die Aktion durchzuführen ist. Die Aktion wird ausgeführt, wenn dieses Feld entweder leer ist oder einen Ausdruck enthält, der als True ausgewertet wird. Die Aktion wird nicht ausgeführt, wenn der Ausdruck falseausgewertet wird. |
| Sequenz  | Eine relative Sequenznummer, mit der die Reihenfolge bestimmt wird, in der Aktionen ausgeführt werden.                                                                                                                                                         |



 

 

 



