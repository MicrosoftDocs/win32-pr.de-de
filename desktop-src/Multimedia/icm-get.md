---
title: ICM_GET Meldung (VFW. h)
description: Die ICM \_ GET-Nachricht Ruft einen von der Anwendung definierten DWORD-Wert von einem Video Komprimierungs Treiber ab.
ms.assetid: 288c0053-16a1-4547-b748-da218a0b588c
keywords:
- ICM_GET-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_GET
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e23cd994546be41b5f938331b2dc632897635c32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740496"
---
# <a name="icm_get-message"></a><span data-ttu-id="173b7-104">ICM- \_ GET-Nachricht</span><span class="sxs-lookup"><span data-stu-id="173b7-104">ICM\_GET message</span></span>

<span data-ttu-id="173b7-105">Die **ICM \_ Get** -Nachricht Ruft einen von der Anwendung definierten **DWORD** -Wert von einem Video Komprimierungs Treiber ab.</span><span class="sxs-lookup"><span data-stu-id="173b7-105">The **ICM\_GET** message retrieves an application-defined **DWORD** value from a video compression driver.</span></span>


```C++
ICM_GET 
wParam = (DWORD) (LPVOID) pv; 
lParam = (DWORD) cb; 
```



## <a name="parameters"></a><span data-ttu-id="173b7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="173b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="173b7-107"><span id="pv"></span><span id="PV"></span>*teuren*</span><span class="sxs-lookup"><span data-stu-id="173b7-107"><span id="pv"></span><span id="PV"></span>*pv*</span></span>
</dt> <dd>

<span data-ttu-id="173b7-108">Ein Zeiger auf einen Speicherblock, der mit dem aktuellen Zustand aufgefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="173b7-108">Pointer to a block of memory to be filled with the current state.</span></span> <span data-ttu-id="173b7-109">Sie können auch **null** angeben, um den von den Zustandsinformationen benötigten Arbeitsspeicher zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="173b7-109">You can also specify **NULL** to determine the amount of memory required by the state information.</span></span>

</dd> <dt>

<span data-ttu-id="173b7-110"><span id="cb"></span><span id="CB"></span>*betrieben*</span><span class="sxs-lookup"><span data-stu-id="173b7-110"><span id="cb"></span><span id="CB"></span>*cb*</span></span>
</dt> <dd>

<span data-ttu-id="173b7-111">Größe des Speicherblocks in Bytes.</span><span class="sxs-lookup"><span data-stu-id="173b7-111">Size, in bytes, of the block of memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="173b7-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="173b7-112">Return Value</span></span>

<span data-ttu-id="173b7-113">Gibt die Größe des Arbeitsspeichers in Bytes zurück, der zum Speichern der Statusinformationen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="173b7-113">Returns the amount of memory, in bytes, required to store the status information.</span></span>

## <a name="remarks"></a><span data-ttu-id="173b7-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="173b7-114">Remarks</span></span>

<span data-ttu-id="173b7-115">Die Struktur, die zum Darstellen von Zustandsinformationen verwendet wird, ist Treiber spezifisch und wird vom Treiber definiert.</span><span class="sxs-lookup"><span data-stu-id="173b7-115">The structure used to represent state information is driver specific and is defined by the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="173b7-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="173b7-116">Requirements</span></span>



| <span data-ttu-id="173b7-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="173b7-117">Requirement</span></span> | <span data-ttu-id="173b7-118">Wert</span><span class="sxs-lookup"><span data-stu-id="173b7-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="173b7-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="173b7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="173b7-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="173b7-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="173b7-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="173b7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="173b7-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="173b7-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="173b7-123">Header</span><span class="sxs-lookup"><span data-stu-id="173b7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="173b7-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="173b7-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="173b7-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="173b7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="173b7-126">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="173b7-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="173b7-127">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="173b7-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





