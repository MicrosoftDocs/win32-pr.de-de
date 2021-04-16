---
title: LVN_LINKCLICK Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass auf einen Link geklickt wurde. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: de8f40d6-b79e-4324-af67-9a3c0915609d
keywords:
- Windows-Steuerelemente für LVN_LINKCLICK Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_LINKCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd69fb463e71523fcbd4eeb65a6a718d27847c09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479431"
---
# <a name="lvn_linkclick-notification-code"></a><span data-ttu-id="8ff89-105">LVN \_ linkclick-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="8ff89-105">LVN\_LINKCLICK notification code</span></span>

<span data-ttu-id="8ff89-106">Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass auf einen Link geklickt wurde.</span><span class="sxs-lookup"><span data-stu-id="8ff89-106">Notifies a list-view control's parent window that a link has been clicked on.</span></span> <span data-ttu-id="8ff89-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="8ff89-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_LINKCLICK
        
    pLinkInfo = (NMLVLINK*) lParam;         
```



## <a name="parameters"></a><span data-ttu-id="8ff89-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ff89-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ff89-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8ff89-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ff89-110">Zeiger auf eine [**NMLVLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlvlink) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="8ff89-110">Pointer to an [**NMLVLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlvlink) structure.</span></span> <span data-ttu-id="8ff89-111">Der Bezeichner der Gruppe, die den Link enthält, befindet sich im **iSubItem** -Member.</span><span class="sxs-lookup"><span data-stu-id="8ff89-111">The identifier of the group containing the link is in the **iSubItem** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ff89-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8ff89-112">Return value</span></span>

<span data-ttu-id="8ff89-113">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="8ff89-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ff89-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ff89-114">Remarks</span></span>

<span data-ttu-id="8ff89-115">Das folgende Beispiel zeigt, wie eine Anwendung in Ihrem [**WM \_**](wm-notify.md) -Benachrichtigungs Meldungs Handler auf diesen Benachrichtigungs Code reagieren könnte.</span><span class="sxs-lookup"><span data-stu-id="8ff89-115">The following example shows how an application might respond to this notification code in its [**WM\_NOTIFY**](wm-notify.md) message handler.</span></span> <span data-ttu-id="8ff89-116">Im Beispiel wird der reduzierte Status der Gruppe gewechselt und der entsprechende Linktext festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8ff89-116">The example toggles the collapsed state of the group and sets the appropriate link text.</span></span>

``` syntax
case LVN_LINKCLICK:
{
    NMLVLINK* pLinkInfo = (NMLVLINK*)lParam;
    HWND hList = pLinkInfo->hdr.hwndFrom;
    LVGROUP groupInfo;
    groupInfo.cbSize = sizeof(groupInfo);
    groupInfo.mask = LVGF_TASK;
    int groupIndex = pLinkInfo->iSubItem;
    if (ListView_GetGroupState(hList, groupIndex, LVGS_COLLAPSED))
    {
        ListView_SetGroupState(hList, groupIndex, LVGS_COLLAPSED, 0);
        groupInfo.pszTask = L"Hide";
    }
    else
    {
        ListView_SetGroupState(hList, groupIndex, LVGS_COLLAPSED, LVGS_COLLAPSED);
        groupInfo.pszTask = L"Show";
     }
      ListView_SetGroupInfo(hList, groupIndex, &groupInfo);
      break;
}
```

## <a name="requirements"></a><span data-ttu-id="8ff89-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ff89-117">Requirements</span></span>



| <span data-ttu-id="8ff89-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ff89-118">Requirement</span></span> | <span data-ttu-id="8ff89-119">Wert</span><span class="sxs-lookup"><span data-stu-id="8ff89-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8ff89-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8ff89-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8ff89-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8ff89-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8ff89-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8ff89-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8ff89-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8ff89-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8ff89-124">Header</span><span class="sxs-lookup"><span data-stu-id="8ff89-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ff89-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ff89-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





