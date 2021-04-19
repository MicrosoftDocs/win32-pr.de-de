---
description: Die getnpptriggerfromblob-Funktion Ruft den Trigger aus dem angegebenen BLOB ab.
ms.assetid: 48a27cf3-57b0-4241-a925-4209e0d384e2
title: Getnpptriggerfromblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPTriggerFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 11622078354012de4796ddd43a698ac812951742
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343041"
---
# <a name="getnpptriggerfromblob-function"></a><span data-ttu-id="76f35-103">Getnpptriggerfromblob-Funktion</span><span class="sxs-lookup"><span data-stu-id="76f35-103">GetNPPTriggerFromBlob function</span></span>

<span data-ttu-id="76f35-104">Die **getnpptriggerfromblob** -Funktion Ruft den Trigger aus dem angegebenen BLOB ab.</span><span class="sxs-lookup"><span data-stu-id="76f35-104">The **GetNPPTriggerFromBlob** function retrieves the trigger from the given BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="76f35-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="76f35-105">Syntax</span></span>


```C++
DWORD GetNPPTriggerFromBlob(
  _In_  HBLOB     hBlob,
  _Out_ LPTRIGGER pTrigger,
  _Out_ HBLOB     hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="76f35-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="76f35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76f35-107">*hblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76f35-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76f35-108">Handle für das BLOB.</span><span class="sxs-lookup"><span data-stu-id="76f35-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="76f35-109">*p-Auslösung* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="76f35-109">*pTrigger* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76f35-110">Zeiger auf den Wert des Auslösers.</span><span class="sxs-lookup"><span data-stu-id="76f35-110">Pointer to the trigger value.</span></span>

</dd> <dt>

<span data-ttu-id="76f35-111">*herrorblob* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="76f35-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76f35-112">Handle für ein fehlerblob, das angibt, wo der Fehler im ursprünglichen BLOB aufgetreten ist (falls vorhanden).</span><span class="sxs-lookup"><span data-stu-id="76f35-112">Handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76f35-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76f35-113">Return value</span></span>

<span data-ttu-id="76f35-114">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="76f35-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="76f35-115">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="76f35-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="76f35-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76f35-116">Remarks</span></span>

<span data-ttu-id="76f35-117">Die Trigger-Informationen werden in der **Trigger** -Kategorie des BLOBs gespeichert.</span><span class="sxs-lookup"><span data-stu-id="76f35-117">The trigger information is stored in the **Trigger** category of the BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="76f35-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76f35-118">Requirements</span></span>



| <span data-ttu-id="76f35-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76f35-119">Requirement</span></span> | <span data-ttu-id="76f35-120">Wert</span><span class="sxs-lookup"><span data-stu-id="76f35-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76f35-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76f35-121">Minimum supported client</span></span><br/> | <span data-ttu-id="76f35-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76f35-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="76f35-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76f35-123">Minimum supported server</span></span><br/> | <span data-ttu-id="76f35-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76f35-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="76f35-125">Header</span><span class="sxs-lookup"><span data-stu-id="76f35-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="76f35-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="76f35-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="76f35-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="76f35-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="76f35-128"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="76f35-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="76f35-129">DLL</span><span class="sxs-lookup"><span data-stu-id="76f35-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76f35-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76f35-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76f35-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76f35-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76f35-132">Getboolfromblob</span><span class="sxs-lookup"><span data-stu-id="76f35-132">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="76f35-133">Getclassidfromblob</span><span class="sxs-lookup"><span data-stu-id="76f35-133">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="76f35-134">Getdwordfromblob</span><span class="sxs-lookup"><span data-stu-id="76f35-134">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="76f35-135">Getmacaddressfromblob</span><span class="sxs-lookup"><span data-stu-id="76f35-135">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="76f35-136">Getnetworkinfofromblob</span><span class="sxs-lookup"><span data-stu-id="76f35-136">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="76f35-137">Getnppaddressfilterfromblob</span><span class="sxs-lookup"><span data-stu-id="76f35-137">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="76f35-138">Getnpppatternfilterfromblob</span><span class="sxs-lookup"><span data-stu-id="76f35-138">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="76f35-139">Getstringfromblob</span><span class="sxs-lookup"><span data-stu-id="76f35-139">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="76f35-140">Getstringsfromblob</span><span class="sxs-lookup"><span data-stu-id="76f35-140">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




