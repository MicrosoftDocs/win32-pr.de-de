---
title: NM_LDOWN Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Steuer Elements, dass die linke Maustaste gedrückt wurde. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 59546fc3-f7c5-4b2d-9fd7-2ff89d72cd9f
keywords:
- Windows-Steuerelemente für NM_LDOWN Benachrichtigungs
topic_type:
- apiref
api_name:
- NM_LDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d62d1570fc0c10ccb64ae6c1f9af6433025ec79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338117"
---
# <a name="nm_ldown-notification-code"></a><span data-ttu-id="39824-105">NM- \_ ldown-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="39824-105">NM\_LDOWN notification code</span></span>

<span data-ttu-id="39824-106">Benachrichtigt das übergeordnete Fenster eines Steuer Elements, dass die linke Maustaste gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="39824-106">Notifies a control's parent window that the left mouse button has been pressed.</span></span> <span data-ttu-id="39824-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="39824-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_LDOWN

   lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="39824-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="39824-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39824-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39824-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39824-110">Ein Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="39824-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39824-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39824-111">Return value</span></span>

<span data-ttu-id="39824-112">Der Rückgabewert wird vom-Steuerelement ignoriert.</span><span class="sxs-lookup"><span data-stu-id="39824-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="39824-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39824-113">Requirements</span></span>



| <span data-ttu-id="39824-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39824-114">Requirement</span></span> | <span data-ttu-id="39824-115">Wert</span><span class="sxs-lookup"><span data-stu-id="39824-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39824-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39824-116">Minimum supported client</span></span><br/> | <span data-ttu-id="39824-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39824-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="39824-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39824-118">Minimum supported server</span></span><br/> | <span data-ttu-id="39824-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39824-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="39824-120">Header</span><span class="sxs-lookup"><span data-stu-id="39824-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="39824-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="39824-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





