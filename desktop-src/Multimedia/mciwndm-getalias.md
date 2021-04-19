---
title: MCIWNDM_GETALIAS Meldung (VFW. h)
description: Die mciwndm \_ getalias-Nachricht Ruft den Alias ab, mit dem ein MCI-Gerät oder eine MCI-Datei mit der mciSendString-Funktion geöffnet wird. Sie können diese Nachricht explizit oder mithilfe des Makros mciwndgetalias senden.
ms.assetid: 37131b89-275c-4ab6-9278-0e08c42471bd
keywords:
- MCIWNDM_GETALIAS-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETALIAS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e971c50b9abc450387ac29f9a7331bfdca5c38c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342182"
---
# <a name="mciwndm_getalias-message"></a><span data-ttu-id="e6b82-105">Mciwndm \_ getalias-Nachricht</span><span class="sxs-lookup"><span data-stu-id="e6b82-105">MCIWNDM\_GETALIAS message</span></span>

<span data-ttu-id="e6b82-106">Die **mciwndm \_ getalias** -Nachricht Ruft den Alias ab, mit dem ein MCI-Gerät oder eine MCI-Datei mit der [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="e6b82-106">The **MCIWNDM\_GETALIAS** message retrieves the alias used to open an MCI device or file with the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span> <span data-ttu-id="e6b82-107">Sie können diese Nachricht explizit oder mithilfe des Makros [**mciwndgetalias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) senden.</span><span class="sxs-lookup"><span data-stu-id="e6b82-107">You can send this message explicitly or by using the [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) macro.</span></span>


```C++
MCIWNDM_GETALIAS 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="e6b82-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6b82-108">Return Value</span></span>

<span data-ttu-id="e6b82-109">Gibt den Gerätealias zurück.</span><span class="sxs-lookup"><span data-stu-id="e6b82-109">Returns the device alias.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6b82-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6b82-110">Requirements</span></span>



| <span data-ttu-id="e6b82-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6b82-111">Requirement</span></span> | <span data-ttu-id="e6b82-112">Wert</span><span class="sxs-lookup"><span data-stu-id="e6b82-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e6b82-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6b82-113">Minimum supported client</span></span><br/> | <span data-ttu-id="e6b82-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6b82-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e6b82-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6b82-115">Minimum supported server</span></span><br/> | <span data-ttu-id="e6b82-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6b82-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e6b82-117">Header</span><span class="sxs-lookup"><span data-stu-id="e6b82-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6b82-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6b82-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6b82-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6b82-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="e6b82-120">[**mciSendString**](/previous-versions//dd757161(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e6b82-120">[**mciSendString**](/previous-versions//dd757161(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e6b82-121">**Mciwndgetalias**</span><span class="sxs-lookup"><span data-stu-id="e6b82-121">**MCIWndGetAlias**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias)
</dt> </dl>

 

