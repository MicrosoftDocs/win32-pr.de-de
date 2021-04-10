---
description: Ruft die Position im Vektor ab, an der die Änderung aufgetreten ist.
ms.assetid: 00756d77-aae0-45f0-8bd4-cf68af9bdc7c
title: 'Ivectorchangedeventargs:: get_Index-Methode (ivectorchangedeventargs. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVectorChangedEventArgs.get_Index
api_type:
- COM
api_location:
- IVectorChangedEventArgs.h
ms.openlocfilehash: 5c131567ec7fc2861ce11db9e5d7ec581f6f663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041736"
---
# <a name="ivectorchangedeventargsget_index-method"></a><span data-ttu-id="a7e68-103">Ivectorchangedeventargs:: get \_ Index-Methode</span><span class="sxs-lookup"><span data-stu-id="a7e68-103">IVectorChangedEventArgs::get\_Index method</span></span>

<span data-ttu-id="a7e68-104">Ruft die Position im Vektor ab, an der die Änderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="a7e68-104">Gets the position in the vector where the change occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7e68-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7e68-105">Syntax</span></span>


```C++
HRESULT get_Index(
  [out, retval] unsigned *value
);
```



## <a name="parameters"></a><span data-ttu-id="a7e68-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7e68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7e68-107">*Wert* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="a7e68-107">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a7e68-108">Typ: \**Ganzzahl ohne Vorzeichen \** _</span><span class="sxs-lookup"><span data-stu-id="a7e68-108">Type: \**unsigned\** _</span></span>

<span data-ttu-id="a7e68-109">Die null basierte Position im Vektor, an der die Änderung aufgetreten ist (falls zutreffend).</span><span class="sxs-lookup"><span data-stu-id="a7e68-109">The zero-based position in the vector where the change occurred, if applicable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7e68-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a7e68-110">Return value</span></span>

<span data-ttu-id="a7e68-111">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="a7e68-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="a7e68-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a7e68-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a7e68-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a7e68-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7e68-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7e68-114">Requirements</span></span>



| <span data-ttu-id="a7e68-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7e68-115">Requirement</span></span> | <span data-ttu-id="a7e68-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a7e68-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7e68-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a7e68-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a7e68-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a7e68-118">Windows 8</span></span><br/>                                                                                 |
| <span data-ttu-id="a7e68-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a7e68-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a7e68-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a7e68-120">Windows Server 2012</span></span><br/>                                                                       |
| <span data-ttu-id="a7e68-121">Header</span><span class="sxs-lookup"><span data-stu-id="a7e68-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7e68-122"><dt>IVector changedebug-args. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7e68-122"><dt>IVectorChangedEventArgs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7e68-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7e68-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7e68-124">**IVector changedebug-args**</span><span class="sxs-lookup"><span data-stu-id="a7e68-124">**IVectorChangedEventArgs**</span></span>](ivectorchangedeventargs.md)
</dt> </dl>

 

 




