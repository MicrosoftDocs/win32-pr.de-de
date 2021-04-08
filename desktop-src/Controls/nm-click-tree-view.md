---
title: Benachrichtigungs Code für NM_CLICK (Strukturansicht) (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass der Benutzer auf die linke Maustaste im Steuerelement geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 39b5716d-cae7-4dc4-b257-0118f4f432c6
keywords:
- NM_CLICK (Strukturansicht) Windows-Steuerelemente für Benachrichtigungs Code
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45809a683d06871398e79419ec08729b1edcd2c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743985"
---
# <a name="nm_click-tree-view-notification-code"></a><span data-ttu-id="654e8-105">NM \_ Klick (Strukturansicht) Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="654e8-105">NM\_CLICK (tree view) notification code</span></span>

<span data-ttu-id="654e8-106">Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass der Benutzer auf die linke Maustaste im Steuerelement geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="654e8-106">Notifies the parent window of a tree-view control that the user has clicked the left mouse button within the control.</span></span> <span data-ttu-id="654e8-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="654e8-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CLICK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="654e8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="654e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="654e8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="654e8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="654e8-110">Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="654e8-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="654e8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="654e8-111">Return value</span></span>

<span data-ttu-id="654e8-112">Gibt einen Wert ungleich 0 (null) zurück, um die Standard Verarbeitung zu verhindern, oder NULL, um die Standard Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="654e8-112">Return nonzero to prevent the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="654e8-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="654e8-113">Requirements</span></span>



| <span data-ttu-id="654e8-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="654e8-114">Requirement</span></span> | <span data-ttu-id="654e8-115">Wert</span><span class="sxs-lookup"><span data-stu-id="654e8-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="654e8-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="654e8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="654e8-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="654e8-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="654e8-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="654e8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="654e8-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="654e8-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="654e8-120">Header</span><span class="sxs-lookup"><span data-stu-id="654e8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="654e8-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="654e8-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





