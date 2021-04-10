---
title: TBN_GETDISPINFO Benachrichtigungs Code (kommctrl. h)
description: Ruft Anzeigeinformationen für ein Symbolleisten Element ab. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: ed6e4141-2bf8-4a92-8349-f3833c87fcf3
keywords:
- Windows-Steuerelemente für TBN_GETDISPINFO Benachrichtigungs
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f3a0a47adfe7f172f7a4d0e4c9139b67aef01d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105027"
---
# <a name="tbn_getdispinfo-notification-code"></a><span data-ttu-id="e20d7-105">TBN- \_ getdispinfo-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="e20d7-105">TBN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="e20d7-106">Ruft Anzeigeinformationen für ein Symbolleisten Element ab.</span><span class="sxs-lookup"><span data-stu-id="e20d7-106">Retrieves display information for a toolbar item.</span></span> <span data-ttu-id="e20d7-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="e20d7-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_GETDISPINFO 

    lptbdi = (LPNMTBDISPINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e20d7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e20d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e20d7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e20d7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e20d7-110">Zeiger auf eine [**nmtbdispinfo**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbdispinfoa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e20d7-110">Pointer to an [**NMTBDISPINFO**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbdispinfoa) structure.</span></span> <span data-ttu-id="e20d7-111">Der **idcommand** -Member gibt den Befehls Bezeichner des Elements an, das **LPARAM** -Element enthält die Anwendungs definierten Daten des Elements, und der **dwMask** -Member gibt an, welche Informationen angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="e20d7-111">The **idCommand** member specifies the item's command identifier, the **lParam** member contains the item's application-defined data, and the **dwMask** member specifies what information is being requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e20d7-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e20d7-112">Return value</span></span>

<span data-ttu-id="e20d7-113">Der Rückgabewert wird vom-Steuerelement ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e20d7-113">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="e20d7-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e20d7-114">Requirements</span></span>



| <span data-ttu-id="e20d7-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e20d7-115">Requirement</span></span> | <span data-ttu-id="e20d7-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e20d7-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e20d7-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e20d7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e20d7-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e20d7-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e20d7-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e20d7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e20d7-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e20d7-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e20d7-121">Header</span><span class="sxs-lookup"><span data-stu-id="e20d7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e20d7-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e20d7-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="e20d7-123">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="e20d7-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e20d7-124">**TBN \_ Getdispinfow** (Unicode) und **TBN \_ getdispinfoa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e20d7-124">**TBN\_GETDISPINFOW** (Unicode) and **TBN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



 

 





