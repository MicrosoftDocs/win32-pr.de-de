---
description: Beendet den Gast Dienst.
ms.assetid: 67FFA46C-0B61-4845-A617-BA10F4D42CBC
title: 'Msvm_GuestService:: Stop Service-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6c396078e2bd623a768f391a645091679694f453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862363"
---
# <a name="msvm_guestservicestopservice-method"></a><span data-ttu-id="cfa84-103">MSVM \_ guestservice:: Stop Service-Methode</span><span class="sxs-lookup"><span data-stu-id="cfa84-103">Msvm\_GuestService::StopService method</span></span>

<span data-ttu-id="cfa84-104">Beendet den Gast Dienst.</span><span class="sxs-lookup"><span data-stu-id="cfa84-104">Stops the guest service.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfa84-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfa84-105">Syntax</span></span>


```C++
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="cfa84-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cfa84-106">Parameters</span></span>

<span data-ttu-id="cfa84-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="cfa84-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cfa84-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cfa84-108">Return value</span></span>

<span data-ttu-id="cfa84-109">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="cfa84-109">This method returns one of the following values.</span></span>



| <span data-ttu-id="cfa84-110">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="cfa84-110">Return code/value</span></span>                                                                                                                                             | <span data-ttu-id="cfa84-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cfa84-111">Description</span></span>         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="cfa84-112"><dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cfa84-112"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="cfa84-113">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="cfa84-113">Success.</span></span><br/> |
| <dl> <span data-ttu-id="cfa84-114"><dt>**Nicht unterstützt**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="cfa84-114"><dt>**Not supported**</dt> <dt>1</dt></span></span> </dl>           |                     |



 

## <a name="requirements"></a><span data-ttu-id="cfa84-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfa84-115">Requirements</span></span>



| <span data-ttu-id="cfa84-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cfa84-116">Requirement</span></span> | <span data-ttu-id="cfa84-117">Wert</span><span class="sxs-lookup"><span data-stu-id="cfa84-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfa84-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cfa84-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cfa84-119">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="cfa84-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="cfa84-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cfa84-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cfa84-121">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cfa84-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cfa84-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="cfa84-122">Namespace</span></span><br/>                | <span data-ttu-id="cfa84-123">\\\\\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="cfa84-123">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="cfa84-124">MOF</span><span class="sxs-lookup"><span data-stu-id="cfa84-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cfa84-125"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cfa84-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cfa84-126">DLL</span><span class="sxs-lookup"><span data-stu-id="cfa84-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfa84-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cfa84-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cfa84-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfa84-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfa84-129">**MSVM- \_ guestservice**</span><span class="sxs-lookup"><span data-stu-id="cfa84-129">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

 




