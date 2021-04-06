---
title: HDN_TRACK Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass der Benutzer einen unter Teiler im Header Steuerelement zieht. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 26660ae1-0d6e-4ee7-8b6a-d621abef352d
keywords:
- Windows-Steuerelemente für HDN_TRACK Benachrichtigungs
topic_type:
- apiref
api_name:
- HDN_TRACK
- HDN_TRACKA
- HDN_TRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91b55ac23e2de17788b17c1f121530308de9e7a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859053"
---
# <a name="hdn_track-notification-code"></a><span data-ttu-id="fe236-105">Benachrichtigungs Code für Hdn- \_ Track</span><span class="sxs-lookup"><span data-stu-id="fe236-105">HDN\_TRACK notification code</span></span>

<span data-ttu-id="fe236-106">Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass der Benutzer einen unter Teiler im Header Steuerelement zieht.</span><span class="sxs-lookup"><span data-stu-id="fe236-106">Notifies a header control's parent window that the user is dragging a divider in the header control.</span></span> <span data-ttu-id="fe236-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="fe236-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_TRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="fe236-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe236-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe236-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe236-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe236-110">Ein Zeiger auf eine [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur, die Informationen über das Header Steuerelement und das Element enthält, dessen Trennzeichen gezogen werden.</span><span class="sxs-lookup"><span data-stu-id="fe236-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the item whose divider is being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe236-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe236-111">Return value</span></span>

<span data-ttu-id="fe236-112">Gibt **false** zurück, um die Nachverfolgung des unter Teilers fortzusetzen, oder **true** zum Beenden der Nachverfolgung</span><span class="sxs-lookup"><span data-stu-id="fe236-112">Returns **FALSE** to continue tracking the divider, or **TRUE** to end tracking.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe236-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe236-113">Requirements</span></span>



| <span data-ttu-id="fe236-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe236-114">Requirement</span></span> | <span data-ttu-id="fe236-115">Wert</span><span class="sxs-lookup"><span data-stu-id="fe236-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe236-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe236-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fe236-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe236-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fe236-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe236-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fe236-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe236-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe236-120">Header</span><span class="sxs-lookup"><span data-stu-id="fe236-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe236-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe236-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="fe236-122">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="fe236-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fe236-123">**Hdn \_ Trackw** (Unicode) und **Hdn \_ tracka** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fe236-123">**HDN\_TRACKW** (Unicode) and **HDN\_TRACKA** (ANSI)</span></span><br/>                       |



 

 





