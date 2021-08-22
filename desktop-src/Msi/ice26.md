---
description: ICE26 überprüft Sequenztabellen in einer Windows Installer-Datenbank.
ms.assetid: 7ea47452-3147-4d39-961d-a10eca8328c9
title: ICE26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf63e0efeec79de35122f7a210c32746af9de50f27ac3e47ad1f88984a6ec77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528860"
---
# <a name="ice26"></a>ICE26

ICE26 überprüft, ob jede [](s-gly.md) der folgenden Sequenztabellen die aktionen enthält, die für die Tabelle erforderlich sind, und enthält keine Aktionen, die in der Tabelle nicht enthalten sind:

-   [AdminUISequence-Tabelle](adminuisequence-table.md)
-   [AdminExecuteSequence-Tabelle](adminexecutesequence-table.md)
-   [InstallUISequence-Tabelle](installuisequence-table.md)
-   [InstallExecuteSequence-Tabelle](installexecutesequence-table.md)

## <a name="result"></a>Ergebnis

ICE26 gibt eine Fehlermeldung aus, wenn das Installationspaket über eine Sequenztabelle verfügt, die keine erforderliche Aktion enthält oder eine Aktion enthält, die für die Tabelle nicht zu verfüglich ist.

## <a name="example"></a>Beispiel



| ICE26-Fehler                                                                   | Beschreibung                                                                                                                                                                    |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aktion: "Action1" ist in der Tabelle InstallExecuteSequence Sequence erforderlich.   | In der angegebenen Sequenztabelle fehlt eine erforderliche Aktion. Weitere Informationen finden template.msi oder die vorgeschlagenen Sequenztabellen unter [Verwenden einer Sequenztabelle.](using-a-sequence-table.md) |
| Aktion: "Action2" ist in der Tabelle InstallExecuteSequence Sequence nicht zulässig. | Diese Aktion kann nicht in der angegebenen Sequenztabelle sein. Entfernen Sie diese Aktion aus der Sequenztabelle.                                                                             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



