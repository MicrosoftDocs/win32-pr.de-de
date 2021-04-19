---
title: TCN_KEYDOWN Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Registerkarten-Steuer Elements, dass eine Taste gedrückt wurde. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 884e79cd-5732-44cd-8c7a-38bb9349ec7d
keywords:
- Windows-Steuerelemente für TCN_KEYDOWN Benachrichtigungs
topic_type:
- apiref
api_name:
- TCN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a1e963b11faf8f75e50e86e8c120ea0b05f0dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339930"
---
# <a name="tcn_keydown-notification-code"></a><span data-ttu-id="105d2-105">TCN- \_ KeyDown-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="105d2-105">TCN\_KEYDOWN notification code</span></span>

<span data-ttu-id="105d2-106">Benachrichtigt das übergeordnete Fenster eines Registerkarten-Steuer Elements, dass eine Taste gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="105d2-106">Notifies a tab control's parent window that a key has been pressed.</span></span> <span data-ttu-id="105d2-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="105d2-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_KEYDOWN 

    pnm = (NMTCKEYDOWN*) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="105d2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="105d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="105d2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="105d2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="105d2-110">Zeiger auf eine [**nmtckeydown**](/windows/win32/api/commctrl/ns-commctrl-nmtckeydown) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="105d2-110">Pointer to an [**NMTCKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtckeydown) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="105d2-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="105d2-111">Return value</span></span>

<span data-ttu-id="105d2-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="105d2-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="105d2-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="105d2-113">Requirements</span></span>



| <span data-ttu-id="105d2-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="105d2-114">Requirement</span></span> | <span data-ttu-id="105d2-115">Wert</span><span class="sxs-lookup"><span data-stu-id="105d2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="105d2-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="105d2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="105d2-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="105d2-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="105d2-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="105d2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="105d2-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="105d2-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="105d2-120">Header</span><span class="sxs-lookup"><span data-stu-id="105d2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="105d2-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="105d2-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





