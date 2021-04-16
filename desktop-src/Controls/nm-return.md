---
title: NM_RETURN Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Steuer Elements, dass das Steuerelement den Eingabefokus besitzt und dass der Benutzer die EINGABETASTE gedrückt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 2c4839bc-6b23-469b-978f-cdf5f7bc0549
keywords:
- Windows-Steuerelemente für NM_RETURN Benachrichtigungs
topic_type:
- apiref
api_name:
- NM_RETURN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c6cebd089873df5471c9b25710efafaab4d246f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518455"
---
# <a name="nm_return-notification-code"></a><span data-ttu-id="54acb-105">NM \_ Rückgabe Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="54acb-105">NM\_RETURN notification code</span></span>

<span data-ttu-id="54acb-106">Benachrichtigt das übergeordnete Fenster eines Steuer Elements, dass das Steuerelement den Eingabefokus besitzt und dass der Benutzer die EINGABETASTE gedrückt hat.</span><span class="sxs-lookup"><span data-stu-id="54acb-106">Notifies a control's parent window that the control has the input focus and that the user has pressed the ENTER key.</span></span> <span data-ttu-id="54acb-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="54acb-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RETURN 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="54acb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="54acb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54acb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54acb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54acb-110">Ein Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="54acb-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54acb-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54acb-111">Return value</span></span>

<span data-ttu-id="54acb-112">Der Rückgabewert wird vom-Steuerelement ignoriert.</span><span class="sxs-lookup"><span data-stu-id="54acb-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="54acb-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54acb-113">Requirements</span></span>



| <span data-ttu-id="54acb-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54acb-114">Requirement</span></span> | <span data-ttu-id="54acb-115">Wert</span><span class="sxs-lookup"><span data-stu-id="54acb-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54acb-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54acb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="54acb-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54acb-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="54acb-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54acb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="54acb-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54acb-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="54acb-120">Header</span><span class="sxs-lookup"><span data-stu-id="54acb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="54acb-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="54acb-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





