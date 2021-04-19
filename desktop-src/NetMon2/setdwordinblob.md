---
description: Die setdwordinblob-Funktion legt den benannten DWORD-Wert eines BLOBs fest.
ms.assetid: 9174cd5c-4442-4fbe-8dc7-f8a74e1cc85d
title: Setdwordinblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetDwordInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 9bca0efe61824c6fb8dd41b0b241791b6303799d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348308"
---
# <a name="setdwordinblob-function"></a><span data-ttu-id="46c6d-103">Setdwordinblob-Funktion</span><span class="sxs-lookup"><span data-stu-id="46c6d-103">SetDwordInBlob function</span></span>

<span data-ttu-id="46c6d-104">Die **setdwordinblob** -Funktion legt den benannten **DWORD** -Wert eines BLOBs fest.</span><span class="sxs-lookup"><span data-stu-id="46c6d-104">The **SetDwordInBlob** function sets the named **DWORD** value of a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="46c6d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="46c6d-105">Syntax</span></span>


```C++
DWORD SetDwordInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_       DWORD Dword
);
```



## <a name="parameters"></a><span data-ttu-id="46c6d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="46c6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46c6d-107">*hblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46c6d-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46c6d-108">Handle für ein BLOB, das festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="46c6d-108">Handle to a BLOB being set.</span></span>

</dd> <dt>

<span data-ttu-id="46c6d-109">*pownername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46c6d-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46c6d-110">Zeiger auf den Namen des BLOB- **Besitzers** , der festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="46c6d-110">Pointer to the BLOB **Owner** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="46c6d-111">*pcategoryname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46c6d-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46c6d-112">Zeiger auf den Namen der BLOB- **Kategorie** , die festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="46c6d-112">Pointer to the BLOB **Category** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="46c6d-113">*ptagname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46c6d-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46c6d-114">Zeiger auf den festzulegenden BLOB- **Tagnamen** .</span><span class="sxs-lookup"><span data-stu-id="46c6d-114">Pointer to the BLOB **Tag** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="46c6d-115">*DWORD* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46c6d-115">*Dword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46c6d-116">Der **DWORD** -Wert des festzulegenden BLOBs.</span><span class="sxs-lookup"><span data-stu-id="46c6d-116">**DWORD** value of the BLOB being set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46c6d-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46c6d-117">Return value</span></span>

<span data-ttu-id="46c6d-118">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="46c6d-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="46c6d-119">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="46c6d-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="46c6d-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46c6d-120">Requirements</span></span>



| <span data-ttu-id="46c6d-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46c6d-121">Requirement</span></span> | <span data-ttu-id="46c6d-122">Wert</span><span class="sxs-lookup"><span data-stu-id="46c6d-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46c6d-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="46c6d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="46c6d-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46c6d-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="46c6d-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="46c6d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="46c6d-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46c6d-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="46c6d-127">Header</span><span class="sxs-lookup"><span data-stu-id="46c6d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="46c6d-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="46c6d-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="46c6d-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="46c6d-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="46c6d-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46c6d-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="46c6d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="46c6d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46c6d-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46c6d-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46c6d-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46c6d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46c6d-134">Getdwordfromblob</span><span class="sxs-lookup"><span data-stu-id="46c6d-134">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="46c6d-135">Setboolinblob</span><span class="sxs-lookup"><span data-stu-id="46c6d-135">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="46c6d-136">Setclassidinblob</span><span class="sxs-lookup"><span data-stu-id="46c6d-136">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="46c6d-137">Setmacaddressinblob</span><span class="sxs-lookup"><span data-stu-id="46c6d-137">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="46c6d-138">Setnetworkinfoinblob</span><span class="sxs-lookup"><span data-stu-id="46c6d-138">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="46c6d-139">Setnppaddressfilterinblob</span><span class="sxs-lookup"><span data-stu-id="46c6d-139">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="46c6d-140">Setnpppatternfilterinblob</span><span class="sxs-lookup"><span data-stu-id="46c6d-140">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="46c6d-141">Setnpptriggerinblob</span><span class="sxs-lookup"><span data-stu-id="46c6d-141">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="46c6d-142">Setstringinblob</span><span class="sxs-lookup"><span data-stu-id="46c6d-142">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




