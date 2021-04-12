---
description: Beendet den Dienst.
ms.assetid: cf100cea-b0e1-42e9-831e-6422aded47c5
title: Stop Service-Methode der Msvm_SecurityService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 68e88e2c88d4f75f4d7671c389bab0cd81d0deb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216769"
---
# <a name="stopservice-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="7d1f3-103">Stop Service-Methode der MSVM \_ SecurityService-Klasse</span><span class="sxs-lookup"><span data-stu-id="7d1f3-103">StopService method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="7d1f3-104">Beendet den Dienst.</span><span class="sxs-lookup"><span data-stu-id="7d1f3-104">Stops the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d1f3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d1f3-105">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="7d1f3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d1f3-106">Parameters</span></span>

<span data-ttu-id="7d1f3-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7d1f3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7d1f3-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7d1f3-108">Return value</span></span>

<span data-ttu-id="7d1f3-109">Bei Erfolg wird 0 zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7d1f3-109">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="7d1f3-110">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="7d1f3-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7d1f3-111">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="7d1f3-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7d1f3-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d1f3-112">Requirements</span></span>



| <span data-ttu-id="7d1f3-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d1f3-113">Requirement</span></span> | <span data-ttu-id="7d1f3-114">Wert</span><span class="sxs-lookup"><span data-stu-id="7d1f3-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d1f3-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7d1f3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7d1f3-116">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d1f3-116">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7d1f3-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7d1f3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7d1f3-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7d1f3-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7d1f3-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="7d1f3-119">Namespace</span></span><br/>                | <span data-ttu-id="7d1f3-120">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="7d1f3-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7d1f3-121">MOF</span><span class="sxs-lookup"><span data-stu-id="7d1f3-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d1f3-122"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7d1f3-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d1f3-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7d1f3-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d1f3-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7d1f3-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7d1f3-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d1f3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d1f3-126">**MSVM- \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="7d1f3-126">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




