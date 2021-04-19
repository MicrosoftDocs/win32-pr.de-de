---
description: Startet den Dienst.
ms.assetid: 59918c15-7216-4cf7-9215-b27532febc72
title: Start Service-Methode der Msvm_SecurityService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bff2721b942b6bb145f2d57492f27d1cabb722bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373390"
---
# <a name="startservice-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="c43f4-103">Start Service-Methode der MSVM \_ SecurityService-Klasse</span><span class="sxs-lookup"><span data-stu-id="c43f4-103">StartService method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="c43f4-104">Startet den Dienst.</span><span class="sxs-lookup"><span data-stu-id="c43f4-104">Starts the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="c43f4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c43f4-105">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="c43f4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c43f4-106">Parameters</span></span>

<span data-ttu-id="c43f4-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c43f4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c43f4-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c43f4-108">Return value</span></span>

<span data-ttu-id="c43f4-109">Bei Erfolg wird 0 zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c43f4-109">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="c43f4-110">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="c43f4-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c43f4-111">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="c43f4-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c43f4-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c43f4-112">Requirements</span></span>



| <span data-ttu-id="c43f4-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c43f4-113">Requirement</span></span> | <span data-ttu-id="c43f4-114">Wert</span><span class="sxs-lookup"><span data-stu-id="c43f4-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c43f4-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c43f4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c43f4-116">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c43f4-116">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c43f4-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c43f4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c43f4-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c43f4-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c43f4-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="c43f4-119">Namespace</span></span><br/>                | <span data-ttu-id="c43f4-120">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="c43f4-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c43f4-121">MOF</span><span class="sxs-lookup"><span data-stu-id="c43f4-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c43f4-122"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c43f4-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c43f4-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c43f4-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c43f4-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c43f4-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c43f4-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c43f4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c43f4-126">**MSVM- \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="c43f4-126">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




