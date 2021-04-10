---
description: Ruft einen Wert ab, der den Erzwingungs Status der Device Guard-Richtlinie für dynamischen .NET-Code beschreibt.
ms.assetid: 11E6C631-0FF8-4DB2-931A-1012B3CA4357
title: Wldpisdynamiccodepolicyaktivierte Funktion (wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpIsDynamicCodePolicyEnabled
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 4df0555f89e9c575a7d97b69a5252c17936eb3d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125852"
---
# <a name="wldpisdynamiccodepolicyenabled-function"></a><span data-ttu-id="efaf3-103">Wldpisdynamiccodepolicyaktivierte Funktion</span><span class="sxs-lookup"><span data-stu-id="efaf3-103">WldpIsDynamicCodePolicyEnabled function</span></span>

<span data-ttu-id="efaf3-104">Ruft einen Wert ab, der den Erzwingungs Status der Device Guard-Richtlinie für dynamischen .NET-Code beschreibt.</span><span class="sxs-lookup"><span data-stu-id="efaf3-104">Retrieves a value that describes the Device Guard policy enforcement status for .NET dynamic code.</span></span>

## <a name="syntax"></a><span data-ttu-id="efaf3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="efaf3-105">Syntax</span></span>


```C++
HRESULT WINAPI WldpIsDynamicCodePolicyEnabled(
  _Out_ PBOOL  isEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="efaf3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="efaf3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efaf3-107">*isaktiviert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="efaf3-107">*isEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="efaf3-108">Bei Erfolg wird " **wahr** " zurückgegeben, wenn die Device Guard-Richtlinie die dynamische .NET-Code Richtlinie erzwingt Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="efaf3-108">On success, returns **true** if the Device Guard policy enforces .NET Dynamic Code policy; otherwise, returns **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efaf3-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="efaf3-109">Return value</span></span>

<span data-ttu-id="efaf3-110">Diese Methode gibt bei Erfolg **S \_ OK** zurück oder andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="efaf3-110">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="efaf3-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="efaf3-111">Remarks</span></span>

<span data-ttu-id="efaf3-112">Dynamischer Code bezieht sich auf dynamisch generierten .net-CRL-Code.</span><span class="sxs-lookup"><span data-stu-id="efaf3-112">Dynamic code refers to .NET CRL dynamically-generated code.</span></span>

## <a name="requirements"></a><span data-ttu-id="efaf3-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="efaf3-113">Requirements</span></span>



| <span data-ttu-id="efaf3-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="efaf3-114">Requirement</span></span> | <span data-ttu-id="efaf3-115">Wert</span><span class="sxs-lookup"><span data-stu-id="efaf3-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="efaf3-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="efaf3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="efaf3-117">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="efaf3-117">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="efaf3-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="efaf3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="efaf3-119">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="efaf3-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="efaf3-120">Header</span><span class="sxs-lookup"><span data-stu-id="efaf3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="efaf3-121"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="efaf3-121"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="efaf3-122">DLL</span><span class="sxs-lookup"><span data-stu-id="efaf3-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efaf3-123"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efaf3-123"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




