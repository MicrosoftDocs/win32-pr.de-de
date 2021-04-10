---
title: NM_OUTOFMEMORY Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Steuer Elements, dass das Steuerelement einen Vorgang nicht beenden konnte, weil nicht genügend Arbeitsspeicher verfügbar war. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: d7d80515-ae6c-4817-a698-d486a9d86c4a
keywords:
- Windows-Steuerelemente für NM_OUTOFMEMORY Benachrichtigungs
topic_type:
- apiref
api_name:
- NM_OUTOFMEMORY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f1321f88360d168b13d16b36f984d9b797dc094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040168"
---
# <a name="nm_outofmemory-notification-code"></a><span data-ttu-id="6c680-105">NM- \_ oudefmemory-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="6c680-105">NM\_OUTOFMEMORY notification code</span></span>

<span data-ttu-id="6c680-106">Benachrichtigt das übergeordnete Fenster eines Steuer Elements, dass das Steuerelement einen Vorgang nicht beenden konnte, weil nicht genügend Arbeitsspeicher verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="6c680-106">Notifies a control's parent window that the control could not complete an operation because there was not enough memory available.</span></span> <span data-ttu-id="6c680-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="6c680-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_OUTOFMEMORY

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="6c680-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c680-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c680-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c680-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c680-110">Ein Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="6c680-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c680-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c680-111">Return value</span></span>

<span data-ttu-id="6c680-112">Der Rückgabewert wird vom-Steuerelement ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6c680-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c680-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c680-113">Requirements</span></span>



| <span data-ttu-id="6c680-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c680-114">Requirement</span></span> | <span data-ttu-id="6c680-115">Wert</span><span class="sxs-lookup"><span data-stu-id="6c680-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c680-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c680-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6c680-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c680-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6c680-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c680-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6c680-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c680-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c680-120">Header</span><span class="sxs-lookup"><span data-stu-id="6c680-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c680-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c680-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





