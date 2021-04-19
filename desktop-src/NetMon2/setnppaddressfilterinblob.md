---
description: Die setnppaddressfilterinblob-Funktion legt den angegebenen Adress Filter im BLOB fest.
ms.assetid: bdd1482d-8be0-4999-9a7a-16b0400412fb
title: Setnppaddressfilterinblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPAddressFilterInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 39e8a85599fa63b1320d707f648731a195dbb48e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352747"
---
# <a name="setnppaddressfilterinblob-function"></a><span data-ttu-id="0a659-103">Setnppaddressfilterinblob-Funktion</span><span class="sxs-lookup"><span data-stu-id="0a659-103">SetNPPAddressFilterInBlob function</span></span>

<span data-ttu-id="0a659-104">Die **setnppaddressfilterinblob** -Funktion legt den angegebenen Adress Filter im BLOB fest.</span><span class="sxs-lookup"><span data-stu-id="0a659-104">The **SetNPPAddressFilterInBlob** function sets the given address filter in the BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a659-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a659-105">Syntax</span></span>


```C++
DWORD SetNPPAddressFilterInBlob(
  _In_ HBLOB          hBlob,
  _In_ LPADDRESSTABLE pAddressTable
);
```



## <a name="parameters"></a><span data-ttu-id="0a659-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a659-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a659-107">*hblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a659-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a659-108">Handle für ein BLOB.</span><span class="sxs-lookup"><span data-stu-id="0a659-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="0a659-109">*padresssstable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a659-109">*pAddressTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a659-110">Ein Zeiger auf eine- [**adressstabile**](addresstable.md) -Struktur, die die vom Benutzer zugeordnete Adress Tabelle definiert.</span><span class="sxs-lookup"><span data-stu-id="0a659-110">Pointer to an [**ADDRESSTABLE**](addresstable.md) structure that defines the user-allocated address table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a659-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0a659-111">Return value</span></span>

<span data-ttu-id="0a659-112">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="0a659-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="0a659-113">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="0a659-113">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a659-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a659-114">Requirements</span></span>



| <span data-ttu-id="0a659-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a659-115">Requirement</span></span> | <span data-ttu-id="0a659-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0a659-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a659-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0a659-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0a659-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a659-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0a659-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0a659-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0a659-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a659-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0a659-121">Header</span><span class="sxs-lookup"><span data-stu-id="0a659-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a659-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a659-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="0a659-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0a659-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="0a659-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a659-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="0a659-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0a659-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a659-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a659-126"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a659-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a659-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a659-128">Getnppaddressfilterfromblob</span><span class="sxs-lookup"><span data-stu-id="0a659-128">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="0a659-129">Setboolinblob</span><span class="sxs-lookup"><span data-stu-id="0a659-129">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="0a659-130">Setclassidinblob</span><span class="sxs-lookup"><span data-stu-id="0a659-130">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="0a659-131">Setdwordinblob</span><span class="sxs-lookup"><span data-stu-id="0a659-131">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="0a659-132">Setmacaddressinblob</span><span class="sxs-lookup"><span data-stu-id="0a659-132">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="0a659-133">Setnetworkinfoinblob</span><span class="sxs-lookup"><span data-stu-id="0a659-133">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="0a659-134">Setnpppatternfilterinblob</span><span class="sxs-lookup"><span data-stu-id="0a659-134">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="0a659-135">Setnpptriggerinblob</span><span class="sxs-lookup"><span data-stu-id="0a659-135">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="0a659-136">Setstringinblob</span><span class="sxs-lookup"><span data-stu-id="0a659-136">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




