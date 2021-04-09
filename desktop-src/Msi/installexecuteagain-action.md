---
description: Mit der InstallExecuteAgain-Aktion wird ein Skript ausgeführt, das alle Vorgänge in der Aktions Sequenz seit dem Start der Installation oder der letzten InstallExecuteAgain-Aktion oder der letzten InstallExecute-Aktion enthält.
ms.assetid: 60ff844f-f8bf-4a55-9523-ba526dac9e29
title: InstallExecuteAgain-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57865c3eec28afa454e440e056d1ee964528f889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958852"
---
# <a name="installexecuteagain-action"></a>InstallExecuteAgain-Aktion

Mit der InstallExecuteAgain-Aktion wird ein Skript ausgeführt, das alle Vorgänge in der Aktions Sequenz seit dem Start der Installation oder der letzten InstallExecuteAgain-Aktion oder der letzten [InstallExecute](installexecute-action.md)-Aktion enthält. Die InstallExecute-Aktion aktualisiert das System, ohne die Transaktion zu beenden. InstallExecuteAgain führt den gleichen Vorgang wie die [InstallExecute-Aktion](installexecute-action.md) aus, sollte jedoch nur nach InstallExecute verwendet werden.

InstallExecuteAgain sollte immer so festgelegt werden, dass Sie nicht während des Entfernens ausgeführt wird. Weitere Informationen finden [Sie unter Verwenden von Eigenschaften in Bedingungs Anweisungen](using-properties-in-conditional-statements.md).

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die InstallExecute-Aktion erfolgt zwischen der Aktion [InstallInitialize](installinitialize-action.md) und der [InstallFinalize](installfinalize-action.md)-Aktion.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen

Es sind keine Aktions Daten Meldungen vorhanden.

## <a name="remarks"></a>Bemerkungen

Die InstallExecuteAgain-Aktion bewirkt dasselbe wie die [InstallExecute-Aktion](installexecute-action.md). Da die Sequenz Tabellen nur über einen Primärschlüssel verfügen, kann die Aktionsspalte nicht in einer bestimmten Sequenz Tabelle wiederholt werden. Es gibt zwei Aktionen, die dasselbe tun, InstallExecute und InstallExecuteAgain, in Fällen, in denen die Funktionalität von InstallExecute zweimal in der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md)benötigt wird. Weitere Informationen finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).

 

 



