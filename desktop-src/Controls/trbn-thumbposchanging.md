---
title: TRBN_THUMBPOSCHANGING Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt, dass sich die Position des Zieh Punkts auf einer TrackBar ändert. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 0876e026-bc07-409d-b174-b97ed704fc11
keywords:
- Windows-Steuerelemente für TRBN_THUMBPOSCHANGING Benachrichtigungs
topic_type:
- apiref
api_name:
- TRBN_THUMBPOSCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f23722b68f28a5157948ac6277858193366242fe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961405"
---
# <a name="trbn_thumbposchanging-notification-code"></a><span data-ttu-id="eec5a-105">Trbn- \_ thumbposchanging-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="eec5a-105">TRBN\_THUMBPOSCHANGING notification code</span></span>

<span data-ttu-id="eec5a-106">Benachrichtigt, dass sich die Position des Zieh Punkts auf einer TrackBar ändert.</span><span class="sxs-lookup"><span data-stu-id="eec5a-106">Notifies that the thumb position on a trackbar is changing.</span></span> <span data-ttu-id="eec5a-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="eec5a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TRBN_THUMBPOSCHANGING

    lpNMTrbThumbPosChanging = (NMTRBTHUMBPOSCHANGING*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="eec5a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="eec5a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eec5a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eec5a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eec5a-110">Zeiger auf eine [**nmtrbthumbposchanging**](/windows/win32/api/commctrl/ns-commctrl-nmtrbthumbposchanging) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="eec5a-110">Pointer to a [**NMTRBTHUMBPOSCHANGING**](/windows/win32/api/commctrl/ns-commctrl-nmtrbthumbposchanging) structure.</span></span> <span data-ttu-id="eec5a-111">Der Aufrufer ist dafür verantwortlich, diese Struktur zuzuordnen und seine Member festzulegen, einschließlich der Member der enthaltenen [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="eec5a-111">The caller is responsible for allocating this structure and setting its members, including the members of the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eec5a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eec5a-112">Return value</span></span>

<span data-ttu-id="eec5a-113">Gibt **true** zurück, um zu verhindern, dass der Ziehpunkt an die angegebene Position verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="eec5a-113">Return **TRUE** to prevent the thumb from moving to the specified position.</span></span>

## <a name="remarks"></a><span data-ttu-id="eec5a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eec5a-114">Remarks</span></span>

<span data-ttu-id="eec5a-115">Senden Sie diese Benachrichtigung an Clients, die nicht auf " [**WM \_ HScroll**](wm-hscroll.md) "-oder " [**WM \_ VScroll**](wm-vscroll.md) "-Nachrichten lauschen.</span><span class="sxs-lookup"><span data-stu-id="eec5a-115">Send this notification to clients that do not listen for [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="eec5a-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eec5a-116">Requirements</span></span>



| <span data-ttu-id="eec5a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eec5a-117">Requirement</span></span> | <span data-ttu-id="eec5a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="eec5a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eec5a-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eec5a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="eec5a-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eec5a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eec5a-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eec5a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="eec5a-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eec5a-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eec5a-123">Header</span><span class="sxs-lookup"><span data-stu-id="eec5a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="eec5a-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="eec5a-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





