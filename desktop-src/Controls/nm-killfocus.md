---
title: NM_KILLFOCUS Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Steuer Elements, dass das Steuerelement den Eingabefokus verloren hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: d7538697-8b4c-4bbd-8b06-02cbc8069a22
keywords:
- Windows-Steuerelemente für NM_KILLFOCUS Benachrichtigungs
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
ms.openlocfilehash: 873af3315dd58a12a61249ca59a317ca5af4b105
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102875"
---
# <a name="nm_killfocus-notification-code"></a><span data-ttu-id="3d71d-105">NM- \_ killfokus-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="3d71d-105">NM\_KILLFOCUS notification code</span></span>

<span data-ttu-id="3d71d-106">Benachrichtigt das übergeordnete Fenster eines Steuer Elements, dass das Steuerelement den Eingabefokus verloren hat.</span><span class="sxs-lookup"><span data-stu-id="3d71d-106">Notifies a control's parent window that the control has lost the input focus.</span></span> <span data-ttu-id="3d71d-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="3d71d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KILLFOCUS

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="3d71d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d71d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d71d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3d71d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d71d-110">Ein Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="3d71d-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d71d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3d71d-111">Return value</span></span>

<span data-ttu-id="3d71d-112">Der Rückgabewert wird vom-Steuerelement ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3d71d-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d71d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d71d-113">Requirements</span></span>



| <span data-ttu-id="3d71d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d71d-114">Requirement</span></span> | <span data-ttu-id="3d71d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="3d71d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3d71d-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3d71d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3d71d-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d71d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3d71d-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3d71d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3d71d-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d71d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3d71d-120">Header</span><span class="sxs-lookup"><span data-stu-id="3d71d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d71d-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d71d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





