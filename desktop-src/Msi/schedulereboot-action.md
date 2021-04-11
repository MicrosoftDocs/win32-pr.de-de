---
description: Fügen Sie die Aktion schedulereboot in die Aktions Sequenz ein, um den Benutzer zur Eingabe eines Neustarts des Systems am Ende der Installation aufzufordern. Verwenden Sie die ForceReboot-Aktion, um während der Installation zur Eingabe eines Neustarts aufzufordern.
ms.assetid: 36f24f57-f1f0-4eca-9b6d-1b25fb73fa96
title: Schedulereboot-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460e3f25283c233fac80b25edd91d4bd102de435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865196"
---
# <a name="schedulereboot-action"></a><span data-ttu-id="e2087-104">Schedulereboot-Aktion</span><span class="sxs-lookup"><span data-stu-id="e2087-104">ScheduleReboot Action</span></span>

<span data-ttu-id="e2087-105">Fügen Sie die Aktion schedulereboot in die Aktions Sequenz ein, um den Benutzer zur Eingabe eines Neustarts des Systems am Ende der Installation aufzufordern.</span><span class="sxs-lookup"><span data-stu-id="e2087-105">Insert the ScheduleReboot action into the action sequence to prompt the user for a restart of the system at the end of the installation.</span></span> <span data-ttu-id="e2087-106">Verwenden Sie die [ForceReboot-Aktion](forcereboot-action.md) , um während der Installation zur Eingabe eines Neustarts aufzufordern.</span><span class="sxs-lookup"><span data-stu-id="e2087-106">Use the [ForceReboot action](forcereboot-action.md) to prompt for a restart during installation.</span></span>

<span data-ttu-id="e2087-107">Wenn die Installation über eine Benutzeroberfläche verfügt, zeigt das Installationsprogramm am Ende der Installation ein Meldungs Feld und eine Schaltfläche an, um zu Fragen, ob der Benutzer das System neu starten möchte.</span><span class="sxs-lookup"><span data-stu-id="e2087-107">If the installation has a user interface, the installer displays a message box and button at the end of installation asking whether the user wants to restart the system.</span></span> <span data-ttu-id="e2087-108">Der Benutzer muss auf diese Eingabeaufforderung Antworten, bevor die Installation abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="e2087-108">The user must respond to this prompt before completing installation.</span></span> <span data-ttu-id="e2087-109">Wenn die Installation über keine Benutzeroberfläche verfügt, wird das System am Ende automatisch neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="e2087-109">If the installation has no user interface, the system automatically restarts at the end.</span></span>

<span data-ttu-id="e2087-110">Wenn das Installationsprogramm feststellt, dass ein Neustart erforderlich ist, wird der Benutzer automatisch aufgefordert, am Ende der Installation neu zu starten, unabhängig davon, ob in der Sequenz ForceReboot-oder schedulereboot-Aktionen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="e2087-110">If the installer determines that a restart is necessary it automatically prompts the user to restart at the end of the installation, whether or not there are any ForceReboot or ScheduleReboot actions in the sequence.</span></span> <span data-ttu-id="e2087-111">Beispielsweise fordert das Installationsprogramm automatisch einen Neustart an, wenn es alle Dateien ersetzen muss, die während der Installation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e2087-111">For example, the installer automatically prompts for a restart if it needs to replace any files that are in use during installation.</span></span>

<span data-ttu-id="e2087-112">Sie können bestimmte Eingabe Aufforderungen für Neustarts unterdrücken, indem Sie die Eigenschaft [**Neustart**](reboot.md) festlegen.</span><span class="sxs-lookup"><span data-stu-id="e2087-112">You can suppress certain prompts for restarts by setting the [**REBOOT**](reboot.md) property.</span></span>

<span data-ttu-id="e2087-113">Wenn die Windows Installer während einer [Installation mit mehreren Paketen](multiple-package-installations.md)auf die Aktion [ForceReboot](forcereboot-action.md) oder schedulereboot stößt, wird das Installationsprogramm beendet und führt ein Rollback der Installation aus.</span><span class="sxs-lookup"><span data-stu-id="e2087-113">If the Windows Installer encounters the [ForceReboot](forcereboot-action.md) or ScheduleReboot action during a [multiple-package installation](multiple-package-installations.md), the installer will stop and roll back the installation.</span></span> <span data-ttu-id="e2087-114">Andere Pakete, die zur Installation mit mehreren Paketen gehören und keine ForceReboot-oder schedulereboot-Aktion enthalten, können installiert werden.</span><span class="sxs-lookup"><span data-stu-id="e2087-114">Other packages belonging to the multiple-package installation, that do not contain a ForceReboot or ScheduleReboot action, can be installed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="e2087-115">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="e2087-115">Sequence Restrictions</span></span>

<span data-ttu-id="e2087-116">Es gibt keine Sequenz Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="e2087-116">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="e2087-117">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="e2087-117">ActionData Messages</span></span>

<span data-ttu-id="e2087-118">Es sind keine Aktions Daten Meldungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e2087-118">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2087-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2087-119">Remarks</span></span>

<span data-ttu-id="e2087-120">Diese Aktion kann z. b. verwendet werden, um das Installationsprogramm zu zwingen, nach der Installation von Treibern, die einen Neustart erfordern, nach einem Neustart zu Fragen.</span><span class="sxs-lookup"><span data-stu-id="e2087-120">For example, this action can be used to force the installer to prompt for a restart after installing drivers that require a restart.</span></span> <span data-ttu-id="e2087-121">Wenn das Installationsprogramm versucht, Dateien zu ersetzen, die verwendet werden, wird der Benutzer automatisch zum Neustart aufgefordert, auch wenn schedulereboot nicht verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e2087-121">If the installer attempts to replace files that are in use, it automatically prompts the user to restart even if ScheduleReboot has not been used.</span></span>

<span data-ttu-id="e2087-122">Die schedulereboot-Aktion wird in der Regel am Ende der Sequenz abgelegt, aber Sie kann an einem beliebigen Punkt in der Sequenz eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="e2087-122">The ScheduleReboot action is typically placed at the end of the sequence, but it can be inserted at any point in the sequence.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2087-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e2087-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2087-124">System Neustarts</span><span class="sxs-lookup"><span data-stu-id="e2087-124">System Reboots</span></span>](system-reboots.md)
</dt> </dl>

 

 



