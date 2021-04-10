---
title: Benachrichtigungs Code für NM_DBLCLK (Strukturansicht) (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass der Benutzer die linke Maustaste im Steuerelement doppelt geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 2ed3b3ad-a252-496a-bfcf-0cec5678f192
keywords:
- NM_DBLCLK (Strukturansicht) Windows-Steuerelemente für Benachrichtigungs Code
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
ms.openlocfilehash: 78f89671e1a26962eacf255d4c98ea0baa1578de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040096"
---
# <a name="nm_dblclk-tree-view-notification-code"></a><span data-ttu-id="de22b-105">NM- \_ dblclk-Benachrichtigungs Code (Strukturansicht)</span><span class="sxs-lookup"><span data-stu-id="de22b-105">NM\_DBLCLK (tree view) notification code</span></span>

<span data-ttu-id="de22b-106">Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass der Benutzer die linke Maustaste im Steuerelement doppelt geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="de22b-106">Notifies the parent window of a tree-view control that the user has double-clicked the left mouse button within the control.</span></span> <span data-ttu-id="de22b-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="de22b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_DBLCLK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="de22b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="de22b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de22b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="de22b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de22b-110">Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="de22b-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de22b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de22b-111">Return value</span></span>

<span data-ttu-id="de22b-112">Gibt einen Wert ungleich 0 (null) zurück, um die Standard Verarbeitung zu verhindern, oder NULL, um die Standard Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="de22b-112">Return nonzero to prevent the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="de22b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de22b-113">Requirements</span></span>



| <span data-ttu-id="de22b-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de22b-114">Requirement</span></span> | <span data-ttu-id="de22b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="de22b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="de22b-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de22b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="de22b-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de22b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="de22b-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de22b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="de22b-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de22b-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="de22b-120">Header</span><span class="sxs-lookup"><span data-stu-id="de22b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="de22b-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="de22b-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





