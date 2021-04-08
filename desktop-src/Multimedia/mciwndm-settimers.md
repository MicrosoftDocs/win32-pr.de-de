---
title: MCIWNDM_SETTIMERS Meldung (VFW. h)
description: Die mciwndm \_ settimers-Nachricht legt die Aktualisierungs Zeiträume fest, die von mciwnd verwendet werden, um die TrackBar im mciwnd-Fenster zu aktualisieren, die in der Fenstertitelleiste angezeigten Positionsinformationen zu aktualisieren und Benachrichtigungs Meldungen an das übergeordnete Fenster zu senden.
ms.assetid: 06407c67-b620-4f80-9fe9-456cdf3d0666
keywords:
- MCIWNDM_SETTIMERS-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMERS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bba3fa2e474a15dc23deb9cdc6d00d148b8cd3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740233"
---
# <a name="mciwndm_settimers-message"></a><span data-ttu-id="b4d9d-104">Mciwndm \_ settimers-Nachricht</span><span class="sxs-lookup"><span data-stu-id="b4d9d-104">MCIWNDM\_SETTIMERS message</span></span>

<span data-ttu-id="b4d9d-105">Die **mciwndm \_ settimers** -Nachricht legt die Aktualisierungs Zeiträume fest, die von mciwnd verwendet werden, um die TrackBar im mciwnd-Fenster zu aktualisieren, die in der Fenstertitelleiste angezeigten Positionsinformationen zu aktualisieren und Benachrichtigungs Meldungen an das übergeordnete Fenster zu senden.</span><span class="sxs-lookup"><span data-stu-id="b4d9d-105">The **MCIWNDM\_SETTIMERS** message sets the update periods used by MCIWnd to update the trackbar in the MCIWnd window, update the position information displayed in the window title bar, and send notification messages to the parent window.</span></span> <span data-ttu-id="b4d9d-106">Sie können diese Nachricht explizit oder mithilfe des Makros [**mciwndsettimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) senden.</span><span class="sxs-lookup"><span data-stu-id="b4d9d-106">You can send this message explicitly or by using the [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) macro.</span></span>


```C++
MCIWNDM_SETTIMERS 
wParam = (WPARAM) (UINT) active; 
lParam = (LPARAM) (UINT) inactive; 
```



## <a name="parameters"></a><span data-ttu-id="b4d9d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4d9d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4d9d-108"><span id="active"></span><span id="ACTIVE"></span>*enden*</span><span class="sxs-lookup"><span data-stu-id="b4d9d-108"><span id="active"></span><span id="ACTIVE"></span>*active*</span></span>
</dt> <dd>

<span data-ttu-id="b4d9d-109">Aktualisierungs Zeitraum, der von mciwnd verwendet wird, wenn es sich um das aktive Fenster handelt.</span><span class="sxs-lookup"><span data-stu-id="b4d9d-109">Update period used by MCIWnd when it is the active window.</span></span> <span data-ttu-id="b4d9d-110">Der Standardwert ist 500 Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="b4d9d-110">The default value is 500 milliseconds.</span></span> <span data-ttu-id="b4d9d-111">Der Speicher für diesen Wert ist auf 16 Bits beschränkt.</span><span class="sxs-lookup"><span data-stu-id="b4d9d-111">Storage for this value is limited to 16 bits.</span></span>

</dd> <dt>

<span data-ttu-id="b4d9d-112"><span id="inactive"></span><span id="INACTIVE"></span>*VSTE*</span><span class="sxs-lookup"><span data-stu-id="b4d9d-112"><span id="inactive"></span><span id="INACTIVE"></span>*inactive*</span></span>
</dt> <dd>

<span data-ttu-id="b4d9d-113">Update Zeitraum, der von mciwnd verwendet wird, wenn es sich um das inaktive Fenster handelt.</span><span class="sxs-lookup"><span data-stu-id="b4d9d-113">Update period used by MCIWnd when it is the inactive window.</span></span> <span data-ttu-id="b4d9d-114">Der Standardwert beträgt 2.000 Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="b4d9d-114">The default value is 2000 milliseconds.</span></span> <span data-ttu-id="b4d9d-115">Der Speicher für diesen Wert ist auf 16 Bits beschränkt.</span><span class="sxs-lookup"><span data-stu-id="b4d9d-115">Storage for this value is limited to 16 bits.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4d9d-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b4d9d-116">Return Value</span></span>

<span data-ttu-id="b4d9d-117">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b4d9d-117">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4d9d-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4d9d-118">Requirements</span></span>



| <span data-ttu-id="b4d9d-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4d9d-119">Requirement</span></span> | <span data-ttu-id="b4d9d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b4d9d-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b4d9d-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b4d9d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b4d9d-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b4d9d-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b4d9d-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b4d9d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b4d9d-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b4d9d-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b4d9d-125">Header</span><span class="sxs-lookup"><span data-stu-id="b4d9d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4d9d-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4d9d-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4d9d-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4d9d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4d9d-128">**Mciwndsettimers**</span><span class="sxs-lookup"><span data-stu-id="b4d9d-128">**MCIWndSetTimers**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers)
</dt> </dl>

 

 





