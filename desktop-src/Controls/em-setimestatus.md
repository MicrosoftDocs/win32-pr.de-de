---
title: EM_SETIMESTATUS Meldung (Winuser. h)
description: Legt die Statusflags fest, die bestimmen, wie ein Bearbeitungs Steuerelement mit dem Eingabemethoden-Editor (IME) interagiert.
ms.assetid: 3de2e8b5-bdd8-4b25-9427-38a11b77a17a
keywords:
- Windows-Steuerelemente für EM_SETIMESTATUS Meldung
topic_type:
- apiref
api_name:
- EM_SETIMESTATUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e896c358281b2d4b5012fe13003720e0d008e6a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742009"
---
# <a name="em_setimestatus-message"></a><span data-ttu-id="bae18-104">EM- \_ Statusmeldung</span><span class="sxs-lookup"><span data-stu-id="bae18-104">EM\_SETIMESTATUS message</span></span>

<span data-ttu-id="bae18-105">Legt die Statusflags fest, die bestimmen, wie ein Bearbeitungs Steuerelement mit dem Eingabemethoden-Editor (IME) interagiert.</span><span class="sxs-lookup"><span data-stu-id="bae18-105">Sets the status flags that determine how an edit control interacts with the Input Method Editor (IME).</span></span>

## <a name="parameters"></a><span data-ttu-id="bae18-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bae18-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bae18-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bae18-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bae18-108">Der Typ des festzulegenden Status.</span><span class="sxs-lookup"><span data-stu-id="bae18-108">The type of status to set.</span></span> <span data-ttu-id="bae18-109">Dieser Parameter kann den folgenden Wert aufweisen:</span><span class="sxs-lookup"><span data-stu-id="bae18-109">This parameter can be the following value.</span></span>



| <span data-ttu-id="bae18-110">Wert</span><span class="sxs-lookup"><span data-stu-id="bae18-110">Value</span></span>                                                                                                                                                                                       | <span data-ttu-id="bae18-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="bae18-111">Meaning</span></span>                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <span data-ttu-id="bae18-112"><dt>**Emsis \_ compositionstring**</dt></span><span class="sxs-lookup"><span data-stu-id="bae18-112"><dt>**EMSIS\_COMPOSITIONSTRING**</dt></span></span> </dl> | <span data-ttu-id="bae18-113">Legt das Verhalten für die Behandlungs Zeichenfolge der Bearbeitung fest</span><span class="sxs-lookup"><span data-stu-id="bae18-113">Sets behavior for the handling composition string.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bae18-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bae18-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bae18-115">Spezifische Daten für den statentyp.</span><span class="sxs-lookup"><span data-stu-id="bae18-115">Data specific to the status type.</span></span> <span data-ttu-id="bae18-116">Wenn *wParam* eine **Emsis- \_ compositionstring** ist, kann dieser Parameter einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="bae18-116">If *wParam* is **EMSIS\_COMPOSITIONSTRING**, this parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="bae18-117">Wert</span><span class="sxs-lookup"><span data-stu-id="bae18-117">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="bae18-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="bae18-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EIMES_GETCOMPSTRATONCE"></span><span id="eimes_getcompstratonce"></span><dl> <span data-ttu-id="bae18-119"><dt>**eimes \_ getcompstratonce**</dt></span><span class="sxs-lookup"><span data-stu-id="bae18-119"><dt>**EIMES\_GETCOMPSTRATONCE**</dt></span></span> </dl>                         | <span data-ttu-id="bae18-120">Wenn dieses Flag festgelegt ist, verknüpft das Bearbeitungs Steuerelement die [**WM- \_ IME- \_ Kompositions**](/windows/desktop/Intl/wm-ime-composition) Nachricht mit *LPARAM* , festgelegt auf GCS \_ ResultStr, und gibt die Ergebnis Zeichenfolge sofort zurück.</span><span class="sxs-lookup"><span data-stu-id="bae18-120">If this flag is set, the edit control hooks the [**WM\_IME\_COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) message with *lParam* set to GCS\_RESULTSTR and returns the result string immediately.</span></span> <span data-ttu-id="bae18-121">Wenn dieses Flag nicht festgelegt ist, übergibt das Bearbeitungs Steuerelement die **WM- \_ IME- \_ Kompositions** Meldung an die Standardfenster Prozedur und verarbeitet die Ergebnis Zeichenfolge aus der [**WM- \_ char**](/windows/desktop/inputdev/wm-char) -Nachricht. Dies ist das Standardverhalten des Bearbeitungs Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="bae18-121">If this flag is not set, the edit control passes the **WM\_IME\_COMPOSITION** message to the default window procedure and handles the result string from the [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message; this is the default behavior of the edit control.</span></span><br/> |
| <span id="EIMES_CANCELCOMPSTRINFOCUS"></span><span id="eimes_cancelcompstrinfocus"></span><dl> <span data-ttu-id="bae18-122"><dt>**eimes \_ cancelcompstrinfocus**</dt></span><span class="sxs-lookup"><span data-stu-id="bae18-122"><dt>**EIMES\_CANCELCOMPSTRINFOCUS**</dt></span></span> </dl>             | <span data-ttu-id="bae18-123">Wenn dieses Flag festgelegt ist, bricht das Bearbeitungs Steuerelement die Kompositions Zeichenfolge ab, wenn es die [**WM- \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus) -Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="bae18-123">If this flag is set, the edit control cancels the composition string when it receives the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message.</span></span> <span data-ttu-id="bae18-124">Wenn dieses Flag nicht festgelegt ist, wird die Kompositions Zeichenfolge vom Bearbeitungs Steuerelement nicht abgebrochen. Dies ist das Standardverhalten des Bearbeitungs Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="bae18-124">If this flag is not set, the edit control does not cancel the composition string; this is the default behavior of the edit control.</span></span><br/>                                                                                                                                                                     |
| <span id="EIMES_COMPLETECOMPSTRKILLFOCUS"></span><span id="eimes_completecompstrkillfocus"></span><dl> <span data-ttu-id="bae18-125"><dt>**eimes \_ completecompstrankillfocus**</dt></span><span class="sxs-lookup"><span data-stu-id="bae18-125"><dt>**EIMES\_COMPLETECOMPSTRKILLFOCUS**</dt></span></span> </dl> | <span data-ttu-id="bae18-126">Wenn dieses Flag festgelegt ist, schließt das Bearbeitungs Steuerelement die Kompositions Zeichenfolge nach dem Empfang der [**WM- \_ killfocus**](/windows/desktop/inputdev/wm-killfocus) -Meldung ab.</span><span class="sxs-lookup"><span data-stu-id="bae18-126">If this flag is set, the edit control completes the composition string upon receiving the [**WM\_KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) message.</span></span> <span data-ttu-id="bae18-127">Wenn dieses Flag nicht festgelegt ist, vervollständigt das Bearbeitungs Steuerelement die Kompositions Zeichenfolge nicht. Dies ist das Standardverhalten des Bearbeitungs Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="bae18-127">If this flag is not set, the edit control does not complete the composition string; this is the default behavior of the edit control.</span></span><br/>                                                                                                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bae18-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bae18-128">Return value</span></span>

<span data-ttu-id="bae18-129">Gibt den vorherigen Wert des *LPARAM* -Parameters zurück.</span><span class="sxs-lookup"><span data-stu-id="bae18-129">Returns the previous value of the *lParam* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="bae18-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bae18-130">Remarks</span></span>

<span data-ttu-id="bae18-131">Umfassende **Bearbeitung:** Die **EM- \_ Status** Meldung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bae18-131">**Rich Edit:** The **EM\_SETIMESTATUS** message is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="bae18-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bae18-132">Requirements</span></span>



| <span data-ttu-id="bae18-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bae18-133">Requirement</span></span> | <span data-ttu-id="bae18-134">Wert</span><span class="sxs-lookup"><span data-stu-id="bae18-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bae18-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bae18-135">Minimum supported client</span></span><br/> | <span data-ttu-id="bae18-136">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bae18-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bae18-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bae18-137">Minimum supported server</span></span><br/> | <span data-ttu-id="bae18-138">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bae18-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bae18-139">Header</span><span class="sxs-lookup"><span data-stu-id="bae18-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="bae18-140"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="bae18-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bae18-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bae18-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bae18-142">**EM \_ getimestatus**</span><span class="sxs-lookup"><span data-stu-id="bae18-142">**EM\_GETIMESTATUS**</span></span>](em-getimestatus.md)
</dt> </dl>

 

