---
description: Die UpgradeCode-Eigenschaft ist eine GUID, die einen zusammenhängenden Satz von Produkten darstellt. Der UpgradeCode wird in der upgradetabelle verwendet, um nach verwandten Versionen des Produkts zu suchen, die bereits installiert sind. Diese Eigenschaft wird von der registerproduct-Aktion verwendet.
ms.assetid: 6cdee5d8-8aa0-4fad-9338-152ee33b8077
title: UpgradeCode-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1e5493ad651e609f6ef9d7ae14e07c0c15b5b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370695"
---
# <a name="upgradecode-property"></a><span data-ttu-id="61cb6-104">UpgradeCode-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="61cb6-104">UpgradeCode property</span></span>

<span data-ttu-id="61cb6-105">Die **UpgradeCode** -Eigenschaft ist eine GUID, die einen zusammenhängenden Satz von Produkten darstellt.</span><span class="sxs-lookup"><span data-stu-id="61cb6-105">The **UpgradeCode** property is a GUID representing a related set of products.</span></span> <span data-ttu-id="61cb6-106">Der **UpgradeCode** wird in der [upgradetabelle](upgrade-table.md) verwendet, um nach verwandten Versionen des Produkts zu suchen, die bereits installiert sind.</span><span class="sxs-lookup"><span data-stu-id="61cb6-106">The **UpgradeCode** is used in the [Upgrade Table](upgrade-table.md) to search for related versions of the product that are already installed.</span></span>

<span data-ttu-id="61cb6-107">Diese Eigenschaft wird von der [registerproduct-Aktion](registerproduct-action.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="61cb6-107">This property is used by the [RegisterProduct action](registerproduct-action.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="61cb6-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61cb6-108">Remarks</span></span>

<span data-ttu-id="61cb6-109">Es wird dringend empfohlen, dass Autoren von Installationspaketen einen **UpgradeCode** für Ihre Anwendung angeben.</span><span class="sxs-lookup"><span data-stu-id="61cb6-109">It is strongly recommended that authors of installation packages specify an **UpgradeCode** for their application.</span></span>

## <a name="requirements"></a><span data-ttu-id="61cb6-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61cb6-110">Requirements</span></span>



| <span data-ttu-id="61cb6-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61cb6-111">Requirement</span></span> | <span data-ttu-id="61cb6-112">Wert</span><span class="sxs-lookup"><span data-stu-id="61cb6-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61cb6-113">Version</span><span class="sxs-lookup"><span data-stu-id="61cb6-113">Version</span></span><br/> | <span data-ttu-id="61cb6-114">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="61cb6-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="61cb6-115">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="61cb6-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="61cb6-116">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="61cb6-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="61cb6-117">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="61cb6-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="61cb6-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61cb6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61cb6-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="61cb6-119">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="61cb6-120">Patchen und Upgrades</span><span class="sxs-lookup"><span data-stu-id="61cb6-120">Patching and Upgrades</span></span>](patching-and-upgrades.md)
</dt> <dt>

[<span data-ttu-id="61cb6-121">Vorbereiten einer Anwendung für zukünftige größere Upgrades</span><span class="sxs-lookup"><span data-stu-id="61cb6-121">Preparing an Application for Future Major Upgrades</span></span>](preparing-an-application-for-future-major-upgrades.md)
</dt> </dl>

 

 




