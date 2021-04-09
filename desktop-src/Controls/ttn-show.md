---
title: TTN_SHOW Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das Besitzer Fenster, dass ein QuickInfo-Steuerelement angezeigt wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: ddfd18cd-0681-4e4a-b258-873f98da7479
keywords:
- Windows-Steuerelemente für TTN_SHOW Benachrichtigungs
topic_type:
- apiref
api_name:
- TTN_SHOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16acb41d1145c176799dd7997b56a850bb45ece7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956536"
---
# <a name="ttn_show-notification-code"></a><span data-ttu-id="1a3ed-105">TTN \_ Anzeigen des Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="1a3ed-105">TTN\_SHOW notification code</span></span>

<span data-ttu-id="1a3ed-106">Benachrichtigt das Besitzer Fenster, dass ein QuickInfo-Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1a3ed-106">Notifies the owner window that a tooltip control is about to be displayed.</span></span> <span data-ttu-id="1a3ed-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="1a3ed-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_SHOW

    pnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="1a3ed-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a3ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a3ed-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1a3ed-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a3ed-110">Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="1a3ed-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a3ed-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1a3ed-111">Return value</span></span>

<span data-ttu-id="1a3ed-112">[Version 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="1a3ed-112">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="1a3ed-113">Wenn die QuickInfo an Ihrem Standard Speicherort angezeigt werden soll, wird NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1a3ed-113">To display the tooltip in its default location, return zero.</span></span> <span data-ttu-id="1a3ed-114">Zum Anpassen der QuickInfo-Position positionieren Sie das QuickInfo-Fenster mit der [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) -Funktion neu, und geben Sie **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="1a3ed-114">To customize the tooltip position, reposition the tooltip window with the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function and return **TRUE**.</span></span>

> [!Note]  
> <span data-ttu-id="1a3ed-115">Bei früheren Versionen als 4,70 gibt es keinen Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="1a3ed-115">For versions earlier than 4.70, there is no return value.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="1a3ed-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a3ed-116">Remarks</span></span>

<span data-ttu-id="1a3ed-117">Ein QuickInfo-Fenster Rechteck ist etwas größer als das Textanzeige Rechteck, und sein Ursprung ist von links nach links.</span><span class="sxs-lookup"><span data-stu-id="1a3ed-117">A tooltip window rectangle is somewhat larger than its text display rectangle, and its origin is offset up and to the left.</span></span> <span data-ttu-id="1a3ed-118">Wenn Sie das Textanzeige Rechteck einer QuickInfo exakt positionieren müssen, konvertiert die [**TTM \_**](ttm-adjustrect.md) -Nachricht "Bildschirm" ein Textanzeige Rechteck in das entsprechende QuickInfo-Fenster Rechteck und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="1a3ed-118">If you need to accurately position the text display rectangle of a tooltip, the [**TTM\_ADJUSTRECT**](ttm-adjustrect.md) message converts a text display rectangle into the corresponding tooltip window rectangle and vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a3ed-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a3ed-119">Requirements</span></span>



| <span data-ttu-id="1a3ed-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1a3ed-120">Requirement</span></span> | <span data-ttu-id="1a3ed-121">Wert</span><span class="sxs-lookup"><span data-stu-id="1a3ed-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1a3ed-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1a3ed-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1a3ed-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1a3ed-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1a3ed-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1a3ed-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1a3ed-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1a3ed-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1a3ed-126">Header</span><span class="sxs-lookup"><span data-stu-id="1a3ed-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a3ed-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a3ed-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

