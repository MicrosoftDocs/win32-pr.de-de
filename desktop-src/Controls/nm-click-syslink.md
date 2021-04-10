---
title: NM_CLICK (Syslink)-Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Steuer Elements, dass der Benutzer auf einen Link mit der linken Maustaste im-Steuerelement geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: e92d7c92-f2c6-44aa-bce5-3bb07c184e7d
keywords:
- NM_CLICK (Syslink)-Benachrichtigungs Code Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ea34682b0cfdfdf1206a133abe4fdb22b8af5cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106641"
---
# <a name="nm_click-syslink-notification-code"></a><span data-ttu-id="b8c69-105">NM \_ Click (Syslink)-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="b8c69-105">NM\_CLICK (syslink) notification code</span></span>

<span data-ttu-id="b8c69-106">Benachrichtigt das übergeordnete Fenster eines Steuer Elements, dass der Benutzer auf einen Link mit der linken Maustaste im-Steuerelement geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="b8c69-106">Notifies a control's parent window that the user has clicked a hyperlink with the left mouse button within the control.</span></span> <span data-ttu-id="b8c69-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="b8c69-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CLICK

    pnmLink = (PNMLINK) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="b8c69-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8c69-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8c69-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8c69-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8c69-110">Zeiger auf eine [**nmlink**](/windows/win32/api/commctrl/ns-commctrl-nmlink) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="b8c69-110">Pointer to an [**NMLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlink) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8c69-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8c69-111">Return value</span></span>

<span data-ttu-id="b8c69-112">Der Rückgabewert wird vom-Steuerelement ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b8c69-112">The return value is ignored by the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8c69-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8c69-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b8c69-114">Zur Verwendung dieses Benachrichtigungs Codes müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="b8c69-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="b8c69-115">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b8c69-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b8c69-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8c69-116">Requirements</span></span>



| <span data-ttu-id="b8c69-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8c69-117">Requirement</span></span> | <span data-ttu-id="b8c69-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b8c69-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8c69-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b8c69-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b8c69-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8c69-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b8c69-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b8c69-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b8c69-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8c69-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b8c69-123">Header</span><span class="sxs-lookup"><span data-stu-id="b8c69-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8c69-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8c69-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8c69-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8c69-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="b8c69-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="b8c69-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b8c69-127">**Nmlink**</span><span class="sxs-lookup"><span data-stu-id="b8c69-127">**NMLINK**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlink)
</dt> <dt>

[<span data-ttu-id="b8c69-128">**WM- \_ Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="b8c69-128">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





