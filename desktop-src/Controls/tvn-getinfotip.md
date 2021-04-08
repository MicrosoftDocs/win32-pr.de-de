---
title: TVN_GETINFOTIP Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Strukturansicht-Steuerelement gesendet, das über den infotip-Stil des Fernsehsystems verfügt \_ . Dieser Benachrichtigungs Code wird gesendet, wenn das Steuerelement zusätzliche Textinformationen anfordert, die in einer QuickInfo angezeigt werden sollen. Der Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 20576710-e279-4e61-be6b-bf1d8ea79555
keywords:
- Windows-Steuerelemente für TVN_GETINFOTIP Benachrichtigungs
topic_type:
- apiref
api_name:
- TVN_GETINFOTIP
- TVN_GETINFOTIPA
- TVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1336571fa2c06e8b22078b1d761d9841217104e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742256"
---
# <a name="tvn_getinfotip-notification-code"></a><span data-ttu-id="d8cb4-106">TVN \_ getinfotip-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="d8cb4-106">TVN\_GETINFOTIP notification code</span></span>

<span data-ttu-id="d8cb4-107">Wird von einem Strukturansicht-Steuerelement gesendet, das über den [**\_ infotip**](tree-view-control-window-styles.md) -Stil des Fernsehsystems verfügt.</span><span class="sxs-lookup"><span data-stu-id="d8cb4-107">Sent by a tree-view control that has the [**TVS\_INFOTIP**](tree-view-control-window-styles.md) style.</span></span> <span data-ttu-id="d8cb4-108">Dieser Benachrichtigungs Code wird gesendet, wenn das Steuerelement zusätzliche Textinformationen anfordert, die in einer QuickInfo angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d8cb4-108">This notification code is sent when the control is requesting additional text information to be displayed in a tooltip.</span></span> <span data-ttu-id="d8cb4-109">Der Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="d8cb4-109">The notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_GETINFOTIP

    lpGetInfoTip = (LPNMTVGETINFOTIP)lParam;
```



## <a name="parameters"></a><span data-ttu-id="d8cb4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8cb4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8cb4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d8cb4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d8cb4-112">Zeiger auf eine [**nmtvgetinfotip**](/windows/win32/api/commctrl/ns-commctrl-nmtvgetinfotipa) -Struktur, die Informationen zu diesem Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="d8cb4-112">Pointer to an [**NMTVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtvgetinfotipa) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8cb4-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d8cb4-113">Return value</span></span>

<span data-ttu-id="d8cb4-114">Das-Steuerelement ignoriert den Rückgabewert für diesen Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="d8cb4-114">The control ignores the return value for this notification code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8cb4-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d8cb4-115">Remarks</span></span>

<span data-ttu-id="d8cb4-116">Dieser Benachrichtigungs Code wird nur von Strukturansicht-Steuerelementen gesendet, die über den [**\_ infotip**](tree-view-control-window-styles.md) -Stil "TV" verfügen.</span><span class="sxs-lookup"><span data-stu-id="d8cb4-116">This notification code is only sent by tree-view controls that have the [**TVS\_INFOTIP**](tree-view-control-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8cb4-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8cb4-117">Requirements</span></span>



| <span data-ttu-id="d8cb4-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8cb4-118">Requirement</span></span> | <span data-ttu-id="d8cb4-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d8cb4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d8cb4-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d8cb4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d8cb4-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d8cb4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d8cb4-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d8cb4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d8cb4-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d8cb4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d8cb4-124">Header</span><span class="sxs-lookup"><span data-stu-id="d8cb4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8cb4-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8cb4-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d8cb4-126">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="d8cb4-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d8cb4-127">**TVN \_ Getinfotipw** (Unicode) und **TVN \_ getinfotipa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d8cb4-127">**TVN\_GETINFOTIPW** (Unicode) and **TVN\_GETINFOTIPA** (ANSI)</span></span><br/>             |



 

 





