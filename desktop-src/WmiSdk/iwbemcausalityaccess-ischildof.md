---
description: Die ischildof-Methode bestimmt, ob eine Anforderung ein untergeordnetes Element einer angegebenen Anforderung (pId) ist.
ms.assetid: 7be52496-7dcf-41c0-853a-859810a57d21
ms.tgt_platform: multiple
title: 'Iwbemkausalityaccess:: ischildof-Methode (wbemint. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess.IsChildOf
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 6deec7521ceb58a76db3dbf8064ccc444019cb9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217119"
---
# <a name="iwbemcausalityaccessischildof-method"></a><span data-ttu-id="cfbd1-103">Iwbemkausalityaccess:: ischildof-Methode</span><span class="sxs-lookup"><span data-stu-id="cfbd1-103">IWbemCausalityAccess::IsChildOf method</span></span>

<span data-ttu-id="cfbd1-104">Die **ischildof** -Methode bestimmt, ob eine Anforderung ein untergeordnetes Element einer angegebenen Anforderung (pId) ist.</span><span class="sxs-lookup"><span data-stu-id="cfbd1-104">The **IsChildOf** method determines if a request is a child of a specified request (pId).</span></span> <span data-ttu-id="cfbd1-105">Eine übergeordnete Anforderung kann über mehrere untergeordnete Anforderungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="cfbd1-105">A parent request can have multiple child requests.</span></span> <span data-ttu-id="cfbd1-106">Jede Anforderung wird durch einen global eindeutigen Bezeichner (GUID) identifiziert und kann über eine übergeordnete Anforderung verfügen oder eine Top-Anforderung sein.</span><span class="sxs-lookup"><span data-stu-id="cfbd1-106">Each request is identified by a Globally Unique Identifier (GUID) and can have a parent request or can be a top request.</span></span> <span data-ttu-id="cfbd1-107">Eine GUID ist eine eindeutige 128-Bit-Zahl.</span><span class="sxs-lookup"><span data-stu-id="cfbd1-107">A GUID is a unique 128-bit number.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfbd1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfbd1-108">Syntax</span></span>


```C++
HRESULT IsChildOf(
  [in] REQUESTID pId
);
```



## <a name="parameters"></a><span data-ttu-id="cfbd1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cfbd1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfbd1-110">*pId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cfbd1-110">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfbd1-111">Der GUID-Wert, der eine Anforderung eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cfbd1-111">The GUID value that uniquely identifies a request.</span></span> <span data-ttu-id="cfbd1-112">Beispiel: 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span><span class="sxs-lookup"><span data-stu-id="cfbd1-112">For example, 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfbd1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cfbd1-113">Return value</span></span>

<span data-ttu-id="cfbd1-114">Gibt erfolgreich zurück, wenn die angegebene Anforderung ein untergeordnetes Element der Anforderung ist, die die **ischildof** -Methode aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="cfbd1-114">Returns successful if the specified request is a child of the request calling the **IsChildOf** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfbd1-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfbd1-115">Requirements</span></span>



| <span data-ttu-id="cfbd1-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cfbd1-116">Requirement</span></span> | <span data-ttu-id="cfbd1-117">Wert</span><span class="sxs-lookup"><span data-stu-id="cfbd1-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfbd1-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cfbd1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cfbd1-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cfbd1-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cfbd1-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cfbd1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cfbd1-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cfbd1-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cfbd1-122">Header</span><span class="sxs-lookup"><span data-stu-id="cfbd1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfbd1-123"><dt>Wbemint. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfbd1-123"><dt>Wbemint.h</dt></span></span> </dl>    |
| <span data-ttu-id="cfbd1-124">DLL</span><span class="sxs-lookup"><span data-stu-id="cfbd1-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfbd1-125"><dt>Fastprox.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfbd1-125"><dt>Fastprox.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfbd1-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfbd1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfbd1-127">**Iwbemkausalityaccess**</span><span class="sxs-lookup"><span data-stu-id="cfbd1-127">**IWbemCausalityAccess**</span></span>](iwbemcausalityaccess.md)
</dt> </dl>

 

 




