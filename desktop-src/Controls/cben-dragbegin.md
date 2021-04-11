---
title: CBEN_DRAGBEGIN Benachrichtigungs Code (kommctrl. h)
description: Wird gesendet, wenn der Benutzer mit dem Ziehen des Bilds des Elements beginnt, das im Bearbeitungsbereich des Steuer Elements angezeigt wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: bdab2700-a605-48af-aee3-bbf573408e3f
keywords:
- Windows-Steuerelemente für CBEN_DRAGBEGIN Benachrichtigungs
topic_type:
- apiref
api_name:
- CBEN_DRAGBEGIN
- CBEN_DRAGBEGINA
- CBEN_DRAGBEGINW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 910e6ac494b49f685a55e77b432e96b4fb22bd29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105758"
---
# <a name="cben_dragbegin-notification-code"></a><span data-ttu-id="37e35-105">Cben \_ dragbegin-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="37e35-105">CBEN\_DRAGBEGIN notification code</span></span>

<span data-ttu-id="37e35-106">Wird gesendet, wenn der Benutzer mit dem Ziehen des Bilds des Elements beginnt, das im Bearbeitungsbereich des Steuer Elements angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="37e35-106">Sent when the user begins dragging the image of the item displayed in the edit portion of the control.</span></span> <span data-ttu-id="37e35-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="37e35-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_DRAGBEGIN

    lpnmdb = (LPNMCBEDRAGBEGIN) lParam;
```



## <a name="parameters"></a><span data-ttu-id="37e35-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="37e35-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37e35-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="37e35-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37e35-110">Ein Zeiger auf eine [**nmcbedragbegin**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) -Struktur, die Informationen über den Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="37e35-110">A pointer to a [**NMCBEDRAGBEGIN**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37e35-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="37e35-111">Return value</span></span>

<span data-ttu-id="37e35-112">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="37e35-112">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="37e35-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37e35-113">Remarks</span></span>

<span data-ttu-id="37e35-114">Wenn die empfangende Anwendung die Drag & Drop-Funktionalität aus dem Steuerelement implementiert, startet die Anwendung den Drag & Drop-Vorgang als Reaktion auf diesen Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="37e35-114">If the receiving application implements drag-and-drop functionality from the control, the application will begin the drag-and-drop operation in response to this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="37e35-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37e35-115">Requirements</span></span>



| <span data-ttu-id="37e35-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37e35-116">Requirement</span></span> | <span data-ttu-id="37e35-117">Wert</span><span class="sxs-lookup"><span data-stu-id="37e35-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="37e35-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37e35-118">Minimum supported client</span></span><br/> | <span data-ttu-id="37e35-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37e35-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="37e35-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37e35-120">Minimum supported server</span></span><br/> | <span data-ttu-id="37e35-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37e35-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="37e35-122">Header</span><span class="sxs-lookup"><span data-stu-id="37e35-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="37e35-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="37e35-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="37e35-124">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="37e35-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="37e35-125">**Cben \_ Dragbeginw** (Unicode) und **cben \_ dragbegina** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="37e35-125">**CBEN\_DRAGBEGINW** (Unicode) and **CBEN\_DRAGBEGINA** (ANSI)</span></span><br/>             |



 

 





