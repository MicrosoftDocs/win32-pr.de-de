---
description: Die msirestartmanagercontrol-Eigenschaft gibt an, ob das Windows Installer Paket die Funktion Restart Manager oder FilesInUse verwendet.
ms.assetid: fefff18b-892a-440e-9f57-d23aeb99af74
title: Msirestartmanagercontrol (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d965f1b814ce2969a6253ba227672c54769791
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359703"
---
# <a name="msirestartmanagercontrol-property"></a><span data-ttu-id="2f82a-103">Msirestartmanagercontrol (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2f82a-103">MSIRESTARTMANAGERCONTROL property</span></span>

<span data-ttu-id="2f82a-104">Die **msirestartmanagercontrol** -Eigenschaft gibt an, ob das Windows Installer Paket die Funktion [Restart Manager](../rstmgr/restart-manager-portal.md) oder [FilesInUse](filesinuse-dialog.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="2f82a-104">The **MSIRESTARTMANAGERCONTROL** Property specifies whether the Windows Installer package uses the [Restart Manager](../rstmgr/restart-manager-portal.md) or [FilesInUse Dialog](filesinuse-dialog.md) functionality.</span></span>

## <a name="value"></a><span data-ttu-id="2f82a-105">Wert</span><span class="sxs-lookup"><span data-stu-id="2f82a-105">Value</span></span>



| <span data-ttu-id="2f82a-106">Wert</span><span class="sxs-lookup"><span data-stu-id="2f82a-106">Value</span></span>                                                                                        | <span data-ttu-id="2f82a-107">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2f82a-107">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2f82a-108"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2f82a-108"><dt>0</dt></span></span> </dl>                 | <span data-ttu-id="2f82a-109">Dies ist der Standardwert, wenn die-Eigenschaft nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2f82a-109">This is the default value if the property is not set.</span></span> <span data-ttu-id="2f82a-110">Windows Installer versucht immer, den [Neustart-Manager](../rstmgr/restart-manager-portal.md) unter Windows Vista zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="2f82a-110">Windows Installer always attempts to use the [Restart Manager](../rstmgr/restart-manager-portal.md) on Windows Vista.</span></span><br/>                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="2f82a-111"><dt>Ier</dt></span><span class="sxs-lookup"><span data-stu-id="2f82a-111"><dt>"Disable"</dt></span></span> </dl>         | <span data-ttu-id="2f82a-112">Deaktiviert die Interaktion des Pakets mit dem [Neustart-Manager](../rstmgr/restart-manager-portal.md).</span><span class="sxs-lookup"><span data-stu-id="2f82a-112">Disables interaction of the package with the [Restart Manager](../rstmgr/restart-manager-portal.md).</span></span> <span data-ttu-id="2f82a-113">Windows Installer verwendet das [FilesInUse-Dialog](filesinuse-dialog.md)Feld.</span><span class="sxs-lookup"><span data-stu-id="2f82a-113">Windows Installer uses the [FilesInUse Dialog](filesinuse-dialog.md).</span></span> <br/>                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="2f82a-114"><dt>"Disableshutdown"</dt></span><span class="sxs-lookup"><span data-stu-id="2f82a-114"><dt>"DisableShutdown"</dt></span></span> </dl> | <span data-ttu-id="2f82a-115">Windows Installer verwendet das [FilesInUse-Dialog](filesinuse-dialog.md)Feld.</span><span class="sxs-lookup"><span data-stu-id="2f82a-115">Windows Installer uses the [FilesInUse Dialog](filesinuse-dialog.md).</span></span> <span data-ttu-id="2f82a-116">Mit dieser Einstellung werden Versuche durch den [Neustart-Manager](../rstmgr/restart-manager-portal.md) deaktiviert, um beim Installieren eines Windows Installer Pakets, das noch nicht für die Verwendung des Neustart-Managers erstellt wurde, Neustarts zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="2f82a-116">This setting disables attempts by the [Restart Manager](../rstmgr/restart-manager-portal.md) to mitigate restarts when installing a Windows Installer package that has not been authored to use the Restart Manager.</span></span> <span data-ttu-id="2f82a-117">Der Installer verwendet weiterhin den Neustart-Manager, um die von Anwendungen verwendeten Dateien zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="2f82a-117">The installer still uses the Restart Manager to detect files in use by applications.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="2f82a-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f82a-118">Remarks</span></span>

<span data-ttu-id="2f82a-119">Die **msirestartmanagercontrol** -Eigenschaft wird ignoriert, wenn der [Neustart-Manager](../rstmgr/restart-manager-portal.md) nicht verfügbar oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2f82a-119">The **MSIRESTARTMANAGERCONTROL** Property is ignored if the [Restart Manager](../rstmgr/restart-manager-portal.md) is unavailable or disabled.</span></span>

<span data-ttu-id="2f82a-120">Der Wert dieser Eigenschaft kann mithilfe von Anpassungs Transformationen oder Upgrades geändert werden.</span><span class="sxs-lookup"><span data-stu-id="2f82a-120">The value of this property can be modified using customization transforms or upgrades.</span></span> <span data-ttu-id="2f82a-121">Das Ändern des Werts dieser Eigenschaft von benutzerdefinierten Aktionen hat keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="2f82a-121">Changing the value of this property from custom actions has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f82a-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f82a-122">Requirements</span></span>



| <span data-ttu-id="2f82a-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f82a-123">Requirement</span></span> | <span data-ttu-id="2f82a-124">Wert</span><span class="sxs-lookup"><span data-stu-id="2f82a-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f82a-125">Version</span><span class="sxs-lookup"><span data-stu-id="2f82a-125">Version</span></span><br/> | <span data-ttu-id="2f82a-126">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2f82a-126">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2f82a-127">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2f82a-127">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2f82a-128">Informationen zu den minimalen Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="2f82a-128">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2f82a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f82a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f82a-130">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2f82a-130">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="2f82a-131">Disableautomaticapplicationshutdown</span><span class="sxs-lookup"><span data-stu-id="2f82a-131">DisableAutomaticApplicationShutdown</span></span>](disableautomaticapplicationshutdown.md)
</dt> <dt>

[<span data-ttu-id="2f82a-132">Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2f82a-132">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
