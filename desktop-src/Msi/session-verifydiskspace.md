---
description: Die verifydiskspace-Eigenschaft ist eine schreibgeschützte Eigenschaft.
ms.assetid: 62f11f71-00b0-4e04-8c45-d6d670238886
title: Session. verifydiskspace-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.VerifyDiskSpace
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a73f2b6f846cb918d5eb10689388a174950c0edc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356087"
---
# <a name="sessionverifydiskspace-property"></a><span data-ttu-id="eba28-103">Session. verifydiskspace-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="eba28-103">Session.VerifyDiskSpace property</span></span>

<span data-ttu-id="eba28-104">Die **verifydiskspace** -Eigenschaft ist eine schreibgeschützte Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="eba28-104">The **VerifyDiskSpace** property is a read-only property.</span></span> <span data-ttu-id="eba28-105">Sie gibt true zurück, wenn ausreichend Speicherplatz vorhanden ist, und false, wenn der Datenträger voll ist.</span><span class="sxs-lookup"><span data-stu-id="eba28-105">It returns true if enough disk space exists and false if the disk is full.</span></span> <span data-ttu-id="eba28-106">Da diese Eigenschaft Informationen verwendet, die von den Kosten Aktionen gesammelt werden, sollte **verifydiskspace** nur nach der Aktion " [costinitialize](costinitialize-action.md)", " [filecost Action](filecost-action.md)" und " [costfinalize](costfinalize-action.md)" aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="eba28-106">Because this property uses information gathered by the costing actions, **VerifyDiskSpace** should only be called after the [CostInitialize action](costinitialize-action.md), [FileCost action](filecost-action.md), and [CostFinalize action](costfinalize-action.md).</span></span>

<span data-ttu-id="eba28-107">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="eba28-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="eba28-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="eba28-108">Syntax</span></span>


```JScript
propVal = Session.VerifyDiskSpace
```



## <a name="property-value"></a><span data-ttu-id="eba28-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="eba28-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="eba28-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eba28-110">Requirements</span></span>



| <span data-ttu-id="eba28-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eba28-111">Requirement</span></span> | <span data-ttu-id="eba28-112">Wert</span><span class="sxs-lookup"><span data-stu-id="eba28-112">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eba28-113">Version</span><span class="sxs-lookup"><span data-stu-id="eba28-113">Version</span></span><br/> | <span data-ttu-id="eba28-114">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="eba28-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="eba28-115">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="eba28-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="eba28-116">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="eba28-116">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="eba28-117">DLL</span><span class="sxs-lookup"><span data-stu-id="eba28-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="eba28-118"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eba28-118"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="eba28-119">IID</span><span class="sxs-lookup"><span data-stu-id="eba28-119">IID</span></span><br/>     | <span data-ttu-id="eba28-120">IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="eba28-120">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




