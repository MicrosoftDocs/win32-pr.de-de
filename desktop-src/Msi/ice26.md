---
description: ICE26 überprüft Sequenz Tabellen in einer Windows Installer Datenbank.
ms.assetid: 7ea47452-3147-4d39-961d-a10eca8328c9
title: ICE26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7b110d0b15b37441170980d0fd3e96e2eb00d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866292"
---
# <a name="ice26"></a>ICE26

ICE26 überprüft, ob jede der folgenden [*Sequenz Tabellen*](s-gly.md) die von der Tabelle benötigten Aktionen enthält und keine Aktionen enthält, die in der Tabelle nicht zulässig sind:

-   [AdminUISequence-Tabelle](adminuisequence-table.md)
-   [AdminExecuteSequence-Tabelle](adminexecutesequence-table.md)
-   [InstallUISequence-Tabelle](installuisequence-table.md)
-   [InstallExecuteSequence-Tabelle](installexecutesequence-table.md)

## <a name="result"></a>Ergebnis

ICE26 gibt eine Fehlermeldung aus, wenn das Installationspaket eine Sequenz Tabelle enthält, für die eine erforderliche Aktion fehlt oder die eine Aktion enthält, die für die Tabelle nicht zulässig ist.

## <a name="example"></a>Beispiel



| ICE26-Fehler                                                                   | BESCHREIBUNG                                                                                                                                                                    |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aktion: ' Action1 ' ist in der InstallExecuteSequence-Sequenz Tabelle erforderlich.   | Eine erforderliche Aktion fehlt in der angegebener Sequenz Tabelle. Weitere Informationen finden Sie in den template.msi oder den vorgeschlagenen Sequenz Tabellen unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md). |
| Aktion: ' Action2 ' ist in der InstallExecuteSequence-Sequenz Tabelle nicht zulässig. | Diese Aktion kann nicht in der angegeben Sequenz Tabelle ausgeführt werden. Entfernen Sie diese Aktion aus der Sequenz Tabelle.                                                                             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



