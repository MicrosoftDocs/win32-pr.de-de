---
title: MCIWNDM_GETERROR Meldung (VFW. h)
description: Die mciwndm \_ getError-Nachricht Ruft den letzten gefundenen MCI-Fehler ab. Sie können diese Nachricht explizit oder mit dem mciwndgeterror-Makro senden.
ms.assetid: f110a9b3-5b05-4bf0-85d1-b49ce7396222
keywords:
- MCIWNDM_GETERROR-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c2977bb079351824b48da21f4ba3cc2dc5afe7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858705"
---
# <a name="mciwndm_geterror-message"></a><span data-ttu-id="e516c-105">Mciwndm \_ getError-Meldung</span><span class="sxs-lookup"><span data-stu-id="e516c-105">MCIWNDM\_GETERROR message</span></span>

<span data-ttu-id="e516c-106">Die **mciwndm \_ getError** -Nachricht Ruft den letzten gefundenen MCI-Fehler ab.</span><span class="sxs-lookup"><span data-stu-id="e516c-106">The **MCIWNDM\_GETERROR** message retrieves the last MCI error encountered.</span></span> <span data-ttu-id="e516c-107">Sie können diese Nachricht explizit oder mit dem [**mciwndgeterror**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="e516c-107">You can send this message explicitly or by using the [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) macro.</span></span>


```C++
MCIWNDM_GETERROR 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="e516c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e516c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e516c-109"><span id="len"></span><span id="LEN"></span>*Nest*</span><span class="sxs-lookup"><span data-stu-id="e516c-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="e516c-110">Größe (in Bytes) des Fehler Puffers.</span><span class="sxs-lookup"><span data-stu-id="e516c-110">Size, in bytes, of the error buffer.</span></span>

</dd> <dt>

<span data-ttu-id="e516c-111"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="e516c-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="e516c-112">Zeiger auf einen Anwendungs definierten Puffer, der zum Zurückgeben der Fehler Zeichenfolge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e516c-112">Pointer to an application-defined buffer used to return the error string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e516c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e516c-113">Return Value</span></span>

<span data-ttu-id="e516c-114">Gibt den ganzzahligen Fehlerwert zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="e516c-114">Returns the integer error value if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e516c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e516c-115">Remarks</span></span>

<span data-ttu-id="e516c-116">Wenn die *LP* ein gültiger Zeiger ist, wird eine mit NULL beendete Zeichenfolge, die dem Fehler entspricht, im Puffer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e516c-116">If *lp* is a valid pointer, a null-terminated string corresponding to the error is returned in its buffer.</span></span> <span data-ttu-id="e516c-117">Wenn die Fehler Zeichenfolge länger als der Puffer ist, wird Sie von mciwnd abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="e516c-117">If the error string is longer than the buffer, MCIWnd truncates it.</span></span>

## <a name="requirements"></a><span data-ttu-id="e516c-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e516c-118">Requirements</span></span>



| <span data-ttu-id="e516c-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e516c-119">Requirement</span></span> | <span data-ttu-id="e516c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="e516c-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e516c-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e516c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e516c-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e516c-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e516c-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e516c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e516c-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e516c-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e516c-125">Header</span><span class="sxs-lookup"><span data-stu-id="e516c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e516c-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e516c-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e516c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e516c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e516c-128">**Mciwndgeterror**</span><span class="sxs-lookup"><span data-stu-id="e516c-128">**MCIWndGetError**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror)
</dt> </dl>

 

 





