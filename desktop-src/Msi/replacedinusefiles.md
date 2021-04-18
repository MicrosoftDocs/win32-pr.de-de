---
description: Die replacedinusefiles-Eigenschaft wird festgelegt, wenn das Installationsprogramm eine Datei schreibt, die in Gebrauch ist.
ms.assetid: cef7d36e-c721-4d47-beaa-53e6749334b6
title: Replacedinusefiles (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d6826f1db2ec1844234cf32f1137e43c89528c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365696"
---
# <a name="replacedinusefiles-property"></a><span data-ttu-id="c49e0-103">Replacedinusefiles (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c49e0-103">ReplacedInUseFiles property</span></span>

<span data-ttu-id="c49e0-104">Die **replacedinusefiles** -Eigenschaft wird festgelegt, wenn das Installationsprogramm eine Datei schreibt, die in Gebrauch ist.</span><span class="sxs-lookup"><span data-stu-id="c49e0-104">The **ReplacedInUseFiles** property is set if the installer writes over a file that is being held in use.</span></span> <span data-ttu-id="c49e0-105">Diese Eigenschaft wird von benutzerdefinierten Aktionen verwendet, um zu erkennen, dass ein Neustart erforderlich ist, um die Installation abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c49e0-105">This property is used by custom actions to detect that a reboot is required to complete the installation.</span></span>

<span data-ttu-id="c49e0-106">Wird während der [InstallExecute](installexecute-action.md) -und [InstallFinalize](installfinalize-action.md) -Aktionen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c49e0-106">Set during the [InstallExecute](installexecute-action.md) and [InstallFinalize](installfinalize-action.md) actions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c49e0-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c49e0-107">Requirements</span></span>



| <span data-ttu-id="c49e0-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c49e0-108">Requirement</span></span> | <span data-ttu-id="c49e0-109">Wert</span><span class="sxs-lookup"><span data-stu-id="c49e0-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c49e0-110">Version</span><span class="sxs-lookup"><span data-stu-id="c49e0-110">Version</span></span><br/> | <span data-ttu-id="c49e0-111">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c49e0-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c49e0-112">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c49e0-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c49e0-113">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c49e0-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c49e0-114">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="c49e0-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c49e0-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c49e0-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c49e0-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c49e0-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 




