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
# <a name="installinitialize-action"></a><span data-ttu-id="50faf-103">InstallInitialize-Aktion</span><span class="sxs-lookup"><span data-stu-id="50faf-103">InstallInitialize Action</span></span>

<span data-ttu-id="50faf-104">Die Aktion installinitialisieren und [InstallFinalize](installfinalize-action.md) markieren den Anfang und das Ende einer Sequenz von Aktionen, durch die das System geändert wird.</span><span class="sxs-lookup"><span data-stu-id="50faf-104">The InstallInitialize action and [InstallFinalize](installfinalize-action.md) action mark the beginning and end of a sequence of actions that change the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="50faf-105">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="50faf-105">Sequence Restrictions</span></span>

<span data-ttu-id="50faf-106">Die InstallInitialize-Aktion muss vor den Aktionen, mit denen das System geändert wird, sequenziert werden, wie z. b. die Aktion [InstallFiles](installfiles-action.md) , die Aktion " [schreiteregistryvalues](writeregistryvalues-action.md) ", die [SelfRegModules](selfregmodules-action.md) -Aktion und die [processcomponents](processcomponents-action.md) -Aktion.</span><span class="sxs-lookup"><span data-stu-id="50faf-106">The InstallInitialize action must be sequenced before any actions that change the system, such as the [InstallFiles](installfiles-action.md) action, the [WriteRegistryValues](writeregistryvalues-action.md) action, the [SelfRegModules](selfregmodules-action.md) action, and the [ProcessComponents](processcomponents-action.md) action.</span></span> <span data-ttu-id="50faf-107">Daher muss die InstallInitialize-Aktion vor der [InstallFinalize](installfinalize-action.md) -Aktion und der [InstallExecute](installexecute-action.md) -Aktion sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="50faf-107">The InstallInitialize action must therefore be sequenced before the [InstallFinalize](installfinalize-action.md) action and the [InstallExecute](installexecute-action.md) action.</span></span>

<span data-ttu-id="50faf-108">[Benutzerdefinierte Aktionen](custom-actions.md) , mit denen das Windows Installer Paket geändert wird, z. b. durch das Hinzufügen von Zeilen zu einer Tabelle, in der installierbare Ressourcen behandelt werden, z. b. die [Registrierungs](registry-table.md) Tabelle oder die [duplicatefile](duplicatefile-table.md) -Tabelle, müssen vor der InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="50faf-108">[Custom actions](custom-actions.md) that modify the Windows Installer package, for example by adding rows to a table that handles installable resources, such as the [Registry](registry-table.md) table or [DuplicateFile](duplicatefile-table.md) table, must be sequenced before InstallInitialize action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="50faf-109">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="50faf-109">ActionData Messages</span></span>

<span data-ttu-id="50faf-110">Es sind keine Aktions Daten Meldungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="50faf-110">There are no ActionData messages.</span></span>

 

 



