---
title: NM_TOOLTIPSCREATED (Symbolleisten-) Benachrichtigungs Code (kommstrg. h)
description: Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass die Symbolleiste ein QuickInfo-Steuerelement erstellt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 0e9517c1-aa3f-4b14-82b4-195a4ce99757
keywords:
- NM_TOOLTIPSCREATED (Symbolleiste) Benachrichtigungs Code Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_TOOLTIPSCREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c13366348da075fab48e7a2f12381f51f7d87bf4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476062"
---
# <a name="nm_tooltipscreated-toolbar-notification-code"></a><span data-ttu-id="08683-105">NM- \_ tooltipscreated-Benachrichtigungs Code (Symbolleiste)</span><span class="sxs-lookup"><span data-stu-id="08683-105">NM\_TOOLTIPSCREATED (toolbar) notification code</span></span>

<span data-ttu-id="08683-106">Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass die Symbolleiste ein QuickInfo-Steuerelement erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="08683-106">Notifies a toolbar's parent window that the toolbar has created a tooltip control.</span></span> <span data-ttu-id="08683-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="08683-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_TOOLTIPSCREATED

    lpnmttc = (LPNMTOOLTIPSCREATED) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="08683-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="08683-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08683-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="08683-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08683-110">Zeiger auf eine [**nmtooltipscreated**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="08683-110">Pointer to an [**NMTOOLTIPSCREATED**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08683-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="08683-111">Return value</span></span>

<span data-ttu-id="08683-112">Das Symbolleisten-Steuerelement ignoriert den Rückgabewert aus diesem Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="08683-112">The toolbar control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="08683-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08683-113">Requirements</span></span>



| <span data-ttu-id="08683-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08683-114">Requirement</span></span> | <span data-ttu-id="08683-115">Wert</span><span class="sxs-lookup"><span data-stu-id="08683-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="08683-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="08683-116">Minimum supported client</span></span><br/> | <span data-ttu-id="08683-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08683-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="08683-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="08683-118">Minimum supported server</span></span><br/> | <span data-ttu-id="08683-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08683-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="08683-120">Header</span><span class="sxs-lookup"><span data-stu-id="08683-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="08683-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="08683-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





