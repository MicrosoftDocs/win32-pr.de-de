---
description: Die Aktion installinitialisieren und InstallFinalize markieren den Anfang und das Ende einer Sequenz von Aktionen, durch die das System geändert wird.
ms.assetid: c2637070-3fd9-422c-9252-cf15045c6485
title: InstallInitialize-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d500779ed018905edfc5347d85d21cc40e6175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752201"
---
# <a name="installinitialize-action"></a>InstallInitialize-Aktion

Die Aktion installinitialisieren und [InstallFinalize](installfinalize-action.md) markieren den Anfang und das Ende einer Sequenz von Aktionen, durch die das System geändert wird.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die InstallInitialize-Aktion muss vor den Aktionen, mit denen das System geändert wird, sequenziert werden, wie z. b. die Aktion [InstallFiles](installfiles-action.md) , die Aktion " [schreiteregistryvalues](writeregistryvalues-action.md) ", die [SelfRegModules](selfregmodules-action.md) -Aktion und die [processcomponents](processcomponents-action.md) -Aktion. Daher muss die InstallInitialize-Aktion vor der [InstallFinalize](installfinalize-action.md) -Aktion und der [InstallExecute](installexecute-action.md) -Aktion sequenziert werden.

[Benutzerdefinierte Aktionen](custom-actions.md) , mit denen das Windows Installer Paket geändert wird, z. b. durch das Hinzufügen von Zeilen zu einer Tabelle, in der installierbare Ressourcen behandelt werden, z. b. die [Registrierungs](registry-table.md) Tabelle oder die [duplicatefile](duplicatefile-table.md) -Tabelle, müssen vor der InstallInitialize

## <a name="actiondata-messages"></a>Aktions Daten Meldungen

Es sind keine Aktions Daten Meldungen vorhanden.

 

 



