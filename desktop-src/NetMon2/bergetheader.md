---
description: Die "bergeteader"-Funktion decodiert einen Choice-Header.
ms.assetid: 2574a9b3-c28e-43d1-904f-d45888617584
title: Bergederader-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetHeader
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 5e2213b15b6b4d2cbaa15b3b9aa9de028e20a62d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106363446"
---
# <a name="bergetheader-function"></a><span data-ttu-id="cad81-103">Bergederader-Funktion</span><span class="sxs-lookup"><span data-stu-id="cad81-103">BERGetHeader function</span></span>

<span data-ttu-id="cad81-104">Die " **bergeteader** "-Funktion decodiert einen Choice-Header.</span><span class="sxs-lookup"><span data-stu-id="cad81-104">The **BERGetHeader** function decodes a choice header.</span></span>

## <a name="syntax"></a><span data-ttu-id="cad81-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cad81-105">Syntax</span></span>


```C++
BOOL BERGetHeader(
   LPBYTE  pCurrentPointer,
   LPBYTE  pTag,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a><span data-ttu-id="cad81-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cad81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cad81-107">*pcurrentpointer*</span><span class="sxs-lookup"><span data-stu-id="cad81-107">*pCurrentPointer*</span></span> 
</dt> <dd>

<span data-ttu-id="cad81-108">Zeiger auf den Choice-Header.</span><span class="sxs-lookup"><span data-stu-id="cad81-108">Pointer to the choice header.</span></span>

</dd> <dt>

<span data-ttu-id="cad81-109">*ptag*</span><span class="sxs-lookup"><span data-stu-id="cad81-109">*pTag*</span></span> 
</dt> <dd>

<span data-ttu-id="cad81-110">Zeiger auf das zurückgegebene Tag.</span><span class="sxs-lookup"><span data-stu-id="cad81-110">Pointer to the returned tag.</span></span>

</dd> <dt>

<span data-ttu-id="cad81-111">*pheaderlength*</span><span class="sxs-lookup"><span data-stu-id="cad81-111">*pHeaderLength*</span></span> 
</dt> <dd>

<span data-ttu-id="cad81-112">Zeiger auf die zurückgegebene Header Länge.</span><span class="sxs-lookup"><span data-stu-id="cad81-112">Pointer to the returned header length.</span></span>

</dd> <dt>

<span data-ttu-id="cad81-113">*pdatalength*</span><span class="sxs-lookup"><span data-stu-id="cad81-113">*pDataLength*</span></span> 
</dt> <dd>

<span data-ttu-id="cad81-114">Zeiger auf die zurückgegebene Daten Länge.</span><span class="sxs-lookup"><span data-stu-id="cad81-114">Pointer to the returned data length.</span></span>

</dd> <dt>

<span data-ttu-id="cad81-115">*ppnext*</span><span class="sxs-lookup"><span data-stu-id="cad81-115">*ppNext*</span></span> 
</dt> <dd>

<span data-ttu-id="cad81-116">Zeiger auf den Header Inhalt.</span><span class="sxs-lookup"><span data-stu-id="cad81-116">Pointer to the header contents.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cad81-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cad81-117">Return value</span></span>

<span data-ttu-id="cad81-118">Wenn die Funktion erfolgreich ist (d. h., es wurde ein gültiger ber Choice-Header gefunden), ist der Rückgabewert " **true**".</span><span class="sxs-lookup"><span data-stu-id="cad81-118">If the function is successful (that is, a valid BER choice header is found) the return value is **TRUE**.</span></span>

<span data-ttu-id="cad81-119">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="cad81-119">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cad81-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cad81-120">Requirements</span></span>



| <span data-ttu-id="cad81-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cad81-121">Requirement</span></span> | <span data-ttu-id="cad81-122">Wert</span><span class="sxs-lookup"><span data-stu-id="cad81-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cad81-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cad81-123">Minimum supported client</span></span><br/> | <span data-ttu-id="cad81-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cad81-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="cad81-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cad81-125">Minimum supported server</span></span><br/> | <span data-ttu-id="cad81-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cad81-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cad81-127">Header</span><span class="sxs-lookup"><span data-stu-id="cad81-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="cad81-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="cad81-128"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="cad81-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cad81-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="cad81-130"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cad81-130"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="cad81-131">DLL</span><span class="sxs-lookup"><span data-stu-id="cad81-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cad81-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cad81-132"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




