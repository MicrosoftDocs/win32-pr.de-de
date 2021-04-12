---
description: Legt den Übereinstimmungs Filter für blobmuster fest.
ms.assetid: 44e7c67a-f430-4d68-bc7f-f6bbd5b9e5a9
title: Setnpppatternfilterinblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPPatternFilterInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: b2e8989264a042368b37926bbb502f48ab2fb04b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526750"
---
# <a name="setnpppatternfilterinblob-function"></a><span data-ttu-id="a9bc6-103">Setnpppatternfilterinblob-Funktion</span><span class="sxs-lookup"><span data-stu-id="a9bc6-103">SetNPPPatternFilterInBlob function</span></span>

<span data-ttu-id="a9bc6-104">Die **setnpppatternfilterinblob** -Funktion legt den Filter für die blobmusterübereinstimmung fest.</span><span class="sxs-lookup"><span data-stu-id="a9bc6-104">The **SetNPPPatternFilterInBlob** function sets the BLOB pattern match filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9bc6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9bc6-105">Syntax</span></span>


```C++
DWORD SetNPPPatternFilterInBlob(
  _In_  HBLOB        hBlob,
  _In_  LPEXPRESSION pExpression,
  _Out_ HBLOB        hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="a9bc6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9bc6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9bc6-107">*hblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9bc6-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9bc6-108">Das Handle für das BLOB.</span><span class="sxs-lookup"><span data-stu-id="a9bc6-108">The handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="a9bc6-109">*pexpression* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9bc6-109">*pExpression* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9bc6-110">Ein Zeiger auf eine [Ausdrucks](expression.md) Struktur, die den festgelegten Filter Ausdruck definiert.</span><span class="sxs-lookup"><span data-stu-id="a9bc6-110">A pointer to an [EXPRESSION](expression.md) structure that defines the filter expression being set.</span></span>

</dd> <dt>

<span data-ttu-id="a9bc6-111">*herrorblob* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a9bc6-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9bc6-112">Das Handle für ein fehlerblob, das angibt, wo der Fehler im ursprünglichen BLOB aufgetreten ist (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="a9bc6-112">The handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9bc6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a9bc6-113">Return value</span></span>

<span data-ttu-id="a9bc6-114">Wenn die **setnpppatternfilterinblob** -Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="a9bc6-114">If the **SetNPPPatternFilterInBlob** function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="a9bc6-115">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="a9bc6-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9bc6-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9bc6-116">Remarks</span></span>

<span data-ttu-id="a9bc6-117">Das Muster entspricht den Filterdaten, die in der Kategorie " **config** " des BLOBs gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="a9bc6-117">The pattern match filter data stored in the **Config** category of the BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9bc6-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9bc6-118">Requirements</span></span>



| <span data-ttu-id="a9bc6-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9bc6-119">Requirement</span></span> | <span data-ttu-id="a9bc6-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a9bc6-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9bc6-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a9bc6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a9bc6-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9bc6-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a9bc6-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a9bc6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a9bc6-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9bc6-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a9bc6-125">Header</span><span class="sxs-lookup"><span data-stu-id="a9bc6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9bc6-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9bc6-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="a9bc6-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a9bc6-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="a9bc6-128"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9bc6-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="a9bc6-129">DLL</span><span class="sxs-lookup"><span data-stu-id="a9bc6-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9bc6-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9bc6-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9bc6-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9bc6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9bc6-132">Getnppaddressfilterfromblob</span><span class="sxs-lookup"><span data-stu-id="a9bc6-132">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="a9bc6-133">Setboolinblob</span><span class="sxs-lookup"><span data-stu-id="a9bc6-133">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="a9bc6-134">Setclassidinblob</span><span class="sxs-lookup"><span data-stu-id="a9bc6-134">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="a9bc6-135">Setdwordinblob</span><span class="sxs-lookup"><span data-stu-id="a9bc6-135">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="a9bc6-136">Setmacaddressinblob</span><span class="sxs-lookup"><span data-stu-id="a9bc6-136">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="a9bc6-137">Setnetworkinfoinblob</span><span class="sxs-lookup"><span data-stu-id="a9bc6-137">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="a9bc6-138">Setnppaddressfilterinblob</span><span class="sxs-lookup"><span data-stu-id="a9bc6-138">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="a9bc6-139">Setnpptriggerinblob</span><span class="sxs-lookup"><span data-stu-id="a9bc6-139">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="a9bc6-140">Setstringinblob</span><span class="sxs-lookup"><span data-stu-id="a9bc6-140">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




