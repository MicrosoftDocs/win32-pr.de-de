---
title: NM_GETCUSTOMSPLITRECT Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Schaltflächen-Steuerelement an das übergeordnete Steuerelement gesendet, um Messungen für die beiden Rechtecke der unterteilten Schaltfläche Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: ce72778d-3cca-46a4-9d05-40954a18681d
keywords:
- Windows-Steuerelemente für NM_GETCUSTOMSPLITRECT Benachrichtigungs
topic_type:
- apiref
api_name:
- NM_GETCUSTOMSPLITRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97b839540da7e07069fdf56ed656ed8772d029eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102879"
---
# <a name="nm_getcustomsplitrect-notification-code"></a><span data-ttu-id="55d24-105">NM \_ getcustomsplitrect-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="55d24-105">NM\_GETCUSTOMSPLITRECT notification code</span></span>

<span data-ttu-id="55d24-106">Wird von einem Schaltflächen-Steuerelement an das übergeordnete Steuerelement gesendet, um Messungen für die beiden Rechtecke der unterteilten Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="55d24-106">Sent by a button control to its parent to get measurements for the two rectangles of the split button.</span></span> <span data-ttu-id="55d24-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="55d24-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_GETCUSTOMSPLITRECT
        
    nmCustomSplit = (NMCUSTOMSPLITRECTINFO *) lParam;
```



## <a name="parameters"></a><span data-ttu-id="55d24-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="55d24-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55d24-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="55d24-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="55d24-110">Ein Zeiger auf eine [**nmcustomsplitrectinfo**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) , um umschließende Rechtecke-Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="55d24-110">A pointer to an [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) to receive bounding rectangles information.</span></span> <span data-ttu-id="55d24-111">Die **nmcustomsplitrectinfo** -Struktur wird mit dem Benachrichtigungs Code als Anforderung gesendet, dass das übergeordnete Element Messungen für die Rechtecke der unterteilten Schaltfläche bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="55d24-111">The **NMCUSTOMSPLITRECTINFO** structure is sent with the notification code as a request for the parent to provide measurements for the rectangles of the split button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55d24-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="55d24-112">Return value</span></span>

<span data-ttu-id="55d24-113">Gibt [**cdrf \_ skipdefault**](cdrf-constants.md) zurück, um das Schaltflächen-Steuerelement anzuweisen, die in der [**nmcustomsplitrectinfo**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) -Struktur zurückgegebenen Werte zu verwenden; andernfalls wird [**cdrf \_ DODEFAULT**](cdrf-constants.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="55d24-113">Return [**CDRF\_SKIPDEFAULT**](cdrf-constants.md) to tell the button control to use the values returned in the [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) structure; otherwise, return [**CDRF\_DODEFAULT**](cdrf-constants.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="55d24-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55d24-114">Remarks</span></span>

<span data-ttu-id="55d24-115">Dieser Benachrichtigungs Code wird von einem Schaltflächen-Steuerelement gesendet, bevor es gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="55d24-115">This notification code is sent by a button control before it is drawn.</span></span> <span data-ttu-id="55d24-116">Die Schaltfläche muss im Format " [**SB \_ SplitButton**](button-styles.md) " oder " [**SB \_ defsplitbutton**](button-styles.md)" lauten.</span><span class="sxs-lookup"><span data-stu-id="55d24-116">The button must be of style [**BS\_SPLITBUTTON**](button-styles.md) or [**BS\_DEFSPLITBUTTON**](button-styles.md).</span></span> <span data-ttu-id="55d24-117">Wenn die an das Steuerelement in *LPARAM* zurückgegebenen Rechtecke nicht gültig sind, werden Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="55d24-117">If the rectangles returned to the control in *lParam* are not valid, they are ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="55d24-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55d24-118">Requirements</span></span>



| <span data-ttu-id="55d24-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55d24-119">Requirement</span></span> | <span data-ttu-id="55d24-120">Wert</span><span class="sxs-lookup"><span data-stu-id="55d24-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="55d24-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="55d24-121">Minimum supported client</span></span><br/> | <span data-ttu-id="55d24-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55d24-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="55d24-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="55d24-123">Minimum supported server</span></span><br/> | <span data-ttu-id="55d24-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55d24-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="55d24-125">Header</span><span class="sxs-lookup"><span data-stu-id="55d24-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="55d24-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="55d24-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





