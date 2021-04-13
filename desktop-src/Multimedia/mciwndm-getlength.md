---
title: MCIWNDM_GETLENGTH Meldung (VFW. h)
description: Die mciwndm \_ GetLength-Nachricht Ruft die Länge des Inhalts oder der Datei ab, die derzeit von einem MCI-Gerät verwendet wird. Sie können diese Nachricht explizit oder mit dem mciwndgetlength-Makro senden.
ms.assetid: bee4d9fc-78eb-4577-98bb-d6c2d9acbb7f
keywords:
- MCIWNDM_GETLENGTH-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETLENGTH
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2347647fcff0beb87be12b7f6a05790b97f36d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475528"
---
# <a name="mciwndm_getlength-message"></a><span data-ttu-id="6c827-105">Mciwndm \_ GetLength-Nachricht</span><span class="sxs-lookup"><span data-stu-id="6c827-105">MCIWNDM\_GETLENGTH message</span></span>

<span data-ttu-id="6c827-106">Die **mciwndm \_ GetLength** -Nachricht Ruft die Länge des Inhalts oder der Datei ab, die derzeit von einem MCI-Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6c827-106">The **MCIWNDM\_GETLENGTH** message retrieves the length of the content or file currently used by an MCI device.</span></span> <span data-ttu-id="6c827-107">Sie können diese Nachricht explizit oder mit dem [**mciwndgetlength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="6c827-107">You can send this message explicitly or by using the [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) macro.</span></span>


```C++
MCIWNDM_GETLENGTH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="6c827-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c827-108">Return Value</span></span>

<span data-ttu-id="6c827-109">Gibt die Länge zurück.</span><span class="sxs-lookup"><span data-stu-id="6c827-109">Returns the length.</span></span> <span data-ttu-id="6c827-110">Die Einheiten für die Länge hängen vom aktuellen Zeitformat ab.</span><span class="sxs-lookup"><span data-stu-id="6c827-110">The units for the length depend on the current time format.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c827-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c827-111">Requirements</span></span>



| <span data-ttu-id="6c827-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c827-112">Requirement</span></span> | <span data-ttu-id="6c827-113">Wert</span><span class="sxs-lookup"><span data-stu-id="6c827-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6c827-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c827-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6c827-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c827-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6c827-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c827-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6c827-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c827-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6c827-118">Header</span><span class="sxs-lookup"><span data-stu-id="6c827-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c827-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c827-119"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c827-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c827-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c827-121">**Mciwndgetlength**</span><span class="sxs-lookup"><span data-stu-id="6c827-121">**MCIWndGetLength**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength)
</dt> </dl>

 

 





