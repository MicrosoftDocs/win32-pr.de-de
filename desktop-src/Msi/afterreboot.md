---
description: Der Installer legt die afterreboot-Eigenschaft nach einem von der ForceReboot-Aktion aufgerufenen Neustart auf 1 fest. Der Installer fügt afterreboot = 1 der Befehlszeile hinzu, die unmittelbar nach dem Neustart ausgeführt wird.
ms.assetid: d8a71d9a-64bf-4a38-9c3b-073c216de7fa
title: Afterreboot (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa891c84e2e8f7bdea5bb90311e9706a37e46e31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370282"
---
# <a name="afterreboot-property"></a><span data-ttu-id="d3e31-104">Afterreboot (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d3e31-104">AFTERREBOOT property</span></span>

<span data-ttu-id="d3e31-105">Der Installer legt die **afterreboot** -Eigenschaft nach einem von der [ForceReboot-Aktion](forcereboot-action.md)aufgerufenen Neustart auf 1 fest.</span><span class="sxs-lookup"><span data-stu-id="d3e31-105">The installer sets the **AFTERREBOOT** property to 1 after a reboot invoked by the [ForceReboot action](forcereboot-action.md).</span></span> <span data-ttu-id="d3e31-106">Der Installer fügt afterreboot = 1 der Befehlszeile hinzu, die unmittelbar nach dem Neustart ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d3e31-106">The installer adds AFTERREBOOT=1 to the command line run immediately after the reboot.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3e31-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3e31-107">Remarks</span></span>

<span data-ttu-id="d3e31-108">Die [ForceReboot-Aktion](forcereboot-action.md) muss immer mit einer Bedingungs Anweisung verwendet werden, damit das Installationsprogramm nur bei Bedarf einen Neustart auslöst.</span><span class="sxs-lookup"><span data-stu-id="d3e31-108">The [ForceReboot action](forcereboot-action.md) must always be used with a conditional statement such that the installer triggers a reboot only when necessary.</span></span> <span data-ttu-id="d3e31-109">Möglicherweise ist ein Neustart erforderlich, wenn eine bestimmte Datei ersetzt oder eine bestimmte Komponente installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d3e31-109">A reboot might be required if a particular file was replaced or a particular component was installed.</span></span> <span data-ttu-id="d3e31-110">Der Fall unterscheidet sich für jedes Produkt, und eine benutzerdefinierte Aktion ist möglicherweise erforderlich, um zu bestimmen, ob ein Neustart erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d3e31-110">The case is different for each product and a custom action might be needed to determine whether a reboot is needed.</span></span> <span data-ttu-id="d3e31-111">Die Bedingung für die ForceReboot-Aktion verwendet in der Regel die Eigenschaft **afterreboot** .</span><span class="sxs-lookup"><span data-stu-id="d3e31-111">The condition on the ForceReboot action commonly makes use of the **AFTERREBOOT** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3e31-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3e31-112">Requirements</span></span>



| <span data-ttu-id="d3e31-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3e31-113">Requirement</span></span> | <span data-ttu-id="d3e31-114">Wert</span><span class="sxs-lookup"><span data-stu-id="d3e31-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3e31-115">Version</span><span class="sxs-lookup"><span data-stu-id="d3e31-115">Version</span></span><br/> | <span data-ttu-id="d3e31-116">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d3e31-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d3e31-117">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d3e31-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d3e31-118">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d3e31-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="d3e31-119">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="d3e31-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d3e31-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3e31-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3e31-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d3e31-121">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="d3e31-122">System Neustarts</span><span class="sxs-lookup"><span data-stu-id="d3e31-122">System Reboots</span></span>](system-reboots.md)
</dt> </dl>

 

 




