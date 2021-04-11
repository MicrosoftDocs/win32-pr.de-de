---
title: EN_CLIPFORMAT Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass ein einfügen mit einem bestimmten Zwischenablage Format stattgefunden hat. Diese Benachrichtigung wird von einem fensterlosen Bearbeitungs Steuerelement mithilfe der itexthost txnotify-Methode gesendet.
ms.assetid: 79FE1350-4D45-447B-B705-63E966AC7F0E
keywords:
- Windows-Steuerelemente für EN_CLIPFORMAT Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_CLIPFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0430e8a4dba0b1a18f81f4e28ec67f2c93551cd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949704"
---
# <a name="en_clipformat-notification-code"></a><span data-ttu-id="85697-105">\_Benachrichtigungs Code für en clipFormat</span><span class="sxs-lookup"><span data-stu-id="85697-105">EN\_CLIPFORMAT notification code</span></span>

<span data-ttu-id="85697-106">Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass ein einfügen mit einem bestimmten Zwischenablage Format stattgefunden hat.</span><span class="sxs-lookup"><span data-stu-id="85697-106">Notifies a rich edit control's parent window that a paste occurred with a particular clipboard format.</span></span> <span data-ttu-id="85697-107">Diese Benachrichtigung wird von einem fensterlosen Bearbeitungs Steuerelement mithilfe der [**itexthost:: txnotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) -Methode gesendet.</span><span class="sxs-lookup"><span data-stu-id="85697-107">A windowless rich edit control sends this notification by using the [**ITextHost::TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) method.</span></span>


```C++
EN_CLIPFORMAT

      pClipboardFmt = (CLIPBOARDFORMAT *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="85697-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="85697-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85697-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="85697-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="85697-110">Die Fenster-ID, die durch Aufrufen der [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) -Funktion mit dem GWL-ID-Wert abgerufen wird \_ .</span><span class="sxs-lookup"><span data-stu-id="85697-110">The window ID retrieved by calling the [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) function with the GWL\_ID value.</span></span>

</dd> <dt>

<span data-ttu-id="85697-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="85697-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="85697-112">Ein Zeiger auf eine [**ClipboardFormat**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat) -Struktur, die Informationen über das Zwischenablage Format enthält.</span><span class="sxs-lookup"><span data-stu-id="85697-112">A pointer to a [**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat) structure that contains information about the clipboard format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85697-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="85697-113">Return value</span></span>

<span data-ttu-id="85697-114">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="85697-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="85697-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85697-115">Remarks</span></span>

<span data-ttu-id="85697-116">Um \_ die Benachrichtigungs Codes von "de clipFormat" zu erhalten, geben Sie " [**ENM \_ clipFormat**](rich-edit-control-event-mask-flags.md) " in der Maske an, die mit der Nachricht " [**EM \_**](em-seteventmask.md) -Nachricht</span><span class="sxs-lookup"><span data-stu-id="85697-116">To receive EN\_CLIPFORMAT notification codes, specify [**ENM\_CLIPFORMAT**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="85697-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85697-117">Requirements</span></span>



| <span data-ttu-id="85697-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85697-118">Requirement</span></span> | <span data-ttu-id="85697-119">Wert</span><span class="sxs-lookup"><span data-stu-id="85697-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="85697-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="85697-120">Minimum supported client</span></span><br/> | <span data-ttu-id="85697-121">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85697-121">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="85697-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="85697-122">Minimum supported server</span></span><br/> | <span data-ttu-id="85697-123">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85697-123">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="85697-124">Header</span><span class="sxs-lookup"><span data-stu-id="85697-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="85697-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="85697-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85697-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85697-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85697-127">**ClipboardFormat**</span><span class="sxs-lookup"><span data-stu-id="85697-127">**CLIPBOARDFORMAT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-clipboardformat)
</dt> </dl>

 

