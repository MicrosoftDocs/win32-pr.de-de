---
description: Die upgradingproductcode-Eigenschaft wird Windows Installer festgelegt, wenn ein Upgrade eine Anwendung entfernt.
ms.assetid: 903e4c22-e7ae-47bd-989b-d8c922de8d1a
title: Upgradingproductcode-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a256ade7f03275752ad4d176e64cd9d0fa12ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358088"
---
# <a name="upgradingproductcode-property"></a><span data-ttu-id="5b6d7-103">Upgradingproductcode-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5b6d7-103">UPGRADINGPRODUCTCODE property</span></span>

<span data-ttu-id="5b6d7-104">Die **upgradingproductcode** -Eigenschaft wird Windows Installer festgelegt, wenn ein Upgrade eine Anwendung entfernt.</span><span class="sxs-lookup"><span data-stu-id="5b6d7-104">The **UPGRADINGPRODUCTCODE** property is set by Windows Installer when an upgrade removes an application.</span></span> <span data-ttu-id="5b6d7-105">Das Installationsprogramm legt diese Eigenschaft fest, wenn die [RemoveExistingProducts-Aktion](removeexistingproducts-action.md)ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5b6d7-105">The installer sets this property when it runs the [RemoveExistingProducts action](removeexistingproducts-action.md).</span></span> <span data-ttu-id="5b6d7-106">Diese Eigenschaft wird nicht festgelegt, indem eine Anwendung mithilfe der Option Software in der Systemsteuerung entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="5b6d7-106">This property is not set by removing an application using the Add or Remove Programs in Control Panel.</span></span> <span data-ttu-id="5b6d7-107">Eine Anwendung bestimmt mithilfe von " **upgradingproductcode**", ob Sie durch ein Upgrade oder die Software zum Hinzufügen oder entfernen entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="5b6d7-107">An application determines whether it is being removed by an upgrade or the Add or Remove Programs by checking **UPGRADINGPRODUCTCODE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b6d7-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b6d7-108">Requirements</span></span>



| <span data-ttu-id="5b6d7-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b6d7-109">Requirement</span></span> | <span data-ttu-id="5b6d7-110">Wert</span><span class="sxs-lookup"><span data-stu-id="5b6d7-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b6d7-111">Version</span><span class="sxs-lookup"><span data-stu-id="5b6d7-111">Version</span></span><br/> | <span data-ttu-id="5b6d7-112">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5b6d7-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5b6d7-113">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5b6d7-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5b6d7-114">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5b6d7-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="5b6d7-115">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="5b6d7-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5b6d7-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b6d7-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b6d7-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5b6d7-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 




