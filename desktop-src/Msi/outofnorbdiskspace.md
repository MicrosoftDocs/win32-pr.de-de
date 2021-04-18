---
description: Der Installer legt die ouesfnorbdiskspace-Eigenschaft auf true fest, wenn ein beliebiges Volume, das ein Ziel der Installation ist, nicht über genügend Speicherplatz verfügt, um die Installation zu ermöglichen.
ms.assetid: 910d6c1d-38d3-4680-b256-2bf30689ce11
title: Ouesbnorbdiskspace (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fa9cdd7c1d444e141103ca148344dd26ea1d2a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360933"
---
# <a name="outofnorbdiskspace-property"></a><span data-ttu-id="de9fd-103">Ouesbnorbdiskspace (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="de9fd-103">OutOfNoRbDiskSpace property</span></span>

<span data-ttu-id="de9fd-104">Der Installer legt die **ouesfnorbdiskspace** -Eigenschaft auf true fest, wenn ein beliebiges Volume, das ein Ziel der Installation ist, nicht über genügend Speicherplatz verfügt, um die Installation zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="de9fd-104">The installer sets the **OutOfNoRbDiskSpace** property to True if any volume that is a target of the installation has insufficient disk space to accommodate the installation.</span></span> <span data-ttu-id="de9fd-105">In diesem Fall wird die **ouesfnorbdiskspace** -Eigenschaft auf true festgelegt, auch wenn das Rollback deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="de9fd-105">In this case, the **OutOfNoRbDiskSpace** property is set to True even if rollback has been disabled.</span></span> <span data-ttu-id="de9fd-106">Wenn alle Volumes über genügend Speicherplatz verfügen, ist der Wert false.</span><span class="sxs-lookup"><span data-stu-id="de9fd-106">If all volumes have sufficient space, the value is False.</span></span>

<span data-ttu-id="de9fd-107">Ein Entwickler eines Installationspakets kann die Situation behandeln, in der die [**outofdiskspace**](outofdiskspace.md) -Eigenschaft "true" ist, und die **outofnorbdiskspace** -Eigenschaft "false" ist, indem eine Benutzeroberfläche erstellt wird, die dem Benutzer die Möglichkeit gibt, das Rollback zu deaktivieren und die Installation fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="de9fd-107">A developer of an installation package can handle the situation when the [**OutOfDiskSpace**](outofdiskspace.md) property is True and the **OutOfNoRbDiskSpace** property is False by authoring a user interface that presents the user with an option to disable rollback and continue the installation.</span></span> <span data-ttu-id="de9fd-108">Informationen zur bedingten Anzeige eines Dialog Felds finden Sie unter [ControlEvent Overview](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="de9fd-108">For information about conditionally displaying a dialog box, see [ControlEvent Overview](controlevent-overview.md).</span></span> <span data-ttu-id="de9fd-109">Weitere Informationen zum Deaktivieren des Rollbacks finden Sie unter [enablerollback ControlEvent](enablerollback-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="de9fd-109">For information about disabling rollback, see [EnableRollback ControlEvent](enablerollback-controlevent.md).</span></span>

<span data-ttu-id="de9fd-110">Die **ouesfnorbdiskspace** -Eigenschaft ist jederzeit gültig, nachdem die [Aktion "costfinalize](costfinalize-action.md) " ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="de9fd-110">The **OutOfNoRbDiskSpace** property is valid at any time after the [CostFinalize action](costfinalize-action.md) has been executed.</span></span> <span data-ttu-id="de9fd-111">Der Status der **ouesfnorbdiskspace** -Eigenschaft wird bei jeder Neuberechnung der Gesamt Installationskosten dynamisch aktualisiert (z. b. wenn der Installationsstatus eines beliebigen Features über das [Auswahl Dialogfeld](selection-dialog.md)geändert wird).</span><span class="sxs-lookup"><span data-stu-id="de9fd-111">The **OutOfNoRbDiskSpace** property status is dynamically updated any time the total installation cost is recalculated (for example, any time the installation state of any feature is changed through the [Selection dialog](selection-dialog.md)).</span></span> <span data-ttu-id="de9fd-112">Auswahl Auflösungs Aktionen verwenden diesen Wert, um eine Installation abzubrechen und ein Dialogfeld zu generieren.</span><span class="sxs-lookup"><span data-stu-id="de9fd-112">Selection resolution actions use this value to cancel an installation and generate a dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="de9fd-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de9fd-113">Requirements</span></span>



| <span data-ttu-id="de9fd-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de9fd-114">Requirement</span></span> | <span data-ttu-id="de9fd-115">Wert</span><span class="sxs-lookup"><span data-stu-id="de9fd-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de9fd-116">Version</span><span class="sxs-lookup"><span data-stu-id="de9fd-116">Version</span></span><br/> | <span data-ttu-id="de9fd-117">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="de9fd-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="de9fd-118">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="de9fd-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="de9fd-119">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="de9fd-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="de9fd-120">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="de9fd-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="de9fd-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de9fd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de9fd-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="de9fd-122">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="de9fd-123">ControlEvent (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="de9fd-123">ControlEvent Overview</span></span>](controlevent-overview.md)
</dt> <dt>

[<span data-ttu-id="de9fd-124">**Ouesf Disk Space (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="de9fd-124">**OutOfDiskSpace property**</span></span>](outofdiskspace.md)
</dt> <dt>

[<span data-ttu-id="de9fd-125">Enablerollback-ControlEvent</span><span class="sxs-lookup"><span data-stu-id="de9fd-125">EnableRollback ControlEvent</span></span>](enablerollback-controlevent.md)
</dt> <dt>

[<span data-ttu-id="de9fd-126">Costfinalize-Aktion</span><span class="sxs-lookup"><span data-stu-id="de9fd-126">CostFinalize action</span></span>](costfinalize-action.md)
</dt> <dt>

[<span data-ttu-id="de9fd-127">Auswahl Dialogfeld</span><span class="sxs-lookup"><span data-stu-id="de9fd-127">Selection dialog</span></span>](selection-dialog.md)
</dt> </dl>

 

 




