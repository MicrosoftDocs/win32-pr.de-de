---
title: EN_SEARCHWEB Benachrichtigungs Code (kommctrl. h)
description: Wird gesendet, wenn ein Bearbeitungs Steuerelement den Tastaturfokus verliert. Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine WM-Benachrichtigungs \_ Meldung.
ms.assetid: c31f4b6c-afed-4506-b98a-65c902b0f63a
keywords:
- Windows-Steuerelemente für EN_SEARCHWEB Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_SEARCHWEB
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 2b995c90e8f4a607d7181adc8a357314acb84dc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475387"
---
# <a name="en_searchweb-notification-code"></a><span data-ttu-id="faa5d-105">EN \_ Searchweb-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="faa5d-105">EN\_SEARCHWEB notification code</span></span>

<span data-ttu-id="faa5d-106">Wird gesendet, nachdem ein Bearbeitungs Steuerelement eine Websuche durchgeführt hat, wenn das Feature "Web suchen" aktiviert ist. Weitere Informationen finden Sie unter [EM_ENABLESEARCHWEB](em-enablesearchweb.md).</span><span class="sxs-lookup"><span data-stu-id="faa5d-106">Sent after an edit control performed a web search when the "Search the web" feature is enabled, see [EM_ENABLESEARCHWEB](em-enablesearchweb.md).</span></span> <span data-ttu-id="faa5d-107">Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="faa5d-107">The parent window of the edit control receives this notification code through a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_SEARCHWEB

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="faa5d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="faa5d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="faa5d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="faa5d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="faa5d-110">Handle für das Bearbeitungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="faa5d-110">Handle to the edit control.</span></span>

</dd> <dt>

<span data-ttu-id="faa5d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="faa5d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="faa5d-112">Ein Zeiger auf eine [**nmsearchweb**](/windows/desktop/api/Commctrl/ns-commctrl-nmsearchweb) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="faa5d-112">A pointer to a [**NMSEARCHWEB**](/windows/desktop/api/Commctrl/ns-commctrl-nmsearchweb) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="faa5d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="faa5d-113">Requirements</span></span>



| <span data-ttu-id="faa5d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="faa5d-114">Requirement</span></span> | <span data-ttu-id="faa5d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="faa5d-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="faa5d-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="faa5d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="faa5d-117">Nur Windows 10, 1809 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="faa5d-117">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="faa5d-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="faa5d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="faa5d-119">Nur Windows Server 2019 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="faa5d-119">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="faa5d-120">Header</span><span class="sxs-lookup"><span data-stu-id="faa5d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="faa5d-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="faa5d-121"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faa5d-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="faa5d-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="faa5d-123">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="faa5d-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="faa5d-124">**EM \_ enablesearchweb**</span><span class="sxs-lookup"><span data-stu-id="faa5d-124">**EM\_ENABLESEARCHWEB**</span></span>](em-enablesearchweb.md)
</dt> <dt>

<span data-ttu-id="faa5d-125">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="faa5d-125">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="faa5d-126">**WM- \_ Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="faa5d-126">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





