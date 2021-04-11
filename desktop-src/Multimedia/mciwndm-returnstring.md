---
title: MCIWNDM_RETURNSTRING Meldung (VFW. h)
description: Die mciwndm- \_ Nachricht "returnstring" Ruft die Antwort auf den aktuellen MCI-Zeichen folgen Befehl ab, der an ein MCI-Gerät gesendet wurde.
ms.assetid: 36a5222c-a63c-4b8c-ad0c-a00477e95b96
keywords:
- MCIWNDM_RETURNSTRING-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_RETURNSTRING
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b99307bd7d61a70db594d0a696cceccd6d246a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040580"
---
# <a name="mciwndm_returnstring-message"></a><span data-ttu-id="029d5-104">Mciwndm- \_ returnstring-Nachricht</span><span class="sxs-lookup"><span data-stu-id="029d5-104">MCIWNDM\_RETURNSTRING message</span></span>

<span data-ttu-id="029d5-105">Die **mciwndm-Nachricht " \_ returnstring** " Ruft die Antwort auf den aktuellen MCI-Zeichen folgen Befehl ab, der an ein MCI-Gerät gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="029d5-105">The **MCIWNDM\_RETURNSTRING** message retrieves the reply to the most recent MCI string command sent to an MCI device.</span></span> <span data-ttu-id="029d5-106">Die Informationen in der Antwort werden als eine auf NULL endenden Zeichenfolge bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="029d5-106">Information in the reply is supplied as a null-terminated string.</span></span> <span data-ttu-id="029d5-107">Sie können diese Nachricht explizit oder mithilfe des [**mciwndreturnstring**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="029d5-107">You can send this message explicitly or by using the [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) macro.</span></span>


```C++
MCIWNDM_RETURNSTRING 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="029d5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="029d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="029d5-109"><span id="len"></span><span id="LEN"></span>*Nest*</span><span class="sxs-lookup"><span data-stu-id="029d5-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="029d5-110">Größe (in Bytes) des Puffers.</span><span class="sxs-lookup"><span data-stu-id="029d5-110">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="029d5-111"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="029d5-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="029d5-112">Ein Zeiger auf einen Anwendungs definierten Puffer, der die auf NULL endenden Zeichenfolge enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="029d5-112">Pointer to an application-defined buffer to contain the null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="029d5-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="029d5-113">Return Value</span></span>

<span data-ttu-id="029d5-114">Gibt eine ganze Zahl zurück, die der MCI-Zeichenfolge entspricht.</span><span class="sxs-lookup"><span data-stu-id="029d5-114">Returns an integer corresponding to the MCI string.</span></span>

## <a name="remarks"></a><span data-ttu-id="029d5-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="029d5-115">Remarks</span></span>

<span data-ttu-id="029d5-116">Wenn die NULL-terminierte Zeichenfolge länger als der Puffer ist, wird die Zeichenfolge abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="029d5-116">If the null-terminated string is longer than the buffer, the string is truncated.</span></span>

## <a name="requirements"></a><span data-ttu-id="029d5-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="029d5-117">Requirements</span></span>



| <span data-ttu-id="029d5-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="029d5-118">Requirement</span></span> | <span data-ttu-id="029d5-119">Wert</span><span class="sxs-lookup"><span data-stu-id="029d5-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="029d5-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="029d5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="029d5-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="029d5-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="029d5-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="029d5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="029d5-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="029d5-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="029d5-124">Header</span><span class="sxs-lookup"><span data-stu-id="029d5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="029d5-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="029d5-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="029d5-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="029d5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="029d5-127">**Mciwndreturnstring**</span><span class="sxs-lookup"><span data-stu-id="029d5-127">**MCIWndReturnString**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring)
</dt> </dl>

 

 





