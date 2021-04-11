---
title: EM_GETIMESTATUS Meldung (Winuser. h)
description: Ruft einen Satz von Statusflags ab, die angeben, wie das Bearbeitungs Steuerelement mit dem Eingabemethoden-Editor (IME) interagiert.
ms.assetid: 56705aed-afab-4f4d-9e0b-dc533b516a15
keywords:
- Windows-Steuerelemente für EM_GETIMESTATUS Meldung
topic_type:
- apiref
api_name:
- EM_GETIMESTATUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a9b449053972db8101db7f5c01d1a03611cae67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105122"
---
# <a name="em_getimestatus-message"></a><span data-ttu-id="d068b-104">EM \_ getimestatus-Meldung</span><span class="sxs-lookup"><span data-stu-id="d068b-104">EM\_GETIMESTATUS message</span></span>

<span data-ttu-id="d068b-105">Ruft einen Satz von Statusflags ab, die angeben, wie das Bearbeitungs Steuerelement mit dem Eingabemethoden-Editor (IME) interagiert.</span><span class="sxs-lookup"><span data-stu-id="d068b-105">Gets a set of status flags that indicate how the edit control interacts with the Input Method Editor (IME).</span></span>

## <a name="parameters"></a><span data-ttu-id="d068b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d068b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d068b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d068b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d068b-108">Der Typ des abzurufenden Status.</span><span class="sxs-lookup"><span data-stu-id="d068b-108">The type of status to retrieve.</span></span> <span data-ttu-id="d068b-109">Dieser Parameter kann den folgenden Wert aufweisen:</span><span class="sxs-lookup"><span data-stu-id="d068b-109">This parameter can be the following value.</span></span>



| <span data-ttu-id="d068b-110">Wert</span><span class="sxs-lookup"><span data-stu-id="d068b-110">Value</span></span>                                                                                                                                                                                       | <span data-ttu-id="d068b-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d068b-111">Meaning</span></span>                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <span data-ttu-id="d068b-112"><dt>**Emsis \_ compositionstring**</dt></span><span class="sxs-lookup"><span data-stu-id="d068b-112"><dt>**EMSIS\_COMPOSITIONSTRING**</dt></span></span> </dl> | <span data-ttu-id="d068b-113">Legt das Verhalten zum Verarbeiten der Kompositions Zeichenfolge fest.</span><span class="sxs-lookup"><span data-stu-id="d068b-113">Sets behavior for handling the composition string.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d068b-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d068b-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d068b-115">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d068b-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d068b-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d068b-116">Return value</span></span>

<span data-ttu-id="d068b-117">Spezifische Daten für den Typ des abzurufenden Status.</span><span class="sxs-lookup"><span data-stu-id="d068b-117">Data specific to the type of status to retrieve.</span></span> <span data-ttu-id="d068b-118">Mit dem Wert " **\_ compositionstring" der Emsis** für " *Status*" ist dieser Rückgabewert mindestens einer der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="d068b-118">With the **EMSIS\_COMPOSITIONSTRING** value for *status*, this return value is one or more of the following values.</span></span>



| <span data-ttu-id="d068b-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d068b-119">Return code</span></span>                                                                                                    | <span data-ttu-id="d068b-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d068b-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d068b-121"><dt>**eimes \_ getcompstratonce**</dt></span><span class="sxs-lookup"><span data-stu-id="d068b-121"><dt>**EIMES\_GETCOMPSTRATONCE**</dt></span></span> </dl>         | <span data-ttu-id="d068b-122">Wenn dieses Flag festgelegt ist, verknüpft das Bearbeitungs Steuerelement die [**WM \_ IME- \_ Kompositions**](/windows/desktop/Intl/wm-ime-composition) Nachricht mit *fFlags* , die auf GCS ResultStr festgelegt ist, \_ und gibt die Ergebnis Zeichenfolge sofort zurück.</span><span class="sxs-lookup"><span data-stu-id="d068b-122">If this flag is set, the edit control hooks the [**WM\_IME\_COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) message with *fFlags* set to GCS\_RESULTSTR and returns the result string immediately.</span></span> <span data-ttu-id="d068b-123">Wenn dieses Flag nicht festgelegt ist, übergibt das Bearbeitungs Steuerelement die **WM- \_ IME- \_ Kompositions** Meldung an die Standardfenster Prozedur und verarbeitet die Ergebnis Zeichenfolge aus der [**WM- \_ char**](/windows/desktop/inputdev/wm-char) -Nachricht. Dies ist das Standardverhalten des Bearbeitungs Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="d068b-123">If this flag is not set, the edit control passes the **WM\_IME\_COMPOSITION** message to the default window procedure and processes the result string from the [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message; this is the default behavior of the edit control.</span></span><br/> |
| <dl> <span data-ttu-id="d068b-124"><dt>**eimes \_ cancelcompstrinfocus**</dt></span><span class="sxs-lookup"><span data-stu-id="d068b-124"><dt>**EIMES\_CANCELCOMPSTRINFOCUS**</dt></span></span> </dl>     | <span data-ttu-id="d068b-125">Wenn dieses Flag festgelegt ist, bricht das Bearbeitungs Steuerelement die Kompositions Zeichenfolge ab, wenn es die [**WM- \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus) -Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="d068b-125">If this flag is set, the edit control cancels the composition string when it receives the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message.</span></span> <span data-ttu-id="d068b-126">Wenn dieses Flag nicht festgelegt ist, wird die Kompositions Zeichenfolge vom Bearbeitungs Steuerelement nicht abgebrochen. Dies ist das Standardverhalten des Bearbeitungs Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="d068b-126">If this flag is not set, the edit control does not cancel the composition string; this is the default behavior of the edit control.</span></span><br/>                                                                                                                                                                       |
| <dl> <span data-ttu-id="d068b-127"><dt>**eimes \_ completecompstrankillfocus**</dt></span><span class="sxs-lookup"><span data-stu-id="d068b-127"><dt>**EIMES\_COMPLETECOMPSTRKILLFOCUS**</dt></span></span> </dl> | <span data-ttu-id="d068b-128">Wenn dieses Flag festgelegt ist, schließt das Bearbeitungs Steuerelement die Kompositions Zeichenfolge nach dem Empfang der [**WM- \_ killfocus**](/windows/desktop/inputdev/wm-killfocus) -Meldung ab.</span><span class="sxs-lookup"><span data-stu-id="d068b-128">If this flag is set, the edit control completes the composition string upon receiving the [**WM\_KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) message.</span></span> <span data-ttu-id="d068b-129">Wenn dieses Flag nicht festgelegt ist, vervollständigt das Bearbeitungs Steuerelement die Kompositions Zeichenfolge nicht. Dies ist das Standardverhalten des Bearbeitungs Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="d068b-129">If this flag is not set, the edit control does not complete the composition string; this is the default behavior of the edit control.</span></span><br/>                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="d068b-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d068b-130">Remarks</span></span>

<span data-ttu-id="d068b-131">Umfassende **Bearbeitung:** Die **\_ getimestatus** -Nachricht wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d068b-131">**Rich Edit:** The **EM\_GETIMESTATUS** message is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="d068b-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d068b-132">Requirements</span></span>



| <span data-ttu-id="d068b-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d068b-133">Requirement</span></span> | <span data-ttu-id="d068b-134">Wert</span><span class="sxs-lookup"><span data-stu-id="d068b-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d068b-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d068b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d068b-136">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d068b-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d068b-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d068b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d068b-138">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d068b-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d068b-139">Header</span><span class="sxs-lookup"><span data-stu-id="d068b-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="d068b-140"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="d068b-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d068b-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d068b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d068b-142">**EM- \_ Zeit Status**</span><span class="sxs-lookup"><span data-stu-id="d068b-142">**EM\_SETIMESTATUS**</span></span>](em-setimestatus.md)
</dt> </dl>

 

