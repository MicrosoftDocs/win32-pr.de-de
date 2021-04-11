---
description: Mit der getclassidfromblob-Funktion wird ein benannter klassenbezeichnerwert aus einem BLOB abgerufen.
ms.assetid: fef29a42-ccd3-4655-958c-d150e5bcd0d7
title: Getclassidfromblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetClassIDFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 70122422c47a986058322ca8d17082093e02a4b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128344"
---
# <a name="getclassidfromblob-function"></a><span data-ttu-id="da0c0-103">Getclassidfromblob-Funktion</span><span class="sxs-lookup"><span data-stu-id="da0c0-103">GetClassIDFromBlob function</span></span>

<span data-ttu-id="da0c0-104">Mit der **getclassidfromblob** -Funktion wird ein benannter klassenbezeichnerwert aus einem BLOB abgerufen.</span><span class="sxs-lookup"><span data-stu-id="da0c0-104">The **GetClassIDFromBlob** function retrieves a named class identifier value from a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="da0c0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="da0c0-105">Syntax</span></span>


```C++
DWORD GetClassIDFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="da0c0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="da0c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da0c0-107">*hblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da0c0-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da0c0-108">Handle für ein BLOB.</span><span class="sxs-lookup"><span data-stu-id="da0c0-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="da0c0-109">*pownername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da0c0-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da0c0-110">Zeiger auf den Namen des BLOB-Besitzers.</span><span class="sxs-lookup"><span data-stu-id="da0c0-110">Pointer to the BLOB owner name.</span></span>

</dd> <dt>

<span data-ttu-id="da0c0-111">*pcategoryname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da0c0-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da0c0-112">Zeiger auf den BLOB-Kategoriename.</span><span class="sxs-lookup"><span data-stu-id="da0c0-112">Pointer to the BLOB category name.</span></span>

</dd> <dt>

<span data-ttu-id="da0c0-113">*ptagname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da0c0-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da0c0-114">Zeiger auf den BLOB-Tagnamen.</span><span class="sxs-lookup"><span data-stu-id="da0c0-114">Pointer to the BLOB tag name.</span></span>

</dd> <dt>

<span data-ttu-id="da0c0-115">*pclsid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="da0c0-115">*pClsID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da0c0-116">Zeiger auf den BLOB-Klassen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="da0c0-116">Pointer to the BLOB class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da0c0-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da0c0-117">Return value</span></span>

<span data-ttu-id="da0c0-118">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="da0c0-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="da0c0-119">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler beschreibt.</span><span class="sxs-lookup"><span data-stu-id="da0c0-119">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="da0c0-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da0c0-120">Requirements</span></span>



| <span data-ttu-id="da0c0-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da0c0-121">Requirement</span></span> | <span data-ttu-id="da0c0-122">Wert</span><span class="sxs-lookup"><span data-stu-id="da0c0-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da0c0-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da0c0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="da0c0-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da0c0-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="da0c0-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da0c0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="da0c0-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da0c0-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="da0c0-127">Header</span><span class="sxs-lookup"><span data-stu-id="da0c0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="da0c0-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="da0c0-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="da0c0-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="da0c0-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="da0c0-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="da0c0-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="da0c0-131">DLL</span><span class="sxs-lookup"><span data-stu-id="da0c0-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da0c0-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da0c0-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da0c0-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da0c0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da0c0-134">Setclassidinblob</span><span class="sxs-lookup"><span data-stu-id="da0c0-134">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="da0c0-135">Getboolfromblob</span><span class="sxs-lookup"><span data-stu-id="da0c0-135">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="da0c0-136">Getdwordfromblob</span><span class="sxs-lookup"><span data-stu-id="da0c0-136">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="da0c0-137">Getmacaddressfromblob</span><span class="sxs-lookup"><span data-stu-id="da0c0-137">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="da0c0-138">Getnetworkinfofromblob</span><span class="sxs-lookup"><span data-stu-id="da0c0-138">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="da0c0-139">Getnppaddressfilterfromblob</span><span class="sxs-lookup"><span data-stu-id="da0c0-139">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="da0c0-140">Getnpppatternfilterfromblob</span><span class="sxs-lookup"><span data-stu-id="da0c0-140">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="da0c0-141">Getnpptriggerfromblob</span><span class="sxs-lookup"><span data-stu-id="da0c0-141">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="da0c0-142">Getstringfromblob</span><span class="sxs-lookup"><span data-stu-id="da0c0-142">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="da0c0-143">Getstringsfromblob</span><span class="sxs-lookup"><span data-stu-id="da0c0-143">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




