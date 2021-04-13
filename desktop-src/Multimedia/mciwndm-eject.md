---
title: MCIWNDM_EJECT Meldung (VFW. h)
description: Die mciwndm- \_ Ausgabenachricht sendet einen Befehl an ein MCI-Gerät, um Ihre Medien auszuewerfen. Sie können diese Nachricht explizit oder mithilfe des mciwndeject-Makros senden.
ms.assetid: a492f504-8b58-480e-9766-bc2878466c44
keywords:
- MCIWNDM_EJECT-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_EJECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e41686ce41b82dc48ee6c22ac556606c79c5b24a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391644"
---
# <a name="mciwndm_eject-message"></a><span data-ttu-id="c47a3-105">Mciwndm- \_ Ausgabenachricht</span><span class="sxs-lookup"><span data-stu-id="c47a3-105">MCIWNDM\_EJECT message</span></span>

<span data-ttu-id="c47a3-106">Die **mciwndm \_ -Ausgabenachricht** sendet einen Befehl an ein MCI-Gerät, um Ihre Medien auszuewerfen.</span><span class="sxs-lookup"><span data-stu-id="c47a3-106">The **MCIWNDM\_EJECT** message sends a command to an MCI device to eject its media.</span></span> <span data-ttu-id="c47a3-107">Sie können diese Nachricht explizit oder mithilfe des [**mciwndeject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="c47a3-107">You can send this message explicitly or by using the [**MCIWndEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject) macro.</span></span>


```C++
MCIWNDM_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="c47a3-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c47a3-108">Return Value</span></span>

<span data-ttu-id="c47a3-109">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="c47a3-109">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c47a3-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c47a3-110">Requirements</span></span>



| <span data-ttu-id="c47a3-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c47a3-111">Requirement</span></span> | <span data-ttu-id="c47a3-112">Wert</span><span class="sxs-lookup"><span data-stu-id="c47a3-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c47a3-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c47a3-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c47a3-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c47a3-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c47a3-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c47a3-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c47a3-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c47a3-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c47a3-117">Header</span><span class="sxs-lookup"><span data-stu-id="c47a3-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="c47a3-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c47a3-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c47a3-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c47a3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c47a3-120">**Mciwndebug**</span><span class="sxs-lookup"><span data-stu-id="c47a3-120">**MCIWndEject**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndeject)
</dt> </dl>

 

 





