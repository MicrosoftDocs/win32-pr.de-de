---
title: DTM_GETSYSTEMTIME Meldung (kommstrg. h)
description: Ruft den aktuell ausgewählten Zeitpunkt von einem DTP-Steuerelement (Date and Time Picker) ab und platziert ihn in einer angegebenen SYSTEMTIME-Struktur. Sie können diese Nachricht explizit senden oder das DateTime- \_ GetSystemTime-Makro verwenden.
ms.assetid: 81c95187-109c-4b36-98ea-a2e77ce42d9a
keywords:
- Windows-Steuerelemente für DTM_GETSYSTEMTIME Meldung
topic_type:
- apiref
api_name:
- DTM_GETSYSTEMTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e14d8c998720cc987a03877e1918e97304bf769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104841"
---
# <a name="dtm_getsystemtime-message"></a><span data-ttu-id="6bcc4-105">DTM \_ GetSystemTime-Nachricht</span><span class="sxs-lookup"><span data-stu-id="6bcc4-105">DTM\_GETSYSTEMTIME message</span></span>

<span data-ttu-id="6bcc4-106">Ruft den aktuell ausgewählten Zeitpunkt von einem DTP-Steuerelement (Date and Time Picker) ab und platziert ihn in einer angegebenen [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="6bcc4-106">Gets the currently selected time from a date and time picker (DTP) control and places it in a specified [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span> <span data-ttu-id="6bcc4-107">Sie können diese Nachricht explizit senden oder das [**DateTime- \_ GetSystemTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="6bcc4-107">You can send this message explicitly or use the [**DateTime\_GetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6bcc4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6bcc4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bcc4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6bcc4-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6bcc4-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="6bcc4-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6bcc4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6bcc4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6bcc4-112">Ein Zeiger auf eine [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="6bcc4-112">A pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span> <span data-ttu-id="6bcc4-113">Wenn bei **DTM \_ GetSystemTime** GDT \_ gültig zurückgegeben wird, enthält diese Struktur den aktuell ausgewählten Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="6bcc4-113">If **DTM\_GETSYSTEMTIME** returns GDT\_VALID, this structure will contain the currently selected time.</span></span> <span data-ttu-id="6bcc4-114">Andernfalls enthält Sie keine gültigen Informationen.</span><span class="sxs-lookup"><span data-stu-id="6bcc4-114">Otherwise, it will not contain valid information.</span></span> <span data-ttu-id="6bcc4-115">Dieser Parameter muss ein gültiger Zeiger sein. Er darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="6bcc4-115">This parameter must be a valid pointer; it cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bcc4-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6bcc4-116">Return value</span></span>

<span data-ttu-id="6bcc4-117">Gibt GDT \_ gültig zurück, wenn die Zeit Informationen erfolgreich in *LPARAM* platziert wurden.</span><span class="sxs-lookup"><span data-stu-id="6bcc4-117">Returns GDT\_VALID if the time information was successfully placed in *lParam*.</span></span> <span data-ttu-id="6bcc4-118">Gibt GDT \_ None zurück, wenn das Steuerelement auf das [**DTS \_ shownone-Format**](date-and-time-picker-control-styles.md) festgelegt wurde und das Kontrollkästchen für das Steuerelement nicht aktiviert war.</span><span class="sxs-lookup"><span data-stu-id="6bcc4-118">Returns GDT\_NONE if the control was set to the [**DTS\_SHOWNONE**](date-and-time-picker-control-styles.md) style and the control check box was not selected.</span></span> <span data-ttu-id="6bcc4-119">Gibt GDT-Fehler zurück, \_ Wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="6bcc4-119">Returns GDT\_ERROR if an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bcc4-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6bcc4-120">Requirements</span></span>



| <span data-ttu-id="6bcc4-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6bcc4-121">Requirement</span></span> | <span data-ttu-id="6bcc4-122">Wert</span><span class="sxs-lookup"><span data-stu-id="6bcc4-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6bcc4-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6bcc4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6bcc4-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6bcc4-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6bcc4-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6bcc4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6bcc4-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6bcc4-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6bcc4-127">Header</span><span class="sxs-lookup"><span data-stu-id="6bcc4-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bcc4-128"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bcc4-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

