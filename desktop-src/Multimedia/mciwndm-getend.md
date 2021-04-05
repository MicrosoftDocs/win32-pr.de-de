---
title: MCIWNDM_GETEND Meldung (VFW. h)
description: Die mciwndm \_ GetEnd-Nachricht Ruft den Speicherort ab, an dem das Ende des Inhalts eines MCI-Geräts oder einer MCI-Datei gespeichert ist. Sie können diese Nachricht explizit oder mithilfe des Makros mciwndgetend senden.
ms.assetid: 3fa45928-af63-4f87-835d-f409011a797e
keywords:
- MCIWNDM_GETEND-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETEND
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00d18057619e31fa9b22d7f6354527c394c02798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859220"
---
# <a name="mciwndm_getend-message"></a><span data-ttu-id="773e3-105">Mciwndm \_ GetEnd-Nachricht</span><span class="sxs-lookup"><span data-stu-id="773e3-105">MCIWNDM\_GETEND message</span></span>

<span data-ttu-id="773e3-106">Die **mciwndm \_ GetEnd** -Nachricht Ruft den Speicherort ab, an dem das Ende des Inhalts eines MCI-Geräts oder einer MCI-Datei gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="773e3-106">The **MCIWNDM\_GETEND** message retrieves the location of the end of the content of an MCI device or file.</span></span> <span data-ttu-id="773e3-107">Sie können diese Nachricht explizit oder mithilfe des Makros [**mciwndgetend**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) senden.</span><span class="sxs-lookup"><span data-stu-id="773e3-107">You can send this message explicitly or by using the [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) macro.</span></span>


```C++
MCIWNDM_GETEND 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="773e3-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="773e3-108">Return Value</span></span>

<span data-ttu-id="773e3-109">Gibt den Speicherort im aktuellen Zeitformat zurück.</span><span class="sxs-lookup"><span data-stu-id="773e3-109">Returns the location in the current time format.</span></span>

## <a name="requirements"></a><span data-ttu-id="773e3-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="773e3-110">Requirements</span></span>



| <span data-ttu-id="773e3-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="773e3-111">Requirement</span></span> | <span data-ttu-id="773e3-112">Wert</span><span class="sxs-lookup"><span data-stu-id="773e3-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="773e3-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="773e3-113">Minimum supported client</span></span><br/> | <span data-ttu-id="773e3-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="773e3-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="773e3-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="773e3-115">Minimum supported server</span></span><br/> | <span data-ttu-id="773e3-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="773e3-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="773e3-117">Header</span><span class="sxs-lookup"><span data-stu-id="773e3-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="773e3-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="773e3-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="773e3-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="773e3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="773e3-120">**Mciwndgetend**</span><span class="sxs-lookup"><span data-stu-id="773e3-120">**MCIWndGetEnd**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend)
</dt> </dl>

 

 





