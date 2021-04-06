---
title: MCI_MAKE_HMS-Makro (mciapi. h)
description: Das MCI \_ -Element "Make \_ HMS" erstellt einen Zeitwert im Format "gepackte Stunden/Minuten/Sekunden" (HMS) aus den angegebenen Stunden, Minuten und Sekunden Werten.
ms.assetid: 470e89eb-36e1-4b05-babd-4c986adc88dd
keywords:
- MCI_MAKE_HMS Makro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_MAKE_HMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f37c95df89ed6a799575e964ae274e01e329ef1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743144"
---
# <a name="mci_make_hms-macro"></a><span data-ttu-id="3b630-104">MCI-Element " \_ \_ HMS"</span><span class="sxs-lookup"><span data-stu-id="3b630-104">MCI\_MAKE\_HMS macro</span></span>

<span data-ttu-id="3b630-105">Das **MCI-Element " \_ make \_ HMS** " erstellt einen Zeitwert im Format "gepackte Stunden/Minuten/Sekunden" (HMS) aus den angegebenen Stunden, Minuten und Sekunden Werten.</span><span class="sxs-lookup"><span data-stu-id="3b630-105">The **MCI\_MAKE\_HMS** macro creates a time value in packed hours/minutes/seconds (HMS) format from the given hours, minutes, and seconds values.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b630-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b630-106">Syntax</span></span>


```C++
DWORD MCI_MAKE_HMS(
   BYTE hours,
   BYTE minutes,
   BYTE seconds
);
```



## <a name="parameters"></a><span data-ttu-id="3b630-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b630-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b630-108">*hours*</span><span class="sxs-lookup"><span data-stu-id="3b630-108">*hours*</span></span> 
</dt> <dd>

<span data-ttu-id="3b630-109">Anzahl der Stunden.</span><span class="sxs-lookup"><span data-stu-id="3b630-109">Number of hours.</span></span>

</dd> <dt>

<span data-ttu-id="3b630-110">*minutes*</span><span class="sxs-lookup"><span data-stu-id="3b630-110">*minutes*</span></span> 
</dt> <dd>

<span data-ttu-id="3b630-111">Anzahl der Minuten.</span><span class="sxs-lookup"><span data-stu-id="3b630-111">Number of minutes.</span></span>

</dd> <dt>

<span data-ttu-id="3b630-112">*Sekunden*</span><span class="sxs-lookup"><span data-stu-id="3b630-112">*seconds*</span></span> 
</dt> <dd>

<span data-ttu-id="3b630-113">Anzahl der Sekunden.</span><span class="sxs-lookup"><span data-stu-id="3b630-113">Number of seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b630-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3b630-114">Return value</span></span>

<span data-ttu-id="3b630-115">Gibt die Zeit im gepackten HMS-Format zurück.</span><span class="sxs-lookup"><span data-stu-id="3b630-115">Returns the time in packed HMS format.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b630-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b630-116">Remarks</span></span>

<span data-ttu-id="3b630-117">Die Zeit im "HMS"-Format wird als **DWORD** -Wert mit dem niedrigsten signifikanten Byte, das Stunden enthält, dem nächst bedeutsamen Byte, das Minuten enthält, und dem nächstniedrigsten Byte mit Sekunden ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="3b630-117">Time in HMS format is expressed as a **DWORD** value with the least significant byte containing hours, the next least significant byte containing minutes, and the next least significant byte containing seconds.</span></span> <span data-ttu-id="3b630-118">Das signifikanteste Byte wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3b630-118">The most significant byte is unused.</span></span>

<span data-ttu-id="3b630-119">Das **MCI-Element " \_ make \_ HMS** " ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="3b630-119">The **MCI\_MAKE\_HMS** macro is defined as follows:</span></span>


```C++
#define MCI_MAKE_HMS(h, m, s) ((DWORD)(((BYTE)(h) | \ 
                              ((WORD)(m) << 8)) | \ 
                              (((DWORD)(BYTE)(s)) << 16))) 
```



## <a name="requirements"></a><span data-ttu-id="3b630-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3b630-120">Requirements</span></span>



| <span data-ttu-id="3b630-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3b630-121">Requirement</span></span> | <span data-ttu-id="3b630-122">Wert</span><span class="sxs-lookup"><span data-stu-id="3b630-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3b630-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3b630-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3b630-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3b630-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3b630-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3b630-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3b630-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3b630-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3b630-127">Header</span><span class="sxs-lookup"><span data-stu-id="3b630-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b630-128"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b630-128"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b630-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b630-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b630-130">MCI</span><span class="sxs-lookup"><span data-stu-id="3b630-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3b630-131">MCI-Makros</span><span class="sxs-lookup"><span data-stu-id="3b630-131">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





