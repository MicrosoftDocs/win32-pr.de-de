---
description: Die msideploymentcompliance-Eigenschaft kann festgelegt werden, um für das Installationsprogramm anzugeben, dass das Paket erstellt und getestet wurde, um die Benutzerkontensteuerung (User Account Control, UAC) in Windows Vista einzuhalten.
ms.assetid: 7ee0dc56-bb9d-4a6e-aa3e-ae4c83f583d7
title: Msideploymentcompliance (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a965b7dce941a3d651e2f9f32e3d8f4993ded33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359619"
---
# <a name="msideploymentcompliant-property"></a><span data-ttu-id="ac9f9-103">Msideploymentcompliance (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ac9f9-103">MSIDEPLOYMENTCOMPLIANT property</span></span>

<span data-ttu-id="ac9f9-104">Die **msideploymentcompliance** -Eigenschaft kann festgelegt werden, um für das Installationsprogramm anzugeben, dass das Paket erstellt und getestet wurde, um die [*Benutzerkontensteuerung (User Account Control*](u-gly.md) , UAC) in Windows Vista einzuhalten.</span><span class="sxs-lookup"><span data-stu-id="ac9f9-104">The **MSIDEPLOYMENTCOMPLIANT** property can be set to indicate to the installer that the package has been authored and tested to comply with [*User Account Control*](u-gly.md) (UAC) in Windows Vista.</span></span> <span data-ttu-id="ac9f9-105">Wenn diese Eigenschaft nicht festgelegt ist, bestimmt das Installationsprogramm, ob das Paket mit der UAC unter Windows Vista kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="ac9f9-105">If this property is not set, the installer will determine whether the package complies with UAC on Windows Vista.</span></span>

<span data-ttu-id="ac9f9-106">Weitere Informationen zu UAC und Windows Installer finden Sie unter [Verwenden von Windows Installer mit UAC](using-windows-installer-with-uac.md) und [Richtlinien für Pakete](guidelines-for-packages.md).</span><span class="sxs-lookup"><span data-stu-id="ac9f9-106">For more information about UAC and Windows Installer, see [Using Windows Installer with UAC](using-windows-installer-with-uac.md) and [Guidelines for Packages](guidelines-for-packages.md).</span></span>

<span data-ttu-id="ac9f9-107">**Windows Installer 3,1, Windows Installer 3,0 und Windows Installer 2,0:** Diese Eigenschaft wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ac9f9-107">**Windows Installer 3.1, Windows Installer 3.0 and Windows Installer 2.0:** This property is ignored.</span></span> <span data-ttu-id="ac9f9-108">Diese Eigenschaft wird nur von Windows Installer 4,0 in Windows Vista verwendet.</span><span class="sxs-lookup"><span data-stu-id="ac9f9-108">This property is only used by Windows Installer 4.0 in Windows Vista.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac9f9-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac9f9-109">Requirements</span></span>



| <span data-ttu-id="ac9f9-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac9f9-110">Requirement</span></span> | <span data-ttu-id="ac9f9-111">Wert</span><span class="sxs-lookup"><span data-stu-id="ac9f9-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac9f9-112">Version</span><span class="sxs-lookup"><span data-stu-id="ac9f9-112">Version</span></span><br/> | <span data-ttu-id="ac9f9-113">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ac9f9-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ac9f9-114">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ac9f9-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ac9f9-115">Informationen zu den minimalen Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="ac9f9-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ac9f9-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac9f9-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac9f9-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ac9f9-117">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="ac9f9-118">Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ac9f9-118">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




