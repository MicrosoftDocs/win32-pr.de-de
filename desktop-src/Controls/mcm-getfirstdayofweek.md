---
title: MCM_GETFIRSTDAYOFWEEK Meldung (kommstrg. h)
description: Ruft den ersten Tag der Woche für ein Monatskalender-Steuerelement ab. Sie können diese Nachricht explizit oder mit dem monthcal \_ getfirstdayof Week-Makro senden.
ms.assetid: bbbc1c45-5693-4a79-908a-ec6e8ef8b218
keywords:
- Windows-Steuerelemente für MCM_GETFIRSTDAYOFWEEK Meldung
topic_type:
- apiref
api_name:
- MCM_GETFIRSTDAYOFWEEK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b625e470e13c111b0274bfef422963e48c9cc7c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339345"
---
# <a name="mcm_getfirstdayofweek-message"></a><span data-ttu-id="034fa-105">MCM \_ getfirstdayof Week-Meldung</span><span class="sxs-lookup"><span data-stu-id="034fa-105">MCM\_GETFIRSTDAYOFWEEK message</span></span>

<span data-ttu-id="034fa-106">Ruft den ersten Tag der Woche für ein Monatskalender-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="034fa-106">Retrieves the first day of the week for a month calendar control.</span></span> <span data-ttu-id="034fa-107">Sie können diese Nachricht explizit oder mit dem [**monthcal \_ getfirstdayof Week**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getfirstdayofweek) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="034fa-107">You can send this message explicitly or by using the [**MonthCal\_GetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getfirstdayofweek) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="034fa-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="034fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="034fa-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="034fa-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="034fa-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="034fa-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="034fa-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="034fa-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="034fa-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="034fa-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="034fa-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="034fa-113">Return value</span></span>

<span data-ttu-id="034fa-114">Gibt einen **DWORD** -Wert zurück, der zwei Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="034fa-114">Returns a **DWORD** value that contains two values.</span></span> <span data-ttu-id="034fa-115">Das hohe Wort ist ein **boolescher** Wert, der ungleich 0 (null) ist, wenn der erste Tag der Woche auf einen anderen Wert als "locale \_ ifirstdayofweek" festgelegt ist, andernfalls "Null".</span><span class="sxs-lookup"><span data-stu-id="034fa-115">The high word is a **BOOL** value that is nonzero if the first day of the week is set to something other than LOCALE\_IFIRSTDAYOFWEEK, or zero otherwise.</span></span> <span data-ttu-id="034fa-116">Das niedrige Wort ist ein int-Wert, der den ersten Tag der Woche darstellt, wobei 0 für Montag, 1 für Dienstag usw. steht.</span><span class="sxs-lookup"><span data-stu-id="034fa-116">The low word is an INT value that represents the first day of the week, where 0 is Monday, 1 is Tuesday, and so on.</span></span>

## <a name="requirements"></a><span data-ttu-id="034fa-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="034fa-117">Requirements</span></span>



| <span data-ttu-id="034fa-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="034fa-118">Requirement</span></span> | <span data-ttu-id="034fa-119">Wert</span><span class="sxs-lookup"><span data-stu-id="034fa-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="034fa-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="034fa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="034fa-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="034fa-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="034fa-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="034fa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="034fa-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="034fa-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="034fa-124">Header</span><span class="sxs-lookup"><span data-stu-id="034fa-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="034fa-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="034fa-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





