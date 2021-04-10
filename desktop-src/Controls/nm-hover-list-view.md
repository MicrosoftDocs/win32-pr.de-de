---
title: NM_HOVER (Listenansicht) Benachrichtigungs Code (kommstrg. h)
description: Wird von einem Listenansicht-Steuerelement gesendet, wenn mit dem Mauszeiger auf ein Element gezeigt wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 0d4a2eee-9c98-43d1-bc05-226d91c0480a
keywords:
- NM_HOVER (Listenansicht) Windows-Steuerelemente für Benachrichtigungs Code
topic_type:
- apiref
api_name:
- NM_HOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e60606dfac73e13b0439ce861f37cb4ec941fda3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858646"
---
# <a name="nm_hover-list-view-notification-code"></a><span data-ttu-id="5709a-105">Anzeige von nm \_ Hover (Listenansicht)</span><span class="sxs-lookup"><span data-stu-id="5709a-105">NM\_HOVER (list view) notification code</span></span>

<span data-ttu-id="5709a-106">Wird von einem Listenansicht-Steuerelement gesendet, wenn mit dem Mauszeiger auf ein Element gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5709a-106">Sent by a list-view control when the mouse hovers over an item.</span></span> <span data-ttu-id="5709a-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="5709a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_HOVER

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="5709a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5709a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5709a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5709a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5709a-110">Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="5709a-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5709a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5709a-111">Return value</span></span>

<span data-ttu-id="5709a-112">Gibt 0 (null) zurück, um zuzulassen, dass die Listenansicht den Mauszeiger ordnungsgemäß verarbeitet, oder ungleich NULL, um zu verhindern, dass der Mauszeiger</span><span class="sxs-lookup"><span data-stu-id="5709a-112">Return zero to allow the list view to process the hover normally, or nonzero to prevent the hover from being processed.</span></span>

## <a name="requirements"></a><span data-ttu-id="5709a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5709a-113">Requirements</span></span>



| <span data-ttu-id="5709a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5709a-114">Requirement</span></span> | <span data-ttu-id="5709a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="5709a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5709a-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5709a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5709a-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5709a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5709a-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5709a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5709a-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5709a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5709a-120">Header</span><span class="sxs-lookup"><span data-stu-id="5709a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5709a-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5709a-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





