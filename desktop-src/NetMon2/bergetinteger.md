---
description: Die bergetinteger-Funktion decodiert eine BER-codierte Ganzzahl.
ms.assetid: 1ab0dcec-05cf-4322-a44e-28aa9131495a
title: Bergetinteger-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetInteger
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: c89cd5e3f4e4eb35157936f990939154f23966d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867027"
---
# <a name="bergetinteger-function"></a><span data-ttu-id="38599-103">Bergetinteger-Funktion</span><span class="sxs-lookup"><span data-stu-id="38599-103">BERGetInteger function</span></span>

<span data-ttu-id="38599-104">Die **bergetinteger** -Funktion decodiert eine BER-codierte Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="38599-104">The **BERGetInteger** function decodes a BER-encoded integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="38599-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="38599-105">Syntax</span></span>


```C++
BOOL BERGetInteger(
   LPBYTE  pCurrentPointer,
   LPBYTE  *ppValuePointer,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a><span data-ttu-id="38599-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="38599-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38599-107">*pcurrentpointer*</span><span class="sxs-lookup"><span data-stu-id="38599-107">*pCurrentPointer*</span></span> 
</dt> <dd>

<span data-ttu-id="38599-108">Ein Zeiger auf die Ganzzahl, die decodiert wird.</span><span class="sxs-lookup"><span data-stu-id="38599-108">Pointer to the integer that is decoded.</span></span>

</dd> <dt>

<span data-ttu-id="38599-109">*ppvaluepointer*</span><span class="sxs-lookup"><span data-stu-id="38599-109">*ppValuePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="38599-110">Zeiger auf den Zeiger auf den zurückgegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="38599-110">Pointer to the pointer to returned value.</span></span>

</dd> <dt>

<span data-ttu-id="38599-111">*pheaderlength*</span><span class="sxs-lookup"><span data-stu-id="38599-111">*pHeaderLength*</span></span> 
</dt> <dd>

<span data-ttu-id="38599-112">Zeiger auf die zurückgegebene Header Länge.</span><span class="sxs-lookup"><span data-stu-id="38599-112">Pointer to the returned header length.</span></span>

</dd> <dt>

<span data-ttu-id="38599-113">*pdatalength*</span><span class="sxs-lookup"><span data-stu-id="38599-113">*pDataLength*</span></span> 
</dt> <dd>

<span data-ttu-id="38599-114">Zeiger auf die Daten Länge.</span><span class="sxs-lookup"><span data-stu-id="38599-114">Pointer to the data length.</span></span>

</dd> <dt>

<span data-ttu-id="38599-115">*ppnext*</span><span class="sxs-lookup"><span data-stu-id="38599-115">*ppNext*</span></span> 
</dt> <dd>

<span data-ttu-id="38599-116">Zeiger auf den Zeiger auf den nächsten ber-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="38599-116">Pointer to the pointer to the next BER entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38599-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="38599-117">Return value</span></span>

<span data-ttu-id="38599-118">Wenn die Funktion erfolgreich ist (d. h., wenn eine gültige ber-codierte Ganzzahl gefunden und konvertiert wird), ist der Rückgabewert " **true**".</span><span class="sxs-lookup"><span data-stu-id="38599-118">If the function is successful (that is, if a valid BER encoded integer is found and converted), the return value is **TRUE**.</span></span>

<span data-ttu-id="38599-119">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="38599-119">If function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="38599-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38599-120">Requirements</span></span>



| <span data-ttu-id="38599-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="38599-121">Requirement</span></span> | <span data-ttu-id="38599-122">Wert</span><span class="sxs-lookup"><span data-stu-id="38599-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="38599-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="38599-123">Minimum supported client</span></span><br/> | <span data-ttu-id="38599-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="38599-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="38599-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="38599-125">Minimum supported server</span></span><br/> | <span data-ttu-id="38599-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="38599-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="38599-127">Header</span><span class="sxs-lookup"><span data-stu-id="38599-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="38599-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="38599-128"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="38599-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="38599-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="38599-130"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38599-130"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="38599-131">DLL</span><span class="sxs-lookup"><span data-stu-id="38599-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38599-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38599-132"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




