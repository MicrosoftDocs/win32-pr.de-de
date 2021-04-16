---
title: LVN_GETINFOTIP Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Listenansicht-Steuerelement mit einer großen Symbol Ansicht gesendet, das über den erweiterten LVS- \_ \_ infotip-Stil verfügt.
ms.assetid: 62be5087-7e49-4722-a63a-1768e030af48
keywords:
- Windows-Steuerelemente für LVN_GETINFOTIP Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_GETINFOTIP
- LVN_GETINFOTIPA
- LVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b4552456a575e2f03e02b2bfb78f7fcc1d8ca1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519327"
---
# <a name="lvn_getinfotip-notification-code"></a><span data-ttu-id="3fa7e-104">LVN \_ getinfotip-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="3fa7e-104">LVN\_GETINFOTIP notification code</span></span>

<span data-ttu-id="3fa7e-105">Wird von einem Listenansicht-Steuerelement mit einer großen Symbol Ansicht gesendet, das über den erweiterten [**LVS- \_ \_ infotip**](extended-list-view-styles.md) -Stil verfügt.</span><span class="sxs-lookup"><span data-stu-id="3fa7e-105">Sent by a large icon view list-view control that has the [**LVS\_EX\_INFOTIP**](extended-list-view-styles.md) extended style.</span></span> <span data-ttu-id="3fa7e-106">Dieser Benachrichtigungs Code wird gesendet, wenn das Listenansicht-Steuerelement zusätzliche Textinformationen anfordert, die in einer QuickInfo angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3fa7e-106">This notification code is sent when the list-view control is requesting additional text information to be displayed in a tooltip.</span></span> <span data-ttu-id="3fa7e-107">Sie wird in Form einer [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="3fa7e-107">It is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_GETINFOTIP

    pGetInfoTip = (LPNMLVGETINFOTIP) lParam;
```



## <a name="parameters"></a><span data-ttu-id="3fa7e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3fa7e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fa7e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3fa7e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3fa7e-110">Zeiger auf eine [**nmlvgetinfotip**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) -Struktur, die Informationen zu diesem Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="3fa7e-110">Pointer to an [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fa7e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3fa7e-111">Return value</span></span>

<span data-ttu-id="3fa7e-112">Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3fa7e-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fa7e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3fa7e-113">Remarks</span></span>

<span data-ttu-id="3fa7e-114">Dieser Benachrichtigungs Code wird nur von Listenansicht-Steuerelementen gesendet, die über die erweiterte [**LVS- \_ \_ infotip**](extended-list-view-styles.md) -Art verfügen.</span><span class="sxs-lookup"><span data-stu-id="3fa7e-114">This notification code is only sent by list-view controls that have the [**LVS\_EX\_INFOTIP**](extended-list-view-styles.md) extended style.</span></span> <span data-ttu-id="3fa7e-115">Der LVN \_ getinfotip-Benachrichtigungs Code wird nur für Unterelement 0 gesendet.</span><span class="sxs-lookup"><span data-stu-id="3fa7e-115">The LVN\_GETINFOTIP notification code is sent only for subitem 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fa7e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3fa7e-116">Requirements</span></span>



| <span data-ttu-id="3fa7e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3fa7e-117">Requirement</span></span> | <span data-ttu-id="3fa7e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="3fa7e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3fa7e-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3fa7e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3fa7e-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3fa7e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3fa7e-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3fa7e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3fa7e-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3fa7e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3fa7e-123">Header</span><span class="sxs-lookup"><span data-stu-id="3fa7e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fa7e-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fa7e-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="3fa7e-125">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="3fa7e-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3fa7e-126">**LVN \_ Getinfotipw** (Unicode) und **LVN \_ getinfotipa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3fa7e-126">**LVN\_GETINFOTIPW** (Unicode) and **LVN\_GETINFOTIPA** (ANSI)</span></span><br/>             |



 

 





