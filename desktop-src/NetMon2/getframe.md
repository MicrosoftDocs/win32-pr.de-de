---
description: Die GetFrame-Funktion gibt ein Handle für einen angegebenen Frame in einer Erfassung zurück.
ms.assetid: d40bc364-0028-4006-a6c2-6ee100366ba3
title: GetFrame-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3f79e7fa6fc4e79f4dea804769cc9d51b8096860
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128341"
---
# <a name="getframe-function"></a><span data-ttu-id="7f515-103">GetFrame-Funktion</span><span class="sxs-lookup"><span data-stu-id="7f515-103">GetFrame function</span></span>

<span data-ttu-id="7f515-104">Die **GetFrame** -Funktion gibt ein Handle für einen angegebenen Frame in einer Erfassung zurück.</span><span class="sxs-lookup"><span data-stu-id="7f515-104">The **GetFrame** function returns a handle to a given frame within a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f515-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f515-105">Syntax</span></span>


```C++
HFRAME WINAPI GetFrame(
  _In_ HCAPTURE hCapture,
  _In_ DWORD    FrameNumber
);
```



## <a name="parameters"></a><span data-ttu-id="7f515-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f515-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f515-107">*hcapture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f515-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f515-108">Handle für eine Erfassung.</span><span class="sxs-lookup"><span data-stu-id="7f515-108">Handle to a capture.</span></span> <span data-ttu-id="7f515-109">Um das Erfassungs Handle abzurufen, rufen Sie die [getframecapturehandle](getframecapturehandle.md) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="7f515-109">To obtain the capture handle, call the [GetFrameCaptureHandle](getframecapturehandle.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="7f515-110">*Framengegen ber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f515-110">*FrameNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f515-111">Die Zahl (null basiert) des Frames.</span><span class="sxs-lookup"><span data-stu-id="7f515-111">Number (zero-based) of the frame.</span></span> <span data-ttu-id="7f515-112">Die Nummer des ersten Frames in einer Erfassung ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="7f515-112">The number of the first frame in a capture is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f515-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7f515-113">Return value</span></span>

<span data-ttu-id="7f515-114">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Handle für den Frame.</span><span class="sxs-lookup"><span data-stu-id="7f515-114">If the function is successful, the return value is a handle to the frame.</span></span>

<span data-ttu-id="7f515-115">Wenn die Funktion nicht erfolgreich ist (d. h., wenn *hcapture* ungültig ist oder die Frame Nummer außerhalb des gültigen Bereichs liegt), ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="7f515-115">If the function is unsuccessful (that is, if *hCapture* is invalid, or the frame number is out of range), the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f515-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f515-116">Remarks</span></span>

<span data-ttu-id="7f515-117">Verwenden Sie die **GetFrame** -Funktion zum Abrufen des Frame Handles, das beim Suchen von Instanzen einer Eigenschaft erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7f515-117">Use the **GetFrame** function to obtain the frame handle needed when locating instances of a property.</span></span> <span data-ttu-id="7f515-118">Die Funktionen, die zum Suchen von Eigenschafts Instanzen verwendet werden, sind [findpropertyinstance](findpropertyinstance.md) , das die erste Instanz sucht, und [findpropertyinstancerestart](findpropertyinstancerestart.md) , die die nächste Instanz sucht.</span><span class="sxs-lookup"><span data-stu-id="7f515-118">The functions used to locate property instances are [FindPropertyInstance](findpropertyinstance.md) which locates the first instance, and [FindPropertyInstanceRestart](findpropertyinstancerestart.md) which locates the next instance.</span></span>

<span data-ttu-id="7f515-119">[*Experten*](e.md) und [*Parser*](p.md) können die **GetFrame** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7f515-119">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrame** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f515-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f515-120">Requirements</span></span>



| <span data-ttu-id="7f515-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f515-121">Requirement</span></span> | <span data-ttu-id="7f515-122">Wert</span><span class="sxs-lookup"><span data-stu-id="7f515-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7f515-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7f515-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7f515-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7f515-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7f515-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7f515-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7f515-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7f515-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7f515-127">Header</span><span class="sxs-lookup"><span data-stu-id="7f515-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f515-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f515-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="7f515-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7f515-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="7f515-130"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f515-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="7f515-131">DLL</span><span class="sxs-lookup"><span data-stu-id="7f515-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f515-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f515-132"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f515-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f515-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f515-134">Findpropertyinstance</span><span class="sxs-lookup"><span data-stu-id="7f515-134">FindPropertyInstance</span></span>](findpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="7f515-135">Findpropertyinstancerestart</span><span class="sxs-lookup"><span data-stu-id="7f515-135">FindPropertyInstanceRestart</span></span>](findpropertyinstancerestart.md)
</dt> </dl>

 

 




