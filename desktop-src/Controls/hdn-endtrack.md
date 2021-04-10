---
title: HDN_ENDTRACK Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass der Benutzer das Ziehen eines unter Teilers abgeschlossen hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: d9b25871-7bd6-439c-91b8-e8249d9be67d
keywords:
- Windows-Steuerelemente für HDN_ENDTRACK Benachrichtigungs
topic_type:
- apiref
api_name:
- HDN_ENDTRACK
- HDN_ENDTRACKA
- HDN_ENDTRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42ab7625690a2de0414f1da391f26f919c1c2617
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040182"
---
# <a name="hdn_endtrack-notification-code"></a><span data-ttu-id="59226-105">Hdn- \_ EndTrack-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="59226-105">HDN\_ENDTRACK notification code</span></span>

<span data-ttu-id="59226-106">Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass der Benutzer das Ziehen eines unter Teilers abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="59226-106">Notifies a header control's parent window that the user has finished dragging a divider.</span></span> <span data-ttu-id="59226-107">Dieser Benachrichtigungs Code wird in Form einer [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="59226-107">This notification code sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ENDTRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="59226-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="59226-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59226-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="59226-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59226-110">Ein Zeiger auf eine [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur, die Informationen über das Header Steuerelement und das Element enthält, dessen Trennzeichen gezogen wurde.</span><span class="sxs-lookup"><span data-stu-id="59226-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the item whose divider was dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59226-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59226-111">Return value</span></span>

<span data-ttu-id="59226-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="59226-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="59226-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59226-113">Requirements</span></span>



| <span data-ttu-id="59226-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59226-114">Requirement</span></span> | <span data-ttu-id="59226-115">Wert</span><span class="sxs-lookup"><span data-stu-id="59226-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="59226-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="59226-116">Minimum supported client</span></span><br/> | <span data-ttu-id="59226-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="59226-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="59226-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="59226-118">Minimum supported server</span></span><br/> | <span data-ttu-id="59226-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="59226-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="59226-120">Header</span><span class="sxs-lookup"><span data-stu-id="59226-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="59226-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="59226-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="59226-122">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="59226-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="59226-123">**Hdn \_ Endtrackw** (Unicode) und **Hdn \_ endtracka** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="59226-123">**HDN\_ENDTRACKW** (Unicode) and **HDN\_ENDTRACKA** (ANSI)</span></span><br/>                 |



 

 





