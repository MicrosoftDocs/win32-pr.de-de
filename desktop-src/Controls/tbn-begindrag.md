---
title: TBN_BEGINDRAG Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass der Benutzer mit dem Ziehen einer Schaltfläche auf einer Symbolleiste begonnen hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 244406e5-e13d-4c80-81fa-81b018b29ec1
keywords:
- Windows-Steuerelemente für TBN_BEGINDRAG Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72cfa7325d1a8e1eab27383d7df918c8896933bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103218"
---
# <a name="tbn_begindrag-notification-code"></a><span data-ttu-id="61547-105">TBN- \_ BeginDrag-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="61547-105">TBN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="61547-106">Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass der Benutzer mit dem Ziehen einer Schaltfläche auf einer Symbolleiste begonnen hat.</span><span class="sxs-lookup"><span data-stu-id="61547-106">Notifies a toolbar's parent window that the user has begun dragging a button in a toolbar.</span></span> <span data-ttu-id="61547-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="61547-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_BEGINDRAG 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="61547-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="61547-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61547-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="61547-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="61547-110">Zeiger auf eine [**nmtoolbar**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="61547-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="61547-111">Der **iItem** -Member enthält den Befehls Bezeichner der gezogenen Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="61547-111">The **iItem** member contains the command identifier of the button being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61547-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="61547-112">Return value</span></span>

<span data-ttu-id="61547-113">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="61547-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="61547-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61547-114">Requirements</span></span>



| <span data-ttu-id="61547-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61547-115">Requirement</span></span> | <span data-ttu-id="61547-116">Wert</span><span class="sxs-lookup"><span data-stu-id="61547-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61547-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="61547-117">Minimum supported client</span></span><br/> | <span data-ttu-id="61547-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61547-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="61547-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="61547-119">Minimum supported server</span></span><br/> | <span data-ttu-id="61547-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61547-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61547-121">Header</span><span class="sxs-lookup"><span data-stu-id="61547-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="61547-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="61547-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





