---
title: HDN_ITEMCLICK Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass der Benutzer auf das Steuerelement geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 25ed0070-5891-4f36-9ae0-fc04e064401f
keywords:
- Windows-Steuerelemente für HDN_ITEMCLICK Benachrichtigungs
topic_type:
- apiref
api_name:
- HDN_ITEMCLICK
- HDN_ITEMCLICKA
- HDN_ITEMCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca49cd4fd77425f202c5d8ee06cb0b3d7712e610
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859169"
---
# <a name="hdn_itemclick-notification-code"></a><span data-ttu-id="66f8b-105">Hdn- \_ itemClick-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="66f8b-105">HDN\_ITEMCLICK notification code</span></span>

<span data-ttu-id="66f8b-106">Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass der Benutzer auf das Steuerelement geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="66f8b-106">Notifies a header control's parent window that the user clicked the control.</span></span> <span data-ttu-id="66f8b-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="66f8b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="66f8b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="66f8b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66f8b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="66f8b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66f8b-110">Ein Zeiger auf eine [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur, die das Header Steuerelement identifiziert und den Index des Header Elements angibt, auf das geklickt wurde, und mit der Maustaste auf das Element geklickt wurde.</span><span class="sxs-lookup"><span data-stu-id="66f8b-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that identifies the header control and specifies the index of the header item that was clicked and the mouse button used to click the item.</span></span> <span data-ttu-id="66f8b-111">Der **pitem** -Member ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="66f8b-111">The **pItem** member is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66f8b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="66f8b-112">Return value</span></span>

<span data-ttu-id="66f8b-113">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="66f8b-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="66f8b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66f8b-114">Remarks</span></span>

<span data-ttu-id="66f8b-115">Ein Header Steuerelement sendet diesen Benachrichtigungs Code, nachdem der Benutzer die linke Maustaste losgelassen hat.</span><span class="sxs-lookup"><span data-stu-id="66f8b-115">A header control sends this notification code after the user releases the left mouse button.</span></span>

## <a name="requirements"></a><span data-ttu-id="66f8b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66f8b-116">Requirements</span></span>



| <span data-ttu-id="66f8b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="66f8b-117">Requirement</span></span> | <span data-ttu-id="66f8b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="66f8b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="66f8b-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="66f8b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="66f8b-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66f8b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="66f8b-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="66f8b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="66f8b-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66f8b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="66f8b-123">Header</span><span class="sxs-lookup"><span data-stu-id="66f8b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="66f8b-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="66f8b-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="66f8b-125">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="66f8b-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="66f8b-126">**Hdn \_ Itemclickw** (Unicode) und **Hdn \_ itemclicka** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="66f8b-126">**HDN\_ITEMCLICKW** (Unicode) and **HDN\_ITEMCLICKA** (ANSI)</span></span><br/>               |



 

 





