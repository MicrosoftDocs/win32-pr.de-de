---
title: NM_THEMECHANGED Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Steuer Elements, dass sich das Design geändert hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 5e6a039e-9c35-4476-8cf1-5aea8977ed2d
keywords:
- Windows-Steuerelemente für NM_THEMECHANGED Benachrichtigungs
topic_type:
- apiref
api_name:
- NM_THEMECHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dab2a133da2ff1fed0949f2bc97ce294168febc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040800"
---
# <a name="nm_themechanged-notification-code"></a><span data-ttu-id="03b65-105">Der von nm \_ gemechanter Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="03b65-105">NM\_THEMECHANGED notification code</span></span>

<span data-ttu-id="03b65-106">Benachrichtigt das übergeordnete Fenster eines Steuer Elements, dass sich das Design geändert hat.</span><span class="sxs-lookup"><span data-stu-id="03b65-106">Notifies a control's parent window that the theme has changed.</span></span> <span data-ttu-id="03b65-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="03b65-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_THEMECHANGED

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="03b65-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="03b65-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03b65-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="03b65-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03b65-110">Ein Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="03b65-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03b65-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="03b65-111">Return value</span></span>

<span data-ttu-id="03b65-112">Der Rückgabewert wird vom-Steuerelement ignoriert.</span><span class="sxs-lookup"><span data-stu-id="03b65-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="03b65-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03b65-113">Requirements</span></span>



| <span data-ttu-id="03b65-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03b65-114">Requirement</span></span> | <span data-ttu-id="03b65-115">Wert</span><span class="sxs-lookup"><span data-stu-id="03b65-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="03b65-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="03b65-116">Minimum supported client</span></span><br/> | <span data-ttu-id="03b65-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03b65-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="03b65-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="03b65-118">Minimum supported server</span></span><br/> | <span data-ttu-id="03b65-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03b65-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="03b65-120">Header</span><span class="sxs-lookup"><span data-stu-id="03b65-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="03b65-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="03b65-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





