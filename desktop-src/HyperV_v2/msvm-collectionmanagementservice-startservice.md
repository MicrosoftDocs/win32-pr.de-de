---
description: Beendet den Dienst.
ms.assetid: 0f9a015d-b895-496a-a4c6-2737c0742746
title: Start Service-Methode der Msvm_CollectionManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f76fa9e5069c2a9e19b83a8ab83136879c6657e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359609"
---
# <a name="startservice-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="800fa-103">Start Service-Methode der MSVM \_ collectionmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="800fa-103">StartService method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="800fa-104">Beendet den Dienst.</span><span class="sxs-lookup"><span data-stu-id="800fa-104">Stops the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="800fa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="800fa-105">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="800fa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="800fa-106">Parameters</span></span>

<span data-ttu-id="800fa-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="800fa-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="800fa-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="800fa-108">Return value</span></span>

<span data-ttu-id="800fa-109">Gibt bei Erfolg 0 zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="800fa-109">Returns 0 if successful; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="800fa-110">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="800fa-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="800fa-111">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="800fa-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="800fa-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="800fa-112">Requirements</span></span>



| <span data-ttu-id="800fa-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="800fa-113">Requirement</span></span> | <span data-ttu-id="800fa-114">Wert</span><span class="sxs-lookup"><span data-stu-id="800fa-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="800fa-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="800fa-115">Minimum supported client</span></span><br/> | <span data-ttu-id="800fa-116">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="800fa-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="800fa-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="800fa-117">Minimum supported server</span></span><br/> | <span data-ttu-id="800fa-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="800fa-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="800fa-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="800fa-119">Namespace</span></span><br/>                | <span data-ttu-id="800fa-120">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="800fa-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="800fa-121">MOF</span><span class="sxs-lookup"><span data-stu-id="800fa-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="800fa-122"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="800fa-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="800fa-123">DLL</span><span class="sxs-lookup"><span data-stu-id="800fa-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="800fa-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="800fa-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="800fa-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="800fa-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="800fa-126">**MSVM \_ collectionmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="800fa-126">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




