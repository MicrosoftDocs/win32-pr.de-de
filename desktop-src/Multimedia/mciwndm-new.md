---
title: MCIWNDM_NEW Meldung (VFW. h)
description: Mit der neuen mciwndm- \_ Meldung wird eine neue Datei für das aktuelle MCI-Gerät erstellt. Sie können diese Nachricht explizit oder mithilfe des mciwndnew-Makros senden.
ms.assetid: 18b2340d-8303-415a-867f-bd346034db2a
keywords:
- MCIWNDM_NEW-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_NEW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 293323cd0404da45e648024b35b7f96ef60fea61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741161"
---
# <a name="mciwndm_new-message"></a><span data-ttu-id="5847d-105">Neue mciwndm- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="5847d-105">MCIWNDM\_NEW message</span></span>

<span data-ttu-id="5847d-106">Mit der **\_ neuen mciwndm** -Meldung wird eine neue Datei für das aktuelle MCI-Gerät erstellt.</span><span class="sxs-lookup"><span data-stu-id="5847d-106">The **MCIWNDM\_NEW** message creates a new file for the current MCI device.</span></span> <span data-ttu-id="5847d-107">Sie können diese Nachricht explizit oder mithilfe des [**mciwndnew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="5847d-107">You can send this message explicitly or by using the [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) macro.</span></span>


```C++
MCIWNDM_NEW 
wParam = 0; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="5847d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5847d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5847d-109"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="5847d-109"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="5847d-110">Zeiger auf einen Puffer, der den Namen des MCI-Geräts enthält, von dem die Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5847d-110">Pointer to a buffer containing the name of the MCI device that will use the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5847d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5847d-111">Return Value</span></span>

<span data-ttu-id="5847d-112">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="5847d-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5847d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5847d-113">Requirements</span></span>



| <span data-ttu-id="5847d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5847d-114">Requirement</span></span> | <span data-ttu-id="5847d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="5847d-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5847d-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5847d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5847d-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5847d-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5847d-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5847d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5847d-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5847d-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5847d-120">Header</span><span class="sxs-lookup"><span data-stu-id="5847d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5847d-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="5847d-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5847d-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5847d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5847d-123">**Mciwndnew**</span><span class="sxs-lookup"><span data-stu-id="5847d-123">**MCIWndNew**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndnew)
</dt> </dl>

 

 





