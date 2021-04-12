---
description: Legt den BLOB-Trigger fest.
ms.assetid: 88bfd5cd-f563-4d0c-81a3-54a846805b87
title: Setnpptriggerinblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPTriggerInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 05b8bb3f7f95dc3246ef10f3945b9ab0868550cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214743"
---
# <a name="setnpptriggerinblob-function"></a><span data-ttu-id="87713-103">Setnpptriggerinblob-Funktion</span><span class="sxs-lookup"><span data-stu-id="87713-103">SetNPPTriggerInBlob function</span></span>

<span data-ttu-id="87713-104">Die **setnpptriggerinblob** -Funktion legt den BLOB-Trigger fest.</span><span class="sxs-lookup"><span data-stu-id="87713-104">The **SetNPPTriggerInBlob** function sets the BLOB trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="87713-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="87713-105">Syntax</span></span>


```C++
DWORD SetNPPTriggerInBlob(
  _In_  HBLOB     hBlob,
  _In_  LPTRIGGER pTrigger,
  _Out_ HBLOB     hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="87713-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="87713-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87713-107">*hblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87713-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87713-108">Das Handle für das BLOB.</span><span class="sxs-lookup"><span data-stu-id="87713-108">The handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="87713-109">*p-Auslösung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87713-109">*pTrigger* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87713-110">Ein Zeiger auf den Wert des Auslösers.</span><span class="sxs-lookup"><span data-stu-id="87713-110">A pointer to the trigger value.</span></span>

</dd> <dt>

<span data-ttu-id="87713-111">*herrorblob* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="87713-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87713-112">Das Handle für ein fehlerblob, das angibt, wo der Fehler im ursprünglichen BLOB aufgetreten ist (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="87713-112">The handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87713-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="87713-113">Return value</span></span>

<span data-ttu-id="87713-114">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="87713-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="87713-115">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="87713-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="87713-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87713-116">Remarks</span></span>

<span data-ttu-id="87713-117">Diese auslöserdaten werden in der **Trigger** -Kategorie des BLOBs gespeichert.</span><span class="sxs-lookup"><span data-stu-id="87713-117">This trigger data is stored in the **Trigger** category of the BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="87713-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87713-118">Requirements</span></span>



| <span data-ttu-id="87713-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87713-119">Requirement</span></span> | <span data-ttu-id="87713-120">Wert</span><span class="sxs-lookup"><span data-stu-id="87713-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87713-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="87713-121">Minimum supported client</span></span><br/> | <span data-ttu-id="87713-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87713-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="87713-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="87713-123">Minimum supported server</span></span><br/> | <span data-ttu-id="87713-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87713-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="87713-125">Header</span><span class="sxs-lookup"><span data-stu-id="87713-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="87713-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="87713-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="87713-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="87713-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="87713-128"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87713-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="87713-129">DLL</span><span class="sxs-lookup"><span data-stu-id="87713-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87713-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87713-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87713-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87713-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87713-132">Getnpptriggerfromblob</span><span class="sxs-lookup"><span data-stu-id="87713-132">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="87713-133">Setboolinblob</span><span class="sxs-lookup"><span data-stu-id="87713-133">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="87713-134">Setclassidinblob</span><span class="sxs-lookup"><span data-stu-id="87713-134">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="87713-135">Setdwordinblob</span><span class="sxs-lookup"><span data-stu-id="87713-135">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="87713-136">Setmacaddressinblob</span><span class="sxs-lookup"><span data-stu-id="87713-136">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="87713-137">Setnetworkinfoinblob</span><span class="sxs-lookup"><span data-stu-id="87713-137">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="87713-138">Setnppaddressfilterinblob</span><span class="sxs-lookup"><span data-stu-id="87713-138">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="87713-139">Setnpppatternfilterinblob</span><span class="sxs-lookup"><span data-stu-id="87713-139">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="87713-140">Setstringinblob</span><span class="sxs-lookup"><span data-stu-id="87713-140">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




