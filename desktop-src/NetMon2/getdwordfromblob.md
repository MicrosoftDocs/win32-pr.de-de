---
description: Die getdwordfromblob-Funktion Ruft den benannten DWORD-Wert aus einem BLOB ab.
ms.assetid: edad74a7-b726-46d9-b49f-9984272d0a29
title: Getdwordfromblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDwordFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 064985f0f3b9a235dc1c00d683fe4b11371df87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128340"
---
# <a name="getdwordfromblob-function"></a><span data-ttu-id="abf20-103">Getdwordfromblob-Funktion</span><span class="sxs-lookup"><span data-stu-id="abf20-103">GetDwordFromBlob function</span></span>

<span data-ttu-id="abf20-104">Die **getdwordfromblob** -Funktion Ruft den benannten **DWORD** -Wert aus einem BLOB ab.</span><span class="sxs-lookup"><span data-stu-id="abf20-104">The **GetDwordFromBlob** function retrieves the named **DWORD** value from a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="abf20-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="abf20-105">Syntax</span></span>


```C++
DWORD GetDwordFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       DWORD *pDword
);
```



## <a name="parameters"></a><span data-ttu-id="abf20-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="abf20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abf20-107">*hblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="abf20-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abf20-108">Handle für ein BLOB.</span><span class="sxs-lookup"><span data-stu-id="abf20-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="abf20-109">*pownername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="abf20-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abf20-110">Zeiger auf den Namen des BLOB-Besitzers.</span><span class="sxs-lookup"><span data-stu-id="abf20-110">Pointer to the BLOB owner name.</span></span>

</dd> <dt>

<span data-ttu-id="abf20-111">*pcategoryname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="abf20-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abf20-112">Zeiger auf den BLOB-Kategoriename.</span><span class="sxs-lookup"><span data-stu-id="abf20-112">Pointer to the BLOB category name.</span></span>

</dd> <dt>

<span data-ttu-id="abf20-113">*ptagname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="abf20-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abf20-114">Zeiger auf den BLOB-Tagnamen.</span><span class="sxs-lookup"><span data-stu-id="abf20-114">Pointer to the BLOB tag name.</span></span>

</dd> <dt>

<span data-ttu-id="abf20-115">*PDWORD* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="abf20-115">*pDword* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abf20-116">Zeiger auf den **DWORD** -Wert des BLOBs.</span><span class="sxs-lookup"><span data-stu-id="abf20-116">Pointer to the **DWORD** value of the BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abf20-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="abf20-117">Return value</span></span>

<span data-ttu-id="abf20-118">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="abf20-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="abf20-119">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler beschreibt.</span><span class="sxs-lookup"><span data-stu-id="abf20-119">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="abf20-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abf20-120">Requirements</span></span>



| <span data-ttu-id="abf20-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="abf20-121">Requirement</span></span> | <span data-ttu-id="abf20-122">Wert</span><span class="sxs-lookup"><span data-stu-id="abf20-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="abf20-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="abf20-123">Minimum supported client</span></span><br/> | <span data-ttu-id="abf20-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abf20-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="abf20-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="abf20-125">Minimum supported server</span></span><br/> | <span data-ttu-id="abf20-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abf20-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="abf20-127">Header</span><span class="sxs-lookup"><span data-stu-id="abf20-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="abf20-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="abf20-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="abf20-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="abf20-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="abf20-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="abf20-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="abf20-131">DLL</span><span class="sxs-lookup"><span data-stu-id="abf20-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abf20-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abf20-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abf20-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abf20-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abf20-134">Setdwordinblob</span><span class="sxs-lookup"><span data-stu-id="abf20-134">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="abf20-135">Getboolfromblob</span><span class="sxs-lookup"><span data-stu-id="abf20-135">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="abf20-136">Getclassidfromblob</span><span class="sxs-lookup"><span data-stu-id="abf20-136">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="abf20-137">Getmacaddressfromblob</span><span class="sxs-lookup"><span data-stu-id="abf20-137">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="abf20-138">Getnetworkinfofromblob</span><span class="sxs-lookup"><span data-stu-id="abf20-138">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="abf20-139">Getnppaddressfilterfromblob</span><span class="sxs-lookup"><span data-stu-id="abf20-139">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="abf20-140">Getnpppatternfilterfromblob</span><span class="sxs-lookup"><span data-stu-id="abf20-140">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="abf20-141">Getnpptriggerfromblob</span><span class="sxs-lookup"><span data-stu-id="abf20-141">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="abf20-142">Getstringfromblob</span><span class="sxs-lookup"><span data-stu-id="abf20-142">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="abf20-143">Getstringsfromblob</span><span class="sxs-lookup"><span data-stu-id="abf20-143">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




