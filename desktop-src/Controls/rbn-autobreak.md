---
title: RBN_AUTOBREAK Meldung (kommstrg. h)
description: Benachrichtigt das übergeordnete Element einer übergeordneten Leiste, dass eine Unterbrechung in der Leiste angezeigt wird. Das übergeordnete Element bestimmt, ob die Unterbrechung vorgenommen werden soll. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: b7a63027-6cfa-4d5a-9ea6-fdd8b4fb6864
keywords:
- Windows-Steuerelemente für RBN_AUTOBREAK Meldung
topic_type:
- apiref
api_name:
- RBN_AUTOBREAK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d614277d89578cb66e528ba16656ed55681ebbcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859277"
---
# <a name="rbn_autobreak-message"></a><span data-ttu-id="4538d-106">RBN- \_ Meldung zum autobreak</span><span class="sxs-lookup"><span data-stu-id="4538d-106">RBN\_AUTOBREAK message</span></span>

<span data-ttu-id="4538d-107">Benachrichtigt das übergeordnete Element einer übergeordneten [Leiste](rebar-controls.md) , dass eine Unterbrechung in der Leiste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4538d-107">Notifies a [rebar's](rebar-controls.md) parent that a break will appear in the bar.</span></span> <span data-ttu-id="4538d-108">Das übergeordnete Element bestimmt, ob die Unterbrechung vorgenommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4538d-108">The parent determines whether to make the break.</span></span> <span data-ttu-id="4538d-109">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="4538d-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_AUTOBREAK

    pnmRebarAutoBreak = (LPNMREBARAUTOBREAK) lParam;
```



## <a name="parameters"></a><span data-ttu-id="4538d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4538d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4538d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4538d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4538d-112">Zeiger auf eine [**nmrebarautobreak**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) -Struktur, die Informationen über den Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="4538d-112">Pointer to a [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4538d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4538d-113">Return value</span></span>

<span data-ttu-id="4538d-114">Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4538d-114">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="4538d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4538d-115">Remarks</span></span>

<span data-ttu-id="4538d-116">Der Wert im **fautobreak** -Member der [**nmrebarautobreak**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) -Struktur gibt an, ob eine Unterbrechung in der Info Leiste auftreten soll.</span><span class="sxs-lookup"><span data-stu-id="4538d-116">The value in the **fAutoBreak** member of the [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) structure indicates whether a break should occur in the rebar.</span></span>

<span data-ttu-id="4538d-117">Geben Sie Comctl32.dll Version 6 im Manifest an, um diesen Benachrichtigungs Code zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4538d-117">To use this notification code, specify Comctl32.dll version 6 in the manifest.</span></span> <span data-ttu-id="4538d-118">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4538d-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4538d-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4538d-119">Requirements</span></span>



| <span data-ttu-id="4538d-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4538d-120">Requirement</span></span> | <span data-ttu-id="4538d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="4538d-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4538d-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4538d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4538d-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4538d-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4538d-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4538d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4538d-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4538d-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4538d-126">Header</span><span class="sxs-lookup"><span data-stu-id="4538d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4538d-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="4538d-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





