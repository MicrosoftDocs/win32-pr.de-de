---
description: Während einer gleichzeitigen Installation legt das Installationsprogramm die Eigenschaft "paramealdatabase" in der Sitzung der gleichzeitigen Installation auf denselben Wert wie die Eigenschaft "originaldatabase" in der übergeordneten Installationssitzung fest.
ms.assetid: 8af1c7e5-313c-47b7-be0f-0e31ef21f6a6
title: Eigenschaft ' genoriginaldatabase '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab69dff7058336a5b68fd3373100f4789059ed7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360900"
---
# <a name="parentoriginaldatabase-property"></a><span data-ttu-id="958fa-103">Eigenschaft ' genoriginaldatabase '</span><span class="sxs-lookup"><span data-stu-id="958fa-103">ParentOriginalDatabase property</span></span>

<span data-ttu-id="958fa-104">Während einer gleichzeitigen Installation legt das Installationsprogramm die Eigenschaft " **paramealdatabase** " in der Sitzung der gleichzeitigen Installation auf denselben Wert wie die Eigenschaft " [**originaldatabase**](originaldatabase.md) " in der übergeordneten Installationssitzung fest.</span><span class="sxs-lookup"><span data-stu-id="958fa-104">During a concurrent installation, the installer sets the **ParentOriginalDatabase** property in the concurrent installation's session to the same value as the [**OriginalDatabase**](originaldatabase.md) property in the parent installation's session.</span></span> <span data-ttu-id="958fa-105">Bei übergeordneten Installationen werden die parallelen Installations Aktionen verwendet, um eine gleichzeitige Installation auszuführen.</span><span class="sxs-lookup"><span data-stu-id="958fa-105">Parent installations use the concurrent installation actions to perform a concurrent installation.</span></span> <span data-ttu-id="958fa-106">Mithilfe eines Installationspakets kann festgestellt werden, ob es durch eine parallele Installations Aktion installiert wird, indem der Wert dieser Eigenschaft überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="958fa-106">An installation package can determine whether it is being installed by a concurrent installation action by checking the value of this property.</span></span>

> [!Note]  
> <span data-ttu-id="958fa-107">Parallele Installationen werden nicht für die Installation von Anwendungen empfohlen, die für die öffentliche Veröffentlichung vorgesehen sind.</span><span class="sxs-lookup"><span data-stu-id="958fa-107">Concurrent installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="958fa-108">Weitere Informationen zu gleichzeitigen Installationen finden Sie unter [parallele Installationen](concurrent-installations.md).</span><span class="sxs-lookup"><span data-stu-id="958fa-108">For information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="958fa-109">Diese Eigenschaft ist nicht festgelegt, wenn die parallele Installation von der Aktion " [RemoveExistingProducts](removeexistingproducts-action.md) " ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="958fa-109">This property is not set if the concurrent installation is being run by the [RemoveExistingProducts](removeexistingproducts-action.md) action.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="958fa-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="958fa-110">Remarks</span></span>

<span data-ttu-id="958fa-111">Fügen Sie der [LaunchCondition](launchcondition-table.md) -Tabelle eine der folgenden Bedingungs Anweisungen hinzu, um zu verhindern, dass ein Paket jemals als gleichzeitige Installation installiert wird.</span><span class="sxs-lookup"><span data-stu-id="958fa-111">To prevent a package from ever being installed as a concurrent installation, add either of the following conditional statements to the [LaunchCondition](launchcondition-table.md) table.</span></span> <span data-ttu-id="958fa-112">Dadurch wird verhindert, dass das Paket jemals durch eine parallele Installations Aktion installiert wird, die von einer anderen Installation ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="958fa-112">This prevents the package from ever being installed by a concurrent installation action run by another installation.</span></span> <span data-ttu-id="958fa-113">Dies verhindert nicht, dass das Paket von der Aktion " [RemoveExistingProducts](removeexistingproducts-action.md) " installiert wird.</span><span class="sxs-lookup"><span data-stu-id="958fa-113">This does not prevent the package from being installed by the [RemoveExistingProducts](removeexistingproducts-action.md) action.</span></span>

``` syntax
"Not ParentProductCode"
```

``` syntax
"Not ParentOriginalDatabase"
```

## <a name="requirements"></a><span data-ttu-id="958fa-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="958fa-114">Requirements</span></span>



| <span data-ttu-id="958fa-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="958fa-115">Requirement</span></span> | <span data-ttu-id="958fa-116">Wert</span><span class="sxs-lookup"><span data-stu-id="958fa-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="958fa-117">Version</span><span class="sxs-lookup"><span data-stu-id="958fa-117">Version</span></span><br/> | <span data-ttu-id="958fa-118">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="958fa-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="958fa-119">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="958fa-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="958fa-120">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="958fa-120">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="958fa-121">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="958fa-121">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="958fa-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="958fa-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="958fa-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="958fa-123">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="958fa-124">**"Parametriproductcode"**</span><span class="sxs-lookup"><span data-stu-id="958fa-124">**ParentProductCode**</span></span>](parentproductcode.md)
</dt> </dl>

 

 




