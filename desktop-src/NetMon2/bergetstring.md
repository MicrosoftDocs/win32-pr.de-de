---
description: Die bergetstring-Funktion decodiert eine BER-codierte Zeichenfolge.
ms.assetid: 1f72f061-c0ed-4634-9709-e08c2b9468bb
title: Bergetstring-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 6f8f864b8042ad49502ae53061e157575192e7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864804"
---
# <a name="bergetstring-function"></a><span data-ttu-id="1d143-103">Bergetstring-Funktion</span><span class="sxs-lookup"><span data-stu-id="1d143-103">BERGetString function</span></span>

<span data-ttu-id="1d143-104">Die **bergetstring** -Funktion decodiert eine BER-codierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="1d143-104">The **BERGetString** function decodes a BER-encoded string.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d143-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d143-105">Syntax</span></span>


```C++
BOOL BERGetString(
   LPBYTE  pCurrentPointer,
   LPBYTE  *ppValuePointer,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a><span data-ttu-id="1d143-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d143-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d143-107">*pcurrentpointer*</span><span class="sxs-lookup"><span data-stu-id="1d143-107">*pCurrentPointer*</span></span> 
</dt> <dd>

<span data-ttu-id="1d143-108">Ein Zeiger auf die Zeichenfolge, die decodiert wird.</span><span class="sxs-lookup"><span data-stu-id="1d143-108">Pointer to the string that is decoded.</span></span>

</dd> <dt>

<span data-ttu-id="1d143-109">*ppvaluepointer*</span><span class="sxs-lookup"><span data-stu-id="1d143-109">*ppValuePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="1d143-110">Zeiger auf den Zeiger der decodierten Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="1d143-110">Pointer to the pointer of the decoded string.</span></span>

</dd> <dt>

<span data-ttu-id="1d143-111">*pheaderlength*</span><span class="sxs-lookup"><span data-stu-id="1d143-111">*pHeaderLength*</span></span> 
</dt> <dd>

<span data-ttu-id="1d143-112">Zeiger auf die zurückgegebene Header Länge.</span><span class="sxs-lookup"><span data-stu-id="1d143-112">Pointer to the returned header length.</span></span>

</dd> <dt>

<span data-ttu-id="1d143-113">*pdatalength*</span><span class="sxs-lookup"><span data-stu-id="1d143-113">*pDataLength*</span></span> 
</dt> <dd>

<span data-ttu-id="1d143-114">Zeiger auf die Zeichen folgen Länge.</span><span class="sxs-lookup"><span data-stu-id="1d143-114">Pointer to the string length.</span></span>

</dd> <dt>

<span data-ttu-id="1d143-115">*ppnext*</span><span class="sxs-lookup"><span data-stu-id="1d143-115">*ppNext*</span></span> 
</dt> <dd>

<span data-ttu-id="1d143-116">Zeiger auf den Zeiger des nächsten ber-Eintrags.</span><span class="sxs-lookup"><span data-stu-id="1d143-116">Pointer to the pointer of the next BER entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d143-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d143-117">Return value</span></span>

<span data-ttu-id="1d143-118">Wenn die Funktion erfolgreich ist (d. h., wenn eine gültige ber-codierte Zeichenfolge decodiert wird), ist der Rückgabewert " **true**".</span><span class="sxs-lookup"><span data-stu-id="1d143-118">If the function is successful (that is, if a valid BER-encoded string is decoded), the return value is **TRUE**.</span></span>

<span data-ttu-id="1d143-119">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="1d143-119">If function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d143-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d143-120">Requirements</span></span>



| <span data-ttu-id="1d143-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d143-121">Requirement</span></span> | <span data-ttu-id="1d143-122">Wert</span><span class="sxs-lookup"><span data-stu-id="1d143-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1d143-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d143-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1d143-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d143-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="1d143-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d143-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1d143-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d143-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1d143-127">Header</span><span class="sxs-lookup"><span data-stu-id="1d143-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d143-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d143-128"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="1d143-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1d143-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="1d143-130"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d143-130"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="1d143-131">DLL</span><span class="sxs-lookup"><span data-stu-id="1d143-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d143-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d143-132"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




