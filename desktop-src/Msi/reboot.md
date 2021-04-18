---
description: Die Reboot-Eigenschaft unterdrückt bestimmte Aufforderungen für einen Neustart des Systems.
ms.assetid: d88752cd-f59d-4214-b5b5-ce126500aa4e
title: Reboot-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d94b08a04f3e95d873f6fc233185ce623cafc25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371599"
---
# <a name="reboot-property"></a><span data-ttu-id="ebf30-103">Reboot-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ebf30-103">REBOOT property</span></span>

<span data-ttu-id="ebf30-104">Die **Reboot** -Eigenschaft unterdrückt bestimmte Aufforderungen für einen Neustart des Systems.</span><span class="sxs-lookup"><span data-stu-id="ebf30-104">The **REBOOT** property suppresses certain prompts for a restart of the system.</span></span> <span data-ttu-id="ebf30-105">Ein Administrator verwendet diese Eigenschaft in der Regel mit einer Reihe von Installationen, um mehrere Produkte gleichzeitig mit nur einem Neustart am Ende zu installieren.</span><span class="sxs-lookup"><span data-stu-id="ebf30-105">An administrator typically uses this property with a series of installations to install several products at the same time with only one restart at the end.</span></span> <span data-ttu-id="ebf30-106">Weitere Informationen finden Sie unter [System Neustarts](system-reboots.md).</span><span class="sxs-lookup"><span data-stu-id="ebf30-106">For more information, see [System Reboots](system-reboots.md).</span></span>

<span data-ttu-id="ebf30-107">Die Aktionen [ForceReboot](forcereboot-action.md) und [schedulereboot](schedulereboot-action.md) informieren das Installationsprogramm darüber, dass der Benutzer aufgefordert wird, das System neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="ebf30-107">The [ForceReboot](forcereboot-action.md) and [ScheduleReboot](schedulereboot-action.md) actions inform the installer to prompt the user to restart the system.</span></span> <span data-ttu-id="ebf30-108">Das Installationsprogramm kann auch feststellen, dass ein Neustart erforderlich ist, unabhängig davon, ob ForceReboot-oder schedulereboot-Aktionen in der Sequenz vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="ebf30-108">The installer can also determine that a restart is necessary whether there are any ForceReboot or ScheduleReboot actions in the sequence.</span></span> <span data-ttu-id="ebf30-109">Beispielsweise fordert das Installationsprogramm automatisch einen Neustart an, wenn die während der Installation verwendeten Dateien ersetzt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="ebf30-109">For example, the installer automatically prompts for a restart if it needs to replace any files in use during the installation.</span></span>

<span data-ttu-id="ebf30-110">Sie können bestimmte Eingabe Aufforderungen für Neustarts unterdrücken, indem Sie die Eigenschaft **Neustart** wie folgt festlegen.</span><span class="sxs-lookup"><span data-stu-id="ebf30-110">You can suppress certain prompts for restarts by setting the **REBOOT** property as follows.</span></span>



| <span data-ttu-id="ebf30-111">Neustart Wert</span><span class="sxs-lookup"><span data-stu-id="ebf30-111">REBOOT value</span></span>   | <span data-ttu-id="ebf30-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ebf30-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebf30-113">Force</span><span class="sxs-lookup"><span data-stu-id="ebf30-113">Force</span></span>          | <span data-ttu-id="ebf30-114">Sie sollten am Ende der Installation immer zum Neustart aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="ebf30-114">Always prompt for a restart at the end of the installation.</span></span> <span data-ttu-id="ebf30-115">Die Benutzeroberfläche fordert den Benutzer immer auf, eine Option zum Neustart am Ende zu starten.</span><span class="sxs-lookup"><span data-stu-id="ebf30-115">The UI always prompts the user with an option to restart at the end.</span></span> <span data-ttu-id="ebf30-116">Wenn keine Benutzeroberfläche vorhanden ist und es sich nicht um eine [Installation mit mehreren Paketen](multiple-package-installations.md)handelt, wird das System am Ende der Installation automatisch neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="ebf30-116">If there is no user interface, and this is not a [multiple-package installation](multiple-package-installations.md), the system automatically restarts at the end of the installation.</span></span> <span data-ttu-id="ebf30-117">Wenn es sich um eine Installation mit mehreren Paketen handelt, gibt es keinen automatischen Neustart des Systems, und das Installationsprogramm gibt einen Fehler bei \_ erfolgreicher \_ Neustarts \_ erforderlich zurück.</span><span class="sxs-lookup"><span data-stu-id="ebf30-117">If this is a multiple-package installation, there is no automatic restart of the system and the installer returns ERROR\_SUCCESS\_REBOOT\_REQUIRED.</span></span> |
| <span data-ttu-id="ebf30-118">Suppress</span><span class="sxs-lookup"><span data-stu-id="ebf30-118">Suppress</span></span>       | <span data-ttu-id="ebf30-119">Unterdrücken von Eingabe Aufforderungen für einen Neustart am Ende der Installation.</span><span class="sxs-lookup"><span data-stu-id="ebf30-119">Suppress prompts for a restart at the end of the installation.</span></span> <span data-ttu-id="ebf30-120">Das Installationsprogramm fordert den Benutzer nach wie vor auf, während der Installation neu zu starten, wenn die [ForceReboot-Aktion](forcereboot-action.md)auftritt.</span><span class="sxs-lookup"><span data-stu-id="ebf30-120">The installer still prompts the user with an option to restart during the installation whenever it encounters the [ForceReboot action](forcereboot-action.md).</span></span> <span data-ttu-id="ebf30-121">Wenn keine Benutzeroberfläche vorhanden ist, wird das System bei jedem ForceReboot automatisch neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="ebf30-121">If there is no user interface, the system automatically restarts at each ForceReboot.</span></span> <span data-ttu-id="ebf30-122">Neustarts am Ende der Installation (z. b. aufgrund des Versuchs, eine verwendete Datei zu installieren) werden unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="ebf30-122">Restarts at the end of the installation (for example, caused by an attempt to install a file in use) are suppressed.</span></span>                                    |
| <span data-ttu-id="ebf30-123">Unterdrücken von reallysup</span><span class="sxs-lookup"><span data-stu-id="ebf30-123">ReallySuppress</span></span> | <span data-ttu-id="ebf30-124">Unterdrücken Sie alle Neustarts und Neustart Aufforderungen, die von ForceReboot während der Installation initiiert wurden.</span><span class="sxs-lookup"><span data-stu-id="ebf30-124">Suppress all restarts and restart prompts initiated by ForceReboot during the installation.</span></span> <span data-ttu-id="ebf30-125">Unterdrücken Sie alle Neustarts, und starten Sie die Eingabe Aufforderungen am Ende der Installation.</span><span class="sxs-lookup"><span data-stu-id="ebf30-125">Suppress all restarts and restart prompts at the end of the installation.</span></span> <span data-ttu-id="ebf30-126">Die Neustart Aufforderung und der Neustart selbst werden unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="ebf30-126">Both the restart prompt and the restart itself are suppressed.</span></span> <span data-ttu-id="ebf30-127">Beispielsweise wird am Ende der Installation ein Neustart durchgeführt, da der Versuch, eine verwendete Datei zu installieren, unterdrückt wird.</span><span class="sxs-lookup"><span data-stu-id="ebf30-127">For example, restarts at the end of the installation, caused by an attempt to install a file in use, are suppressed.</span></span>                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="ebf30-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ebf30-128">Remarks</span></span>

<span data-ttu-id="ebf30-129">Das Installationsprogramm wertet nur das erste Zeichen der **Reboot** -Eigenschaft aus.</span><span class="sxs-lookup"><span data-stu-id="ebf30-129">The installer only evaluates the first character of the **REBOOT** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebf30-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ebf30-130">Requirements</span></span>



| <span data-ttu-id="ebf30-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ebf30-131">Requirement</span></span> | <span data-ttu-id="ebf30-132">Wert</span><span class="sxs-lookup"><span data-stu-id="ebf30-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebf30-133">Version</span><span class="sxs-lookup"><span data-stu-id="ebf30-133">Version</span></span><br/> | <span data-ttu-id="ebf30-134">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ebf30-134">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ebf30-135">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ebf30-135">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ebf30-136">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ebf30-136">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="ebf30-137">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="ebf30-137">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ebf30-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ebf30-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebf30-139">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ebf30-139">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="ebf30-140">**REBOOTPROMPT (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="ebf30-140">**REBOOTPROMPT Property**</span></span>](rebootprompt.md)
</dt> <dt>

[<span data-ttu-id="ebf30-141">System Neustarts</span><span class="sxs-lookup"><span data-stu-id="ebf30-141">System Reboots</span></span>](system-reboots.md)
</dt> </dl>

 

 




