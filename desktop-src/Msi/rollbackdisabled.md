---
description: Der Installer legt die rollbackdeaktiviert-Eigenschaft fest, wenn das Rollback deaktiviert wurde.
ms.assetid: 72215b0f-2fc4-49aa-abf8-3206bdfc765f
title: Rollbackdeaktiviert (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f50c8e344ed4291210afb1714ce97d90b590999
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369465"
---
# <a name="rollbackdisabled-property"></a><span data-ttu-id="88054-103">Rollbackdeaktiviert (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="88054-103">RollbackDisabled property</span></span>

<span data-ttu-id="88054-104">Der Installer legt die **rollbackdeaktiviert** -Eigenschaft fest, wenn das Rollback deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="88054-104">The installer sets the **RollbackDisabled** property when rollback has been disabled.</span></span> <span data-ttu-id="88054-105">**Rollbackdeaktiviert** wird von Paket Autoren verwendet, die sicherstellen müssen, dass das Rollback vom Installationsprogramm nicht deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="88054-105">**RollbackDisabled** is used by package authors who need to ensure that the installer has not disabled rollback.</span></span> <span data-ttu-id="88054-106">Die **rollbackdeaktiviert** -Eigenschaft kann in einem bedingten Ausdruck verwendet werden, der die Fortsetzung mit der Installation verweigert, wenn die **rollbackdeaktiviert** -Eigenschaft festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="88054-106">The **RollbackDisabled** property can be used in a conditional expression that effectively refuses to continue with the installation if **RollbackDisabled** property is set.</span></span>

## <a name="default-value"></a><span data-ttu-id="88054-107">Standardwert</span><span class="sxs-lookup"><span data-stu-id="88054-107">Default Value</span></span>

<span data-ttu-id="88054-108">Standardmäßig ist das Rollback aktiviert.</span><span class="sxs-lookup"><span data-stu-id="88054-108">By default, rollback is enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="88054-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88054-109">Remarks</span></span>

<span data-ttu-id="88054-110">Da [Rollback](rollback-custom-actions.md) und [Commit](commit-custom-actions.md) nicht ausgeführt werden, während ein Rollback deaktiviert ist, kann das Installationsprogramm ein Paket, das diese Typen von benutzerdefinierten Aktionen in einer Transaktion verwendet, während der Installation nicht ordnungsgemäß installieren.</span><span class="sxs-lookup"><span data-stu-id="88054-110">Because [rollback](rollback-custom-actions.md) and [commit](commit-custom-actions.md) do not run while rollback is disabled, the installer cannot properly install a package that uses these types of custom actions in a transaction during the installation.</span></span> <span data-ttu-id="88054-111">In diesem Fall sollte der Autor des Pakets eine Bedingung mithilfe von DISABLEROLLBACK einschließen, mit der verhindert wird, dass die Installation fortgesetzt wird, wenn das Rollback deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="88054-111">In this case, the author of the package should include a condition using DisableRollback that prevents the installation from continuing if rollback is disabled.</span></span>

<span data-ttu-id="88054-112">Der Wert der DISABLEROLLBACK-Richtlinie kann von einem Administrator als Teil der Zuweisung von Systemrichtlinien festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="88054-112">The DisableRollback policy value can be set by an administrator as a part of assigning system policy.</span></span> <span data-ttu-id="88054-113">Administratoren wird empfohlen, Rollbacks nur dann zu deaktivieren, wenn dies erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="88054-113">Administrators are advised to not disable rollback unless necessary.</span></span> <span data-ttu-id="88054-114">Weitere Informationen zum Wert der DISABLEROLLBACK-Richtlinie finden Sie unter [System Richtlinie](system-policy.md).</span><span class="sxs-lookup"><span data-stu-id="88054-114">For more information about DisableRollback policy value, see [System Policy](system-policy.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="88054-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88054-115">Requirements</span></span>



| <span data-ttu-id="88054-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88054-116">Requirement</span></span> | <span data-ttu-id="88054-117">Wert</span><span class="sxs-lookup"><span data-stu-id="88054-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88054-118">Version</span><span class="sxs-lookup"><span data-stu-id="88054-118">Version</span></span><br/> | <span data-ttu-id="88054-119">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="88054-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="88054-120">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="88054-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="88054-121">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="88054-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="88054-122">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="88054-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="88054-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88054-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88054-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="88054-124">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="88054-125">Rollback-Installation</span><span class="sxs-lookup"><span data-stu-id="88054-125">Rollback Installation</span></span>](rollback-installation.md)
</dt> <dt>

[<span data-ttu-id="88054-126">Systemrichtlinie</span><span class="sxs-lookup"><span data-stu-id="88054-126">System Policy</span></span>](system-policy.md)
</dt> <dt>

[<span data-ttu-id="88054-127">Zurücksetzen von benutzerdefinierten Aktionen</span><span class="sxs-lookup"><span data-stu-id="88054-127">rollback custom actions</span></span>](rollback-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="88054-128">Commit für benutzerdefinierte Aktionen</span><span class="sxs-lookup"><span data-stu-id="88054-128">commit custom actions</span></span>](commit-custom-actions.md)
</dt> </dl>

 

 




