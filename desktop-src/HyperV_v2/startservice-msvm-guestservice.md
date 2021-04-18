---
description: Versetzt den Gast Dienst in den Zustand "gestartet".
ms.assetid: 1DC6A5B3-0F91-4AC1-99D5-0E8CF5ED35A2
title: 'Msvm_GuestService:: StartService-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1a87bc9933bd7b3a54bd59169b0099e34eb04c52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355080"
---
# <a name="msvm_guestservicestartservice-method"></a><span data-ttu-id="326af-103">MSVM \_ guestservice:: StartService-Methode</span><span class="sxs-lookup"><span data-stu-id="326af-103">Msvm\_GuestService::StartService method</span></span>

<span data-ttu-id="326af-104">Versetzt den Gast Dienst in den Zustand "gestartet".</span><span class="sxs-lookup"><span data-stu-id="326af-104">Puts the guest service in a started state.</span></span>

## <a name="syntax"></a><span data-ttu-id="326af-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="326af-105">Syntax</span></span>


```C++
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="326af-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="326af-106">Parameters</span></span>

<span data-ttu-id="326af-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="326af-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="326af-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="326af-108">Return value</span></span>

<span data-ttu-id="326af-109">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="326af-109">This method returns one of the following values.</span></span>



| <span data-ttu-id="326af-110">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="326af-110">Return code/value</span></span>                                                                                                                                             | <span data-ttu-id="326af-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="326af-111">Description</span></span>         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="326af-112"><dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="326af-112"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="326af-113">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="326af-113">Success.</span></span><br/> |
| <dl> <span data-ttu-id="326af-114"><dt>**Nicht unterstützt**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="326af-114"><dt>**Not supported**</dt> <dt>1</dt></span></span> </dl>           |                     |



 

## <a name="requirements"></a><span data-ttu-id="326af-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="326af-115">Requirements</span></span>



| <span data-ttu-id="326af-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="326af-116">Requirement</span></span> | <span data-ttu-id="326af-117">Wert</span><span class="sxs-lookup"><span data-stu-id="326af-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="326af-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="326af-118">Minimum supported client</span></span><br/> | <span data-ttu-id="326af-119">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="326af-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="326af-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="326af-120">Minimum supported server</span></span><br/> | <span data-ttu-id="326af-121">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="326af-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="326af-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="326af-122">Namespace</span></span><br/>                | <span data-ttu-id="326af-123">\\\\\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="326af-123">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="326af-124">MOF</span><span class="sxs-lookup"><span data-stu-id="326af-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="326af-125"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="326af-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="326af-126">DLL</span><span class="sxs-lookup"><span data-stu-id="326af-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="326af-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="326af-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="326af-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="326af-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="326af-129">**MSVM- \_ guestservice**</span><span class="sxs-lookup"><span data-stu-id="326af-129">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

 




