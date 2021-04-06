---
title: DTN_DATETIMECHANGE Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Steuerelement für die Datums-und Zeitauswahl (DTP) gesendet, wenn eine Änderung auftritt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 65cdd8fb-1f07-4447-b503-d40fdfa37202
keywords:
- Windows-Steuerelemente für DTN_DATETIMECHANGE Benachrichtigungs
topic_type:
- apiref
api_name:
- DTN_DATETIMECHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a40072a54732a0a3575e3153ddb901ca1df291b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859077"
---
# <a name="dtn_datetimechange-notification-code"></a><span data-ttu-id="543b8-105">DTN \_ datetimechange-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="543b8-105">DTN\_DATETIMECHANGE notification code</span></span>

<span data-ttu-id="543b8-106">Wird von einem Steuerelement für die Datums-und Zeitauswahl (DTP) gesendet, wenn eine Änderung auftritt.</span><span class="sxs-lookup"><span data-stu-id="543b8-106">Sent by a date and time picker (DTP) control whenever a change occurs.</span></span> <span data-ttu-id="543b8-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="543b8-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_DATETIMECHANGE

    lpChange = (LPNMDATETIMECHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="543b8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="543b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="543b8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="543b8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="543b8-110">Ein Zeiger auf eine [**nmdatetimechange**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange) -Struktur, die Informationen über die Änderung enthält, die im Steuerelement stattfindet.</span><span class="sxs-lookup"><span data-stu-id="543b8-110">A pointer to an [**NMDATETIMECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange) structure containing information about the change that took place in the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="543b8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="543b8-111">Return value</span></span>

<span data-ttu-id="543b8-112">Der Besitzer des Steuer Elements muss 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="543b8-112">The owner of the control must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="543b8-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="543b8-113">Requirements</span></span>



| <span data-ttu-id="543b8-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="543b8-114">Requirement</span></span> | <span data-ttu-id="543b8-115">Wert</span><span class="sxs-lookup"><span data-stu-id="543b8-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="543b8-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="543b8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="543b8-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="543b8-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="543b8-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="543b8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="543b8-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="543b8-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="543b8-120">Header</span><span class="sxs-lookup"><span data-stu-id="543b8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="543b8-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="543b8-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





