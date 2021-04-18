---
description: Setzt das Gerät zurück.
ms.assetid: 4ac8ee27-0629-45aa-80ee-f308c044d7fc
title: Reset-Methode der Msvm_SerialController-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialController.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bf5fd2ff0218a4a4f39e64921e41fd497753d04e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358931"
---
# <a name="reset-method-of-the-msvm_serialcontroller-class"></a><span data-ttu-id="4b33a-103">Reset-Methode der MSVM \_ SerialController-Klasse</span><span class="sxs-lookup"><span data-stu-id="4b33a-103">Reset method of the Msvm\_SerialController class</span></span>

<span data-ttu-id="4b33a-104">Setzt das Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="4b33a-104">Resets the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b33a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b33a-105">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="4b33a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b33a-106">Parameters</span></span>

<span data-ttu-id="4b33a-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="4b33a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b33a-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4b33a-108">Return value</span></span>

<span data-ttu-id="4b33a-109">Gibt bei Erfolg 0 zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4b33a-109">Returns 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="4b33a-110">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="4b33a-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4b33a-111">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="4b33a-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="4b33a-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b33a-112">Requirements</span></span>



| <span data-ttu-id="4b33a-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b33a-113">Requirement</span></span> | <span data-ttu-id="4b33a-114">Wert</span><span class="sxs-lookup"><span data-stu-id="4b33a-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b33a-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4b33a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4b33a-116">Windows 8.1, Version 1703</span><span class="sxs-lookup"><span data-stu-id="4b33a-116">Windows 8.1, version 1703</span></span><br/>                                                                    |
| <span data-ttu-id="4b33a-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4b33a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4b33a-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4b33a-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="4b33a-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="4b33a-119">Namespace</span></span><br/>                | <span data-ttu-id="4b33a-120">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="4b33a-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4b33a-121">MOF</span><span class="sxs-lookup"><span data-stu-id="4b33a-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b33a-122"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4b33a-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b33a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="4b33a-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b33a-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4b33a-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4b33a-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b33a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b33a-126">**MSVM \_ SerialController**</span><span class="sxs-lookup"><span data-stu-id="4b33a-126">**Msvm\_SerialController**</span></span>](msvm-serialcontroller.md)
</dt> </dl>

 

 




