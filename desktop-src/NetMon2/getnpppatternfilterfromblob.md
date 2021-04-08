---
description: Die getnpppatternfilterfromblob-Funktion Ruft den Muster Übereinstimmungs Filter aus einem bestimmten BLOB ab.
ms.assetid: b17cde55-8abb-4699-960f-676cbbb24326
title: Getnpppatternfilterfromblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPPatternFilterFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5758c53fe21231d300058a9168e556e9f9ceaa43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750081"
---
# <a name="getnpppatternfilterfromblob-function"></a><span data-ttu-id="1b307-103">Getnpppatternfilterfromblob-Funktion</span><span class="sxs-lookup"><span data-stu-id="1b307-103">GetNPPPatternFilterFromBlob function</span></span>

<span data-ttu-id="1b307-104">Die **getnpppatternfilterfromblob** -Funktion Ruft den Muster Übereinstimmungs Filter aus einem bestimmten BLOB ab.</span><span class="sxs-lookup"><span data-stu-id="1b307-104">The **GetNPPPatternFilterFromBlob** function retrieves the pattern match filter from a specific BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b307-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b307-105">Syntax</span></span>


```C++
DWORD GetNPPPatternFilterFromBlob(
  _In_  HBLOB        hBlob,
  _In_  LPEXPRESSION pExpression,
  _Out_ HBLOB        hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="1b307-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b307-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b307-107">*hblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b307-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b307-108">Handle für das BLOB.</span><span class="sxs-lookup"><span data-stu-id="1b307-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="1b307-109">*pexpression* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b307-109">*pExpression* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b307-110">Zeiger auf den Filter Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="1b307-110">Pointer to the filter expression.</span></span>

</dd> <dt>

<span data-ttu-id="1b307-111">*herrorblob* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1b307-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b307-112">Handle für ein fehlerblob, das angibt, wo der Fehler im ursprünglichen BLOB aufgetreten ist (falls vorhanden).</span><span class="sxs-lookup"><span data-stu-id="1b307-112">Handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b307-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b307-113">Return value</span></span>

<span data-ttu-id="1b307-114">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="1b307-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="1b307-115">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="1b307-115">If the function is unsuccessful, the return value is a NMERR that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b307-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b307-116">Remarks</span></span>

<span data-ttu-id="1b307-117">Die Filter Informationen für die Muster Übereinstimmung werden in der Kategorie **config** des BLOBs gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1b307-117">The pattern match filter information is stored in the **Config** category of the BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b307-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b307-118">Requirements</span></span>



| <span data-ttu-id="1b307-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b307-119">Requirement</span></span> | <span data-ttu-id="1b307-120">Wert</span><span class="sxs-lookup"><span data-stu-id="1b307-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b307-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b307-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1b307-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b307-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1b307-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b307-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1b307-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b307-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1b307-125">Header</span><span class="sxs-lookup"><span data-stu-id="1b307-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b307-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b307-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="1b307-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1b307-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="1b307-128"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b307-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="1b307-129">DLL</span><span class="sxs-lookup"><span data-stu-id="1b307-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b307-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b307-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b307-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b307-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b307-132">Setnpppatternfilterinblob</span><span class="sxs-lookup"><span data-stu-id="1b307-132">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="1b307-133">Getboolfromblob</span><span class="sxs-lookup"><span data-stu-id="1b307-133">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="1b307-134">Getclassidfromblob</span><span class="sxs-lookup"><span data-stu-id="1b307-134">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="1b307-135">Getdwordfromblob</span><span class="sxs-lookup"><span data-stu-id="1b307-135">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="1b307-136">Getmacaddressfromblob</span><span class="sxs-lookup"><span data-stu-id="1b307-136">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="1b307-137">Getnetworkinfofromblob</span><span class="sxs-lookup"><span data-stu-id="1b307-137">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="1b307-138">Getnppaddressfilterfromblob</span><span class="sxs-lookup"><span data-stu-id="1b307-138">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="1b307-139">Getnpptriggerfromblob</span><span class="sxs-lookup"><span data-stu-id="1b307-139">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="1b307-140">Getstringfromblob</span><span class="sxs-lookup"><span data-stu-id="1b307-140">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="1b307-141">Getstringsfromblob</span><span class="sxs-lookup"><span data-stu-id="1b307-141">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




