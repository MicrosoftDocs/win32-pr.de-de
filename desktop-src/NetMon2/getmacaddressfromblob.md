---
description: Die getmacaddressfromblob-Funktion Ruft die benannte Mac-Adresse aus einem BLOB ab.
ms.assetid: 1769c92c-0946-447c-885a-fcf175fa1bf3
title: Getmacaddressfromblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetMacAddressFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 022d4f618c09652c368f6664b194b4ebafc81717
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363366"
---
# <a name="getmacaddressfromblob-function"></a><span data-ttu-id="3dca2-103">Getmacaddressfromblob-Funktion</span><span class="sxs-lookup"><span data-stu-id="3dca2-103">GetMacAddressFromBlob function</span></span>

<span data-ttu-id="3dca2-104">Die **getmacaddressfromblob** -Funktion Ruft die benannte Mac-Adresse aus einem BLOB ab.</span><span class="sxs-lookup"><span data-stu-id="3dca2-104">The **GetMacAddressFromBlob** function retrieves the named MAC address from a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dca2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3dca2-105">Syntax</span></span>


```C++
DWORD GetMacAddressFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       BYTE  *pMacAddress
);
```



## <a name="parameters"></a><span data-ttu-id="3dca2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3dca2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dca2-107">*hblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3dca2-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dca2-108">Handle für ein BLOB.</span><span class="sxs-lookup"><span data-stu-id="3dca2-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="3dca2-109">*pownername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3dca2-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dca2-110">Zeiger auf den Namen des BLOB-Besitzers.</span><span class="sxs-lookup"><span data-stu-id="3dca2-110">Pointer to the BLOB owner name.</span></span>

</dd> <dt>

<span data-ttu-id="3dca2-111">*pcategoryname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3dca2-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dca2-112">Zeiger auf den BLOB-Kategoriename.</span><span class="sxs-lookup"><span data-stu-id="3dca2-112">Pointer to the BLOB category name.</span></span>

</dd> <dt>

<span data-ttu-id="3dca2-113">*ptagname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3dca2-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dca2-114">Zeiger auf den BLOB-Tagnamen.</span><span class="sxs-lookup"><span data-stu-id="3dca2-114">Pointer to the BLOB tag name.</span></span>

</dd> <dt>

<span data-ttu-id="3dca2-115">*pmacaddress* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3dca2-115">*pMacAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3dca2-116">Ein Zeiger auf die Mac-Adresse des BLOBs.</span><span class="sxs-lookup"><span data-stu-id="3dca2-116">Pointer to the MAC address of the BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dca2-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3dca2-117">Return value</span></span>

<span data-ttu-id="3dca2-118">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="3dca2-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="3dca2-119">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler beschreibt.</span><span class="sxs-lookup"><span data-stu-id="3dca2-119">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dca2-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3dca2-120">Requirements</span></span>



| <span data-ttu-id="3dca2-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3dca2-121">Requirement</span></span> | <span data-ttu-id="3dca2-122">Wert</span><span class="sxs-lookup"><span data-stu-id="3dca2-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3dca2-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3dca2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3dca2-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3dca2-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3dca2-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3dca2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3dca2-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3dca2-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3dca2-127">Header</span><span class="sxs-lookup"><span data-stu-id="3dca2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dca2-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3dca2-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="3dca2-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3dca2-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="3dca2-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3dca2-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="3dca2-131">DLL</span><span class="sxs-lookup"><span data-stu-id="3dca2-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3dca2-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3dca2-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dca2-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3dca2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dca2-134">Setmacaddressinblob</span><span class="sxs-lookup"><span data-stu-id="3dca2-134">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="3dca2-135">Getboolfromblob</span><span class="sxs-lookup"><span data-stu-id="3dca2-135">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="3dca2-136">Getclassidfromblob</span><span class="sxs-lookup"><span data-stu-id="3dca2-136">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="3dca2-137">Getdwordfromblob</span><span class="sxs-lookup"><span data-stu-id="3dca2-137">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="3dca2-138">Getnetworkinfofromblob</span><span class="sxs-lookup"><span data-stu-id="3dca2-138">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="3dca2-139">Getnppaddressfilterfromblob</span><span class="sxs-lookup"><span data-stu-id="3dca2-139">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="3dca2-140">Getnpppatternfilterfromblob</span><span class="sxs-lookup"><span data-stu-id="3dca2-140">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="3dca2-141">Getnpptriggerfromblob</span><span class="sxs-lookup"><span data-stu-id="3dca2-141">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="3dca2-142">Getstringfromblob</span><span class="sxs-lookup"><span data-stu-id="3dca2-142">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="3dca2-143">Getstringsfromblob</span><span class="sxs-lookup"><span data-stu-id="3dca2-143">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




