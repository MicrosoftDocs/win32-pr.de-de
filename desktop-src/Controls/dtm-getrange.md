---
title: DTM_GETRANGE Meldung (kommstrg. h)
description: Ruft die aktuellen minimal-und maximal zulässigen Systemzeiten für ein DTP-Steuerelement (Datums-und Zeitauswahl) ab. Sie können diese Nachricht explizit senden oder das DateTime- \_ GetRange-Makro verwenden.
ms.assetid: 190cada6-49ee-483f-a464-d3d789127159
keywords:
- Windows-Steuerelemente für DTM_GETRANGE Meldung
topic_type:
- apiref
api_name:
- DTM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a50a2ae9fe4ca77198f9e63548f709e0f571fdb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477934"
---
# <a name="dtm_getrange-message"></a><span data-ttu-id="ab171-105">DTM- \_ GetRange-Nachricht</span><span class="sxs-lookup"><span data-stu-id="ab171-105">DTM\_GETRANGE message</span></span>

<span data-ttu-id="ab171-106">Ruft die aktuellen minimal-und maximal zulässigen Systemzeiten für ein DTP-Steuerelement (Datums-und Zeitauswahl) ab.</span><span class="sxs-lookup"><span data-stu-id="ab171-106">Gets the current minimum and maximum allowable system times for a date and time picker (DTP) control.</span></span> <span data-ttu-id="ab171-107">Sie können diese Nachricht explizit senden oder das [**DateTime- \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="ab171-107">You can send this message explicitly or use the [**DateTime\_GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ab171-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab171-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab171-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ab171-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ab171-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="ab171-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ab171-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ab171-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ab171-112">Ein Zeiger auf ein zwei-Element-Array von [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="ab171-112">A pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab171-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab171-113">Return value</span></span>

<span data-ttu-id="ab171-114">Gibt einen **DWORD** -Wert zurück, der eine Kombination aus dstr \_ Min oder dstr \_ Max ist.</span><span class="sxs-lookup"><span data-stu-id="ab171-114">Returns a **DWORD** value that is a combination of GDTR\_MIN or GDTR\_MAX.</span></span> <span data-ttu-id="ab171-115">Das erste Element des [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Arrays enthält die zulässige Mindestzeit, wenn dstr \_ Min festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ab171-115">The first element of the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) array contains the minimum allowable time if GDTR\_MIN is set.</span></span> <span data-ttu-id="ab171-116">Das zweite Element des **SYSTEMTIME** -Arrays enthält die maximal zulässige Zeit, wenn dstr \_ Max festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ab171-116">The second element of the **SYSTEMTIME** array contains the maximum allowable time if GDTR\_MAX is set.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab171-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab171-117">Remarks</span></span>

<span data-ttu-id="ab171-118">Die Datums-und Uhrzeit Auswahl zeigt nur Datumsangaben/Uhrzeiten an, die innerhalb des angegebenen Bereichs liegen, sodass der Benutzer kein Datum und keine Uhrzeit auswählen kann, die außerhalb des Bereichs liegt.</span><span class="sxs-lookup"><span data-stu-id="ab171-118">The date and time picker displays only dates/times that fall within the specified range, preventing the user from selecting a date and time that falls outside the range.</span></span> <span data-ttu-id="ab171-119">Wenn die [**DTM- \_ SetSystemTime**](dtm-setsystemtime.md) -Nachricht ein Datum und eine Uhrzeit angibt, die außerhalb des Bereichs liegen, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="ab171-119">If the [**DTM\_SETSYSTEMTIME**](dtm-setsystemtime.md) message specifies a date and time that falls outside the range, it will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab171-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab171-120">Requirements</span></span>



| <span data-ttu-id="ab171-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab171-121">Requirement</span></span> | <span data-ttu-id="ab171-122">Wert</span><span class="sxs-lookup"><span data-stu-id="ab171-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ab171-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ab171-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ab171-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ab171-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ab171-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ab171-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ab171-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ab171-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ab171-127">Header</span><span class="sxs-lookup"><span data-stu-id="ab171-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab171-128"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab171-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

