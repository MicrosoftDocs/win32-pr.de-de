---
title: HDN_BEGINTRACK Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass der Benutzer mit dem Ziehen eines unter Teilers im-Steuerelement begonnen hat (d. h., der Benutzer hat mit der linken Maustaste gedrückt, während sich der Mauszeiger auf einem unter Teiler im Header Steuerelement befindet).
ms.assetid: 363b14bc-2b7e-4c37-9caf-7671fcc3cfa5
keywords:
- Windows-Steuerelemente für HDN_BEGINTRACK Benachrichtigungs
topic_type:
- apiref
api_name:
- HDN_BEGINTRACK
- HDN_BEGINTRACKA
- HDN_BEGINTRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6da4ae2c360b13077a612b92ab19a739a58a07e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106683"
---
# <a name="hdn_begintrack-notification-code"></a><span data-ttu-id="b6954-104">Hdn \_ BeginTrack-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="b6954-104">HDN\_BEGINTRACK notification code</span></span>

<span data-ttu-id="b6954-105">Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass der Benutzer mit dem Ziehen eines unter Teilers im-Steuerelement begonnen hat (d. h., der Benutzer hat mit der linken Maustaste gedrückt, während sich der Mauszeiger auf einem unter Teiler im Header Steuerelement befindet).</span><span class="sxs-lookup"><span data-stu-id="b6954-105">Notifies a header control's parent window that the user has begun dragging a divider in the control (that is, the user has pressed the left mouse button while the mouse cursor is on a divider in the header control).</span></span> <span data-ttu-id="b6954-106">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="b6954-106">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_BEGINTRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="b6954-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6954-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6954-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6954-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6954-109">Ein Zeiger auf eine [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur, die Informationen über das Header Steuerelement und das Element enthält, dessen Trennzeichen gezogen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b6954-109">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the item whose divider is to be dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6954-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b6954-110">Return value</span></span>

<span data-ttu-id="b6954-111">Gibt **false** zurück, um die Nachverfolgung des unter Teilers zuzulassen, oder **true** , um die Überwachung zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="b6954-111">Returns **FALSE** to allow tracking of the divider, or **TRUE** to prevent tracking.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6954-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6954-112">Requirements</span></span>



| <span data-ttu-id="b6954-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6954-113">Requirement</span></span> | <span data-ttu-id="b6954-114">Wert</span><span class="sxs-lookup"><span data-stu-id="b6954-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6954-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b6954-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b6954-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6954-116">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b6954-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b6954-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b6954-118">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6954-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b6954-119">Header</span><span class="sxs-lookup"><span data-stu-id="b6954-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6954-120"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6954-120"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="b6954-121">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="b6954-121">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b6954-122">**Hdn \_ Begintrackw** (Unicode) und **Hdn \_ begintracka** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b6954-122">**HDN\_BEGINTRACKW** (Unicode) and **HDN\_BEGINTRACKA** (ANSI)</span></span><br/>             |



 

 





