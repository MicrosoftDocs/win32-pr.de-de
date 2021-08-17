---
description: Die InstallExecute-Aktion führt ein Skript aus, das alle Vorgänge in der Aktionssequenz seit dem Start der Installation oder der letzten InstallExecute-Aktion oder der InstallExecuteAndroin-Aktion enthält.
ms.assetid: a124e9fb-f9fa-4ed3-8f32-4f1fab392530
title: InstallExecute-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 249a83f283b3abee97fbddf99d755b158678726fbb36c066791e3f87ae718f46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946128"
---
# <a name="installexecute-action"></a>InstallExecute-Aktion

Die InstallExecute-Aktion führt ein Skript aus, das alle Vorgänge in der Aktionssequenz seit dem Start der Installation oder der letzten InstallExecute-Aktion oder [der InstallExecuteAndroin-Aktion](installexecuteagain-action.md)enthält. Die InstallExecute-Aktion aktualisiert das System, ohne die Transaktion zu beenden.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die InstallExecute-Aktion wird zwischen der [InstallInitialize-Aktion](installinitialize-action.md) und der [InstallFinalize-Aktion ausgeführt.](installfinalize-action.md)

## <a name="actiondata-messages"></a>ActionData-Nachrichten

Es sind keine ActionData-Meldungen vorhanden.

## <a name="remarks"></a>Hinweise

Die [InstallExecuteAndroin-Aktion](installexecuteagain-action.md) führt die gleiche Aktion wie die InstallExecute-Aktion aus. Da die Sequenztabellen nur über einen Primärschlüssel , die Action-Spalte, verfügen, kann dieselbe Aktion nicht in einer bestimmten Sequenztabelle wiederholt werden. Es gibt zwei Aktionen, die dasselbe tun: InstallExecute und InstallExecuteAndroin, wenn die Funktionalität von InstallExecute zweimal in der [Tabelle InstallExecuteSequence](installexecutesequence-table.md)benötigt wird. Weitere Informationen finden Sie unter [Verwenden einer Sequenztabelle.](using-a-sequence-table.md)

 

 



