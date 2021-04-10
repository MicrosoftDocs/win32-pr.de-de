---
title: WM_CAP_FILE_SET_INFOCHUNK Meldung (VFW. h)
description: Die WM \_ \_ -Cap \_ -Datei Satz \_ -Infoblock-Nachricht legt Informationsblöcke fest und löscht diese.
ms.assetid: 67d11a05-a2b4-45d2-ba66-83a198745303
keywords:
- WM_CAP_FILE_SET_INFOCHUNK-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SET_INFOCHUNK
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 067ba00563a5ca511f13b23615fc4542090ba397
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040134"
---
# <a name="wm_cap_file_set_infochunk-message"></a><span data-ttu-id="131c5-104">WM- \_ Abdeckungs \_ Datei \_ Satz- \_ infochunk-Nachricht</span><span class="sxs-lookup"><span data-stu-id="131c5-104">WM\_CAP\_FILE\_SET\_INFOCHUNK message</span></span>

<span data-ttu-id="131c5-105">Die **WM- \_ Cap- \_ Datei Satz- \_ \_ Infoblock** -Nachricht legt Informationsblöcke fest und löscht diese.</span><span class="sxs-lookup"><span data-stu-id="131c5-105">The **WM\_CAP\_FILE\_SET\_INFOCHUNK** message sets and clears information chunks.</span></span> <span data-ttu-id="131c5-106">Informationsblöcke können während der Erfassung in eine AVI-Datei eingefügt werden, um Text Zeichenfolgen oder benutzerdefinierte Daten einzubetten.</span><span class="sxs-lookup"><span data-stu-id="131c5-106">Information chunks can be inserted in an AVI file during capture to embed text strings or custom data.</span></span> <span data-ttu-id="131c5-107">Sie können diese Nachricht explizit oder mithilfe des [**capflesetinfochunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="131c5-107">You can send this message explicitly or by using the [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) macro.</span></span>


```C++
WM_CAP_FILE_SET_INFOCHUNK 
wParam = (WPARAM)0; 
lParam = (LPARAM) (LPCAPINFOCHUNK) (lpInfoChunk); 
```



## <a name="parameters"></a><span data-ttu-id="131c5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="131c5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="131c5-109"><span id="lpInfoChunk"></span><span id="lpinfochunk"></span><span id="LPINFOCHUNK"></span>*lpinfochunk*</span><span class="sxs-lookup"><span data-stu-id="131c5-109"><span id="lpInfoChunk"></span><span id="lpinfochunk"></span><span id="LPINFOCHUNK"></span>*lpInfoChunk*</span></span>
</dt> <dd>

<span data-ttu-id="131c5-110">Ein Zeiger auf eine [**capinfochunk**](/windows/win32/api/vfw/ns-vfw-capinfochunk) -Struktur, die den zu erstellenden oder zu löschenden Informationsblock definiert.</span><span class="sxs-lookup"><span data-stu-id="131c5-110">Pointer to a [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) structure defining the information chunk to be created or deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="131c5-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="131c5-111">Return Value</span></span>

<span data-ttu-id="131c5-112">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="131c5-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="131c5-113">Wenn ein Fehler auftritt und eine Fehler Rückruffunktion mithilfe der WM- [**\_ Cap- \_ \_ Rückruf \_ Fehlermeldung**](wm-cap-set-callback-error.md) festgelegt wird, wird die Fehler Rückruffunktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="131c5-113">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="131c5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="131c5-114">Remarks</span></span>

<span data-ttu-id="131c5-115">Einer AVI-Datei können mehrere registrierte Informations Segmente hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="131c5-115">Multiple registered information chunks can be added to an AVI file.</span></span> <span data-ttu-id="131c5-116">Nachdem ein Informationsblock festgelegt wurde, wird er weiterhin zu nachfolgenden Erfassungs Dateien hinzugefügt, bis entweder der Eintrag gelöscht oder alle Informationsblock Einträge gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="131c5-116">After an information chunk is set, it continues to be added to subsequent capture files until either the entry is cleared or all information chunk entries are cleared.</span></span> <span data-ttu-id="131c5-117">Um einen einzelnen Eintrag zu löschen, geben Sie die Informationen im Member **fccinfoid** und **null** im **lpdata** -Member der [**capinfochunk**](/windows/win32/api/vfw/ns-vfw-capinfochunk) -Struktur an.</span><span class="sxs-lookup"><span data-stu-id="131c5-117">To clear a single entry, specify the information chunk in the **fccInfoID** member and **NULL** in the **lpData** member of the [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) structure.</span></span> <span data-ttu-id="131c5-118">Wenn Sie alle Einträge löschen möchten, geben Sie **null** in **fccinfoid** an.</span><span class="sxs-lookup"><span data-stu-id="131c5-118">To clear all entries, specify **NULL** in **fccInfoID**.</span></span>

## <a name="requirements"></a><span data-ttu-id="131c5-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="131c5-119">Requirements</span></span>



| <span data-ttu-id="131c5-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="131c5-120">Requirement</span></span> | <span data-ttu-id="131c5-121">Wert</span><span class="sxs-lookup"><span data-stu-id="131c5-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="131c5-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="131c5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="131c5-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="131c5-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="131c5-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="131c5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="131c5-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="131c5-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="131c5-126">Header</span><span class="sxs-lookup"><span data-stu-id="131c5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="131c5-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="131c5-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="131c5-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="131c5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="131c5-129">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="131c5-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="131c5-130">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="131c5-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





