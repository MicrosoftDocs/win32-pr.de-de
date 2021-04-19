---
description: Ruft einen benannten booleschen Wert aus einem BLOB ab.
ms.assetid: 26acfd2a-5b17-47ad-8f7b-7793174a13c3
title: Getboolfromblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBoolFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: e09a35f71181343cd401b3288c2b2c74a46f677b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346275"
---
# <a name="getboolfromblob-function"></a><span data-ttu-id="60d79-103">Getboolfromblob-Funktion</span><span class="sxs-lookup"><span data-stu-id="60d79-103">GetBoolFromBlob function</span></span>

<span data-ttu-id="60d79-104">Mit der **getboolfromblob** -Funktion wird ein benannter boolescher Wert aus einem BLOB abgerufen.</span><span class="sxs-lookup"><span data-stu-id="60d79-104">The **GetBoolFromBlob** function retrieves a named Boolean value from a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="60d79-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="60d79-105">Syntax</span></span>


```C++
DWORD GetBoolFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       BOOL  *pBool
);
```



## <a name="parameters"></a><span data-ttu-id="60d79-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="60d79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60d79-107">*hblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60d79-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60d79-108">Ein Handle für ein BLOB.</span><span class="sxs-lookup"><span data-stu-id="60d79-108">A handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="60d79-109">*pownername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60d79-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60d79-110">Ein Zeiger auf den Namen des BLOB-Besitzers.</span><span class="sxs-lookup"><span data-stu-id="60d79-110">A pointer to the BLOB owner name.</span></span>

</dd> <dt>

<span data-ttu-id="60d79-111">*pcategoryname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60d79-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60d79-112">Ein Zeiger auf den BLOB-Kategoriename.</span><span class="sxs-lookup"><span data-stu-id="60d79-112">A pointer to the BLOB category name.</span></span>

</dd> <dt>

<span data-ttu-id="60d79-113">*ptagname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60d79-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60d79-114">Ein Zeiger auf den BLOB-Tagnamen.</span><span class="sxs-lookup"><span data-stu-id="60d79-114">A pointer to the BLOB tag name.</span></span>

</dd> <dt>

<span data-ttu-id="60d79-115">*pbool* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="60d79-115">*pBool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60d79-116">Zeiger auf den booleschen Wert des BLOBs.</span><span class="sxs-lookup"><span data-stu-id="60d79-116">Pointer to the Boolean value of the BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60d79-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="60d79-117">Return value</span></span>

<span data-ttu-id="60d79-118">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="60d79-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="60d79-119">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler beschreibt.</span><span class="sxs-lookup"><span data-stu-id="60d79-119">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="60d79-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60d79-120">Requirements</span></span>



| <span data-ttu-id="60d79-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60d79-121">Requirement</span></span> | <span data-ttu-id="60d79-122">Wert</span><span class="sxs-lookup"><span data-stu-id="60d79-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60d79-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60d79-123">Minimum supported client</span></span><br/> | <span data-ttu-id="60d79-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60d79-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="60d79-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="60d79-125">Minimum supported server</span></span><br/> | <span data-ttu-id="60d79-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60d79-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="60d79-127">Header</span><span class="sxs-lookup"><span data-stu-id="60d79-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="60d79-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="60d79-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="60d79-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="60d79-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="60d79-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60d79-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="60d79-131">DLL</span><span class="sxs-lookup"><span data-stu-id="60d79-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60d79-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60d79-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60d79-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60d79-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60d79-134">Setboolinblob</span><span class="sxs-lookup"><span data-stu-id="60d79-134">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="60d79-135">Getclassidfromblob</span><span class="sxs-lookup"><span data-stu-id="60d79-135">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="60d79-136">Getdwordfromblob</span><span class="sxs-lookup"><span data-stu-id="60d79-136">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="60d79-137">Getmacaddressfromblob</span><span class="sxs-lookup"><span data-stu-id="60d79-137">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="60d79-138">Getnetworkinfofromblob</span><span class="sxs-lookup"><span data-stu-id="60d79-138">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="60d79-139">Getnppaddressfilterfromblob</span><span class="sxs-lookup"><span data-stu-id="60d79-139">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="60d79-140">Getnpppatternfilterfromblob</span><span class="sxs-lookup"><span data-stu-id="60d79-140">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="60d79-141">Getnpptriggerfromblob</span><span class="sxs-lookup"><span data-stu-id="60d79-141">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="60d79-142">Getstringfromblob</span><span class="sxs-lookup"><span data-stu-id="60d79-142">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="60d79-143">Getstringsfromblob</span><span class="sxs-lookup"><span data-stu-id="60d79-143">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




