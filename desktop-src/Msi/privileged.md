---
description: Mit der Eigenschaft "privilegiert" wird angegeben, ob die Installation im Kontext erhöhter Berechtigungen erfolgt.
ms.assetid: 483ab73a-3ff7-4111-a6b5-eac990d85bd7
title: Privilegierte Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d28a7079e7ab12b9832447172f1b3b2c8650a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370332"
---
# <a name="privileged-property"></a><span data-ttu-id="01876-103">Privilegierte Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="01876-103">Privileged property</span></span>

<span data-ttu-id="01876-104">Mit der Eigenschaft " **privilegiert** " wird angegeben, ob die Installation im Kontext erhöhter Berechtigungen erfolgt.</span><span class="sxs-lookup"><span data-stu-id="01876-104">The **Privileged** property indicates whether the installation is performed in the context of elevated privileges.</span></span> <span data-ttu-id="01876-105">Der Installer legt diese Eigenschaft fest, wenn der Benutzer über Administratorrechte verfügt, wenn die Anwendung von einem Systemadministrator zugewiesen wurde, oder wenn die Benutzer-und Computer Richtlinien alwaysinstallerhöhten auf true festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="01876-105">The installer sets this property if the user has administrator privileges, if the application has been assigned by a system administrator, or if both the user and machine policies AlwaysInstallElevated are set to true.</span></span>

## <a name="default-value"></a><span data-ttu-id="01876-106">Standardwert</span><span class="sxs-lookup"><span data-stu-id="01876-106">Default Value</span></span>

<span data-ttu-id="01876-107">Diese Eigenschaft wird vom Installationsprogramm nicht festgelegt, wenn der Benutzer nicht mit erhöhten Rechten installieren darf.</span><span class="sxs-lookup"><span data-stu-id="01876-107">The installer does not set this property if the user is not allowed to install with elevated privileges.</span></span>

## <a name="remarks"></a><span data-ttu-id="01876-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01876-108">Remarks</span></span>

<span data-ttu-id="01876-109">Entwickler von Installer-Paketen können mithilfe der Eigenschaft **privilegiert** die Installation abhängig von der System Richtlinie, dem Benutzer, der Administrator ist, oder der Zuweisung durch einen Administrator machen.</span><span class="sxs-lookup"><span data-stu-id="01876-109">Developers of installer packages can use the **Privileged** property to make the installation conditional upon system policy, the user being an administrator, or assignment by an administrator.</span></span>

<span data-ttu-id="01876-110">Bei der Ausführung unter Windows Vista sind die Berechtigungen " **privilegiert** " und " [**AdminUser**](adminuser.md) " identisch.</span><span class="sxs-lookup"><span data-stu-id="01876-110">When running on Windows Vista, the **Privileged** and [**AdminUser**](adminuser.md) are the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="01876-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01876-111">Requirements</span></span>



| <span data-ttu-id="01876-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01876-112">Requirement</span></span> | <span data-ttu-id="01876-113">Wert</span><span class="sxs-lookup"><span data-stu-id="01876-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01876-114">Version</span><span class="sxs-lookup"><span data-stu-id="01876-114">Version</span></span><br/> | <span data-ttu-id="01876-115">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="01876-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="01876-116">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="01876-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="01876-117">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="01876-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="01876-118">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="01876-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="01876-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01876-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01876-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="01876-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




