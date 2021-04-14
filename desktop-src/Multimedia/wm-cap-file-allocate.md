---
title: WM_CAP_FILE_ALLOCATE Meldung (VFW. h)
description: Die "WM Cap"-Datei Zuordnungs \_ \_ \_ Nachricht erstellt eine Erfassungs Datei mit einer angegebenen Größe (weist diese vorab zu). Sie können diese Nachricht explizit oder mithilfe des capfilezuc-Makros senden.
ms.assetid: 31ebe824-4a30-4212-9479-a5cbd8fc1e1d
keywords:
- WM_CAP_FILE_ALLOCATE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_FILE_ALLOCATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d36cec54e5775641118679b24b0d4b3b1767693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475855"
---
# <a name="wm_cap_file_allocate-message"></a><span data-ttu-id="63b93-105">Datei Zuordnungs Nachricht für WM- \_ Cap \_ \_</span><span class="sxs-lookup"><span data-stu-id="63b93-105">WM\_CAP\_FILE\_ALLOCATE message</span></span>

<span data-ttu-id="63b93-106">Die " **WM Cap"- \_ \_ Datei \_** Zuordnungs Nachricht erstellt eine Erfassungs Datei mit einer angegebenen Größe (weist diese vorab zu).</span><span class="sxs-lookup"><span data-stu-id="63b93-106">The **WM\_CAP\_FILE\_ALLOCATE** message creates (preallocates) a capture file of a specified size.</span></span> <span data-ttu-id="63b93-107">Sie können diese Nachricht explizit oder mithilfe des [**capfilezuc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="63b93-107">You can send this message explicitly or by using the [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) macro.</span></span>


```C++
WM_CAP_FILE_ALLOCATE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (DWORD) (dwSize); 
```



## <a name="parameters"></a><span data-ttu-id="63b93-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="63b93-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63b93-109"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>*dwSize*</span><span class="sxs-lookup"><span data-stu-id="63b93-109"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>*dwSize*</span></span>
</dt> <dd>

<span data-ttu-id="63b93-110">Größe (in Bytes) zum Erstellen der Erfassungs Datei.</span><span class="sxs-lookup"><span data-stu-id="63b93-110">Size, in bytes, to create the capture file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63b93-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="63b93-111">Return Value</span></span>

<span data-ttu-id="63b93-112">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="63b93-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="63b93-113">Wenn ein Fehler auftritt und eine Fehler Rückruffunktion mithilfe der WM- [**\_ Cap- \_ \_ Rückruf \_ Fehlermeldung**](wm-cap-set-callback-error.md) festgelegt wird, wird die Fehler Rückruffunktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="63b93-113">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="63b93-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="63b93-114">Remarks</span></span>

<span data-ttu-id="63b93-115">Sie können die Leistung des Streamings erheblich verbessern, indem Sie eine Erfassungs Datei, die groß genug zum Speichern eines gesamten Videoclips ist, vorab zuordnen und die Erfassungs Datei vor dem Erfassen des Clips defragmentieren.</span><span class="sxs-lookup"><span data-stu-id="63b93-115">You can improve streaming capture performance significantly by preallocating a capture file large enough to store an entire video clip and by defragmenting the capture file before capturing the clip.</span></span>

## <a name="requirements"></a><span data-ttu-id="63b93-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63b93-116">Requirements</span></span>



| <span data-ttu-id="63b93-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63b93-117">Requirement</span></span> | <span data-ttu-id="63b93-118">Wert</span><span class="sxs-lookup"><span data-stu-id="63b93-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="63b93-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="63b93-119">Minimum supported client</span></span><br/> | <span data-ttu-id="63b93-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="63b93-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="63b93-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="63b93-121">Minimum supported server</span></span><br/> | <span data-ttu-id="63b93-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="63b93-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="63b93-123">Header</span><span class="sxs-lookup"><span data-stu-id="63b93-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="63b93-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="63b93-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63b93-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63b93-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63b93-126">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="63b93-126">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="63b93-127">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="63b93-127">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





