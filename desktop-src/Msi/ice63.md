---
description: ICE63 überprüft die ordnungsgemäße Sequenzierung der RemoveExistingProducts-Aktion.
ms.assetid: 4dd67bb0-c08a-4a44-b687-0394a3afc2c4
title: ICE63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f0de847a3b79c87b8ddc7dbaf3be64f88b9ef34df80d92737b6d9005ffdad24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142494"
---
# <a name="ice63"></a>ICE63

ICE63 überprüft die ordnungsgemäße Sequenzierung der [RemoveExistingProducts-Aktion.](removeexistingproducts-action.md) Die Aktion RemoveExistingProducts kann platziert werden:

1.  Zwischen InstallValidate und InstallInitialize
2.  Unmittelbar nach InstallInitialize oder nach InstallInitialize, wenn die Aktionen zwischen InstallInitialize und RemoveExistingProducts keine Skriptaktionen generieren.
3.  Unmittelbar nach InstallExecute oder InstallExecuteAndroin und vor InstallFinalize (die gleiche Einschränkung wie oben gilt).
4.  Nach InstallFinalize.

Wenn eine von ICE63 gemeldete Warnung oder ein Fehler nicht behoben wird, führt dies zu einem Fehler beim Upgrade.

## <a name="result"></a>Ergebnis

ICE63 gibt eine Warnung oder einen Fehler aus, wenn die Sequenzierung der Aktion RemoveExistingProducts nicht richtig ist.

## <a name="example"></a>Beispiel

ICE63 meldet den folgenden Fehler für das gezeigte Beispiel.

``` syntax
WARNING: Some action falls between InstallInitialize and RemoveExistingProducts.
```

Die Aktion "MyCustomAction" tritt zwischen InstallInitialize und RemoveExistingProducts auf. Wenn MyCustomAction Aktionen im Skript generiert, führt dies zu Problemen bei der Installation.

Um diesen Fehler zu beheben, überprüfen Sie, ob MyCustomAction keine Skriptaktionen generiert, oder stellen Sie die Aktionen erneut aus.

[InstallExecuteSequence-Tabelle](installexecutesequence-table.md)



| Aktion                 | Bedingung | Sequenz |
|------------------------|-----------|----------|
| InstallInitialize      |           | 1000     |
| MyCustomAction         |           | 1010     |
| RemoveExistingProducts |           | 1020     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



