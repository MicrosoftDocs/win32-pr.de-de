---
description: Ruft den Typ der Änderung ab, die im Vektor aufgetreten ist.
ms.assetid: 213f4794-b972-44e3-a400-8a24b1583ddd
title: 'Ivectorchangedeventargs:: get_CollectionChange-Methode (ivectorchangedeventargs. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVectorChangedEventArgs.get_CollectionChange
api_type:
- COM
api_location:
- IVectorChangedEventArgs.h
ms.openlocfilehash: a843574bcaf93ec524173ba76800cc15012c89fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214604"
---
# <a name="ivectorchangedeventargsget_collectionchange-method"></a><span data-ttu-id="bb273-103">Ivectorchangedeventargs:: get \_ CollectionChange-Methode</span><span class="sxs-lookup"><span data-stu-id="bb273-103">IVectorChangedEventArgs::get\_CollectionChange method</span></span>

<span data-ttu-id="bb273-104">Ruft den Typ der Änderung ab, die im Vektor aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="bb273-104">Gets the type of change that occurred in the vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb273-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb273-105">Syntax</span></span>


```C++
HRESULT get_CollectionChange(
  [out, retval] CollectionChange *value
);
```



## <a name="parameters"></a><span data-ttu-id="bb273-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb273-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb273-107">*Wert* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="bb273-107">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="bb273-108">Typ: \**CollectionChange \** _</span><span class="sxs-lookup"><span data-stu-id="bb273-108">Type: \**CollectionChange\** _</span></span>

<span data-ttu-id="bb273-109">Ein Wert aus der [_ *CollectionChange* \*](/uwp/api/Windows.Foundation.Collections.CollectionChange?view=winrt-19041) -Enumeration, der die Änderung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="bb273-109">A value from the [_ *CollectionChange*\*](/uwp/api/Windows.Foundation.Collections.CollectionChange?view=winrt-19041) enumeration that describes the change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb273-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb273-110">Return value</span></span>

<span data-ttu-id="bb273-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bb273-111">Type: **HRESULT**</span></span>

<span data-ttu-id="bb273-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="bb273-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bb273-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bb273-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb273-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb273-114">Requirements</span></span>



| <span data-ttu-id="bb273-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb273-115">Requirement</span></span> | <span data-ttu-id="bb273-116">Wert</span><span class="sxs-lookup"><span data-stu-id="bb273-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb273-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb273-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bb273-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="bb273-118">Windows 8</span></span><br/>                                                                                 |
| <span data-ttu-id="bb273-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb273-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bb273-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bb273-120">Windows Server 2012</span></span><br/>                                                                       |
| <span data-ttu-id="bb273-121">Header</span><span class="sxs-lookup"><span data-stu-id="bb273-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb273-122"><dt>IVector changedebug-args. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb273-122"><dt>IVectorChangedEventArgs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb273-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb273-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb273-124">**IVector changedebug-args**</span><span class="sxs-lookup"><span data-stu-id="bb273-124">**IVectorChangedEventArgs**</span></span>](ivectorchangedeventargs.md)
</dt> </dl>

 

 
