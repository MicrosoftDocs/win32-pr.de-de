---
description: ICE84 überprüft die AdvtExecuteSequence-Tabelle, die AdminExecuteSequence-Tabelle und die InstallExecuteSequence-Tabelle, um zu überprüfen, ob die folgenden Standard Aktionen nicht mit Bedingungen im Bedingungs Feld festgelegt wurden.
ms.assetid: 0d1bbf4b-ffab-409e-a292-891dfa823433
title: ICE84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8960f53f5a01e9bec95a02bb3241487aa31aaae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347778"
---
# <a name="ice84"></a>ICE84

ICE84 überprüft die [AdvtExecuteSequence-Tabelle](advtexecutesequence-table.md), die [AdminExecuteSequence-Tabelle](adminexecutesequence-table.md)und die [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) , um zu überprüfen, ob die folgenden [Standard Aktionen](standard-actions.md) nicht mit Bedingungen im Bedingungs Feld festgelegt wurden.

-   [Costinitialize-Aktion](costinitialize-action.md)
-   [Costfinalize-Aktion](costfinalize-action.md)
-   [Filecost-Aktion](filecost-action.md)
-   [InstallValidate-Aktion](installvalidate-action.md)
-   [InstallInitialize-Aktion](installinitialize-action.md)
-   [InstallFinalize-Aktion](installfinalize-action.md)
-   [Processcomponents-Aktion](processcomponents-action.md)
-   [Publishfeatures-Aktion](publishfeatures-action.md)
-   [Publishproduct-Aktion](publishproduct-action.md)
-   [Registerproduct-Aktion](registerproduct-action.md)
-   [Unpublishfeatures-Aktion](unpublishfeatures-action.md)

Wenn Bedingungen gefunden werden, gibt ICE84 eine Warnung aus.

## <a name="result"></a>Ergebnis

ICE84 gibt die folgende Warnung aus.



| ICE84-Fehler                                                             | BESCHREIBUNG                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| Die \[ \] in der% s-Tabelle gefundene Aktion ' 1 ' ist eine erforderliche Aktion mit einer Bedingung. | Eine erforderliche Aktion wurde mit einer Bedingung erstellt. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



