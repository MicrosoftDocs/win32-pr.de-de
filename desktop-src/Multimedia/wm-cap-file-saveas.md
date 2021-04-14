---
title: WM_CAP_FILE_SAVEAS Meldung (VFW. h)
description: Die "WM Cap"- \_ \_ Datei " \_ SaveAs" kopiert den Inhalt der Erfassungs Datei in eine andere Datei. Sie können diese Nachricht explizit oder mithilfe des "capfilesaveas"-Makros senden.
ms.assetid: fab37bee-3160-4ebc-b58f-46021ed49b55
keywords:
- WM_CAP_FILE_SAVEAS-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEAS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aca099fefab7ca0f4ef391b1b65e89938a947a01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391712"
---
# <a name="wm_cap_file_saveas-message"></a><span data-ttu-id="9613e-105">\_Datei " \_ \_ SaveAs" der WM-Cap-Datei</span><span class="sxs-lookup"><span data-stu-id="9613e-105">WM\_CAP\_FILE\_SAVEAS message</span></span>

<span data-ttu-id="9613e-106">Die " **WM Cap"- \_ Datei " \_ \_ SaveAs** " kopiert den Inhalt der Erfassungs Datei in eine andere Datei.</span><span class="sxs-lookup"><span data-stu-id="9613e-106">The **WM\_CAP\_FILE\_SAVEAS** message copies the contents of the capture file to another file.</span></span> <span data-ttu-id="9613e-107">Sie können diese Nachricht explizit oder mithilfe des " [**capfilesaveas**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) "-Makros senden.</span><span class="sxs-lookup"><span data-stu-id="9613e-107">You can send this message explicitly or by using the [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) macro.</span></span>


```C++
WM_CAP_FILE_SAVEAS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="9613e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9613e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9613e-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="9613e-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="9613e-110">Ein Zeiger auf die auf NULL endende Zeichenfolge, die den Namen der zum Kopieren der Datei verwendeten Zieldatei enthält.</span><span class="sxs-lookup"><span data-stu-id="9613e-110">Pointer to the null-terminated string that contains the name of the destination file used to copy the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9613e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9613e-111">Return Value</span></span>

<span data-ttu-id="9613e-112">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="9613e-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="9613e-113">Wenn ein Fehler auftritt und eine Fehler Rückruffunktion mithilfe der WM- [**\_ Cap- \_ \_ Rückruf \_ Fehlermeldung**](wm-cap-set-callback-error.md) festgelegt wird, wird die Fehler Rückruffunktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="9613e-113">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="9613e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9613e-114">Remarks</span></span>

<span data-ttu-id="9613e-115">Diese Meldung ändert nicht den Namen oder den Inhalt der aktuellen Erfassungs Datei.</span><span class="sxs-lookup"><span data-stu-id="9613e-115">This message does not change the name or contents of the current capture file.</span></span>

<span data-ttu-id="9613e-116">Wenn der Kopiervorgang aufgrund eines vollständigen Festplattenfehlers nicht erfolgreich ist, wird die Zieldatei automatisch gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9613e-116">If the copy operation is unsuccessful due to a disk full error, the destination file is automatically deleted.</span></span>

<span data-ttu-id="9613e-117">In der Regel wird eine Erfassungs Datei für das größte erwartete Erfassungs Segment reserviert, und nur ein Teil davon kann zum Erfassen von Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9613e-117">Typically, a capture file is preallocated for the largest capture segment anticipated and only a portion of it might be used to capture data.</span></span> <span data-ttu-id="9613e-118">Diese Nachricht kopiert nur den Teil der Datei, in der die Aufzeichnungsdaten enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="9613e-118">This message copies only the portion of the file containing the capture data.</span></span>

## <a name="requirements"></a><span data-ttu-id="9613e-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9613e-119">Requirements</span></span>



| <span data-ttu-id="9613e-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9613e-120">Requirement</span></span> | <span data-ttu-id="9613e-121">Wert</span><span class="sxs-lookup"><span data-stu-id="9613e-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9613e-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9613e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9613e-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9613e-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9613e-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9613e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9613e-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9613e-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9613e-126">Header</span><span class="sxs-lookup"><span data-stu-id="9613e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9613e-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="9613e-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9613e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9613e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9613e-129">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="9613e-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="9613e-130">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="9613e-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





