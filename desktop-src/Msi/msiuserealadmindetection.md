---
description: Legen Sie die msiuserealadminerkennungs-Eigenschaft auf 1 fest, um anzufordern, dass das Installationsprogramm beim Festlegen der AdminUser-Eigenschaft tatsächliche Benutzerinformationen verwendet.
ms.assetid: eb0ed6e3-377b-40f4-afee-346a83e310cf
title: Msiuserealadminerkennungs (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0989174f41bc4b58f89e440dd9852dfde6249a5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369184"
---
# <a name="msiuserealadmindetection-property"></a><span data-ttu-id="ace73-103">Msiuserealadminerkennungs (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ace73-103">MSIUSEREALADMINDETECTION property</span></span>

<span data-ttu-id="ace73-104">Legen Sie die **msiuserealadminerkennungs** -Eigenschaft auf 1 fest, um anzufordern, dass das Installationsprogramm beim Festlegen der [**AdminUser**](adminuser.md) -Eigenschaft tatsächliche Benutzerinformationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ace73-104">Set the **MSIUSEREALADMINDETECTION** property to 1 to request that the installer use actual user information when setting the [**AdminUser**](adminuser.md) property.</span></span> <span data-ttu-id="ace73-105">Bei der Ausführung unter Windows Vista sind die Berechtigungen " [**privilegiert**](privileged.md) " und " **AdminUser** " identisch.</span><span class="sxs-lookup"><span data-stu-id="ace73-105">When running on Windows Vista, the [**Privileged**](privileged.md) and **AdminUser** are the same.</span></span> <span data-ttu-id="ace73-106">Autoren sollten die **privilegierte** Eigenschaft in neuen Paketen verwenden.</span><span class="sxs-lookup"><span data-stu-id="ace73-106">Authors should used the **Privileged** property in new packages.</span></span> <span data-ttu-id="ace73-107">Legacy Pakete, die unterschiedliche **privilegierte** Eigenschaften und **AdminUser** -Eigenschaften erfordern, können den Unterschied wiederherstellen, indem Sie die **msiuserealadminerkennungs** -Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="ace73-107">Legacy packages that require distinct **Privileged** and **AdminUser** properties can restore the difference by setting the **MSIUSEREALADMINDETECTION** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ace73-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ace73-108">Requirements</span></span>



| <span data-ttu-id="ace73-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ace73-109">Requirement</span></span> | <span data-ttu-id="ace73-110">Wert</span><span class="sxs-lookup"><span data-stu-id="ace73-110">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ace73-111">Version</span><span class="sxs-lookup"><span data-stu-id="ace73-111">Version</span></span><br/> | <span data-ttu-id="ace73-112">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ace73-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ace73-113">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ace73-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ace73-114">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="ace73-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ace73-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ace73-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ace73-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ace73-116">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="ace73-117">Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ace73-117">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




