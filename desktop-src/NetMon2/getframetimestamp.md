---
description: Die getframetimestamp-Funktion gibt den Zeitstempel eines angegebenen Frames zurück.
ms.assetid: 4ac50400-6674-40fa-9a69-9c0ccb55b92c
title: Getframetimestamp-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameTimeStamp
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 37a75f946a5fc0ddb2b32d99334368a272fdf2e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348643"
---
# <a name="getframetimestamp-function"></a><span data-ttu-id="bdc0b-103">Getframetimestamp-Funktion</span><span class="sxs-lookup"><span data-stu-id="bdc0b-103">GetFrameTimeStamp function</span></span>

<span data-ttu-id="bdc0b-104">Die **getframetimestamp** -Funktion gibt den Zeitstempel eines angegebenen Frames zurück.</span><span class="sxs-lookup"><span data-stu-id="bdc0b-104">The **GetFrameTimeStamp** function returns the time stamp of a given frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdc0b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdc0b-105">Syntax</span></span>


```C++
__int64 WINAPI GetFrameTimeStamp(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="bdc0b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdc0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdc0b-107">*hframe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bdc0b-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdc0b-108">Handle für den Frame.</span><span class="sxs-lookup"><span data-stu-id="bdc0b-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdc0b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bdc0b-109">Return value</span></span>

<span data-ttu-id="bdc0b-110">Wenn die Funktion erfolgreich ist, ist der Rückgabewert der Zeitstempel des Frames in Mikrosekunden.</span><span class="sxs-lookup"><span data-stu-id="bdc0b-110">If the function is successful, the return value is the time stamp of the frame   in microseconds.</span></span>

<span data-ttu-id="bdc0b-111">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert minus eins (-1).</span><span class="sxs-lookup"><span data-stu-id="bdc0b-111">If the function is unsuccessful, the return value is minus one (-1).</span></span>

## <a name="remarks"></a><span data-ttu-id="bdc0b-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bdc0b-112">Remarks</span></span>

<span data-ttu-id="bdc0b-113">Die **getframetimestamp** -Funktion gibt einen Zeitstempel zurück, der die verstrichene Zeit zwischen dem Start des Aufzeichnungsprozesses und der Aufzeichnung des Frames anzeigt.</span><span class="sxs-lookup"><span data-stu-id="bdc0b-113">The **GetFrameTimeStamp** function returns a time stamp that shows the elapsed time between the start of the capture process, and the recording of the frame.</span></span>

<span data-ttu-id="bdc0b-114">[*Experten*](e.md) und [*Parser*](p.md) können die **getframetimestamp** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bdc0b-114">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameTimeStamp** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdc0b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bdc0b-115">Requirements</span></span>



| <span data-ttu-id="bdc0b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bdc0b-116">Requirement</span></span> | <span data-ttu-id="bdc0b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="bdc0b-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bdc0b-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bdc0b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bdc0b-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bdc0b-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="bdc0b-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bdc0b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bdc0b-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bdc0b-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bdc0b-122">Header</span><span class="sxs-lookup"><span data-stu-id="bdc0b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdc0b-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdc0b-123"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="bdc0b-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bdc0b-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="bdc0b-125"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bdc0b-125"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="bdc0b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="bdc0b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bdc0b-127"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdc0b-127"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




