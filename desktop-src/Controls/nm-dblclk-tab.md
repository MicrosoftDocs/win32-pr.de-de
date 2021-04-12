---
title: NM_DBLCLK (Registerkarte) Benachrichtigungs Code (kommstrg. h)
description: Benachrichtigt ein übergeordnetes Fenster eines Registerkarten-Steuer Elements, dass der Benutzer die linke Maustaste im Steuerelement doppelt geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: fd99f195-ceac-47e8-b584-d814b055fa21
keywords:
- Windows-Steuerelemente (Registerkarte) NM_DBLCLK
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c8171696e57684be55e6e42792666ae206d890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105453"
---
# <a name="nm_dblclk-tab-notification-code"></a><span data-ttu-id="fdd0f-105">NM- \_ dblclk (Registerkarte)-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="fdd0f-105">NM\_DBLCLK (tab) notification code</span></span>

<span data-ttu-id="fdd0f-106">Benachrichtigt ein übergeordnetes Fenster eines Registerkarten-Steuer Elements, dass der Benutzer die linke Maustaste im Steuerelement doppelt geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="fdd0f-106">Notifies a parent window of a tab control that the user has double-clicked the left mouse button within the control.</span></span> <span data-ttu-id="fdd0f-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="fdd0f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_DBLCLK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="fdd0f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fdd0f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdd0f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fdd0f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fdd0f-110">Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="fdd0f-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdd0f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fdd0f-111">Return value</span></span>

<span data-ttu-id="fdd0f-112">Gibt einen Wert ungleich 0 (null) zurück, um die Standard Verarbeitung nicht zuzulassen, oder NULL, um die Standard Verarbeitung zuzulassen</span><span class="sxs-lookup"><span data-stu-id="fdd0f-112">Return nonzero to not allow the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdd0f-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fdd0f-113">Requirements</span></span>



| <span data-ttu-id="fdd0f-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fdd0f-114">Requirement</span></span> | <span data-ttu-id="fdd0f-115">Wert</span><span class="sxs-lookup"><span data-stu-id="fdd0f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fdd0f-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fdd0f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fdd0f-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fdd0f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fdd0f-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fdd0f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fdd0f-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fdd0f-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fdd0f-120">Header</span><span class="sxs-lookup"><span data-stu-id="fdd0f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdd0f-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdd0f-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





