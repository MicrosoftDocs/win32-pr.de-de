---
title: EN_OBJECTPOSITIONS Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, wenn das-Steuerelement Objekte einliest. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: 1965185f-8a13-4989-8574-af8b9b30f6b0
keywords:
- Windows-Steuerelemente für EN_OBJECTPOSITIONS Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_OBJECTPOSITIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35681f6734457eb6b6ebcac1bcb67227cbd3b9e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858947"
---
# <a name="en_objectpositions-notification-code"></a><span data-ttu-id="5b892-105">EN \_ objectpositions-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="5b892-105">EN\_OBJECTPOSITIONS notification code</span></span>

<span data-ttu-id="5b892-106">Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, wenn das-Steuerelement Objekte einliest.</span><span class="sxs-lookup"><span data-stu-id="5b892-106">Notifies a rich edit control's parent window when the control reads in objects.</span></span> <span data-ttu-id="5b892-107">Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="5b892-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_OBJECTPOSITIONS

    pOjectPositions = (OBJECTPOSITIONS *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="5b892-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b892-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b892-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b892-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b892-110">Eine [**objectpositions**](/windows/desktop/api/Richedit/ns-richedit-objectpositions) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="5b892-110">An [**OBJECTPOSITIONS**](/windows/desktop/api/Richedit/ns-richedit-objectpositions) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b892-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5b892-111">Return value</span></span>

<span data-ttu-id="5b892-112">Gibt NULL zurück, um den **Lese** Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="5b892-112">Return zero to continue the **Read** operation.</span></span>

<span data-ttu-id="5b892-113">Gibt einen Wert ungleich 0 (null) zurück, um den **Lese** Vorgang anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="5b892-113">Return a nonzero value to stop the **Read** operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b892-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b892-114">Remarks</span></span>

<span data-ttu-id="5b892-115">Um einen en \_ objectpositions-Benachrichtigungs Code zu erhalten, geben Sie das [**ENM \_ objectpositions**](rich-edit-control-event-mask-flags.md) -Flag in der mit der [**EM \_ SetEventMask**](em-seteventmask.md) -Nachricht gesendeten Maske an.</span><span class="sxs-lookup"><span data-stu-id="5b892-115">To receive an EN\_OBJECTPOSITIONS notification code, specify the [**ENM\_OBJECTPOSITIONS**](rich-edit-control-event-mask-flags.md) flag in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b892-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b892-116">Requirements</span></span>



| <span data-ttu-id="5b892-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b892-117">Requirement</span></span> | <span data-ttu-id="5b892-118">Wert</span><span class="sxs-lookup"><span data-stu-id="5b892-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b892-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5b892-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5b892-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5b892-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5b892-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5b892-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5b892-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5b892-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5b892-123">Header</span><span class="sxs-lookup"><span data-stu-id="5b892-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b892-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b892-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b892-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b892-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="5b892-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="5b892-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5b892-127">**EM-- \_ einventmask**</span><span class="sxs-lookup"><span data-stu-id="5b892-127">**EM\_SETEVENTMASK**</span></span>](em-seteventmask.md)
</dt> <dt>

[<span data-ttu-id="5b892-128">**Objectpositions**</span><span class="sxs-lookup"><span data-stu-id="5b892-128">**OBJECTPOSITIONS**</span></span>](/windows/desktop/api/Richedit/ns-richedit-objectpositions)
</dt> <dt>

[<span data-ttu-id="5b892-129">**WM- \_ Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="5b892-129">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> <dt>

<span data-ttu-id="5b892-130">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="5b892-130">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="5b892-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5b892-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="5b892-132">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5b892-132">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> </dl>

 

