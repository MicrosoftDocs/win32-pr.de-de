---
title: LVN_KEYDOWN Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass eine Taste gedrückt wurde. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 3aa3d165-7227-41c4-8bc2-3e51a0f52ee3
keywords:
- Windows-Steuerelemente für LVN_KEYDOWN Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 516c64e9050a6946d3a135ecc0d00d7e384e9844
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957259"
---
# <a name="lvn_keydown-notification-code"></a><span data-ttu-id="aff15-105">LVN- \_ KeyDown-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="aff15-105">LVN\_KEYDOWN notification code</span></span>

<span data-ttu-id="aff15-106">Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass eine Taste gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="aff15-106">Notifies a list-view control's parent window that a key has been pressed.</span></span> <span data-ttu-id="aff15-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="aff15-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_KEYDOWN

    pnkd = (LPNMLVKEYDOWN) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="aff15-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="aff15-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aff15-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aff15-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aff15-110">Zeiger auf eine [**nmlvkeydown**](/windows/win32/api/commctrl/ns-commctrl-nmlvkeydown) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="aff15-110">Pointer to an [**NMLVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmlvkeydown) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aff15-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aff15-111">Return value</span></span>

<span data-ttu-id="aff15-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="aff15-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="aff15-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aff15-113">Requirements</span></span>



| <span data-ttu-id="aff15-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aff15-114">Requirement</span></span> | <span data-ttu-id="aff15-115">Wert</span><span class="sxs-lookup"><span data-stu-id="aff15-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aff15-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aff15-116">Minimum supported client</span></span><br/> | <span data-ttu-id="aff15-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aff15-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aff15-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aff15-118">Minimum supported server</span></span><br/> | <span data-ttu-id="aff15-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aff15-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aff15-120">Header</span><span class="sxs-lookup"><span data-stu-id="aff15-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="aff15-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="aff15-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





