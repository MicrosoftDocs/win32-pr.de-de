---
title: ICM_ABOUT Meldung (VFW. h)
description: In der ICM Info- \_ Meldung wird ein Video Komprimierungs Treiber benachrichtigt, um das Dialogfeld Info anzuzeigen, oder ein Video Komprimierungs Treiber wird abgefragt, um zu bestimmen, ob er über ein Dialogfeld Info verfügt Sie können diese Nachricht explizit oder mithilfe des icabout-Makros senden.
ms.assetid: 6eca69a3-0463-48e6-befb-5003b7515e7d
keywords:
- ICM_ABOUT-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_ABOUT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1e03e88993ba1e345a3ea32a9de7adb2d63abe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040079"
---
# <a name="icm_about-message"></a><span data-ttu-id="2df20-105">ICM \_ zur Meldung</span><span class="sxs-lookup"><span data-stu-id="2df20-105">ICM\_ABOUT message</span></span>

<span data-ttu-id="2df20-106">In der ICM Info-Meldung wird ein Video Komprimierungs Treiber benachrichtigt, um das Dialogfeld Info anzuzeigen, oder ein Video Komprimierungs Treiber wird abgefragt, um zu bestimmen, ob er über ein Dialogfeld Info verfügt **\_**</span><span class="sxs-lookup"><span data-stu-id="2df20-106">The **ICM\_ABOUT** message notifies a video compression driver to display its About dialog box or queries a video compression driver to determine if it has an About dialog box.</span></span> <span data-ttu-id="2df20-107">Sie können diese Nachricht explizit oder mithilfe des [**icabout**](/windows/desktop/api/Vfw/nf-vfw-icabout) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="2df20-107">You can send this message explicitly or by using the [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) macro.</span></span>


```C++
ICM_ABOUT 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="2df20-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2df20-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2df20-109"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="2df20-109"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="2df20-110">Handle für das übergeordnete Fenster des angezeigten Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="2df20-110">Handle to the parent window of the displayed dialog box.</span></span> <span data-ttu-id="2df20-111">Sie können auch bestimmen, ob ein Treiber über ein Dialogfeld Info verfügt, indem Sie-1 in diesem Parameter angeben, wie im [**icqueryabout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) -Makro.</span><span class="sxs-lookup"><span data-stu-id="2df20-111">You can also determine if a driver has an About dialog box by specifying -1 in this parameter, as in the [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) macro.</span></span> <span data-ttu-id="2df20-112">Der Treiber gibt ICERR \_ OK zurück, wenn ein Info Dialogfeld oder ICERR \_ nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="2df20-112">The driver returns ICERR\_OK if it has an About dialog box or ICERR\_UNSUPPORTED otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2df20-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2df20-113">Return Value</span></span>

<span data-ttu-id="2df20-114">Gibt ICERR \_ OK zurück, wenn der Treiber diese Nachricht unterstützt oder wenn ICERR \_ andernfalls nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="2df20-114">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="2df20-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2df20-115">Requirements</span></span>



| <span data-ttu-id="2df20-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2df20-116">Requirement</span></span> | <span data-ttu-id="2df20-117">Wert</span><span class="sxs-lookup"><span data-stu-id="2df20-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2df20-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2df20-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2df20-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2df20-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2df20-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2df20-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2df20-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2df20-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2df20-122">Header</span><span class="sxs-lookup"><span data-stu-id="2df20-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2df20-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2df20-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2df20-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2df20-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2df20-125">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="2df20-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="2df20-126">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="2df20-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





