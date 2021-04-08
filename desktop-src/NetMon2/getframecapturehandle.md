---
description: Die getframecapturehandle-Funktion gibt ein Handle für die Erfassung basierend auf einem angegebenen Frame zurück.
ms.assetid: 71b32799-194c-40f8-8438-36aebaba31c7
title: Getframecapturehandle-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameCaptureHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3770ad0fd3db7d1c076b5d1f286c1fdbdc2707a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862011"
---
# <a name="getframecapturehandle-function"></a><span data-ttu-id="f4a5f-103">Getframecapturehandle-Funktion</span><span class="sxs-lookup"><span data-stu-id="f4a5f-103">GetFrameCaptureHandle function</span></span>

<span data-ttu-id="f4a5f-104">Die **getframecapturehandle** -Funktion gibt ein Handle für die Erfassung basierend auf einem angegebenen Frame zurück.</span><span class="sxs-lookup"><span data-stu-id="f4a5f-104">The **GetFrameCaptureHandle** function returns a handle to the capture based on a given frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4a5f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4a5f-105">Syntax</span></span>


```C++
HCAPTURE WINAPI GetFrameCaptureHandle(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="f4a5f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4a5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4a5f-107">*hframe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f4a5f-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4a5f-108">Handle für einen Frame.</span><span class="sxs-lookup"><span data-stu-id="f4a5f-108">Handle to a frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4a5f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f4a5f-109">Return value</span></span>

<span data-ttu-id="f4a5f-110">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Handle für die Erfassung.</span><span class="sxs-lookup"><span data-stu-id="f4a5f-110">If the function is successful, the return value is a handle to the capture.</span></span>

<span data-ttu-id="f4a5f-111">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert 0.</span><span class="sxs-lookup"><span data-stu-id="f4a5f-111">If the function is unsuccessful, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4a5f-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4a5f-112">Remarks</span></span>

<span data-ttu-id="f4a5f-113">[*Experten*](e.md) und [*Parser*](p.md) können die **getframecapturehandle** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f4a5f-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameCaptureHandle** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4a5f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4a5f-114">Requirements</span></span>



| <span data-ttu-id="f4a5f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4a5f-115">Requirement</span></span> | <span data-ttu-id="f4a5f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f4a5f-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f4a5f-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f4a5f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f4a5f-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4a5f-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f4a5f-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f4a5f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f4a5f-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4a5f-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f4a5f-121">Header</span><span class="sxs-lookup"><span data-stu-id="f4a5f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4a5f-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4a5f-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="f4a5f-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f4a5f-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="f4a5f-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f4a5f-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f4a5f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f4a5f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4a5f-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4a5f-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




