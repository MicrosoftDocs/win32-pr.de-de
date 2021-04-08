---
description: ICE63 prüft, ob die Aktion "RemoveExistingProducts" ordnungsgemäß sequenziert werden soll.
ms.assetid: 4dd67bb0-c08a-4a44-b687-0394a3afc2c4
title: ICE63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5faa6f2ddbcb95cdf12966c2887fe9438a5d610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866719"
---
# <a name="ice63"></a>ICE63

ICE63 prüft, ob die Aktion " [RemoveExistingProducts](removeexistingproducts-action.md)" ordnungsgemäß sequenziert werden soll. Die Aktion "RemoveExistingProducts" kann platziert werden:

1.  Zwischen InstallValidate und InstallInitialize
2.  Direkt nach InstallInitialize oder nach InstallInitialize, wenn die Aktionen zwischen InstallInitialize und RemoveExistingProducts keine Skript Aktionen generieren.
3.  Unmittelbar nach InstallExecute oder InstallExecuteAgain und vor InstallFinalize (dieselbe Einschränkung wie oben).
4.  Nach InstallFinalize.

Wenn eine Warnung oder ein von ICE63 gemeldeter Fehler nicht behoben werden konnte, führt dies zu einem Fehler des Upgrades.

## <a name="result"></a>Ergebnis

ICE63 gibt eine Warnung oder einen Fehler aus, wenn die Sequenzierung der RemoveExistingProducts-Aktion nicht korrekt ist.

## <a name="example"></a>Beispiel

ICE63 meldet den folgenden Fehler für das gezeigte Beispiel.

``` syntax
WARNING: Some action falls between InstallInitialize and RemoveExistingProducts.
```

Die Aktion "MyCustomAction" erfolgt zwischen "InstallInitialize" und "RemoveExistingProducts". Wenn MyCustomAction Aktionen im Skript generiert, verursacht dies Probleme bei der Installation.

Um diesen Fehler zu beheben, überprüfen Sie, ob MyCustomAction keine Skript Aktionen generiert oder die Aktionen neu sequenziert.

[InstallExecuteSequence-Tabelle](installexecutesequence-table.md)



| Aktion                 | Bedingung | Sequenz |
|------------------------|-----------|----------|
| Installinitialisieren      |           | 1000     |
| MyCustomAction         |           | 1010     |
| RemoveExistingProducts |           | 1020     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



