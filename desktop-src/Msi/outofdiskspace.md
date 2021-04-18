---
description: Der Installer legt die ouesfdiskspace-Eigenschaft auf true fest, wenn ein beliebiges Volume, das ein Ziel der aktuellen Installation ist, nicht über genügend Speicherplatz verfügt, um die Installation zu ermöglichen.
ms.assetid: fb1e3be7-12dd-4036-b657-b91b480fca4a
title: Ouesf Disk Space (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3a438661e931547b0025f2bf85a2ccc03899f5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364951"
---
# <a name="outofdiskspace-property"></a><span data-ttu-id="baece-103">Ouesf Disk Space (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="baece-103">OutOfDiskSpace property</span></span>

<span data-ttu-id="baece-104">Der Installer legt die **ouesfdiskspace** -Eigenschaft auf true fest, wenn ein beliebiges Volume, das ein Ziel der aktuellen Installation ist, nicht über genügend Speicherplatz verfügt, um die Installation zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="baece-104">The installer sets the **OutOfDiskSpace** property to TRUE if any volume that is a target of the current installation has insufficient disk space to accommodate the installation.</span></span> <span data-ttu-id="baece-105">Wenn alle Volumes über genügend Speicherplatz verfügen, ist der Wert false.</span><span class="sxs-lookup"><span data-stu-id="baece-105">If all volumes have sufficient space, the value is FALSE.</span></span> <span data-ttu-id="baece-106">Auswahl Auflösungs Aktionen verwenden diesen Wert, um eine Installation abzubrechen und ein Dialogfeld zu generieren.</span><span class="sxs-lookup"><span data-stu-id="baece-106">Selection resolution actions use this value to cancel an installation and generate a dialog box.</span></span>

<span data-ttu-id="baece-107">Diese Eigenschaft ist jederzeit gültig, nachdem die [Aktion "costfinalize](costfinalize-action.md) " ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="baece-107">This property is valid at any time after the [CostFinalize action](costfinalize-action.md) is executed.</span></span> <span data-ttu-id="baece-108">Der Status der [**ouesfnorbdiskspace**](outofnorbdiskspace.md) -Eigenschaft wird bei jeder Neuberechnung der Gesamt Installationskosten dynamisch aktualisiert (z. b. wenn der Installationsstatus eines beliebigen Features über das [Auswahl](selection-dialog.md) Dialogfeld geändert wird).</span><span class="sxs-lookup"><span data-stu-id="baece-108">The [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) property status is dynamically updated any time the total installation cost is recalculated (for example, any time the installation state of any feature is changed through the [Selection](selection-dialog.md) dialog).</span></span>

## <a name="remarks"></a><span data-ttu-id="baece-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="baece-109">Remarks</span></span>

<span data-ttu-id="baece-110">Alle Dialogfelder, die sich auf die **oudefdiskspace** -Eigenschaft stützen, um zu bestimmen, ob ein Dialogfeld angezeigt werden soll, müssen das Dialogfeld Format des Dialog Felds " [trackdiskspace](trackdiskspace-dialog-style-bit.md) " für das Dialogfeld festlegen, um den Speicherplatz</span><span class="sxs-lookup"><span data-stu-id="baece-110">Any dialog relying on the **OutOfDiskSpace** property to determine whether to bring up a dialog must set the [TrackDiskSpace Dialog Style Bit](trackdiskspace-dialog-style-bit.md) for the dialog to dynamically update space on the target volumes.</span></span>

## <a name="requirements"></a><span data-ttu-id="baece-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="baece-111">Requirements</span></span>



| <span data-ttu-id="baece-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="baece-112">Requirement</span></span> | <span data-ttu-id="baece-113">Wert</span><span class="sxs-lookup"><span data-stu-id="baece-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="baece-114">Version</span><span class="sxs-lookup"><span data-stu-id="baece-114">Version</span></span><br/> | <span data-ttu-id="baece-115">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="baece-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="baece-116">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="baece-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="baece-117">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="baece-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="baece-118">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="baece-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="baece-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="baece-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baece-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="baece-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




