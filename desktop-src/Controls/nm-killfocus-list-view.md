---
title: NM_KILLFOCUS (Listenansicht) Benachrichtigungs Code (kommstrg. h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass das Steuerelement den Eingabefokus verloren hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: f60064da-21e1-4555-ae72-cda8bd76175a
keywords:
- NM_KILLFOCUS (Listenansicht) Windows-Steuerelemente für Benachrichtigungs Code
topic_type:
- apiref
api_name:
- NM_KILLFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c031f3ab23d9f79ccf7f29dcfdf5472162214
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475147"
---
# <a name="nm_killfocus-list-view-notification-code"></a><span data-ttu-id="ec767-105">NM- \_ killfokus (Listenansicht) Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="ec767-105">NM\_KILLFOCUS (list view) notification code</span></span>

<span data-ttu-id="ec767-106">Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass das Steuerelement den Eingabefokus verloren hat.</span><span class="sxs-lookup"><span data-stu-id="ec767-106">Notifies a list-view control's parent window that the control has lost the input focus.</span></span> <span data-ttu-id="ec767-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="ec767-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KILLFOCUS

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ec767-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec767-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec767-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec767-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec767-110">Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="ec767-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec767-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ec767-111">Return value</span></span>

<span data-ttu-id="ec767-112">Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ec767-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec767-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec767-113">Requirements</span></span>



| <span data-ttu-id="ec767-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ec767-114">Requirement</span></span> | <span data-ttu-id="ec767-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ec767-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec767-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ec767-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ec767-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec767-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ec767-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ec767-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ec767-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec767-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ec767-120">Header</span><span class="sxs-lookup"><span data-stu-id="ec767-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec767-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec767-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





