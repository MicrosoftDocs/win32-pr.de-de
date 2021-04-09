---
description: Fordert an, dass der Vorgang zum Anhalten der APP verzögert wird.
ms.assetid: 5AB84652-165D-4173-A047-541B05848871
title: 'Isuspendingoperation:: getdeferral-Methode (Windows. applicationmodel. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation.GetDeferral
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 6874eb31e73fa1c20399f68850fc69204d0e0f6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862611"
---
# <a name="isuspendingoperationgetdeferral-method"></a><span data-ttu-id="14590-103">Isuspendingoperation:: getdeferral-Methode</span><span class="sxs-lookup"><span data-stu-id="14590-103">ISuspendingOperation::GetDeferral method</span></span>

<span data-ttu-id="14590-104">Fordert an, dass der Vorgang zum Anhalten der APP verzögert wird.</span><span class="sxs-lookup"><span data-stu-id="14590-104">Requests that the app suspending operation be delayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="14590-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="14590-105">Syntax</span></span>


```C++
HRESULT GetDeferral(
  [out, retval] ISuspendingDeferral **deferral
);
```



## <a name="parameters"></a><span data-ttu-id="14590-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="14590-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14590-107">*Verzögerung* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="14590-107">*deferral* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="14590-108">Die Unterbrechung der Verzögerung.</span><span class="sxs-lookup"><span data-stu-id="14590-108">The deferral suspension.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14590-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="14590-109">Return value</span></span>

<span data-ttu-id="14590-110">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="14590-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="14590-111">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="14590-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="14590-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14590-112">Requirements</span></span>



| <span data-ttu-id="14590-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14590-113">Requirement</span></span> | <span data-ttu-id="14590-114">Wert</span><span class="sxs-lookup"><span data-stu-id="14590-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14590-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="14590-115">Minimum supported client</span></span><br/> | <span data-ttu-id="14590-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="14590-116">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="14590-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="14590-117">Minimum supported server</span></span><br/> | <span data-ttu-id="14590-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="14590-118">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="14590-119">Header</span><span class="sxs-lookup"><span data-stu-id="14590-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="14590-120"><dt>Windows. applicationmodel. h</dt></span><span class="sxs-lookup"><span data-stu-id="14590-120"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="14590-121">IDL</span><span class="sxs-lookup"><span data-stu-id="14590-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="14590-122"><dt>Windows. applicationmodel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="14590-122"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14590-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14590-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14590-124">**Isuspendingoperation**</span><span class="sxs-lookup"><span data-stu-id="14590-124">**ISuspendingOperation**</span></span>](isuspendingoperation.md)
</dt> </dl>

 

 




