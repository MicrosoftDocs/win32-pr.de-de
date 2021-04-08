---
title: TBN_HOTITEMCHANGE Benachrichtigungs Code (kommctrl. h)
description: Wird von einem ToolBar-Steuerelement gesendet, wenn sich das heiße Element (hervorgehoben) ändert. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 49e68e2a-d9c0-463d-954d-34c9adfad62b
keywords:
- Windows-Steuerelemente für TBN_HOTITEMCHANGE Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d314a7250128a0f3e6b3fed54e5765487619d8e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739889"
---
# <a name="tbn_hotitemchange-notification-code"></a><span data-ttu-id="90198-105">TBN- \_ meldeänderungs-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="90198-105">TBN\_HOTITEMCHANGE notification code</span></span>

<span data-ttu-id="90198-106">Wird von einem ToolBar-Steuerelement gesendet, wenn sich das heiße Element (hervorgehoben) ändert.</span><span class="sxs-lookup"><span data-stu-id="90198-106">Sent by a toolbar control when the hot (highlighted) item changes.</span></span> <span data-ttu-id="90198-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="90198-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_HOTITEMCHANGE

    lpnmhi = (LPNMTBHOTITEM) lParam;
```



## <a name="parameters"></a><span data-ttu-id="90198-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="90198-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90198-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="90198-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90198-110">Zeiger auf eine [**nmtbhutitem**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) -Struktur, die Informationen zu diesem Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="90198-110">Pointer to an [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90198-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="90198-111">Return value</span></span>

<span data-ttu-id="90198-112">Gibt NULL zurück, damit das Element hervorgehoben werden kann, oder ungleich NULL, um zu verhindern, dass das Element hervorgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="90198-112">Return zero to allow the item to be highlighted, or nonzero to prevent the item from being highlighted.</span></span>

## <a name="requirements"></a><span data-ttu-id="90198-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90198-113">Requirements</span></span>



| <span data-ttu-id="90198-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90198-114">Requirement</span></span> | <span data-ttu-id="90198-115">Wert</span><span class="sxs-lookup"><span data-stu-id="90198-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90198-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="90198-116">Minimum supported client</span></span><br/> | <span data-ttu-id="90198-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90198-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="90198-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="90198-118">Minimum supported server</span></span><br/> | <span data-ttu-id="90198-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90198-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="90198-120">Header</span><span class="sxs-lookup"><span data-stu-id="90198-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="90198-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="90198-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





