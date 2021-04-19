---
description: Die Funktion "modifyframe" ändert einen vorhandenen Frame mit neuen Daten.
ms.assetid: ebd248e4-b248-4f4a-8b94-a6d1c331d12a
title: Modifyframe-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ModifyFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: af3ef6c2c5ccae2b6410ac8fc81c815f790b17a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345754"
---
# <a name="modifyframe-function"></a><span data-ttu-id="bc6df-103">Modifyframe-Funktion</span><span class="sxs-lookup"><span data-stu-id="bc6df-103">ModifyFrame function</span></span>

<span data-ttu-id="bc6df-104">Die Funktion " **modifyframe** " ändert einen vorhandenen Frame mit neuen Daten.</span><span class="sxs-lookup"><span data-stu-id="bc6df-104">The **ModifyFrame** function alters an existing frame with new data.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc6df-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc6df-105">Syntax</span></span>


```C++
HFRAME WINAPI ModifyFrame(
  _In_  HCAPTURE hCapture,
  _In_  DWORD    FrameNumber,
  _In_  LPBYTE   FrameData,
  _In_  DWORD    FrameLength,
  _Out_ __int64  TimeStamp
);
```



## <a name="parameters"></a><span data-ttu-id="bc6df-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc6df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc6df-107">*hcapture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc6df-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc6df-108">Handle für die Erfassung.</span><span class="sxs-lookup"><span data-stu-id="bc6df-108">Handle to the capture.</span></span> <span data-ttu-id="bc6df-109">Weitere Informationen zum Abrufen des Aufzeichnungs Handles finden Sie im Abschnitt "Hinweise" in diesem Thema zu **modifyframe** .</span><span class="sxs-lookup"><span data-stu-id="bc6df-109">For information about obtaining the capture handle, see the Remarks section of this **ModifyFrame** topic.</span></span>

</dd> <dt>

<span data-ttu-id="bc6df-110">*Framengegen ber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc6df-110">*FrameNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc6df-111">Die Rahmen Indexnummer.</span><span class="sxs-lookup"><span data-stu-id="bc6df-111">Frame index number.</span></span>

</dd> <dt>

<span data-ttu-id="bc6df-112">*FrameData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc6df-112">*FrameData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc6df-113">Zeiger auf ein Bytearray, das die neuen Frame Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="bc6df-113">Pointer to an array of bytes that contain the new frame data.</span></span>

</dd> <dt>

<span data-ttu-id="bc6df-114">*Framelength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc6df-114">*FrameLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc6df-115">Länge der neuen Daten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="bc6df-115">Length of the new data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="bc6df-116">*Zeitstempel* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bc6df-116">*TimeStamp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc6df-117">Zeitstempel, der angibt, wann der Rahmen geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="bc6df-117">Time stamp indicating when the frame was modified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc6df-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc6df-118">Return value</span></span>

<span data-ttu-id="bc6df-119">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Handle für einen neuen Frame.</span><span class="sxs-lookup"><span data-stu-id="bc6df-119">If the function is successful, the return value is a handle to a new frame.</span></span>

<span data-ttu-id="bc6df-120">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="bc6df-120">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc6df-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc6df-121">Remarks</span></span>

<span data-ttu-id="bc6df-122">Wenn der-Befehl erfolgreich ausgeführt wurde, zerstört die **modifyframe** -Funktion den ursprünglichen Frame.</span><span class="sxs-lookup"><span data-stu-id="bc6df-122">If the call is successful, the **ModifyFrame** function destroys the original frame.</span></span>

<span data-ttu-id="bc6df-123">[*Experten*](e.md) und [*Parser*](p.md) können die Funktion " **modifyframe** " aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="bc6df-123">[*Experts*](e.md) and [*parsers*](p.md) can call the **ModifyFrame** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc6df-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc6df-124">Requirements</span></span>



| <span data-ttu-id="bc6df-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc6df-125">Requirement</span></span> | <span data-ttu-id="bc6df-126">Wert</span><span class="sxs-lookup"><span data-stu-id="bc6df-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bc6df-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc6df-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bc6df-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc6df-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="bc6df-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc6df-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bc6df-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc6df-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bc6df-131">Header</span><span class="sxs-lookup"><span data-stu-id="bc6df-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc6df-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc6df-132"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="bc6df-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bc6df-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="bc6df-134"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc6df-134"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="bc6df-135">DLL</span><span class="sxs-lookup"><span data-stu-id="bc6df-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc6df-136"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc6df-136"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




