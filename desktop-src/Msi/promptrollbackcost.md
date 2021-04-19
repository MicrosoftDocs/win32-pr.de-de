---
description: Die promptrollbackcost-Eigenschaft gibt die Aktion an, die das Installationsprogramm durchführt, wenn Rollback-Installationsfunktionen aktiviert sind und nicht genügend Speicherplatz vorhanden ist, um die Installation abzuschließen. Die möglichen Werte von promptrollbackcost lauten wie folgt. Valueaktionpdisplay ein Dialogfeld mit der Frage, ob der Vorgang ohne Rollback fortgesetzt werden soll. Ddeaktivieren Sie das Rollback, und fahren Sie fort, ohne den Benutzer Ffail mit der Fehlermeldung "nicht genügend Speicherplatz".
ms.assetid: 6ffd0b3f-79b8-4ce3-a262-4d27ffc5a175
title: Promptrollbackcost (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3801ee894a66ad6e458cbad37252e289f724b9ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356074"
---
# <a name="promptrollbackcost-property"></a><span data-ttu-id="2abfc-103">Promptrollbackcost (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2abfc-103">PROMPTROLLBACKCOST property</span></span>

<span data-ttu-id="2abfc-104">Die **promptrollbackcost** -Eigenschaft gibt die Aktion an, die das Installationsprogramm durchführt, wenn [Rollback-Installations](rollback-installation.md) Funktionen aktiviert sind und nicht genügend Speicherplatz vorhanden ist, um die Installation abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="2abfc-104">The **PROMPTROLLBACKCOST** property specifies the action the installer takes if [rollback installation](rollback-installation.md) capabilities are enabled and there is insufficient disk space to complete the installation.</span></span>

<span data-ttu-id="2abfc-105">Die möglichen Werte von **promptrollbackcost** lauten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="2abfc-105">The possible values of **PROMPTROLLBACKCOST** are as follows.</span></span>



| <span data-ttu-id="2abfc-106">Wert</span><span class="sxs-lookup"><span data-stu-id="2abfc-106">Value</span></span> | <span data-ttu-id="2abfc-107">Aktion</span><span class="sxs-lookup"><span data-stu-id="2abfc-107">Action</span></span>                                                              |
|-------|---------------------------------------------------------------------|
| <span data-ttu-id="2abfc-108">P</span><span class="sxs-lookup"><span data-stu-id="2abfc-108">P</span></span>     | <span data-ttu-id="2abfc-109">Zeigt ein Dialogfeld an, in dem Sie gefragt werden, ob ohne Rollback fortgefahren werden</span><span class="sxs-lookup"><span data-stu-id="2abfc-109">Display a dialog box asking whether to continue without a rollback.</span></span> |
| <span data-ttu-id="2abfc-110">D</span><span class="sxs-lookup"><span data-stu-id="2abfc-110">D</span></span>     | <span data-ttu-id="2abfc-111">Deaktivieren Sie Rollback, und fahren Sie ohne Benutzer ab.</span><span class="sxs-lookup"><span data-stu-id="2abfc-111">Disable rollback and continue without asking user.</span></span>                  |
| <span data-ttu-id="2abfc-112">F</span><span class="sxs-lookup"><span data-stu-id="2abfc-112">F</span></span>     | <span data-ttu-id="2abfc-113">Fehler bei der Eingabeaufforderung für nicht genügend Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="2abfc-113">Fail with the out-of-disk-space error prompt.</span></span>                       |



 

## <a name="remarks"></a><span data-ttu-id="2abfc-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2abfc-114">Remarks</span></span>

<span data-ttu-id="2abfc-115">Wenn die Benutzeroberfläche auf der Ebene "Standard" oder "keine Benutzeroberfläche" ausgeführt wird, verarbeitet das Installationsprogramm automatisch die gesamte Logik für nicht genügend Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="2abfc-115">When the user interface is run at the Basic or no UI level, the installer handles all the out-of-disk-space logic automatically.</span></span>

<span data-ttu-id="2abfc-116">Wenn die Benutzeroberfläche vollständig ausgeführt wird, können dem Benutzer zusätzliche Optionen zugewiesen werden, z. b. eine Eingabeaufforderung, bevor ein Rollback ausgeführt wird, ein Rollback deaktiviert wird oder der Vorgang ohne Rollback fortgesetzt wird, wenn der Datenträger voll ist.</span><span class="sxs-lookup"><span data-stu-id="2abfc-116">When the user interface runs at the Full level, the user can be given additional options, such as prompting before proceeding with a rollback, disabling rollback, or proceeding without rollback when the disk is full.</span></span> <span data-ttu-id="2abfc-117">Der Paket Entwickler muss die Dialogfeld Sequenz verfassen, um dem Benutzer die entsprechenden Optionen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="2abfc-117">It is up to the package developer to author the dialog box sequence to provide the appropriate choices to the user.</span></span> <span data-ttu-id="2abfc-118">Die Elemente, die hierfür verfügbar sind, sind die [enablerollback ControlEvent](enablerollback-controlevent.md)-, [**outo fdiskspace**](outofdiskspace.md) -Eigenschaft, [**ouesfnorbdiskspace**](outofnorbdiskspace.md) -Eigenschaft und die **promptrollbackcost** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="2abfc-118">The elements available to do this are the [EnableRollback ControlEvent](enablerollback-controlevent.md), [**OutOfDiskSpace**](outofdiskspace.md) property, [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) property, and the **PROMPTROLLBACKCOST** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="2abfc-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2abfc-119">Requirements</span></span>



| <span data-ttu-id="2abfc-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2abfc-120">Requirement</span></span> | <span data-ttu-id="2abfc-121">Wert</span><span class="sxs-lookup"><span data-stu-id="2abfc-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2abfc-122">Version</span><span class="sxs-lookup"><span data-stu-id="2abfc-122">Version</span></span><br/> | <span data-ttu-id="2abfc-123">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2abfc-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2abfc-124">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2abfc-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2abfc-125">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2abfc-125">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="2abfc-126">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="2abfc-126">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2abfc-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2abfc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2abfc-128">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2abfc-128">Properties</span></span>](properties.md)
</dt> </dl>

 

 




