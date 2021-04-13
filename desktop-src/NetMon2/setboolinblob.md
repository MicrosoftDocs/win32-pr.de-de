---
description: Die setboolinblob-Funktion legt einen booleschen Wert an einer bestimmten Position innerhalb eines BLOBs fest.
ms.assetid: 354d22be-b8c4-4068-8356-19b30ac188d0
title: Setboolinblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetBoolInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5cfbb9a3410d511ab143f1d77584a0144435c230
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528640"
---
# <a name="setboolinblob-function"></a><span data-ttu-id="50d8a-103">Setboolinblob-Funktion</span><span class="sxs-lookup"><span data-stu-id="50d8a-103">SetBoolInBlob function</span></span>

<span data-ttu-id="50d8a-104">Die **setboolinblob** -Funktion legt einen booleschen Wert an einer bestimmten Position innerhalb eines BLOBs fest.</span><span class="sxs-lookup"><span data-stu-id="50d8a-104">The **SetBoolInBlob** function sets a Boolean value at a given location within a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="50d8a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="50d8a-105">Syntax</span></span>


```C++
DWORD SetBoolInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_       BOOL  Bool
);
```



## <a name="parameters"></a><span data-ttu-id="50d8a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="50d8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50d8a-107">*hblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50d8a-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50d8a-108">Handle für ein BLOB.</span><span class="sxs-lookup"><span data-stu-id="50d8a-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="50d8a-109">*pownername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50d8a-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50d8a-110">Zeiger auf den Namen des BLOB- **Besitzers** .</span><span class="sxs-lookup"><span data-stu-id="50d8a-110">Pointer to the BLOB **Owner** name.</span></span>

</dd> <dt>

<span data-ttu-id="50d8a-111">*pcategoryname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50d8a-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50d8a-112">Zeiger auf den BLOB- **Kategoriename** .</span><span class="sxs-lookup"><span data-stu-id="50d8a-112">Pointer to the BLOB **Category** name.</span></span>

</dd> <dt>

<span data-ttu-id="50d8a-113">*ptagname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50d8a-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50d8a-114">Zeiger auf den BLOB- **Tagnamen** .</span><span class="sxs-lookup"><span data-stu-id="50d8a-114">Pointer to the BLOB **Tag** name.</span></span>

</dd> <dt>

<span data-ttu-id="50d8a-115">*Bool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50d8a-115">*Bool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50d8a-116">Boolescher Wert, der an der angegebenen Position festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="50d8a-116">Boolean value that is set at the given location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50d8a-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50d8a-117">Return value</span></span>

<span data-ttu-id="50d8a-118">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="50d8a-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="50d8a-119">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="50d8a-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="50d8a-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50d8a-120">Requirements</span></span>



| <span data-ttu-id="50d8a-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50d8a-121">Requirement</span></span> | <span data-ttu-id="50d8a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="50d8a-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50d8a-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50d8a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="50d8a-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50d8a-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="50d8a-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50d8a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="50d8a-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50d8a-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="50d8a-127">Header</span><span class="sxs-lookup"><span data-stu-id="50d8a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="50d8a-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="50d8a-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="50d8a-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="50d8a-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="50d8a-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50d8a-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="50d8a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="50d8a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50d8a-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50d8a-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50d8a-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50d8a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50d8a-134">Getboolfromblob</span><span class="sxs-lookup"><span data-stu-id="50d8a-134">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="50d8a-135">Setclassidinblob</span><span class="sxs-lookup"><span data-stu-id="50d8a-135">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="50d8a-136">Setdwordinblob</span><span class="sxs-lookup"><span data-stu-id="50d8a-136">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="50d8a-137">Setmacaddressinblob</span><span class="sxs-lookup"><span data-stu-id="50d8a-137">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="50d8a-138">Setnetworkinfoinblob</span><span class="sxs-lookup"><span data-stu-id="50d8a-138">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="50d8a-139">Setnppaddressfilterinblob</span><span class="sxs-lookup"><span data-stu-id="50d8a-139">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="50d8a-140">Setnpppatternfilterinblob</span><span class="sxs-lookup"><span data-stu-id="50d8a-140">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="50d8a-141">Setnpptriggerinblob</span><span class="sxs-lookup"><span data-stu-id="50d8a-141">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="50d8a-142">Setstringinblob</span><span class="sxs-lookup"><span data-stu-id="50d8a-142">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




