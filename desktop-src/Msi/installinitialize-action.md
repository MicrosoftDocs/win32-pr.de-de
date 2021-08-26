---
description: Die Aktion InstallInitialize und installFinalize markieren den Anfang und das Ende einer Sequenz von Aktionen, die das System ändern.
ms.assetid: c2637070-3fd9-422c-9252-cf15045c6485
title: InstallInitialize-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7031ab79bc099ea067fd8d83cb83d8cefd1f36a1e83f696a1ee3b4487b3cac88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996570"
---
# <a name="installinitialize-action"></a>InstallInitialize-Aktion

Die Aktion InstallInitialize und [installFinalize](installfinalize-action.md) markieren den Anfang und das Ende einer Sequenz von Aktionen, die das System ändern.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die InstallInitialize-Aktion muss vor allen Aktionen sequenziert werden, die das System ändern, z. B. die [InstallFiles-Aktion,](installfiles-action.md) die [WriteRegistryValues-Aktion,](writeregistryvalues-action.md) die [SelfRegModules-Aktion](selfregmodules-action.md) und die [ProcessComponents-Aktion.](processcomponents-action.md) Die InstallInitialize-Aktion muss daher vor der [InstallFinalize-Aktion](installfinalize-action.md) und der [InstallExecute-Aktion sequenziert](installexecute-action.md) werden.

[Benutzerdefinierte](custom-actions.md) Aktionen, die das Windows Installer-Paket ändern, z. B. durch Hinzufügen von Zeilen zu einer Tabelle, die installierbare Ressourcen behandelt, z. B. die Tabelle [Registry](registry-table.md) oder [DuplicateFile,](duplicatefile-table.md) müssen vor der InstallInitialize-Aktion sequenziert werden.

## <a name="actiondata-messages"></a>ActionData-Meldungen

Es sind keine ActionData-Meldungen enthalten.

 

 



