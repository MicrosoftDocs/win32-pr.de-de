---
description: Die Eigenschaft für das CCP- \_ Laufwerk wird auf den Stammpfad des Wechsel Datenträgers festgelegt, das von RMCCPSEARCH durchsucht werden soll.
ms.assetid: 567b7d11-6d80-4ec5-810d-f32b9ebf5809
title: CCP_DRIVE-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6215881cd3a998cd63a958bfe258ad3f9872ab1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354137"
---
# <a name="ccp_drive-property"></a><span data-ttu-id="32173-103">CCP- \_ Laufwerks Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="32173-103">CCP\_DRIVE property</span></span>

<span data-ttu-id="32173-104">Die Eigenschaft für das **CCP- \_ Laufwerk** wird auf den Stammpfad des Wechsel Datenträgers festgelegt, das von [RMCCPSEARCH](rmccpsearch-action.md)durchsucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="32173-104">The **CCP\_DRIVE** property is set to the root path of the removable volume that is to be searched by [RMCCPSearch](rmccpsearch-action.md).</span></span> <span data-ttu-id="32173-105">Die RMCCPSEARCH-Aktion verwendet Datei Signaturen, um zu überprüfen, ob qualifizierte Produkte auf einem System installiert sind, bevor eine Upgrade-Installation durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="32173-105">The RMCCPSearch action uses file signatures to validate that qualifying products are installed on a system before performing an upgrade installation.</span></span>

<span data-ttu-id="32173-106">Diese Eigenschaft wird in der Regel über die Benutzeroberfläche oder eine benutzerdefinierte Aktion festgelegt.</span><span class="sxs-lookup"><span data-stu-id="32173-106">This property is typically set via the user interface or a custom action.</span></span> <span data-ttu-id="32173-107">Diese Eigenschaft muss festgelegt werden, bevor die [RMCCPSEARCH](rmccpsearch-action.md) -Aktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="32173-107">This property should be set before the [RMCCPSearch](rmccpsearch-action.md) action is run.</span></span>

## <a name="requirements"></a><span data-ttu-id="32173-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32173-108">Requirements</span></span>



| <span data-ttu-id="32173-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="32173-109">Requirement</span></span> | <span data-ttu-id="32173-110">Wert</span><span class="sxs-lookup"><span data-stu-id="32173-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32173-111">Version</span><span class="sxs-lookup"><span data-stu-id="32173-111">Version</span></span><br/> | <span data-ttu-id="32173-112">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="32173-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="32173-113">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="32173-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="32173-114">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="32173-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="32173-115">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="32173-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="32173-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32173-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32173-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="32173-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 




