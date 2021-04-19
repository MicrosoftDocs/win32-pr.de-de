---
title: SBN_SIMPLEMODECHANGE Benachrichtigungs Code (kommctrl. h)
description: Wird von einem StatusBar-Steuerelement gesendet, wenn sich der einfache Modus aufgrund einer einfachen SB- \_ Nachricht ändert. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: b2df8feb-5028-4488-a99b-4ceff5b48a92
keywords:
- Windows-Steuerelemente für SBN_SIMPLEMODECHANGE Benachrichtigungs
topic_type:
- apiref
api_name:
- SBN_SIMPLEMODECHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b998f0c39ecb00322bf5a423f99b3231338283f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338775"
---
# <a name="sbn_simplemodechange-notification-code"></a><span data-ttu-id="3f655-105">SBN \_ simplemodechange-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="3f655-105">SBN\_SIMPLEMODECHANGE notification code</span></span>

<span data-ttu-id="3f655-106">Wird von einem StatusBar-Steuerelement gesendet, wenn sich der einfache Modus aufgrund einer [**\_ einfachen SB**](sb-simple.md) -Nachricht ändert.</span><span class="sxs-lookup"><span data-stu-id="3f655-106">Sent by a status bar control when the simple mode changes due to a [**SB\_SIMPLE**](sb-simple.md) message.</span></span> <span data-ttu-id="3f655-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="3f655-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
SBN_SIMPLEMODECHANGE

    lpnmh = (NMHDR*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="3f655-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f655-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f655-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3f655-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3f655-110">Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die Informationen über den Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="3f655-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f655-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3f655-111">Return value</span></span>

<span data-ttu-id="3f655-112">Der Rückgabewert wird von der Statusleiste ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3f655-112">The return value is ignored by the status bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f655-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f655-113">Requirements</span></span>



| <span data-ttu-id="3f655-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f655-114">Requirement</span></span> | <span data-ttu-id="3f655-115">Wert</span><span class="sxs-lookup"><span data-stu-id="3f655-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3f655-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3f655-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3f655-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f655-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3f655-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3f655-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3f655-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f655-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3f655-120">Header</span><span class="sxs-lookup"><span data-stu-id="3f655-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f655-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f655-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





