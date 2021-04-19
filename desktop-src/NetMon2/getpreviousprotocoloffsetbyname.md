---
description: Die getpreviousprotocoloffsetbyname-Funktion gibt die vorherige Instanz eines bestimmten Protokolls zurück.
ms.assetid: 94f80776-564f-4089-9e3a-fdf38d9dfe8a
title: Getpreviousprotcoloffsetbyname-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPreviousProtocolOffsetByName
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2720d309224def5f368babf4f9ace85955907347
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339748"
---
# <a name="getpreviousprotocoloffsetbyname-function"></a><span data-ttu-id="d7f8f-103">Getpreviousprotcoloffsetbyname-Funktion</span><span class="sxs-lookup"><span data-stu-id="d7f8f-103">GetPreviousProtocolOffsetByName function</span></span>

<span data-ttu-id="d7f8f-104">Die **getpreviousprotocoloffsetbyname** -Funktion gibt die vorherige Instanz eines bestimmten Protokolls zurück.</span><span class="sxs-lookup"><span data-stu-id="d7f8f-104">The **GetPreviousProtocolOffsetByName** function returns the previous instance of a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7f8f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7f8f-105">Syntax</span></span>


```C++
DWORD WINAPI GetPreviousProtocolOffsetByName(
  _In_  HFRAME hFrame,
  _In_  DWORD  dwStartOffset,
  _In_  LPSTR  szProtocolName,
  _Out_ DWORD  *pdwPreviousOffset
);
```



## <a name="parameters"></a><span data-ttu-id="d7f8f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7f8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7f8f-107">*hframe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7f8f-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7f8f-108">Handle für den Frame.</span><span class="sxs-lookup"><span data-stu-id="d7f8f-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="d7f8f-109">*dwstarto ffset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7f8f-109">*dwStartOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7f8f-110">Offset im Frame.</span><span class="sxs-lookup"><span data-stu-id="d7f8f-110">Offset in the frame.</span></span>

</dd> <dt>

<span data-ttu-id="d7f8f-111">*szprotocolname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7f8f-111">*szProtocolName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7f8f-112">Der Name des Protokolls, nach dem Sie suchen möchten.</span><span class="sxs-lookup"><span data-stu-id="d7f8f-112">Name of the protocol you want to search for.</span></span>

</dd> <dt>

<span data-ttu-id="d7f8f-113">*pdwpreviousoffset* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d7f8f-113">*pdwPreviousOffset* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7f8f-114">Zeiger auf ein **DWORD** , das den Offset zum vorherigen Protokoll enthält (wenn die Funktion erfolgreich ausgeführt wird).</span><span class="sxs-lookup"><span data-stu-id="d7f8f-114">Pointer to a **DWORD** that contains the offset to the previous protocol (if the function succeeds).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7f8f-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d7f8f-115">Return value</span></span>

<span data-ttu-id="d7f8f-116">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="d7f8f-116">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="d7f8f-117">Wenn die Funktion nicht erfolgreich ist, wird das nmerr- \_ Protokoll \_ nicht \_ gefunden.</span><span class="sxs-lookup"><span data-stu-id="d7f8f-117">If the function is unsuccessful, the return value is NMERR\_PROTOCOL\_NOT\_FOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7f8f-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d7f8f-118">Remarks</span></span>

<span data-ttu-id="d7f8f-119">[*Experten*](e.md) und [*Parser*](p.md) können **getpreviousproycoloffsetbyname** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d7f8f-119">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetPreviousProtocolOffsetByName**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7f8f-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7f8f-120">Requirements</span></span>



| <span data-ttu-id="d7f8f-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7f8f-121">Requirement</span></span> | <span data-ttu-id="d7f8f-122">Wert</span><span class="sxs-lookup"><span data-stu-id="d7f8f-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f8f-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d7f8f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d7f8f-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7f8f-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d7f8f-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d7f8f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d7f8f-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7f8f-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d7f8f-127">Header</span><span class="sxs-lookup"><span data-stu-id="d7f8f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7f8f-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7f8f-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d7f8f-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d7f8f-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="d7f8f-130"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7f8f-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d7f8f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d7f8f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7f8f-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7f8f-132"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




