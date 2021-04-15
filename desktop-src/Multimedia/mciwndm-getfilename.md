---
title: MCIWNDM_GETFILENAME Meldung (VFW. h)
description: Die mciwndm \_ GetFileName-Nachricht Ruft den Dateinamen ab, der derzeit von einem MCI-Gerät verwendet wird. Sie können diese Nachricht explizit oder mit dem mciwndgetfilename-Makro senden.
ms.assetid: d61b1b6d-0fae-4732-993c-41e08a4e05be
keywords:
- MCIWNDM_GETFILENAME-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETFILENAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 232a1d829b5cdd6da23e7dd3fb0294b95ca79f4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517426"
---
# <a name="mciwndm_getfilename-message"></a><span data-ttu-id="87efc-105">Mciwndm \_ GetFileName-Meldung</span><span class="sxs-lookup"><span data-stu-id="87efc-105">MCIWNDM\_GETFILENAME message</span></span>

<span data-ttu-id="87efc-106">Die **mciwndm \_ GetFileName** -Nachricht Ruft den Dateinamen ab, der derzeit von einem MCI-Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="87efc-106">The **MCIWNDM\_GETFILENAME** message retrieves the filename currently used by an MCI device.</span></span> <span data-ttu-id="87efc-107">Sie können diese Nachricht explizit oder mit dem [**mciwndgetfilename**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="87efc-107">You can send this message explicitly or by using the [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) macro.</span></span>


```C++
MCIWNDM_GETFILENAME 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="87efc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="87efc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87efc-109"><span id="len"></span><span id="LEN"></span>*Nest*</span><span class="sxs-lookup"><span data-stu-id="87efc-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="87efc-110">Größe (in Bytes) des Puffers.</span><span class="sxs-lookup"><span data-stu-id="87efc-110">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="87efc-111"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="87efc-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="87efc-112">Zeiger auf einen Anwendungs definierten Puffer, um den Dateinamen zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="87efc-112">Pointer to an application-defined buffer to return the filename.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87efc-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="87efc-113">Return Value</span></span>

<span data-ttu-id="87efc-114">Gibt NULL zurück, wenn erfolgreich oder andernfalls 1.</span><span class="sxs-lookup"><span data-stu-id="87efc-114">Returns zero if successful or 1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="87efc-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87efc-115">Remarks</span></span>

<span data-ttu-id="87efc-116">Wenn die mit NULL endenden Zeichenfolge, die den Dateinamen enthält, länger ist als der Puffer, wird der Dateiname von mciwnd abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="87efc-116">If the null-terminated string containing the filename is longer than the buffer, MCIWnd truncates the filename.</span></span>

## <a name="requirements"></a><span data-ttu-id="87efc-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87efc-117">Requirements</span></span>



| <span data-ttu-id="87efc-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87efc-118">Requirement</span></span> | <span data-ttu-id="87efc-119">Wert</span><span class="sxs-lookup"><span data-stu-id="87efc-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="87efc-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="87efc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="87efc-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87efc-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="87efc-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="87efc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="87efc-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87efc-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="87efc-124">Header</span><span class="sxs-lookup"><span data-stu-id="87efc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="87efc-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="87efc-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87efc-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87efc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87efc-127">**Mciwndgetfilename**</span><span class="sxs-lookup"><span data-stu-id="87efc-127">**MCIWndGetFileName**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename)
</dt> </dl>

 

 





