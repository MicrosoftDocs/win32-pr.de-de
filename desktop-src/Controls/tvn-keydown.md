---
title: TVN_KEYDOWN Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass der Benutzer eine Taste gedrückt hat und das Strukturansicht-Steuerelement den Eingabefokus besitzt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: da0d2b62-2295-4dce-9b37-a250f3be087f
keywords:
- Windows-Steuerelemente für TVN_KEYDOWN Benachrichtigungs
topic_type:
- apiref
api_name:
- TVN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ccb18c3bf7dc03056abb55575850821e11eb9bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475123"
---
# <a name="tvn_keydown-notification-code"></a><span data-ttu-id="22b8e-105">TVN- \_ KeyDown-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="22b8e-105">TVN\_KEYDOWN notification code</span></span>

<span data-ttu-id="22b8e-106">Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass der Benutzer eine Taste gedrückt hat und das Strukturansicht-Steuerelement den Eingabefokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="22b8e-106">Notifies a tree-view control's parent window that the user pressed a key and the tree-view control has the input focus.</span></span> <span data-ttu-id="22b8e-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="22b8e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_KEYDOWN 

    ptvkd = (LPNMTVKEYDOWN) lParam 
```



## <a name="parameters"></a><span data-ttu-id="22b8e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="22b8e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22b8e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="22b8e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22b8e-110">Zeiger auf eine [**nmtvkeydown**](/windows/win32/api/commctrl/ns-commctrl-nmtvkeydown) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="22b8e-110">Pointer to an [**NMTVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtvkeydown) structure.</span></span> <span data-ttu-id="22b8e-111">Der **wvkey** -Member gibt den Code des virtuellen Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="22b8e-111">The **wVKey** member specifies the virtual key code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22b8e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22b8e-112">Return value</span></span>

<span data-ttu-id="22b8e-113">Wenn der **wvkey** -Member von *LPARAM* ein Zeichen Schlüsselcode ist, wird das Zeichen im Rahmen einer inkrementellen Suche verwendet.</span><span class="sxs-lookup"><span data-stu-id="22b8e-113">If the **wVKey** member of *lParam* is a character key code, the character will be used as part of an incremental search.</span></span> <span data-ttu-id="22b8e-114">Gibt einen Wert ungleich 0 (null) zurück, wenn das Zeichen aus der inkrementellen Suche ausgeschlossen werden soll</span><span class="sxs-lookup"><span data-stu-id="22b8e-114">Return nonzero to exclude the character from the incremental search, or zero to include the character in the search.</span></span> <span data-ttu-id="22b8e-115">Bei allen anderen Schlüsseln wird der Rückgabewert ignoriert.</span><span class="sxs-lookup"><span data-stu-id="22b8e-115">For all other keys, the return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="22b8e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22b8e-116">Requirements</span></span>



| <span data-ttu-id="22b8e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22b8e-117">Requirement</span></span> | <span data-ttu-id="22b8e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="22b8e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="22b8e-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="22b8e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="22b8e-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22b8e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="22b8e-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="22b8e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="22b8e-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22b8e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="22b8e-123">Header</span><span class="sxs-lookup"><span data-stu-id="22b8e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="22b8e-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="22b8e-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





