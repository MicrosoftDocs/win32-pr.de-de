---
title: DTM_SETSYSTEMTIME Meldung (kommstrg. h)
description: Legt die Zeit in einem DTP-Steuerelement (Datums-und Zeitauswahl) fest. Sie können diese Nachricht explizit senden oder das DateTime- \_ SetSystemTime-Makro verwenden.
ms.assetid: aab023ac-22ef-485b-be2f-2aa76dfcf57f
keywords:
- Windows-Steuerelemente für DTM_SETSYSTEMTIME Meldung
topic_type:
- apiref
api_name:
- DTM_SETSYSTEMTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b2a3c625ad4ff02bed138a8086ca0da984de35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956940"
---
# <a name="dtm_setsystemtime-message"></a><span data-ttu-id="e12a4-105">DTM- \_ SetSystemTime-Nachricht</span><span class="sxs-lookup"><span data-stu-id="e12a4-105">DTM\_SETSYSTEMTIME message</span></span>

<span data-ttu-id="e12a4-106">Legt die Zeit in einem DTP-Steuerelement (Datums-und Zeitauswahl) fest.</span><span class="sxs-lookup"><span data-stu-id="e12a4-106">Sets the time in a date and time picker (DTP) control.</span></span> <span data-ttu-id="e12a4-107">Sie können diese Nachricht explizit senden oder das [**DateTime- \_ SetSystemTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="e12a4-107">You can send this message explicitly or use the [**DateTime\_SetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e12a4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e12a4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e12a4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e12a4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e12a4-110">Ein-Wert, der die Aktion angibt, die ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e12a4-110">A value specifying the action that should be performed.</span></span> <span data-ttu-id="e12a4-111">Dieser Wert muss auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="e12a4-111">This value must be set to one of the following:</span></span>



| <span data-ttu-id="e12a4-112">Wert</span><span class="sxs-lookup"><span data-stu-id="e12a4-112">Value</span></span>                                                                                                                                             | <span data-ttu-id="e12a4-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e12a4-113">Meaning</span></span>                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDT_VALID"></span><span id="gdt_valid"></span><dl> <span data-ttu-id="e12a4-114"><dt>**GDT \_ gültig**</dt></span><span class="sxs-lookup"><span data-stu-id="e12a4-114"><dt>**GDT\_VALID**</dt></span></span> </dl> | <span data-ttu-id="e12a4-115">Legen Sie das DTP-Steuerelement gemäß den Daten in der Struktur fest, auf die *LPARAM* zeigt.</span><span class="sxs-lookup"><span data-stu-id="e12a4-115">Set the DTP control according to the data within the structure that *lParam* points to.</span></span> <br/>                                                                                                                                                                 |
| <span id="GDT_NONE"></span><span id="gdt_none"></span><dl> <span data-ttu-id="e12a4-116"><dt>**GDT \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="e12a4-116"><dt>**GDT\_NONE**</dt></span></span> </dl>    | <span data-ttu-id="e12a4-117">Legen Sie das DTP-Steuerelement auf "No Date" fest, und deaktivieren Sie das entsprechende Kontrollkästchen.</span><span class="sxs-lookup"><span data-stu-id="e12a4-117">Set the DTP control to "no date" and clear its check box.</span></span> <span data-ttu-id="e12a4-118">Wenn dieses Flag angegeben wird, wird *LPARAM* ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e12a4-118">When this flag is specified, *lParam* is ignored.</span></span> <span data-ttu-id="e12a4-119">Dieses Flag gilt nur für DTP-Steuerelemente, die auf den [**DTS- \_ shownone**](date-and-time-picker-control-styles.md) -Stil festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="e12a4-119">This flag applies only to DTP controls that are set to the [**DTS\_SHOWNONE**](date-and-time-picker-control-styles.md) style.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="e12a4-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e12a4-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e12a4-121">Ein Zeiger auf eine [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur, die die zum Festlegen des DTP-Steuer Elements verwendete Systemzeit enthält.</span><span class="sxs-lookup"><span data-stu-id="e12a4-121">A pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure containing the system time used to set the DTP control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e12a4-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e12a4-122">Return value</span></span>

<span data-ttu-id="e12a4-123">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="e12a4-123">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e12a4-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e12a4-124">Requirements</span></span>



| <span data-ttu-id="e12a4-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e12a4-125">Requirement</span></span> | <span data-ttu-id="e12a4-126">Wert</span><span class="sxs-lookup"><span data-stu-id="e12a4-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e12a4-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e12a4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e12a4-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e12a4-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e12a4-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e12a4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e12a4-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e12a4-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e12a4-131">Header</span><span class="sxs-lookup"><span data-stu-id="e12a4-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e12a4-132"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e12a4-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

