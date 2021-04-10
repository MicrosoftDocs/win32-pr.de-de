---
title: DTM_GETMONTHCAL Meldung (kommstrg. h)
description: Ruft das Handle für das Kalender Steuerelement (DTP) des untergeordneten Monats eines Datums und einer Uhrzeit Auswahl ab. Sie können diese Nachricht explizit senden oder das DateTime- \_ getmonthcal-Makro verwenden.
ms.assetid: 78bbdcc9-2b2b-420b-be9b-6f2f573d60b6
keywords:
- Windows-Steuerelemente für DTM_GETMONTHCAL Meldung
topic_type:
- apiref
api_name:
- DTM_GETMONTHCAL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99609ed3a437990889066da9a3424ef147c3d6b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956831"
---
# <a name="dtm_getmonthcal-message"></a><span data-ttu-id="9a13d-105">DTM \_ getmonthcal-Nachricht</span><span class="sxs-lookup"><span data-stu-id="9a13d-105">DTM\_GETMONTHCAL message</span></span>

<span data-ttu-id="9a13d-106">Ruft das Handle für das Kalender Steuerelement (DTP) des untergeordneten Monats eines Datums und einer Uhrzeit Auswahl ab.</span><span class="sxs-lookup"><span data-stu-id="9a13d-106">Gets the handle to a date and time picker's (DTP) child month calendar control.</span></span> <span data-ttu-id="9a13d-107">Sie können diese Nachricht explizit senden oder das [**DateTime- \_ getmonthcal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="9a13d-107">You can send this message explicitly or use the [**DateTime\_GetMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9a13d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a13d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a13d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9a13d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9a13d-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="9a13d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9a13d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9a13d-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9a13d-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="9a13d-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a13d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a13d-113">Return value</span></span>

<span data-ttu-id="9a13d-114">Gibt das Handle für das Steuerelement des untergeordneten Monats Kalenders des DTP-Steuer Elements zurück, wenn erfolgreich, andernfalls **null** .</span><span class="sxs-lookup"><span data-stu-id="9a13d-114">Returns the handle to a DTP control's child month calendar control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a13d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a13d-115">Remarks</span></span>

<span data-ttu-id="9a13d-116">DTP-Steuerelemente erstellen ein untergeordnetes Monatskalender-Steuerelement, wenn der Benutzer auf den Dropdown Pfeil klickt ([Dtn- \_ Dropdown](dtn-dropdown.md) Benachrichtigung).</span><span class="sxs-lookup"><span data-stu-id="9a13d-116">DTP controls create a child month calendar control when the user clicks the drop-down arrow ([DTN\_DROPDOWN](dtn-dropdown.md) notification).</span></span> <span data-ttu-id="9a13d-117">Wenn der Monatskalender nicht mehr benötigt wird, wird er zerstört (eine [Dtn- \_ closeup](dtn-closeup.md) -Benachrichtigung wird bei der Zerstörung gesendet).</span><span class="sxs-lookup"><span data-stu-id="9a13d-117">When the month calendar is no longer needed, it is destroyed (a [DTN\_CLOSEUP](dtn-closeup.md) notification is sent on destruction).</span></span> <span data-ttu-id="9a13d-118">Daher darf Ihre Anwendung nicht auf ein statisches Handle für den untergeordneten Monatskalender des DTP-Steuer Elements zurückgreifen.</span><span class="sxs-lookup"><span data-stu-id="9a13d-118">So your application must not rely on a static handle to the DTP control's child month calendar.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a13d-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a13d-119">Requirements</span></span>



| <span data-ttu-id="9a13d-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a13d-120">Requirement</span></span> | <span data-ttu-id="9a13d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="9a13d-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9a13d-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9a13d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9a13d-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a13d-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9a13d-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9a13d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9a13d-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a13d-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9a13d-126">Header</span><span class="sxs-lookup"><span data-stu-id="9a13d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a13d-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a13d-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a13d-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a13d-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="9a13d-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="9a13d-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9a13d-130">DTN- \_ Schließung</span><span class="sxs-lookup"><span data-stu-id="9a13d-130">DTN\_CLOSEUP</span></span>](dtn-closeup.md)
</dt> <dt>

[<span data-ttu-id="9a13d-131">DTN- \_ Dropdown</span><span class="sxs-lookup"><span data-stu-id="9a13d-131">DTN\_DROPDOWN</span></span>](dtn-dropdown.md)
</dt> </dl>

 

 





