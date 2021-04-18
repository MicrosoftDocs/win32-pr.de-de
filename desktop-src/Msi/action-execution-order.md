---
description: Die Reihenfolge der Aktions Ausführung wird durch die Abfolge der Aktionen bestimmt, die in den Sequenz Tabellen und in der Reihenfolge, in der das Installationsprogramm die Sequenz Tabellen ausführt, erstellt wurden.
ms.assetid: f4666f49-4ea1-42fb-b32d-ce77de79b212
title: Aktions Ausführungsreihenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 954c44f6e2525deb3375cb9ea72d0320df3a5f02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343855"
---
# <a name="action-execution-order"></a>Aktions Ausführungsreihenfolge

Die Reihenfolge der Aktions Ausführung wird durch die Abfolge der Aktionen bestimmt, die in den [*Sequenz Tabellen*](s-gly.md) und in der Reihenfolge, in der das Installationsprogramm die Sequenz Tabellen ausführt, erstellt wurden. Weitere Informationen finden Sie in den empfohlenen Aktions Sequenzen unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).

Das Installationsprogramm führt Sequenz Tabellen als Antwort auf eine Anforderung für eine Installation [, eine](advertisement.md)Ankündigung oder eine [Administrative Installation](administrative-installation.md)aus. Beispielsweise werden in Reaktion auf die [Befehlszeilenoptionen](command-line-options.md)/I,/J oder/A die Aktionen [install](install-action.md) [, Ankündigungs und](advertise-action.md) [Admin](admin-action.md) nicht innerhalb der Aktions Sequenz aufgerufen. Diese Aktionen auf hoher Ebene werden stattdessen an das Installationsprogramm übermittelt, wenn das Installationsprogramm initialisiert wird.

Wenn das Installationsprogramm an die Installations Aktion weitergeleitet wird und das Installationspaket mit einer Benutzeroberfläche erstellt wurde, führt das Installationsprogramm zuerst die Aktionen in der [Tabelle "InstallUISequence](installuisequence-table.md) " aus und führt dann die Aktionen in der [Tabelle InstallExecuteSequence](installexecutesequence-table.md) aus. Wenn das Paket keine Benutzeroberfläche besitzt, führt das Installationsprogramm die Aktionen in der InstallExecuteSequence-Tabelle in der angegebenen Reihenfolge aus.

Wenn das Installationsprogramm an die Administrator Aktion weitergeleitet wird und das Installationspaket mit einer Benutzeroberfläche erstellt wurde, führt das Installationsprogramm zuerst die [Tabelle AdminUISequence](adminuisequence-table.md) aus und führt dann die [Tabelle AdminExecuteSequence](adminexecutesequence-table.md)aus. Wenn das Paket keine Benutzeroberfläche hat, führt das Installationsprogramm die Tabelle adminexecute aus.

Wenn dem Installer die Aktion ankündigen übermittelt wird, führt das Installationsprogramm die [AdvtExecuteSequence](advtexecutesequence-table.md) -Tabelle aus.

> [!Note]  
> Das Installationsprogramm verwendet nicht die [advtuisequence](advtuisequence-table.md) -Tabelle. Die advtuisequence-Tabelle sollte nicht in der Installations Datenbank vorhanden sein, oder Sie sollte leer gelassen werden.

 

Wenn das Installationsprogramm eine Sequenz Tabelle ausführt, führt es Aktionen in der Reihenfolge der Sequenznummern aus, die in der Sequence-Spalte aufgelistet sind. Die Aktions Reihenfolge ist immer linear, ohne Verzweigungen oder Schleifen. Paket Entwickler können bedingt verhindern, dass eine bestimmte Aktion ausgeführt wird, indem Sie einen logischen Ausdruck in der Spalte Bedingung erstellen. Das Installationsprogramm überspringt die Aktion immer dann, wenn die Bedingung als false ausgewertet wird. Weitere Informationen finden [Sie unter Verwenden einer Sequenz Tabelle](using-a-sequence-table.md) und [Syntax einer bedingten Anweisung](conditional-statement-syntax.md).

Alle Sequenz Tabellen weisen die folgenden Spalten auf.



| Column    | BESCHREIBUNG                                                                                                                                                                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aktion    | Der Primärschlüssel für die Tabelle. der Aktionsname muss eindeutig sein.                                                                                                                                                                                |
| Bedingung | Ein boolescher Ausdruck, mit dem bestimmt wird, ob die Aktion ausgeführt werden soll. Die Aktion wird ausgeführt, wenn dieses Feld leer ist oder einen Ausdruck enthält, der als true ausgewertet wird. Die Aktion wird nicht ausgeführt, wenn der Ausdruck zu false ausgewertet wird. |
| Sequenz  | Eine relative Sequenznummer, die verwendet wird, um die Reihenfolge zu bestimmen, in der Aktionen ausgeführt werden.                                                                                                                                                         |



 

 

 



