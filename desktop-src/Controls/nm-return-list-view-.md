---
title: NM_RETURN (Listenansicht) Benachrichtigungs Code (kommstrg. h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass das Steuerelement den Eingabefokus besitzt und dass der Benutzer die EINGABETASTE gedrückt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 21a8d308-d747-4020-8925-d982234bcf81
keywords:
- NM_RETURN (Listenansicht) Windows-Steuerelemente für Benachrichtigungs Code
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
ms.openlocfilehash: 9b221189ced0e351f088493f00fa7b8849717668
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956892"
---
# <a name="nm_return-list-view-notification-code"></a><span data-ttu-id="f4a16-105">NM \_ Rückgabe (Listenansicht) Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="f4a16-105">NM\_RETURN (list view) notification code</span></span>

<span data-ttu-id="f4a16-106">Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass das Steuerelement den Eingabefokus besitzt und dass der Benutzer die EINGABETASTE gedrückt hat.</span><span class="sxs-lookup"><span data-stu-id="f4a16-106">Notifies a list-view control's parent window that the control has the input focus and that the user has pressed the ENTER key.</span></span> <span data-ttu-id="f4a16-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="f4a16-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RETURN 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f4a16-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4a16-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4a16-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f4a16-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4a16-110">Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="f4a16-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4a16-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f4a16-111">Return value</span></span>

<span data-ttu-id="f4a16-112">Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4a16-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4a16-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4a16-113">Requirements</span></span>



| <span data-ttu-id="f4a16-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4a16-114">Requirement</span></span> | <span data-ttu-id="f4a16-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f4a16-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f4a16-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f4a16-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f4a16-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4a16-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f4a16-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f4a16-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f4a16-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4a16-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f4a16-120">Header</span><span class="sxs-lookup"><span data-stu-id="f4a16-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4a16-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4a16-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





