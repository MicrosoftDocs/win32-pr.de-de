---
title: NM_CUSTOMTEXT Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Steuer Elements über benutzerdefinierte Textoperationen. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: b4bde648-3479-4fac-ad32-b34c7272c1fc
keywords:
- Windows-Steuerelemente für NM_CUSTOMTEXT Benachrichtigungs
topic_type:
- apiref
api_name:
- NM_CUSTOMTEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eebc4033a76d137e28a0c4170c5c613c7933562
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391514"
---
# <a name="nm_customtext-notification-code"></a><span data-ttu-id="c9b76-105">NM \_ CustomText-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="c9b76-105">NM\_CUSTOMTEXT notification code</span></span>

<span data-ttu-id="c9b76-106">Benachrichtigt das übergeordnete Fenster eines Steuer Elements über benutzerdefinierte Textoperationen.</span><span class="sxs-lookup"><span data-stu-id="c9b76-106">Notifies a control's parent window about custom text operations.</span></span> <span data-ttu-id="c9b76-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="c9b76-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMTEXT

    lpnmct = (NMCUSTOMTEXT) lParam;
```



## <a name="parameters"></a><span data-ttu-id="c9b76-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9b76-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9b76-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c9b76-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9b76-110">Ein Zeiger auf eine [**nmcustomtext**](/windows/win32/api/commctrl/ns-commctrl-nmcustomtext) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="c9b76-110">A pointer to an [**NMCUSTOMTEXT**](/windows/win32/api/commctrl/ns-commctrl-nmcustomtext) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9b76-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c9b76-111">Return value</span></span>

<span data-ttu-id="c9b76-112">Der Rückgabewert wird vom-Steuerelement ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c9b76-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9b76-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9b76-113">Requirements</span></span>



| <span data-ttu-id="c9b76-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9b76-114">Requirement</span></span> | <span data-ttu-id="c9b76-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c9b76-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9b76-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c9b76-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c9b76-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9b76-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c9b76-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c9b76-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c9b76-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9b76-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c9b76-120">Header</span><span class="sxs-lookup"><span data-stu-id="c9b76-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9b76-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9b76-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





