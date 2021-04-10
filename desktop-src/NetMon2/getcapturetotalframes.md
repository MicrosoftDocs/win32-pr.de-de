---
description: Die getcapturetotalframes-Funktion gibt die Gesamtzahl der Frames in der Erfassung zurück.
ms.assetid: a2b7902c-b80f-4a0a-b12a-2a139df30fca
title: Getcapturetotalframes-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureTotalFrames
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: aa7c81e690e9f7eab258c832ae374f18f9b7afc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862015"
---
# <a name="getcapturetotalframes-function"></a><span data-ttu-id="537aa-103">Getcapturetotalframes-Funktion</span><span class="sxs-lookup"><span data-stu-id="537aa-103">GetCaptureTotalFrames function</span></span>

<span data-ttu-id="537aa-104">Die **getcapturetotalframes** -Funktion gibt die Gesamtzahl der Frames in der Erfassung zurück.</span><span class="sxs-lookup"><span data-stu-id="537aa-104">The **GetCaptureTotalFrames** function returns the total number of frames in the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="537aa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="537aa-105">Syntax</span></span>


```C++
DWORD WINAPI GetCaptureTotalFrames(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="537aa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="537aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="537aa-107">*hcapture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="537aa-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="537aa-108">Handle für die Erfassung.</span><span class="sxs-lookup"><span data-stu-id="537aa-108">Handle to the capture.</span></span> <span data-ttu-id="537aa-109">Weitere Informationen zum Abrufen des Aufzeichnungs Handles finden Sie im Abschnitt "Hinweise" in diesem Thema zu **getcapturetotalframes** .</span><span class="sxs-lookup"><span data-stu-id="537aa-109">For information about obtaining the capture handle, see the Remarks section of this **GetCaptureTotalFrames** topic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="537aa-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="537aa-110">Return value</span></span>

<span data-ttu-id="537aa-111">Wenn die Funktion erfolgreich ist, ist der Rückgabewert die Gesamtzahl der Frames in der Erfassung.</span><span class="sxs-lookup"><span data-stu-id="537aa-111">If the function is successful, the return value is the total number of frames in the capture.</span></span>

<span data-ttu-id="537aa-112">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert 0.</span><span class="sxs-lookup"><span data-stu-id="537aa-112">If the function is unsuccessful, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="537aa-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="537aa-113">Remarks</span></span>

<span data-ttu-id="537aa-114">[*Experten*](e.md) und [*Parser*](p.md) können die **getcapturetotalframes** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="537aa-114">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureTotalFrames** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="537aa-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="537aa-115">Requirements</span></span>



| <span data-ttu-id="537aa-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="537aa-116">Requirement</span></span> | <span data-ttu-id="537aa-117">Wert</span><span class="sxs-lookup"><span data-stu-id="537aa-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="537aa-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="537aa-118">Minimum supported client</span></span><br/> | <span data-ttu-id="537aa-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="537aa-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="537aa-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="537aa-120">Minimum supported server</span></span><br/> | <span data-ttu-id="537aa-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="537aa-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="537aa-122">Header</span><span class="sxs-lookup"><span data-stu-id="537aa-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="537aa-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="537aa-123"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="537aa-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="537aa-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="537aa-125"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="537aa-125"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="537aa-126">DLL</span><span class="sxs-lookup"><span data-stu-id="537aa-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="537aa-127"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="537aa-127"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




