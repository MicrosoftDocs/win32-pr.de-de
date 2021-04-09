---
description: Die getframenumber-Funktion gibt die Anzahl von Frames zurück.
ms.assetid: 97d343a3-2a1e-47d7-bfc2-b63f8d84b29d
title: Getframenumschlag-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameNumber
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: de04fa513fab98b1a82d036f6f40a6c67cdda3ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958716"
---
# <a name="getframenumber-function"></a><span data-ttu-id="55fbe-103">Getframenumschlag-Funktion</span><span class="sxs-lookup"><span data-stu-id="55fbe-103">GetFrameNumber function</span></span>

<span data-ttu-id="55fbe-104">Die **getframenumber** -Funktion gibt die Anzahl von Frames zurück.</span><span class="sxs-lookup"><span data-stu-id="55fbe-104">The **GetFrameNumber** function returns the number of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="55fbe-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="55fbe-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameNumber(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="55fbe-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="55fbe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55fbe-107">*hframe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55fbe-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55fbe-108">Handle für den Frame.</span><span class="sxs-lookup"><span data-stu-id="55fbe-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55fbe-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="55fbe-109">Return value</span></span>

<span data-ttu-id="55fbe-110">Wenn die Funktion erfolgreich ist, ist der Rückgabewert eine Null basierte Frame Nummer.</span><span class="sxs-lookup"><span data-stu-id="55fbe-110">If the function is successful, the return value is a zero-based frame number.</span></span>

<span data-ttu-id="55fbe-111">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert minus eins (-1).</span><span class="sxs-lookup"><span data-stu-id="55fbe-111">If the function is not successful, the return value is minus one (-1).</span></span>

## <a name="remarks"></a><span data-ttu-id="55fbe-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55fbe-112">Remarks</span></span>

<span data-ttu-id="55fbe-113">[*Experten*](e.md) und [*Parser*](p.md) können die **getframenumschlag** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="55fbe-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameNumber** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="55fbe-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55fbe-114">Requirements</span></span>



| <span data-ttu-id="55fbe-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55fbe-115">Requirement</span></span> | <span data-ttu-id="55fbe-116">Wert</span><span class="sxs-lookup"><span data-stu-id="55fbe-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="55fbe-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="55fbe-117">Minimum supported client</span></span><br/> | <span data-ttu-id="55fbe-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55fbe-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="55fbe-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="55fbe-119">Minimum supported server</span></span><br/> | <span data-ttu-id="55fbe-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55fbe-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="55fbe-121">Header</span><span class="sxs-lookup"><span data-stu-id="55fbe-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="55fbe-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="55fbe-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="55fbe-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="55fbe-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="55fbe-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55fbe-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="55fbe-125">DLL</span><span class="sxs-lookup"><span data-stu-id="55fbe-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55fbe-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55fbe-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




