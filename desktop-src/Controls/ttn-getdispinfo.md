---
title: TTN_GETDISPINFO Benachrichtigungs Code (kommctrl. h)
description: Wird von einem QuickInfo-Steuerelement zum Abrufen der zum Anzeigen eines QuickInfo-Fensters benötigten Informationen gesendet. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: af9ecc27-2004-4c45-9f1d-9ee0b2b50ff6
keywords:
- Windows-Steuerelemente für TTN_GETDISPINFO Benachrichtigungs
topic_type:
- apiref
api_name:
- TTN_GETDISPINFO
- TTN_GETDISPINFOA
- TTN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc1fe07d12331e523fed9e1ff46b9e265487bc31
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859048"
---
# <a name="ttn_getdispinfo-notification-code"></a><span data-ttu-id="83916-105">TTN \_ getdispinfo-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="83916-105">TTN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="83916-106">Wird von einem QuickInfo-Steuerelement zum Abrufen der zum Anzeigen eines QuickInfo-Fensters benötigten Informationen gesendet.</span><span class="sxs-lookup"><span data-stu-id="83916-106">Sent by a tooltip control to retrieve information needed to display a tooltip window.</span></span> <span data-ttu-id="83916-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="83916-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_GETDISPINFO

    lpnmtdi = (LPNMTTDISPINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="83916-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="83916-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83916-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="83916-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83916-110">Ein Zeiger auf eine [**nmttdispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) -Struktur, die das Tool identifiziert, das Text benötigt und die angeforderten Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="83916-110">Pointer to an [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure that identifies the tool that needs text and receives the requested information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83916-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="83916-111">Return value</span></span>

<span data-ttu-id="83916-112">Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="83916-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="83916-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83916-113">Remarks</span></span>

<span data-ttu-id="83916-114">Füllen Sie die entsprechenden Member der Struktur aus, um die angeforderten Informationen an das ToolTip-Steuerelement zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="83916-114">Fill the structure's appropriate members to return the requested information to the tooltip control.</span></span> <span data-ttu-id="83916-115">Wenn Ihr Nachrichten Handler den **uFlags** -Member der [**nmttdispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) -Struktur auf ttf \_ di \_ SetItem festlegt, speichert das QuickInfo-Steuerelement die Informationen und fordert Sie nicht erneut an.</span><span class="sxs-lookup"><span data-stu-id="83916-115">If your message handler sets the **uFlags** member of the [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure to TTF\_DI\_SETITEM, the tooltip control stores the information and will not request it again.</span></span>

## <a name="requirements"></a><span data-ttu-id="83916-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="83916-116">Requirements</span></span>



| <span data-ttu-id="83916-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="83916-117">Requirement</span></span> | <span data-ttu-id="83916-118">Wert</span><span class="sxs-lookup"><span data-stu-id="83916-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83916-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="83916-119">Minimum supported client</span></span><br/> | <span data-ttu-id="83916-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="83916-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="83916-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="83916-121">Minimum supported server</span></span><br/> | <span data-ttu-id="83916-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="83916-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="83916-123">Header</span><span class="sxs-lookup"><span data-stu-id="83916-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="83916-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="83916-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="83916-125">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="83916-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="83916-126">**TTN \_ Getdispinfow** (Unicode) und **TTN \_ getdispinfoa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="83916-126">**TTN\_GETDISPINFOW** (Unicode) and **TTN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



 

 





