---
description: Das Installationsprogramm legt den Wert der msirestartmanagersessionkey-Eigenschaft auf den Sitzungsschlüssel für die Restart Manager-Sitzung fest.
ms.assetid: efbf11f2-38ab-4509-aa01-23fa8cfdaa60
title: Msirestartmanagersessionkey (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489095e0af617c7ae403811f0eab800c5502e3bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365567"
---
# <a name="msirestartmanagersessionkey-property"></a><span data-ttu-id="3cde4-103">Msirestartmanagersessionkey (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3cde4-103">MsiRestartManagerSessionKey property</span></span>

<span data-ttu-id="3cde4-104">Das Installationsprogramm legt den Wert der **msirestartmanagersessionkey** -Eigenschaft auf den Sitzungsschlüssel für die [Restart Manager](../rstmgr/restart-manager-portal.md) -Sitzung fest.</span><span class="sxs-lookup"><span data-stu-id="3cde4-104">The installer sets the value of the **MsiRestartManagerSessionKey** property to the session key for the [Restart Manager](../rstmgr/restart-manager-portal.md) session.</span></span> <span data-ttu-id="3cde4-105">Benutzerdefinierte Aktionen können den Sitzungsschlüssel verwenden, um der Sitzung für den [Neustart-Manager](../rstmgr/restart-manager-portal.md) beizutreten.</span><span class="sxs-lookup"><span data-stu-id="3cde4-105">Custom actions can use the session key to join the [Restart Manager](../rstmgr/restart-manager-portal.md) session.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cde4-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3cde4-106">Remarks</span></span>

<span data-ttu-id="3cde4-107">Der Installer legt den Wert der Eigenschaft " **msirestartmanagersessionkey** " bei der Initialisierung fest und löscht dann den Wert während der [InstallValidate](installvalidate-action.md) -Aktion.</span><span class="sxs-lookup"><span data-stu-id="3cde4-107">The installer sets the value of the **MsiRestartManagerSessionKey** property at initialization, and then clears the value during the [InstallValidate](installvalidate-action.md) action.</span></span> <span data-ttu-id="3cde4-108">Benutzerdefinierte Aktionen, für die der Wert der **msirestartmanagersessionkey** -Eigenschaft erforderlich ist, müssen vor der InstallValidate-Aktion in der Aktions Sequenz liegen.</span><span class="sxs-lookup"><span data-stu-id="3cde4-108">Custom actions that need the value of the **MsiRestartManagerSessionKey** property must be come before the InstallValidate action in the action sequence.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cde4-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3cde4-109">Requirements</span></span>



| <span data-ttu-id="3cde4-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3cde4-110">Requirement</span></span> | <span data-ttu-id="3cde4-111">Wert</span><span class="sxs-lookup"><span data-stu-id="3cde4-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cde4-112">Version</span><span class="sxs-lookup"><span data-stu-id="3cde4-112">Version</span></span><br/> | <span data-ttu-id="3cde4-113">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3cde4-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3cde4-114">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3cde4-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3cde4-115">Informationen zu den minimalen Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="3cde4-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3cde4-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3cde4-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cde4-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3cde4-117">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="3cde4-118">Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3cde4-118">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
