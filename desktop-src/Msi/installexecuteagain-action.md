---
description: Die InstallExecuteExecuteExecin-Aktion führt ein Skript aus, das alle Vorgänge in der Aktionssequenz seit dem Start der Installation, der letzten InstallExecuteExecuteExecin-Aktion oder der letzten InstallExecute-Aktion enthält.
ms.assetid: 60ff844f-f8bf-4a55-9523-ba526dac9e29
title: InstallExecuteExecin-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2133fcf7acee7027337864eb8e33b6b297499e96979155f066538edbd6fec00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893980"
---
# <a name="installexecuteagain-action"></a>InstallExecuteExecin-Aktion

Die InstallExecuteExecuteExecin-Aktion führt ein Skript aus, das alle Vorgänge in der Aktionssequenz seit dem Start der Installation, der letzten InstallExecuteExecuteExecin-Aktion oder der letzten [InstallExecute-Aktion enthält.](installexecute-action.md) Die Aktion InstallExecute aktualisiert das System, ohne die Transaktion zu beenden. InstallExecuteExecuteExecin führt denselben Vorgang wie die [InstallExecute-Aktion](installexecute-action.md) aus, sollte aber nur nach InstallExecute verwendet werden.

InstallExecuteExecuteExecin sollte immer so festgelegt werden, dass es während des Entfernens nicht ausgeführt wird. Weitere Informationen finden Sie unter [Verwenden von Eigenschaften in bedingten Anweisungen.](using-properties-in-conditional-statements.md)

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die InstallExecute-Aktion liegt zwischen der [InstallInitialize-Aktion](installinitialize-action.md) und der [InstallFinalize-Aktion.](installfinalize-action.md)

## <a name="actiondata-messages"></a>ActionData-Meldungen

Es sind keine ActionData-Meldungen enthalten.

## <a name="remarks"></a>Hinweise

Die InstallExecuteExecuteExecin-Aktion führt dasselbe wie die [InstallExecute-Aktion aus.](installexecute-action.md) Da die Sequenztabellen nur über einen Primärschlüssel verfügen, die Spalte Aktion, kann dieselbe Aktion nicht in einer bestimmten Sequenztabelle wiederholt werden. Es gibt zwei Aktionen, die dasselbe tun: InstallExecute und InstallExecuteExecuteExecin, für Fälle, in denen die Funktionalität von InstallExecute zweimal in der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md)benötigt wird. Weitere Informationen finden Sie unter [Verwenden einer Sequenztabelle.](using-a-sequence-table.md)

 

 



