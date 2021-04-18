---
description: Die getRequestID-Methode gibt einen GUID-Wert (Global Unique Identifier) für eine Anforderung zurück. Eine GUID ist eine eindeutige 128-Bit-Zahl.
ms.assetid: c8df15cf-ab48-491f-ac18-1dad567bbc0b
ms.tgt_platform: multiple
title: 'Iwbemkausalityaccess:: getRequestID-Methode (wbemint. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess.GetRequestId
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 075be627b26d99a8b4f03c5a4a962b41f153c8a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347701"
---
# <a name="iwbemcausalityaccessgetrequestid-method"></a><span data-ttu-id="26588-104">Iwbemkausalityaccess:: getRequestID-Methode</span><span class="sxs-lookup"><span data-stu-id="26588-104">IWbemCausalityAccess::GetRequestId method</span></span>

<span data-ttu-id="26588-105">Die **getRequestID-** Methode gibt einen GUID-Wert (Global Unique Identifier) für eine Anforderung zurück.</span><span class="sxs-lookup"><span data-stu-id="26588-105">The **GetRequestId** method returns a Globally Unique Identifier (GUID) value for a request.</span></span> <span data-ttu-id="26588-106">Eine GUID ist eine eindeutige 128-Bit-Zahl.</span><span class="sxs-lookup"><span data-stu-id="26588-106">A GUID is a unique 128-bit number.</span></span>

## <a name="syntax"></a><span data-ttu-id="26588-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="26588-107">Syntax</span></span>


```C++
HRESULT GetRequestId(
  [out] REQUESTID *pId
);
```



## <a name="parameters"></a><span data-ttu-id="26588-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="26588-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26588-109">*pId* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="26588-109">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26588-110">Der GUID-Wert, der eine Anforderung eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="26588-110">The GUID value that uniquely identifies a request.</span></span> <span data-ttu-id="26588-111">Beispiel: 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span><span class="sxs-lookup"><span data-stu-id="26588-111">For example, 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26588-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="26588-112">Return value</span></span>

<span data-ttu-id="26588-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="26588-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="26588-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="26588-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="26588-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26588-115">Requirements</span></span>



| <span data-ttu-id="26588-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26588-116">Requirement</span></span> | <span data-ttu-id="26588-117">Wert</span><span class="sxs-lookup"><span data-stu-id="26588-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26588-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="26588-118">Minimum supported client</span></span><br/> | <span data-ttu-id="26588-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26588-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="26588-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="26588-120">Minimum supported server</span></span><br/> | <span data-ttu-id="26588-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26588-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="26588-122">Header</span><span class="sxs-lookup"><span data-stu-id="26588-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="26588-123"><dt>Wbemint. h</dt></span><span class="sxs-lookup"><span data-stu-id="26588-123"><dt>Wbemint.h</dt></span></span> </dl>    |
| <span data-ttu-id="26588-124">DLL</span><span class="sxs-lookup"><span data-stu-id="26588-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26588-125"><dt>Fastprox.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26588-125"><dt>Fastprox.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26588-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26588-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26588-127">**Iwbemkausalityaccess**</span><span class="sxs-lookup"><span data-stu-id="26588-127">**IWbemCausalityAccess**</span></span>](iwbemcausalityaccess.md)
</dt> </dl>

 

 




