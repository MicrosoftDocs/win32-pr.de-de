---
title: Benachrichtigungs Code für NM_KILLFOCUS (Strukturansicht) (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass das Steuerelement den Eingabefokus verloren hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: f6646a39-6480-4417-9c1c-ffd2417ca7dd
keywords:
- NM_KILLFOCUS (Strukturansicht) Windows-Steuerelemente für Benachrichtigungs Code
topic_type:
- apiref
api_name:
- NM_KILLFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7123f47469a02fcec92805a27d81e173c5e1d10a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949413"
---
# <a name="nm_killfocus-tree-view-notification-code"></a><span data-ttu-id="19fef-105">NM- \_ killfokus (Strukturansicht) Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="19fef-105">NM\_KILLFOCUS (tree view) notification code</span></span>

<span data-ttu-id="19fef-106">Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass das Steuerelement den Eingabefokus verloren hat.</span><span class="sxs-lookup"><span data-stu-id="19fef-106">Notifies a tree-view control's parent window that the control has lost the input focus.</span></span> <span data-ttu-id="19fef-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="19fef-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KILLFOCUS

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="19fef-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="19fef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19fef-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="19fef-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19fef-110">Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="19fef-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19fef-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19fef-111">Return value</span></span>

<span data-ttu-id="19fef-112">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="19fef-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="19fef-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19fef-113">Requirements</span></span>



| <span data-ttu-id="19fef-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19fef-114">Requirement</span></span> | <span data-ttu-id="19fef-115">Wert</span><span class="sxs-lookup"><span data-stu-id="19fef-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19fef-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19fef-116">Minimum supported client</span></span><br/> | <span data-ttu-id="19fef-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19fef-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="19fef-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19fef-118">Minimum supported server</span></span><br/> | <span data-ttu-id="19fef-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19fef-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="19fef-120">Header</span><span class="sxs-lookup"><span data-stu-id="19fef-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="19fef-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="19fef-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





