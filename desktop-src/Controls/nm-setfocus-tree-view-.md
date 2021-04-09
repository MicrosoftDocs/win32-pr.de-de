---
title: Benachrichtigungs Code für NM_SETFOCUS (Strukturansicht) (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass das Steuerelement den Eingabefokus erhalten hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 4bdd6cd2-afd3-4c0b-914b-8fff55e474a9
keywords:
- NM_SETFOCUS (Strukturansicht) Windows-Steuerelemente für Benachrichtigungs Code
topic_type:
- apiref
api_name:
- NM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b9e24d95b95b3c66fe43920f780b2e8d0f66679
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858958"
---
# <a name="nm_setfocus-tree-view-notification-code"></a><span data-ttu-id="dd6fd-105">NM \_ SetFocus-Benachrichtigungs Code (Strukturansicht)</span><span class="sxs-lookup"><span data-stu-id="dd6fd-105">NM\_SETFOCUS (tree view) notification code</span></span>

<span data-ttu-id="dd6fd-106">Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass das Steuerelement den Eingabefokus erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="dd6fd-106">Notifies a tree-view control's parent window that the control has received the input focus.</span></span> <span data-ttu-id="dd6fd-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="dd6fd-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_SETFOCUS 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="dd6fd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd6fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd6fd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dd6fd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd6fd-110">Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="dd6fd-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd6fd-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dd6fd-111">Return value</span></span>

<span data-ttu-id="dd6fd-112">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="dd6fd-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd6fd-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd6fd-113">Requirements</span></span>



| <span data-ttu-id="dd6fd-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd6fd-114">Requirement</span></span> | <span data-ttu-id="dd6fd-115">Wert</span><span class="sxs-lookup"><span data-stu-id="dd6fd-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd6fd-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dd6fd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dd6fd-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd6fd-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dd6fd-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dd6fd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dd6fd-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd6fd-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dd6fd-120">Header</span><span class="sxs-lookup"><span data-stu-id="dd6fd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd6fd-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd6fd-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





