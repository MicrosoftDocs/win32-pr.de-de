---
title: CBEN_INSERTITEM Benachrichtigungs Code (kommctrl. h)
description: Wird gesendet, wenn ein neues Element in das Steuerelement eingefügt wurde. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: caf60156-10d2-4cfb-91c4-def6ee99c471
keywords:
- Windows-Steuerelemente für CBEN_INSERTITEM Benachrichtigungs
topic_type:
- apiref
api_name:
- CBEN_INSERTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63ccd05ea75015479ef32415d920bbe639664ac2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743817"
---
# <a name="cben_insertitem-notification-code"></a><span data-ttu-id="7d10c-105">Cben \_ InsertItem-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="7d10c-105">CBEN\_INSERTITEM notification code</span></span>

<span data-ttu-id="7d10c-106">Wird gesendet, wenn ein neues Element in das Steuerelement eingefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="7d10c-106">Sent when a new item has been inserted in the control.</span></span> <span data-ttu-id="7d10c-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="7d10c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_INSERTITEM

    pNMInfo = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7d10c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d10c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d10c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7d10c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d10c-110">Ein Zeiger auf eine [**nmcomboboxex**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) -Struktur, die Informationen über den Benachrichtigungs Code und das eingefügte Element enthält.</span><span class="sxs-lookup"><span data-stu-id="7d10c-110">A pointer to an [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) structure containing information about the notification code and the item that was inserted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d10c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7d10c-111">Return value</span></span>

<span data-ttu-id="7d10c-112">Die Anwendung, die diesen Benachrichtigungs Code verarbeitet, muss NULL zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="7d10c-112">The application processing this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d10c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d10c-113">Requirements</span></span>



| <span data-ttu-id="7d10c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d10c-114">Requirement</span></span> | <span data-ttu-id="7d10c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7d10c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d10c-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7d10c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7d10c-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d10c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7d10c-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7d10c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7d10c-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d10c-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7d10c-120">Header</span><span class="sxs-lookup"><span data-stu-id="7d10c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d10c-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d10c-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





