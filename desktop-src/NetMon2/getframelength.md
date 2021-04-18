---
description: Die getFrameLength-Funktion gibt die Länge des Frames zurück.
ms.assetid: 30be1f5c-9b13-42ad-944a-92b1aee8a6bc
title: GetFrameLength-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 29a2a08ac105414a914e14a9ce8e69976725700c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344040"
---
# <a name="getframelength-function"></a><span data-ttu-id="77b6a-103">GetFrameLength-Funktion</span><span class="sxs-lookup"><span data-stu-id="77b6a-103">GetFrameLength function</span></span>

<span data-ttu-id="77b6a-104">Die **getFrameLength** -Funktion gibt die Länge des Frames zurück.</span><span class="sxs-lookup"><span data-stu-id="77b6a-104">The **GetFrameLength** function returns the length of the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="77b6a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="77b6a-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="77b6a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="77b6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77b6a-107">*hframe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77b6a-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77b6a-108">Handle für einen Frame.</span><span class="sxs-lookup"><span data-stu-id="77b6a-108">Handle to a frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77b6a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="77b6a-109">Return value</span></span>

<span data-ttu-id="77b6a-110">Wenn die Funktion erfolgreich ist, ist der Rückgabewert die Länge des Frames in Bytes.</span><span class="sxs-lookup"><span data-stu-id="77b6a-110">If the function is successful, the return value is the length of the frame   in bytes.</span></span>

<span data-ttu-id="77b6a-111">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="77b6a-111">If the function is unsuccessful, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="77b6a-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77b6a-112">Remarks</span></span>

<span data-ttu-id="77b6a-113">[*Experten*](e.md) und [*Parser*](p.md) können die **getFrameLength** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="77b6a-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameLength** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="77b6a-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77b6a-114">Requirements</span></span>



| <span data-ttu-id="77b6a-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="77b6a-115">Requirement</span></span> | <span data-ttu-id="77b6a-116">Wert</span><span class="sxs-lookup"><span data-stu-id="77b6a-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="77b6a-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="77b6a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="77b6a-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77b6a-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="77b6a-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="77b6a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="77b6a-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77b6a-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="77b6a-121">Header</span><span class="sxs-lookup"><span data-stu-id="77b6a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="77b6a-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="77b6a-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="77b6a-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="77b6a-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="77b6a-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77b6a-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="77b6a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="77b6a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77b6a-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77b6a-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




