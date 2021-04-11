---
title: TTN_NEEDTEXT Benachrichtigungs Code (kommctrl. h)
description: Wird von einem QuickInfo-Steuerelement zum Abrufen der zum Anzeigen eines QuickInfo-Fensters benötigten Informationen gesendet. Dieser Benachrichtigungs Code ist identisch mit TTN \_ getdispinfo. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 5fd82096-cfad-4b58-aa88-101d73116ec9
keywords:
- Windows-Steuerelemente für TTN_NEEDTEXT Benachrichtigungs
topic_type:
- apiref
api_name:
- TTN_NEEDTEXT
- TTN_NEEDTEXTA
- TTN_NEEDTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31b498f48534d7f6b270027bc1279244c67e26ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104426"
---
# <a name="ttn_needtext-notification-code"></a><span data-ttu-id="8c7e7-106">TTN- \_ needtext-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="8c7e7-106">TTN\_NEEDTEXT notification code</span></span>

<span data-ttu-id="8c7e7-107">Wird von einem QuickInfo-Steuerelement zum Abrufen der zum Anzeigen eines QuickInfo-Fensters benötigten Informationen gesendet.</span><span class="sxs-lookup"><span data-stu-id="8c7e7-107">Sent by a tooltip control to retrieve information needed to display a tooltip window.</span></span> <span data-ttu-id="8c7e7-108">Dieser Benachrichtigungs Code ist identisch mit [TTN \_ getdispinfo](ttn-getdispinfo.md).</span><span class="sxs-lookup"><span data-stu-id="8c7e7-108">This notification code is identical to [TTN\_GETDISPINFO](ttn-getdispinfo.md).</span></span> <span data-ttu-id="8c7e7-109">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="8c7e7-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_NEEDTEXT

    lpnmtdi = (LPNMTTDISPINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="8c7e7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c7e7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c7e7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c7e7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c7e7-112">Ein Zeiger auf eine [**nmttdispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) -Struktur, die das Tool identifiziert, das Text benötigt und die angeforderten Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="8c7e7-112">Pointer to an [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure that identifies the tool that needs text and receives the requested information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c7e7-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c7e7-113">Return value</span></span>

<span data-ttu-id="8c7e7-114">Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8c7e7-114">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c7e7-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c7e7-115">Remarks</span></span>

<span data-ttu-id="8c7e7-116">Füllen Sie die entsprechenden Member der Struktur aus, um die angeforderten Informationen an das ToolTip-Steuerelement zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="8c7e7-116">Fill the structure's appropriate members to return the requested information to the tooltip control.</span></span> <span data-ttu-id="8c7e7-117">Wenn Ihr Nachrichten Handler den **uFlags** -Member der [**nmttdispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) -Struktur auf ttf \_ di \_ SetItem festlegt, speichert das QuickInfo-Steuerelement die Informationen und fordert Sie nicht erneut an.</span><span class="sxs-lookup"><span data-stu-id="8c7e7-117">If your message handler sets the **uFlags** member of the [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure to TTF\_DI\_SETITEM, the tooltip control stores the information and will not request it again.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c7e7-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c7e7-118">Requirements</span></span>



| <span data-ttu-id="8c7e7-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c7e7-119">Requirement</span></span> | <span data-ttu-id="8c7e7-120">Wert</span><span class="sxs-lookup"><span data-stu-id="8c7e7-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c7e7-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8c7e7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8c7e7-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c7e7-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8c7e7-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8c7e7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8c7e7-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c7e7-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8c7e7-125">Header</span><span class="sxs-lookup"><span data-stu-id="8c7e7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c7e7-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c7e7-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="8c7e7-127">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="8c7e7-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8c7e7-128">**TTN \_ Needtextw** (Unicode) und **TTN \_ needtexta** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8c7e7-128">**TTN\_NEEDTEXTW** (Unicode) and **TTN\_NEEDTEXTA** (ANSI)</span></span><br/>                 |



 

 





