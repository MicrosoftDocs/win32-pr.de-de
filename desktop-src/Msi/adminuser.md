---
description: Der Installer legt diese Eigenschaft fest, wenn der Benutzer über Administratorrechte verfügt.
ms.assetid: 2e7fd269-bd5f-40b7-b123-36b9c783a917
title: AdminUser (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11651f0d7103edabbcf7b40087db91f999b1a5b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367854"
---
# <a name="adminuser-property"></a><span data-ttu-id="f6af1-103">AdminUser (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f6af1-103">AdminUser property</span></span>

<span data-ttu-id="f6af1-104">Der Installer legt diese Eigenschaft fest, wenn der Benutzer über Administratorrechte verfügt.</span><span class="sxs-lookup"><span data-stu-id="f6af1-104">The installer sets this property if the user has administrator privileges.</span></span>

<span data-ttu-id="f6af1-105">**Windows Server 2008 und Windows Vista:** Die **AdminUser** -Eigenschaft ist identisch mit der Eigenschaft [**privilegiert**](privileged.md) .</span><span class="sxs-lookup"><span data-stu-id="f6af1-105">**Windows Server 2008 and Windows Vista:** The **AdminUser** property is the same as the [**Privileged**](privileged.md) property.</span></span> <span data-ttu-id="f6af1-106">Autoren sollten die **privilegierte** Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="f6af1-106">Authors should used the **Privileged** property.</span></span> <span data-ttu-id="f6af1-107">Der Installer legt diese Eigenschaften fest, wenn der Benutzer über Administratorrechte verfügt, wenn die Anwendung von einem Systemadministrator zugewiesen wurde, oder wenn die Benutzer-und Computer Richtlinien alwaysinstallerhöhten auf true festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="f6af1-107">The installer sets these properties if the user has administrator privileges, if the application has been assigned by a system administrator, or if both the user and machine policies AlwaysInstallElevated are set to true.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6af1-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f6af1-108">Remarks</span></span>

<span data-ttu-id="f6af1-109">Die Unterschiede zwischen diesen Eigenschaften können in einigen Legacy Paketen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6af1-109">The differences between these properties may have been used in some legacy packages.</span></span> <span data-ttu-id="f6af1-110">Beispielsweise kann " **AdminUser** " anstelle von " [**privilegiert**](privileged.md) " in bedingten Anweisungen verwendet werden, da das Installationsprogramm nur die **AdminUser** -Eigenschaft festlegt, wenn der Benutzer ein Administrator ist.</span><span class="sxs-lookup"><span data-stu-id="f6af1-110">For example, **AdminUser** may have been used instead of [**Privileged**](privileged.md) in conditional statements, because the installer only sets the **AdminUser** property if the user is an administrator.</span></span> <span data-ttu-id="f6af1-111">Der Installer legt die **privilegierte** Eigenschaft fest, wenn der Benutzer ein Administrator ist, oder wenn die Richtlinie dem Benutzer ermöglicht, mit erhöhten Rechten zu installieren.</span><span class="sxs-lookup"><span data-stu-id="f6af1-111">The installer sets the **Privileged** property if the user is an administrator, or if policy enables the user to install with elevated privileges.</span></span>

<span data-ttu-id="f6af1-112">**Windows Server 2008 und Windows Vista:** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f6af1-112">**Windows Server 2008 and Windows Vista:** Not supported.</span></span> <span data-ttu-id="f6af1-113">Die Berechtigungen " [**privilegiert**](privileged.md) " und " **AdminUser** " sind identisch.</span><span class="sxs-lookup"><span data-stu-id="f6af1-113">The [**Privileged**](privileged.md) and **AdminUser** are the same.</span></span> <span data-ttu-id="f6af1-114">Pakete, die unterschiedliche **privilegierte** Eigenschaften und **AdminUser** -Eigenschaften erfordern, können den Unterschied wiederherstellen, indem Sie die Eigenschaft [**msiuserealadminerkennungs**](msiuserealadmindetection.md) festlegen.</span><span class="sxs-lookup"><span data-stu-id="f6af1-114">Packages that require distinct **Privileged** and **AdminUser** properties can restore the difference by setting the [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md) property.</span></span>

<span data-ttu-id="f6af1-115">Weitere Informationen finden Sie unter [Installieren eines Pakets mit erhöhten Rechten für eine nicht-Administrator-](installing-a-package-with-elevated-privileges-for-a-non-admin.md)und [**privilegierte**](privileged.md) Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f6af1-115">For more information, see [Installing a Package with Elevated Privileges for a Non-Admin](installing-a-package-with-elevated-privileges-for-a-non-admin.md), and [**Privileged**](privileged.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6af1-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6af1-116">Requirements</span></span>



| <span data-ttu-id="f6af1-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f6af1-117">Requirement</span></span> | <span data-ttu-id="f6af1-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f6af1-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6af1-119">Version</span><span class="sxs-lookup"><span data-stu-id="f6af1-119">Version</span></span><br/> | <span data-ttu-id="f6af1-120">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f6af1-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f6af1-121">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Vista oder Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="f6af1-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Vista or Windows Server 2008.</span></span> <span data-ttu-id="f6af1-122">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f6af1-122">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="f6af1-123">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="f6af1-123">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f6af1-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6af1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6af1-125">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f6af1-125">Properties</span></span>](properties.md)
</dt> </dl>

 

 




