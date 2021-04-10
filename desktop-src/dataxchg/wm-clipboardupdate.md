---
title: WM_CLIPBOARDUPDATE Meldung (Winuser. h)
description: Wird gesendet, wenn sich der Inhalt der Zwischenablage geändert hat.
ms.assetid: 1508aa22-9cf0-40a2-8cb0-ce7c8671df2c
keywords:
- WM_CLIPBOARDUPDATE Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_CLIPBOARDUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303110f0d094cfed336a9f92006b3720a0ccc83b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104085"
---
# <a name="wm_clipboardupdate-message"></a><span data-ttu-id="b810b-104">WM \_ clipboardupdate-Meldung</span><span class="sxs-lookup"><span data-stu-id="b810b-104">WM\_CLIPBOARDUPDATE message</span></span>

<span data-ttu-id="b810b-105">Wird gesendet, wenn sich der Inhalt der Zwischenablage geändert hat.</span><span class="sxs-lookup"><span data-stu-id="b810b-105">Sent when the contents of the clipboard have changed.</span></span>


```C++
#define WM_CLIPBOARDUPDATE              0x031D
```



## <a name="parameters"></a><span data-ttu-id="b810b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b810b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b810b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b810b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b810b-108">Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="b810b-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b810b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b810b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b810b-110">Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="b810b-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b810b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b810b-111">Return value</span></span>

<span data-ttu-id="b810b-112">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b810b-112">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b810b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b810b-113">Remarks</span></span>

<span data-ttu-id="b810b-114">Verwenden Sie die [**addclipboardformatlistener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) -Funktion, um ein Fenster für den Empfang dieser Nachricht zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="b810b-114">To register a window to receive this message, use the [**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b810b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b810b-115">Requirements</span></span>



| <span data-ttu-id="b810b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b810b-116">Requirement</span></span> | <span data-ttu-id="b810b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="b810b-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b810b-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b810b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b810b-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b810b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b810b-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b810b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b810b-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b810b-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b810b-122">Header</span><span class="sxs-lookup"><span data-stu-id="b810b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b810b-123"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="b810b-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b810b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b810b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b810b-125">**Addclipboardformatlistener**</span><span class="sxs-lookup"><span data-stu-id="b810b-125">**AddClipboardFormatListener**</span></span>](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener)
</dt> <dt>

[<span data-ttu-id="b810b-126">**Removeclipboardformatlistener**</span><span class="sxs-lookup"><span data-stu-id="b810b-126">**RemoveClipboardFormatListener**</span></span>](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener)
</dt> <dt>

[<span data-ttu-id="b810b-127">**Getclipboardsequencenumschlag**</span><span class="sxs-lookup"><span data-stu-id="b810b-127">**GetClipboardSequenceNumber**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber)
</dt> </dl>

 

 





