---
description: Mit der ForceReboot-Aktion wird der Benutzer zur Eingabe eines Neustarts des Systems während der Installation aufgefordert.
ms.assetid: e1bcdd59-8cbc-46f7-b908-c8cbc2ea0539
title: ForceReboot-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 807bab474f1faacfbc7684797b7a0b7b74f354d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350313"
---
# <a name="forcereboot-action"></a><span data-ttu-id="a9c6b-103">ForceReboot-Aktion</span><span class="sxs-lookup"><span data-stu-id="a9c6b-103">ForceReboot Action</span></span>

<span data-ttu-id="a9c6b-104">Mit der ForceReboot-Aktion wird der Benutzer zur Eingabe eines Neustarts des Systems während der Installation aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="a9c6b-104">The ForceReboot action prompts the user for a restart of the system during the installation.</span></span> <span data-ttu-id="a9c6b-105">Die ForceReboot-Aktion unterscheidet sich von der [schedulereboot](schedulereboot-action.md) -Aktion darin, dass die schedulereboot-Aktion verwendet wird, um eine Aufforderung zum Neustart am Ende der Installation zu planen.</span><span class="sxs-lookup"><span data-stu-id="a9c6b-105">The ForceReboot action is different from the [ScheduleReboot action](schedulereboot-action.md) in that the ScheduleReboot action is used to schedule a prompt to restart at the end of the installation.</span></span>

<span data-ttu-id="a9c6b-106">Wenn die Installation über eine Benutzeroberfläche verfügt, zeigt das Installationsprogramm bei jeder ForceReboot-Aktion ein Dialogfeld an, das den Benutzer auffordert, das System neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="a9c6b-106">If the installation has a user interface, the installer displays a dialog box at each ForceReboot action which prompts the user to restart the system.</span></span> <span data-ttu-id="a9c6b-107">Der Benutzer muss auf diese Eingabeaufforderung Antworten, bevor die Installation fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="a9c6b-107">The user must respond to this prompt before continuing with the installation.</span></span> <span data-ttu-id="a9c6b-108">Wenn die Installation über keine Benutzeroberfläche verfügt, wird das System bei der ForceReboot-Aktion automatisch neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="a9c6b-108">If the installation has no user interface, the system automatically restarts at the ForceReboot action.</span></span>

<span data-ttu-id="a9c6b-109">Wenn das Installationsprogramm feststellt, dass ein Neustart erforderlich ist, wird der Benutzer automatisch aufgefordert, am Ende der Installation neu zu starten, unabhängig davon, ob ForceReboot-oder schedulereboot-Aktionen in der Sequenz vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a9c6b-109">If the installer determines that a restart is necessary, it automatically prompts the user to restart at the end of the installation, whether or not there are any ForceReboot or ScheduleReboot actions in the sequence.</span></span> <span data-ttu-id="a9c6b-110">Beispielsweise wird das Installationsprogramm automatisch zur Eingabe eines Neustarts aufgefordert, wenn alle während der Installation verwendeten Dateien ersetzt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="a9c6b-110">For example, the installer automatically prompts for a restart if it needs to replace any files used during the installation.</span></span>

<span data-ttu-id="a9c6b-111">Unterdrücken Sie bestimmte Neustart Aufforderungen, indem Sie die Eigenschaft [**Neustart**](reboot.md) festlegen.</span><span class="sxs-lookup"><span data-stu-id="a9c6b-111">Suppress certain restart prompts by setting the [**REBOOT**](reboot.md) property.</span></span>

<span data-ttu-id="a9c6b-112">Wenn die Windows Installer während einer [Installation mit mehreren Paketen](multiple-package-installations.md)auf die Aktion ForceReboot oder [schedulereboot](schedulereboot-action.md) stößt, wird das Installationsprogramm beendet und führt ein Rollback der Installation aus.</span><span class="sxs-lookup"><span data-stu-id="a9c6b-112">If the Windows Installer encounters the ForceReboot or [ScheduleReboot](schedulereboot-action.md) action during a [multiple-package installation](multiple-package-installations.md), the installer will stop and roll back the installation.</span></span> <span data-ttu-id="a9c6b-113">Andere Pakete, die zur Installation mit mehreren Paketen gehören und keine ForceReboot-oder schedulereboot-Aktion enthalten, können installiert werden.</span><span class="sxs-lookup"><span data-stu-id="a9c6b-113">Other packages belonging to the multiple-package installation, that do not contain a ForceReboot or ScheduleReboot action, can be installed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="a9c6b-114">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="a9c6b-114">Sequence Restrictions</span></span>

<span data-ttu-id="a9c6b-115">Die folgenden Aktionen treten in der Regel als Gruppe in der Aktions Sequenz auf.</span><span class="sxs-lookup"><span data-stu-id="a9c6b-115">The following actions commonly occur together as a group in the action sequence.</span></span> <span data-ttu-id="a9c6b-116">Es wird empfohlen, dass die ForceReboot-Aktion nach dieser Gruppe geplant wird.</span><span class="sxs-lookup"><span data-stu-id="a9c6b-116">It is recommended that the ForceReboot action be scheduled to come after this group.</span></span> <span data-ttu-id="a9c6b-117">Wenn die ForceReboot-Aktion vor der [registerproduct-Aktion](registerproduct-action.md)geplant wird, benötigt das Installationsprogramm erneut die Quelle des Installationspakets nach dem Neustart.</span><span class="sxs-lookup"><span data-stu-id="a9c6b-117">If the ForceReboot action is scheduled before the [RegisterProduct action](registerproduct-action.md), the installer again requires the source of the installation package after the restart.</span></span> <span data-ttu-id="a9c6b-118">Daher folgt die bevorzugte Sequenz für ForceReboot unmittelbar auf diese Aktions Sequenz.</span><span class="sxs-lookup"><span data-stu-id="a9c6b-118">Therefore, the preferred sequence for ForceReboot is immediately following this action sequence.</span></span>

-   [<span data-ttu-id="a9c6b-119">Register Product</span><span class="sxs-lookup"><span data-stu-id="a9c6b-119">RegisterProduct</span></span>](registerproduct-action.md)
-   [<span data-ttu-id="a9c6b-120">Register User</span><span class="sxs-lookup"><span data-stu-id="a9c6b-120">RegisterUser</span></span>](registeruser-action.md)
-   [<span data-ttu-id="a9c6b-121">Publishproduct</span><span class="sxs-lookup"><span data-stu-id="a9c6b-121">PublishProduct</span></span>](publishproduct-action.md)
-   [<span data-ttu-id="a9c6b-122">Publishfeatures</span><span class="sxs-lookup"><span data-stu-id="a9c6b-122">PublishFeatures</span></span>](publishfeatures-action.md)
-   [<span data-ttu-id="a9c6b-123">"Kreateshortcuts"</span><span class="sxs-lookup"><span data-stu-id="a9c6b-123">CreateShortcuts</span></span>](createshortcuts-action.md)
-   [<span data-ttu-id="a9c6b-124">Registermimeinfo</span><span class="sxs-lookup"><span data-stu-id="a9c6b-124">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)
-   [<span data-ttu-id="a9c6b-125">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="a9c6b-125">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="a9c6b-126">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="a9c6b-126">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="a9c6b-127">Registerprogidinfo</span><span class="sxs-lookup"><span data-stu-id="a9c6b-127">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)

<span data-ttu-id="a9c6b-128">Die ForceReboot-Aktion muss in der Aktions Sequenz der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md)zwischen [InstallInitialize](installinitialize-action.md) und [InstallFinalize](installfinalize-action.md) erfolgen.</span><span class="sxs-lookup"><span data-stu-id="a9c6b-128">The ForceReboot action must come between [InstallInitialize](installinitialize-action.md) and [InstallFinalize](installfinalize-action.md) in the action sequence of the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="a9c6b-129">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="a9c6b-129">ActionData Messages</span></span>

<span data-ttu-id="a9c6b-130">Es sind keine Aktions Daten Meldungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a9c6b-130">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9c6b-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9c6b-131">Remarks</span></span>

<span data-ttu-id="a9c6b-132">Die ForceReboot-Aktion muss immer mit einer Bedingungs Anweisung verwendet werden, damit das Installationsprogramm einen Neustart nur bei Bedarf auslöst.</span><span class="sxs-lookup"><span data-stu-id="a9c6b-132">The ForceReboot action must always be used with a conditional statement such that the installer triggers a restart only when necessary.</span></span> <span data-ttu-id="a9c6b-133">Beispielsweise kann ein Neustart nur erforderlich sein, wenn eine bestimmte Datei ersetzt oder eine bestimmte Komponente installiert ist.</span><span class="sxs-lookup"><span data-stu-id="a9c6b-133">For example, a restart may only be required if a particular file is replaced or a particular component is installed.</span></span> <span data-ttu-id="a9c6b-134">Jede Produktinstallation ist eindeutig, und eine benutzerdefinierte Aktion ist möglicherweise erforderlich, um zu bestimmen, ob ein Neustart erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a9c6b-134">Each product installation is unique and a custom action may be required to determine whether a restart is needed.</span></span> <span data-ttu-id="a9c6b-135">Die Bedingung für die ForceReboot-Aktion verwendet in der Regel die Eigenschaft [**afterreboot**](afterreboot.md) .</span><span class="sxs-lookup"><span data-stu-id="a9c6b-135">The condition on the ForceReboot action commonly makes use of the [**AFTERREBOOT**](afterreboot.md) property.</span></span>

<span data-ttu-id="a9c6b-136">ForceReboot führt System Vorgänge aus, die von vorherigen Aktionen generiert wurden, bevor die Aufforderung zum Neustart oder Neustarten angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="a9c6b-136">ForceReboot runs system operations generated by any previous actions before prompting for a restart or restarting.</span></span> <span data-ttu-id="a9c6b-137">Beispielsweise werden die von " [InstallFiles](installfiles-action.md) " und " [schreiteregistryvalues](writeregistryvalues-action.md) " generierten System Vorgänge vor einem Neustart ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a9c6b-137">For example, the system operations generated by [InstallFiles](installfiles-action.md) and [WriteRegistryValues](writeregistryvalues-action.md) are run before a restart.</span></span>

<span data-ttu-id="a9c6b-138">Mit der ForceReboot-Aktion wird ein Registrierungsschlüssel geschrieben, der bewirkt, dass das Installationsprogramm nach einem Neustart gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="a9c6b-138">The ForceReboot action writes a registry key that causes the installer to start after restarting.</span></span> <span data-ttu-id="a9c6b-139">Der Speicherort dieses Schlüssels ist **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**.</span><span class="sxs-lookup"><span data-stu-id="a9c6b-139">The location of this key is **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\RunOnce**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9c6b-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a9c6b-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9c6b-141">System Neustarts</span><span class="sxs-lookup"><span data-stu-id="a9c6b-141">System Reboots</span></span>](system-reboots.md)
</dt> </dl>

 

 



