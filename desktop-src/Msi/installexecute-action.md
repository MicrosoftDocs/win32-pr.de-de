---
description: Mit der InstallExecute-Aktion wird ein Skript ausgeführt, das alle Vorgänge in der Aktions Sequenz seit dem Start der Installation oder der letzten InstallExecute-Aktion oder InstallExecuteAgain-Aktion enthält.
ms.assetid: a124e9fb-f9fa-4ed3-8f32-4f1fab392530
title: InstallExecute-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76417a4f188849f9a5af5a90b08e1f4bb5977afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128380"
---
# <a name="installexecute-action"></a>InstallExecute-Aktion

Mit der InstallExecute-Aktion wird ein Skript ausgeführt, das alle Vorgänge in der Aktions Sequenz seit dem Start der Installation oder der letzten InstallExecute-Aktion oder [InstallExecuteAgain](installexecuteagain-action.md)-Aktion enthält. Die InstallExecute-Aktion aktualisiert das System, ohne die Transaktion zu beenden.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die InstallExecute-Aktion erfolgt zwischen der Aktion [InstallInitialize](installinitialize-action.md) und der [InstallFinalize](installfinalize-action.md)-Aktion.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen

Es sind keine Aktions Daten Meldungen vorhanden.

## <a name="remarks"></a>Bemerkungen

Die [InstallExecuteAgain-Aktion](installexecuteagain-action.md) bewirkt dasselbe wie die InstallExecute-Aktion. Da die Sequenz Tabellen nur über einen Primärschlüssel verfügen, kann die Aktionsspalte nicht in einer bestimmten Sequenz Tabelle wiederholt werden. Es gibt zwei Aktionen, die dasselbe tun, InstallExecute und InstallExecuteAgain, in Fällen, in denen die Funktionalität von InstallExecute zweimal in der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md)benötigt wird. Weitere Informationen finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).

 

 



