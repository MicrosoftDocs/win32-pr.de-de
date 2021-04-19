---
description: Die costingcomplete-Eigenschaft gibt an, ob das Installationsprogramm den Speicherplatz auf dem Datenträger abgeschlossen hat
ms.assetid: 23688f1e-3ae8-4cd9-824c-36077cc7838f
title: Costingcomplete (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 817b4d38b71e377bbf9b51588efef33e4fd6e93e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352924"
---
# <a name="costingcomplete-property"></a><span data-ttu-id="5ede2-103">Costingcomplete (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5ede2-103">CostingComplete property</span></span>

<span data-ttu-id="5ede2-104">Die **costingcomplete** -Eigenschaft gibt an, ob das Installationsprogramm den Speicherplatz auf dem Datenträger abgeschlossen hat</span><span class="sxs-lookup"><span data-stu-id="5ede2-104">The **CostingComplete** property indicates whether the installer has completed disk space costing.</span></span> <span data-ttu-id="5ede2-105">Diese Eigenschaft kann verwendet werden, um ein Dialogfeld zu erstellen, das ausgelöst wird, wenn die Kosten nicht abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="5ede2-105">This property can be used to author a dialog box triggered if costing has not been completed.</span></span> <span data-ttu-id="5ede2-106">Die-Eigenschaft wird während der Kosten für den Speicherplatz dynamisch festgelegt, und wird auf 1 festgelegt, sobald die Kosten erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="5ede2-106">The property is set dynamically during disk space costing and is set to 1 as soon as the costing is complete.</span></span> <span data-ttu-id="5ede2-107">Diese Eigenschaft wird von der [costfinalize-Aktion](costfinalize-action.md)auf 0 (null) initialisiert.</span><span class="sxs-lookup"><span data-stu-id="5ede2-107">This property is initialized to 0 by the [CostFinalize action](costfinalize-action.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5ede2-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ede2-108">Remarks</span></span>

<span data-ttu-id="5ede2-109">Ein Beispiel für das Erstellen eines "Bitte warten.</span><span class="sxs-lookup"><span data-stu-id="5ede2-109">For an example of how to author a "Please wait .</span></span> <span data-ttu-id="5ede2-110">.</span><span class="sxs-lookup"><span data-stu-id="5ede2-110">.</span></span> <span data-ttu-id="5ede2-111">.</span><span class="sxs-lookup"><span data-stu-id="5ede2-111">.</span></span> <span data-ttu-id="5ede2-112">"das Dialogfeld, das während der Speicherplatz Kosten angezeigt wird, finden Sie im Abschnitt [Erstellen einer bedingten" Bitte warten... " ](authoring-a-conditional-please-wait-------message-box.md)Meldungs Feld.</span><span class="sxs-lookup"><span data-stu-id="5ede2-112">" dialog box that pops up during disk space costing, see the section [Authoring a Conditional "Please wait . . ." Message Box](authoring-a-conditional-please-wait-------message-box.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5ede2-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ede2-113">Requirements</span></span>



| <span data-ttu-id="5ede2-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ede2-114">Requirement</span></span> | <span data-ttu-id="5ede2-115">Wert</span><span class="sxs-lookup"><span data-stu-id="5ede2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ede2-116">Version</span><span class="sxs-lookup"><span data-stu-id="5ede2-116">Version</span></span><br/> | <span data-ttu-id="5ede2-117">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5ede2-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5ede2-118">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5ede2-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5ede2-119">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5ede2-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="5ede2-120">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="5ede2-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5ede2-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ede2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ede2-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5ede2-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




