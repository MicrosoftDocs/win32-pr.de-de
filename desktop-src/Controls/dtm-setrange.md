---
title: DTM_SETRANGE Meldung (kommstrg. h)
description: Legt die minimalen und maximalen zulässigen Systemzeiten für ein DTP-Steuerelement (Datums-und Zeitauswahl) fest. Sie können diese Nachricht explizit senden oder das "DateTime"- \_ Makro verwenden.
ms.assetid: ef0f48f2-906e-4ae0-839d-177e0fb7f14e
keywords:
- Windows-Steuerelemente für DTM_SETRANGE Meldung
topic_type:
- apiref
api_name:
- DTM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70578e7d468c6a0e54d1373af2d46e680afbbe5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742560"
---
# <a name="dtm_setrange-message"></a><span data-ttu-id="57598-105">DTM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="57598-105">DTM\_SETRANGE message</span></span>

<span data-ttu-id="57598-106">Legt die minimalen und maximalen zulässigen Systemzeiten für ein DTP-Steuerelement (Datums-und Zeitauswahl) fest.</span><span class="sxs-lookup"><span data-stu-id="57598-106">Sets the minimum and maximum allowable system times for a date and time picker (DTP) control.</span></span> <span data-ttu-id="57598-107">Sie können diese Nachricht explizit senden oder das " [**DateTime \_**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange) "-Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="57598-107">You can send this message explicitly or use the [**DateTime\_SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="57598-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="57598-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57598-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="57598-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57598-110">Ein-Wert, der angibt, welche Bereichs Werte gültig sind.</span><span class="sxs-lookup"><span data-stu-id="57598-110">A value specifying which range values are valid.</span></span> <span data-ttu-id="57598-111">Dieser Parameter kann eine Kombination der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="57598-111">This parameter can be a combination of the following values:</span></span>



| <span data-ttu-id="57598-112">Wert</span><span class="sxs-lookup"><span data-stu-id="57598-112">Value</span></span>                                                                                                                                          | <span data-ttu-id="57598-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="57598-113">Meaning</span></span>                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <span data-ttu-id="57598-114"><dt>**dstr \_ Min.**</dt></span><span class="sxs-lookup"><span data-stu-id="57598-114"><dt>**GDTR\_MIN**</dt></span></span> </dl> | <span data-ttu-id="57598-115">Das erste Element im [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur Array ist gültig und wird verwendet, um die minimal zulässige Systemzeit festzulegen.</span><span class="sxs-lookup"><span data-stu-id="57598-115">The first element in the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure array is valid and will be used to set the minimum allowable system time.</span></span><br/>  |
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <span data-ttu-id="57598-116"><dt>**maximal zulässige dstr \_**</dt></span><span class="sxs-lookup"><span data-stu-id="57598-116"><dt>**GDTR\_MAX**</dt></span></span> </dl> | <span data-ttu-id="57598-117">Das zweite Element im [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur Array ist gültig und wird verwendet, um die maximal zulässige Systemzeit festzulegen.</span><span class="sxs-lookup"><span data-stu-id="57598-117">The second element in the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure array is valid and will be used to set the maximum allowable system time.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="57598-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="57598-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57598-119">Ein Zeiger auf ein zwei-Element-Array von [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="57598-119">A pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures.</span></span> <span data-ttu-id="57598-120">Das erste Element des **SYSTEMTIME** -Arrays enthält die zulässige Mindestzeit.</span><span class="sxs-lookup"><span data-stu-id="57598-120">The first element of the **SYSTEMTIME** array contains the minimum allowable time.</span></span> <span data-ttu-id="57598-121">Das zweite Element des **SYSTEMTIME** -Arrays enthält die maximal zulässige Zeit.</span><span class="sxs-lookup"><span data-stu-id="57598-121">The second element of the **SYSTEMTIME** array contains the maximum allowable time.</span></span> <span data-ttu-id="57598-122">Es ist nicht erforderlich, ein Array Element auszufüllen, das nicht im *wParam* -Parameter angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="57598-122">It is not necessary to fill an array element that is not specified in the *wParam* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57598-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="57598-123">Return value</span></span>

<span data-ttu-id="57598-124">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="57598-124">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="57598-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="57598-125">Remarks</span></span>

<span data-ttu-id="57598-126">Die Datums-und Uhrzeit Auswahl zeigt nur Datumsangaben/Uhrzeiten an, die innerhalb des angegebenen Bereichs liegen, sodass der Benutzer kein Datum und keine Uhrzeit auswählen kann, die außerhalb des Bereichs liegt.</span><span class="sxs-lookup"><span data-stu-id="57598-126">The date and time picker displays only dates/times that fall within the specified range, preventing the user from selecting a date and time that falls outside the range.</span></span> <span data-ttu-id="57598-127">Wenn die [**DTM- \_ SetSystemTime**](dtm-setsystemtime.md) -Nachricht ein Datum und eine Uhrzeit angibt, die außerhalb des Bereichs liegen, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="57598-127">If the [**DTM\_SETSYSTEMTIME**](dtm-setsystemtime.md) message specifies a date and time that falls outside the range, it will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="57598-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57598-128">Requirements</span></span>



| <span data-ttu-id="57598-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57598-129">Requirement</span></span> | <span data-ttu-id="57598-130">Wert</span><span class="sxs-lookup"><span data-stu-id="57598-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="57598-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="57598-131">Minimum supported client</span></span><br/> | <span data-ttu-id="57598-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57598-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="57598-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="57598-133">Minimum supported server</span></span><br/> | <span data-ttu-id="57598-134">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57598-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="57598-135">Header</span><span class="sxs-lookup"><span data-stu-id="57598-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="57598-136"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="57598-136"><dt>Commctrl.h</dt></span></span> </dl> |



 

