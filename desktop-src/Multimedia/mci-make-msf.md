---
title: MCI_MAKE_MSF-Makro (mciapi. h)
description: Das MCI \_ make \_ MSF-Makro erstellt einen Zeitwert im MSF-Format (gepackt Minutes/seconds/Frames) aus den angegebenen Minuten, Sekunden und Frame Werten.
ms.assetid: 8c981d84-b049-4448-a820-bff30896065e
keywords:
- MCI_MAKE_MSF Makro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_MAKE_MSF
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae7e8566986337d6b9b5161c85bcc62cecc52be0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957161"
---
# <a name="mci_make_msf-macro"></a><span data-ttu-id="8fdc2-104">MCI- \_ make \_ MSF-Makro</span><span class="sxs-lookup"><span data-stu-id="8fdc2-104">MCI\_MAKE\_MSF macro</span></span>

<span data-ttu-id="8fdc2-105">Das **MCI \_ make \_ MSF** -Makro erstellt einen Zeitwert im MSF-Format (gepackt Minutes/seconds/Frames) aus den angegebenen Minuten, Sekunden und Frame Werten.</span><span class="sxs-lookup"><span data-stu-id="8fdc2-105">The **MCI\_MAKE\_MSF** macro creates a time value in packed minutes/seconds/frames (MSF) format from the given minutes, seconds, and frame values.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fdc2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8fdc2-106">Syntax</span></span>


```C++
DWORD MCI_MAKE_MSF(
   BYTE minutes,
   BYTE seconds,
   BYTE frames
);
```



## <a name="parameters"></a><span data-ttu-id="8fdc2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8fdc2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fdc2-108">*minutes*</span><span class="sxs-lookup"><span data-stu-id="8fdc2-108">*minutes*</span></span> 
</dt> <dd>

<span data-ttu-id="8fdc2-109">Anzahl der Minuten.</span><span class="sxs-lookup"><span data-stu-id="8fdc2-109">Number of minutes.</span></span>

</dd> <dt>

<span data-ttu-id="8fdc2-110">*Sekunden*</span><span class="sxs-lookup"><span data-stu-id="8fdc2-110">*seconds*</span></span> 
</dt> <dd>

<span data-ttu-id="8fdc2-111">Anzahl der Sekunden.</span><span class="sxs-lookup"><span data-stu-id="8fdc2-111">Number of seconds.</span></span>

</dd> <dt>

<span data-ttu-id="8fdc2-112">*SSE*</span><span class="sxs-lookup"><span data-stu-id="8fdc2-112">*frames*</span></span> 
</dt> <dd>

<span data-ttu-id="8fdc2-113">Anzahl der Frames.</span><span class="sxs-lookup"><span data-stu-id="8fdc2-113">Number of frames.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fdc2-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8fdc2-114">Return value</span></span>

<span data-ttu-id="8fdc2-115">Gibt die Zeit im gepackten MSF-Format zurück.</span><span class="sxs-lookup"><span data-stu-id="8fdc2-115">Returns the time in packed MSF format.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fdc2-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8fdc2-116">Remarks</span></span>

<span data-ttu-id="8fdc2-117">Die Zeit im MSF-Format wird als **DWORD** -Wert mit dem niedrigsten signifikanten Byte, das Minuten enthält, dem nächst bedeutsamen Byte, das Sekunden enthält, und dem nächstniedrigsten Byte mit Frames ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="8fdc2-117">Time in MSF format is expressed as a **DWORD** value with the least significant byte containing minutes, the next least significant byte containing seconds, and the next least significant byte containing frames.</span></span> <span data-ttu-id="8fdc2-118">Das signifikanteste Byte wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8fdc2-118">The most significant byte is unused.</span></span>

<span data-ttu-id="8fdc2-119">Das **MCI- \_ make- \_ MSF** -Makro wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="8fdc2-119">The **MCI\_MAKE\_MSF** macro is defined as follows:</span></span>


```C++
#define MCI_MAKE_MSF(m, s, f) ((DWORD)(((BYTE)(m) | \ 
                              ((WORD)(s) << 8)) | \ 
                              (((DWORD)(BYTE)(f)) << 16))) 
```



## <a name="requirements"></a><span data-ttu-id="8fdc2-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8fdc2-120">Requirements</span></span>



| <span data-ttu-id="8fdc2-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8fdc2-121">Requirement</span></span> | <span data-ttu-id="8fdc2-122">Wert</span><span class="sxs-lookup"><span data-stu-id="8fdc2-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8fdc2-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8fdc2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8fdc2-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8fdc2-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8fdc2-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8fdc2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8fdc2-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8fdc2-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8fdc2-127">Header</span><span class="sxs-lookup"><span data-stu-id="8fdc2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fdc2-128"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fdc2-128"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fdc2-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8fdc2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fdc2-130">MCI</span><span class="sxs-lookup"><span data-stu-id="8fdc2-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8fdc2-131">MCI-Makros</span><span class="sxs-lookup"><span data-stu-id="8fdc2-131">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





