---
description: Eine Anwendung sendet die WM- \_ mdiiconarrange-Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um alle minimierten untergeordneten MDI-Fenster anzuordnen. Untergeordnete Fenster, die nicht minimiert sind, sind nicht betroffen.
ms.assetid: 935b9e29-224d-449e-b89f-b6062bed7702
title: WM_MDIICONARRANGE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc2d50d4bccebe3e9758752cc7d0d259e973875c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484755"
---
# <a name="wm_mdiiconarrange-message"></a><span data-ttu-id="8559d-104">WM- \_ mdiiconanordnen-Meldung</span><span class="sxs-lookup"><span data-stu-id="8559d-104">WM\_MDIICONARRANGE message</span></span>

<span data-ttu-id="8559d-105">Eine Anwendung sendet die **WM- \_ mdiiconarrange** -Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um alle minimierten untergeordneten MDI-Fenster anzuordnen.</span><span class="sxs-lookup"><span data-stu-id="8559d-105">An application sends the **WM\_MDIICONARRANGE** message to a multiple-document interface (MDI) client window to arrange all minimized MDI child windows.</span></span> <span data-ttu-id="8559d-106">Untergeordnete Fenster, die nicht minimiert sind, sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="8559d-106">It does not affect child windows that are not minimized.</span></span>


```C++
#define WM_MDIICONARRANGE               0x0228
```



## <a name="parameters"></a><span data-ttu-id="8559d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8559d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8559d-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8559d-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8559d-109">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="8559d-109">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8559d-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8559d-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8559d-111">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="8559d-111">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8559d-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8559d-112">Requirements</span></span>



| <span data-ttu-id="8559d-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8559d-113">Requirement</span></span> | <span data-ttu-id="8559d-114">Wert</span><span class="sxs-lookup"><span data-stu-id="8559d-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8559d-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8559d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8559d-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8559d-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8559d-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8559d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8559d-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8559d-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8559d-119">Header</span><span class="sxs-lookup"><span data-stu-id="8559d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="8559d-120"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="8559d-120"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8559d-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8559d-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="8559d-122">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="8559d-122">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8559d-123">**WM- \_ mdicascade**</span><span class="sxs-lookup"><span data-stu-id="8559d-123">**WM\_MDICASCADE**</span></span>](wm-mdicascade.md)
</dt> <dt>

[<span data-ttu-id="8559d-124">**WM- \_ mditile**</span><span class="sxs-lookup"><span data-stu-id="8559d-124">**WM\_MDITILE**</span></span>](wm-mditile.md)
</dt> <dt>

<span data-ttu-id="8559d-125">**Licher**</span><span class="sxs-lookup"><span data-stu-id="8559d-125">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8559d-126">Mehrere Dokument Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8559d-126">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




