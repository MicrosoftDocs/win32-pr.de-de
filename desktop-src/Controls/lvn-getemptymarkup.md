---
title: LVN_GETEMPTYMARKUP Benachrichtigungs Code (kommctrl. h)
description: Wird vom Listenansicht-Steuerelement an das übergeordnete Fenster gesendet, wenn das Steuerelement keine Elemente aufweist. Der LVN \_ getemptymarkup-Benachrichtigungs Code ist eine Anforderung für das übergeordnete Fenster, einen Markup Text bereitzustellen. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 5ea74120-f347-493a-af14-6bda5b8f6082
keywords:
- Windows-Steuerelemente für LVN_GETEMPTYMARKUP Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_GETEMPTYMARKUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea693475ca42f962be07936f980cd3f5d52479c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859346"
---
# <a name="lvn_getemptymarkup-notification-code"></a><span data-ttu-id="852e4-106">LVN \_ getemptymarkup-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="852e4-106">LVN\_GETEMPTYMARKUP notification code</span></span>

<span data-ttu-id="852e4-107">Wird vom Listenansicht-Steuerelement an das übergeordnete Fenster gesendet, wenn das Steuerelement keine Elemente aufweist.</span><span class="sxs-lookup"><span data-stu-id="852e4-107">Sent by list-view control to its parent window when the control has no items.</span></span> <span data-ttu-id="852e4-108">Der LVN \_ getemptymarkup-Benachrichtigungs Code ist eine Anforderung für das übergeordnete Fenster, einen Markup Text bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="852e4-108">The LVN\_GETEMPTYMARKUP notification code is a request for the parent window to provide markup text.</span></span> <span data-ttu-id="852e4-109">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="852e4-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_GETEMPTYMARKUP
        
    pnmMarkup = (NMLVEMPTYMARKUP*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="852e4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="852e4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="852e4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="852e4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="852e4-112">Zeiger auf eine [**nmlvemptymarkup**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="852e4-112">Pointer to a [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) structure.</span></span> <span data-ttu-id="852e4-113">Legen Sie die Elemente dieser Struktur so fest, dass Sie Markup Text für das Listenansicht-Steuerelement bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="852e4-113">Set the members of this structure to provide markup text for the list-view control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="852e4-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="852e4-114">Return value</span></span>

<span data-ttu-id="852e4-115">Gibt " **true** " zurück, um den Markup Text im Listenansicht-Steuerelement festzulegen, andernfalls " **false** ".</span><span class="sxs-lookup"><span data-stu-id="852e4-115">Return **TRUE** to set the markup text in the list-view control, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="852e4-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="852e4-116">Remarks</span></span>

<span data-ttu-id="852e4-117">Der Benachrichtigungs Empfänger wandelt *LPARAM* ein, um die [**nmlvemptymarkup**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) -Struktur abzurufen.</span><span class="sxs-lookup"><span data-stu-id="852e4-117">The notification receiver casts *lParam* to retrieve the [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) structure.</span></span> <span data-ttu-id="852e4-118">Der *wParam* -Parameter enthält die ID des Steuer Elements, das diese Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="852e4-118">The *wParam* parameter contains the ID of the control that sends this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="852e4-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="852e4-119">Requirements</span></span>



| <span data-ttu-id="852e4-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="852e4-120">Requirement</span></span> | <span data-ttu-id="852e4-121">Wert</span><span class="sxs-lookup"><span data-stu-id="852e4-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="852e4-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="852e4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="852e4-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="852e4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="852e4-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="852e4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="852e4-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="852e4-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="852e4-126">Header</span><span class="sxs-lookup"><span data-stu-id="852e4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="852e4-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="852e4-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





