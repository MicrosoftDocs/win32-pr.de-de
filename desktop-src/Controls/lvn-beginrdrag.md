---
title: LVN_BEGINRDRAG Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass ein Drag & Drop-Vorgang mit der rechten Maustaste initiiert wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 93feba3b-8e3e-4a04-bf2c-7ff67a85d4fb
keywords:
- Windows-Steuerelemente für LVN_BEGINRDRAG Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_BEGINRDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77b4f55c01ca2b5e43419ea926401ac3393d9a9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949459"
---
# <a name="lvn_beginrdrag-notification-code"></a><span data-ttu-id="24d80-105">LVN \_ beginrdrag-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="24d80-105">LVN\_BEGINRDRAG notification code</span></span>

<span data-ttu-id="24d80-106">Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass ein Drag & Drop-Vorgang mit der rechten Maustaste initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="24d80-106">Notifies a list-view control's parent window that a drag-and-drop operation involving the right mouse button is being initiated.</span></span> <span data-ttu-id="24d80-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="24d80-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_BEGINRDRAG

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="24d80-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="24d80-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24d80-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="24d80-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24d80-110">Zeiger auf eine [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="24d80-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="24d80-111">Der **iItem** -Member identifiziert das Element, das gezogen wird, und die anderen Elemente sind 0 (null).</span><span class="sxs-lookup"><span data-stu-id="24d80-111">The **iItem** member identifies the item being dragged, and the other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24d80-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="24d80-112">Return value</span></span>

<span data-ttu-id="24d80-113">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="24d80-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="24d80-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24d80-114">Requirements</span></span>



| <span data-ttu-id="24d80-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="24d80-115">Requirement</span></span> | <span data-ttu-id="24d80-116">Wert</span><span class="sxs-lookup"><span data-stu-id="24d80-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="24d80-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="24d80-117">Minimum supported client</span></span><br/> | <span data-ttu-id="24d80-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="24d80-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="24d80-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="24d80-119">Minimum supported server</span></span><br/> | <span data-ttu-id="24d80-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="24d80-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="24d80-121">Header</span><span class="sxs-lookup"><span data-stu-id="24d80-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="24d80-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="24d80-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





