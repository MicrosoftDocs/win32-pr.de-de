---
title: LVN_MARQUEEBEGIN Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass eine Begrenzungsfeld Auswahl (Marquee) begonnen hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: e9daa264-1861-4791-9a12-cf95d86a688e
keywords:
- Windows-Steuerelemente für LVN_MARQUEEBEGIN Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_MARQUEEBEGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d46d399b8355bea0ddb2054340d52db59c3ad27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340020"
---
# <a name="lvn_marqueebegin-notification-code"></a><span data-ttu-id="ded00-105">LVN- \_ marqueebegin-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="ded00-105">LVN\_MARQUEEBEGIN notification code</span></span>

<span data-ttu-id="ded00-106">Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass eine Begrenzungsfeld Auswahl (Marquee) begonnen hat.</span><span class="sxs-lookup"><span data-stu-id="ded00-106">Notifies a list-view control's parent window that a bounding box (marquee) selection has begun.</span></span> <span data-ttu-id="ded00-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="ded00-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_MARQUEEBEGIN

    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="ded00-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ded00-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ded00-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ded00-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ded00-110">Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="ded00-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ded00-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ded00-111">Return value</span></span>

<span data-ttu-id="ded00-112">Um den Benachrichtigungs Code zu akzeptieren, wird NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ded00-112">To accept the notification code, return zero.</span></span> <span data-ttu-id="ded00-113">Um die Begrenzungsfeld Auswahl zu beenden, geben Sie einen Wert ungleich 0 (null)</span><span class="sxs-lookup"><span data-stu-id="ded00-113">To quit the bounding box selection, return nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ded00-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ded00-114">Remarks</span></span>

<span data-ttu-id="ded00-115">Bei der *Auswahl eines Begrenzungs* Rahmens handelt es sich um den Prozess, bei dem auf den Client Bereich der Listenansicht geklickt und mehrere Elemente gleichzeitig ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="ded00-115">A *bounding box selection* is the process of clicking the list-view window's client area and dragging to select multiple items simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="ded00-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ded00-116">Requirements</span></span>



| <span data-ttu-id="ded00-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ded00-117">Requirement</span></span> | <span data-ttu-id="ded00-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ded00-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ded00-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ded00-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ded00-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ded00-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ded00-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ded00-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ded00-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ded00-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ded00-123">Header</span><span class="sxs-lookup"><span data-stu-id="ded00-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ded00-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ded00-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





