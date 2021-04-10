---
title: LVN_BEGINDRAG Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass ein Drag & Drop-Vorgang mit der linken Maustaste initiiert wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 2b9bbff8-f5f7-47ac-b662-a327ff49caf7
keywords:
- Windows-Steuerelemente für LVN_BEGINDRAG Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69166cd38242db915f70772b5dfbd3bab6ba56df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040172"
---
# <a name="lvn_begindrag-notification-code"></a><span data-ttu-id="de1ea-105">LVN \_ BeginDrag-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="de1ea-105">LVN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="de1ea-106">Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass ein Drag & Drop-Vorgang mit der linken Maustaste initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="de1ea-106">Notifies a list-view control's parent window that a drag-and-drop operation involving the left mouse button is being initiated.</span></span> <span data-ttu-id="de1ea-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="de1ea-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_BEGINDRAG

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="de1ea-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="de1ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de1ea-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="de1ea-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de1ea-110">Zeiger auf eine [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="de1ea-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="de1ea-111">Der **iItem** -Member identifiziert das Element, das gezogen wird, und die anderen Elemente sind 0 (null).</span><span class="sxs-lookup"><span data-stu-id="de1ea-111">The **iItem** member identifies the item being dragged, and the other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de1ea-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de1ea-112">Return value</span></span>

<span data-ttu-id="de1ea-113">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="de1ea-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="de1ea-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de1ea-114">Requirements</span></span>



| <span data-ttu-id="de1ea-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de1ea-115">Requirement</span></span> | <span data-ttu-id="de1ea-116">Wert</span><span class="sxs-lookup"><span data-stu-id="de1ea-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="de1ea-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de1ea-117">Minimum supported client</span></span><br/> | <span data-ttu-id="de1ea-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de1ea-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="de1ea-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de1ea-119">Minimum supported server</span></span><br/> | <span data-ttu-id="de1ea-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de1ea-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="de1ea-121">Header</span><span class="sxs-lookup"><span data-stu-id="de1ea-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="de1ea-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="de1ea-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





