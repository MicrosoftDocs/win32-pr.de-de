---
title: DTM_SETFORMAT Meldung (kommstrg. h)
description: Legt die Anzeige eines DTP-Steuer Elements auf der Grundlage einer angegebenen Format Zeichenfolge fest. Sie können diese Nachricht explizit senden oder das DateTime- \_ SetFormat-Makro verwenden.
ms.assetid: a89fa3ad-9894-4c52-ab56-fb62208e39b3
keywords:
- Windows-Steuerelemente für DTM_SETFORMAT Meldung
topic_type:
- apiref
api_name:
- DTM_SETFORMAT
- DTM_SETFORMATA
- DTM_SETFORMATW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17669ed2e1ed23e3b090b77701bbe05d23a5ccb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040809"
---
# <a name="dtm_setformat-message"></a><span data-ttu-id="d5ee8-105">DTM- \_ SetFormat-Meldung</span><span class="sxs-lookup"><span data-stu-id="d5ee8-105">DTM\_SETFORMAT message</span></span>

<span data-ttu-id="d5ee8-106">Legt die Anzeige eines DTP-Steuer Elements auf der Grundlage einer angegebenen Format Zeichenfolge fest.</span><span class="sxs-lookup"><span data-stu-id="d5ee8-106">Sets the display of a date and time picker (DTP) control based on a given format string.</span></span> <span data-ttu-id="d5ee8-107">Sie können diese Nachricht explizit senden oder das [**DateTime- \_ SetFormat**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="d5ee8-107">You can send this message explicitly or use the [**DateTime\_SetFormat**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d5ee8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5ee8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5ee8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d5ee8-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d5ee8-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="d5ee8-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d5ee8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d5ee8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5ee8-112">Ein Zeiger auf eine NULL terminierte [Format Zeichenfolge](date-and-time-picker-controls.md) , die die gewünschte Anzeige definiert.</span><span class="sxs-lookup"><span data-stu-id="d5ee8-112">A pointer to a zero-terminated [format string](date-and-time-picker-controls.md) that defines the desired display.</span></span> <span data-ttu-id="d5ee8-113">Wenn dieser Parameter auf **null** festgelegt wird, wird das Steuerelement auf die Standardformat Zeichenfolge für den aktuellen Stil zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="d5ee8-113">Setting this parameter to **NULL** will reset the control to the default format string for the current style.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5ee8-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d5ee8-114">Return value</span></span>

<span data-ttu-id="d5ee8-115">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="d5ee8-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5ee8-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5ee8-116">Remarks</span></span>

<span data-ttu-id="d5ee8-117">Es ist zulässig, zusätzliche Zeichen innerhalb der Format Zeichenfolge einzuschließen, um eine umfangreichere Anzeige zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d5ee8-117">It is acceptable to include extra characters within the format string to produce a more rich display.</span></span> <span data-ttu-id="d5ee8-118">Alle nicht Formatierungszeichen müssen jedoch in einfache Anführungszeichen eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="d5ee8-118">However, any nonformat characters must be enclosed within single quotes.</span></span> <span data-ttu-id="d5ee8-119">Die Format Zeichenfolge "" heute beispielsweise: "hh": 'm ": es ddddmmmdd", "yyy", erzeugt eine Ausgabe wie "Today is: 04:22:31 Tuesday Mar 23, 1996".</span><span class="sxs-lookup"><span data-stu-id="d5ee8-119">For example, the format string "'Today is: 'hh':'m':'s ddddMMMdd', 'yyy" would produce output like "Today is: 04:22:31 Tuesday Mar 23, 1996".</span></span>

> [!Note]  
> <span data-ttu-id="d5ee8-120">Ein DTP-Steuerelement verfolgt Gebiets Schema Änderungen, wenn es die Standardformat Zeichenfolge verwendet.</span><span class="sxs-lookup"><span data-stu-id="d5ee8-120">A DTP control tracks locale changes when it is using the default format string.</span></span> <span data-ttu-id="d5ee8-121">Wenn Sie eine benutzerdefinierte Format Zeichenfolge festlegen, wird Sie nicht als Reaktion auf Gebiets Schema Änderungen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d5ee8-121">If you set a custom format string, it will not be updated in response to locale changes.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d5ee8-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5ee8-122">Requirements</span></span>



| <span data-ttu-id="d5ee8-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5ee8-123">Requirement</span></span> | <span data-ttu-id="d5ee8-124">Wert</span><span class="sxs-lookup"><span data-stu-id="d5ee8-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5ee8-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d5ee8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d5ee8-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5ee8-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d5ee8-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d5ee8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d5ee8-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5ee8-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d5ee8-129">Header</span><span class="sxs-lookup"><span data-stu-id="d5ee8-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5ee8-130"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5ee8-130"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d5ee8-131">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="d5ee8-131">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d5ee8-132">**DTM \_ Setformatw** (Unicode) und **DTM \_ setformata** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d5ee8-132">**DTM\_SETFORMATW** (Unicode) and **DTM\_SETFORMATA** (ANSI)</span></span><br/>               |



 

 





