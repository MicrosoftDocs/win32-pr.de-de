---
description: Die setmacaddressinblob-Funktion legt die angeforderte Mac-Adresse eines BLOBs fest.
ms.assetid: f44d0cec-ced7-4d2a-a58e-aeb476bfe800
title: Setmacaddressinblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetMacAddressInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 2183f5635dcdb15362a86a77ae2b3c109c71dbd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866699"
---
# <a name="setmacaddressinblob-function"></a><span data-ttu-id="b424f-103">Setmacaddressinblob-Funktion</span><span class="sxs-lookup"><span data-stu-id="b424f-103">SetMacAddressInBlob function</span></span>

<span data-ttu-id="b424f-104">Die **setmacaddressinblob** -Funktion legt die angeforderte Mac-Adresse eines BLOBs fest.</span><span class="sxs-lookup"><span data-stu-id="b424f-104">The **SetMacAddressInBlob** function sets the requested MAC address of a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="b424f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b424f-105">Syntax</span></span>


```C++
DWORD SetMacAddressInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const BYTE  *pMacAddress
);
```



## <a name="parameters"></a><span data-ttu-id="b424f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b424f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b424f-107">*hblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b424f-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b424f-108">Handle für das festzulegende BLOB.</span><span class="sxs-lookup"><span data-stu-id="b424f-108">Handle to the BLOB being set.</span></span>

</dd> <dt>

<span data-ttu-id="b424f-109">*pownername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b424f-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b424f-110">Zeiger auf den Namen des BLOB- **Besitzers** , der festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="b424f-110">Pointer to the BLOB **Owner** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="b424f-111">*pcategoryname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b424f-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b424f-112">Zeiger auf den Namen der BLOB- **Kategorie** , die festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="b424f-112">Pointer to the BLOB **Category** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="b424f-113">*ptagname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b424f-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b424f-114">Zeiger auf den festzulegenden BLOB- **Tagnamen** .</span><span class="sxs-lookup"><span data-stu-id="b424f-114">Pointer to the BLOB **Tag** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="b424f-115">*pmacaddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b424f-115">*pMacAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b424f-116">Ein Zeiger auf die Mac-Adresse des festgelegten BLOBs.</span><span class="sxs-lookup"><span data-stu-id="b424f-116">Pointer to the MAC address of the BLOB being set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b424f-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b424f-117">Return value</span></span>

<span data-ttu-id="b424f-118">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="b424f-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="b424f-119">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="b424f-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="b424f-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b424f-120">Requirements</span></span>



| <span data-ttu-id="b424f-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b424f-121">Requirement</span></span> | <span data-ttu-id="b424f-122">Wert</span><span class="sxs-lookup"><span data-stu-id="b424f-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b424f-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b424f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b424f-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b424f-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b424f-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b424f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b424f-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b424f-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b424f-127">Header</span><span class="sxs-lookup"><span data-stu-id="b424f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b424f-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b424f-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="b424f-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b424f-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="b424f-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b424f-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="b424f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b424f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b424f-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b424f-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b424f-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b424f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b424f-134">Getmacaddressfromblob</span><span class="sxs-lookup"><span data-stu-id="b424f-134">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="b424f-135">Setboolinblob</span><span class="sxs-lookup"><span data-stu-id="b424f-135">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="b424f-136">Setclassidinblob</span><span class="sxs-lookup"><span data-stu-id="b424f-136">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="b424f-137">Setdwordinblob</span><span class="sxs-lookup"><span data-stu-id="b424f-137">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="b424f-138">Setnetworkinfoinblob</span><span class="sxs-lookup"><span data-stu-id="b424f-138">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="b424f-139">Setnppaddressfilterinblob</span><span class="sxs-lookup"><span data-stu-id="b424f-139">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="b424f-140">Setnpppatternfilterinblob</span><span class="sxs-lookup"><span data-stu-id="b424f-140">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="b424f-141">Setnpptriggerinblob</span><span class="sxs-lookup"><span data-stu-id="b424f-141">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="b424f-142">Setstringinblob</span><span class="sxs-lookup"><span data-stu-id="b424f-142">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




