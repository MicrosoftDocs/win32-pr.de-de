---
title: NM_FONTCHANGED Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Listenansicht-Steuerelement gesendet, wenn das Steuerelement eine Schriftart geändert hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: ffa019b0-34be-4bb3-b9dd-c267545fec84
keywords:
- Windows-Steuerelemente für NM_FONTCHANGED Benachrichtigungs
topic_type:
- apiref
api_name:
- NM_FONTCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75003021f83276c953b5aa2cf0b812d20d60857b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858647"
---
# <a name="nm_fontchanged-notification-code"></a><span data-ttu-id="efc58-105">NM \_ FontChanged-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="efc58-105">NM\_FONTCHANGED notification code</span></span>

<span data-ttu-id="efc58-106">Wird von einem Listenansicht-Steuerelement gesendet, wenn das Steuerelement eine Schriftart geändert hat.</span><span class="sxs-lookup"><span data-stu-id="efc58-106">Sent by a list-view control when the control has changed a font.</span></span> <span data-ttu-id="efc58-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="efc58-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_FONTCHANGED
        
    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="efc58-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="efc58-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efc58-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="efc58-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="efc58-110">Ein Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="efc58-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efc58-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="efc58-111">Return value</span></span>

<span data-ttu-id="efc58-112">Der Rückgabewert wird vom-Steuerelement ignoriert.</span><span class="sxs-lookup"><span data-stu-id="efc58-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="efc58-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="efc58-113">Requirements</span></span>



| <span data-ttu-id="efc58-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="efc58-114">Requirement</span></span> | <span data-ttu-id="efc58-115">Wert</span><span class="sxs-lookup"><span data-stu-id="efc58-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="efc58-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="efc58-116">Minimum supported client</span></span><br/> | <span data-ttu-id="efc58-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="efc58-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="efc58-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="efc58-118">Minimum supported server</span></span><br/> | <span data-ttu-id="efc58-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="efc58-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="efc58-120">Header</span><span class="sxs-lookup"><span data-stu-id="efc58-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="efc58-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="efc58-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





