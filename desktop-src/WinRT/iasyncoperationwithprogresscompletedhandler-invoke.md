---
description: Ruft die Methode auf, die aufgerufen wird, wenn der angegebene asynchrone Vorgang den Status meldet.
ms.assetid: FB60DDC0-7521-4999-8DD8-175556004198
title: 'Iasyncoperationwithprogresscompletedhandler<TResult, tprogress>:: Aufrufen-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>.Invoke
api_type:
- COM
api_location: ''
ms.openlocfilehash: 469686cbd96dedc7f816fdd1f482d3474362688e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129236"
---
# <a name="iasyncoperationwithprogresscompletedhandlertresulttprogressinvoke-method"></a><span data-ttu-id="894cb-103">Iasyncoperationwithprogresscompletedhandler<TResult, tprogress>:: Aufrufen-Methode</span><span class="sxs-lookup"><span data-stu-id="894cb-103">IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>::Invoke method</span></span>

<span data-ttu-id="894cb-104">Ruft die Methode auf, die aufgerufen wird, wenn der angegebene asynchrone Vorgang den Status meldet.</span><span class="sxs-lookup"><span data-stu-id="894cb-104">Invokes the method that is called when the specified asynchronous operation reports progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="894cb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="894cb-105">Syntax</span></span>


```C++
HRESULT Invoke(
  [in] IAsyncOperationWithProgress<TResult,TProgress> *asyncInfo
);
```



## <a name="parameters"></a><span data-ttu-id="894cb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="894cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="894cb-107">*asyncinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="894cb-107">*asyncInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="894cb-108">Geben Sie Folgendes ein: \**[**iasyncoperationwithprogress<TResult, tprogress>**](/previous-versions//br205807(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="894cb-108">Type: \**[**IAsyncOperationWithProgress<TResult,TProgress>**](/previous-versions//br205807(v=vs.85))\** _</span></span>

<span data-ttu-id="894cb-109">Die asynchrone Aktion, die den Abschluss meldet.</span><span class="sxs-lookup"><span data-stu-id="894cb-109">The asynchronous action that reports completion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="894cb-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="894cb-110">Return value</span></span>

<span data-ttu-id="894cb-111">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="894cb-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="894cb-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="894cb-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="894cb-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="894cb-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="894cb-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="894cb-114">Requirements</span></span>



| <span data-ttu-id="894cb-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="894cb-115">Requirement</span></span> | <span data-ttu-id="894cb-116">Wert</span><span class="sxs-lookup"><span data-stu-id="894cb-116">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="894cb-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="894cb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="894cb-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="894cb-118">Windows 8</span></span><br/>           |
| <span data-ttu-id="894cb-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="894cb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="894cb-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="894cb-120">Windows Server 2012</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="894cb-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="894cb-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="894cb-122">[**Iasyncoperationwithprogresscompletedhandler<TResult, tprogress>**](/previous-versions//br205808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="894cb-122">[**IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>**](/previous-versions//br205808(v=vs.85))</span></span>
</dt> </dl>

 

 
