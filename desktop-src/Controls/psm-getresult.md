---
title: PSM_GETRESULT Meldung (prsht. h)
description: Wird von nicht modalen Eigenschaften Blättern zum Abrufen der Informationen verwendet, die von PropertySheet an modale Eigenschaften Blätter zurückgegeben werden. Sie können diese Nachricht explizit senden oder das propsheet \_ GetResult-Makro verwenden.
ms.assetid: e0f609ea-5d7e-4c17-ade1-3c1051c5a5bf
keywords:
- Windows-Steuerelemente für PSM_GETRESULT Meldung
topic_type:
- apiref
api_name:
- PSM_GETRESULT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d41609f625cbd3938fa78e9a2f91ab70168ecc29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518530"
---
# <a name="psm_getresult-message"></a><span data-ttu-id="418b9-105">PSM \_ GetResult-Nachricht</span><span class="sxs-lookup"><span data-stu-id="418b9-105">PSM\_GETRESULT message</span></span>

<span data-ttu-id="418b9-106">Wird von nicht modalen Eigenschaften Blättern zum Abrufen der Informationen verwendet, die von [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)an modale Eigenschaften Blätter zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="418b9-106">Used by modeless property sheets to retrieve the information returned to modal property sheets by [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta).</span></span> <span data-ttu-id="418b9-107">Sie können diese Nachricht explizit senden oder das [**propsheet \_ GetResult**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="418b9-107">You can send this message explicitly or use the [**PropSheet\_GetResult**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="418b9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="418b9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="418b9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="418b9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="418b9-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="418b9-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="418b9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="418b9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="418b9-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="418b9-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="418b9-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="418b9-113">Return value</span></span>

<span data-ttu-id="418b9-114">Gibt einen positiven Wert zurück, wenn erfolgreich, andernfalls-1.</span><span class="sxs-lookup"><span data-stu-id="418b9-114">Returns a positive value if successful, or -1 otherwise.</span></span> <span data-ttu-id="418b9-115">Die folgenden Rückgabewerte haben eine besondere Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="418b9-115">The following return values have a special meaning.</span></span>



| <span data-ttu-id="418b9-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="418b9-116">Return code</span></span>                                                                                         | <span data-ttu-id="418b9-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="418b9-117">Description</span></span>                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="418b9-118"><dt>**ID \_ psrebootsystem**</dt></span><span class="sxs-lookup"><span data-stu-id="418b9-118"><dt>**ID\_PSREBOOTSYSTEM**</dt></span></span> </dl>   | <span data-ttu-id="418b9-119">Eine Seite hat eine [**PSM- \_ rebootsystemmeldung**](psm-rebootsystem.md) an das Eigenschaften Blatt gesendet.</span><span class="sxs-lookup"><span data-stu-id="418b9-119">A page sent a [**PSM\_REBOOTSYSTEM**](psm-rebootsystem.md) message to the property sheet.</span></span> <span data-ttu-id="418b9-120">Der Computer muss neu gestartet werden, damit die Änderungen des Benutzers wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="418b9-120">The computer must be restarted for the user's changes to take effect.</span></span><br/> |
| <dl> <span data-ttu-id="418b9-121"><dt>**ID \_ psrestartwindows**</dt></span><span class="sxs-lookup"><span data-stu-id="418b9-121"><dt>**ID\_PSRESTARTWINDOWS**</dt></span></span> </dl> | <span data-ttu-id="418b9-122">Eine Seite hat eine [**PSM- \_ restartwindows**](psm-restartwindows.md) -Meldung an das Eigenschaften Blatt gesendet.</span><span class="sxs-lookup"><span data-stu-id="418b9-122">A page sent a [**PSM\_RESTARTWINDOWS**](psm-restartwindows.md) message to the property sheet.</span></span> <span data-ttu-id="418b9-123">Windows muss neu gestartet werden, damit die Änderungen des Benutzers wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="418b9-123">Windows must be restarted for the user's changes to take effect.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="418b9-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="418b9-124">Remarks</span></span>

<span data-ttu-id="418b9-125">Um erweiterte Fehlerinformationen abzurufen, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)auf.</span><span class="sxs-lookup"><span data-stu-id="418b9-125">To retrieve extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

<span data-ttu-id="418b9-126">Der Rückgabewert für diese Nachricht ist identisch mit dem, was [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) für ein modales Eigenschaften Blatt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="418b9-126">The return value for this message is identical to what [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) returns for a modal property sheet.</span></span>

[<span data-ttu-id="418b9-127">Version 5,80.</span><span class="sxs-lookup"><span data-stu-id="418b9-127">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="418b9-128">Der Rückgabewert [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) enthält unterschiedliche Informationen für modale und nicht modale Eigenschaften Blätter.</span><span class="sxs-lookup"><span data-stu-id="418b9-128">The [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) return value carries different information for modal and modeless property sheets.</span></span> <span data-ttu-id="418b9-129">In einigen Fällen benötigen nicht modale Eigenschaften Blätter möglicherweise die Informationen, die Sie von **PropertySheet** erhalten haben, wenn Sie Modal waren.</span><span class="sxs-lookup"><span data-stu-id="418b9-129">In some cases, modeless property sheets may need the information they would have received from **PropertySheet** if they had been modal.</span></span> <span data-ttu-id="418b9-130">Insbesondere müssen Sie möglicherweise wissen, ob ID \_ psrebootsystem oder ID \_ psrestartwindows zurückgegeben worden wäre.</span><span class="sxs-lookup"><span data-stu-id="418b9-130">In particular, they may need to know whether ID\_PSREBOOTSYSTEM or ID\_PSRESTARTWINDOWS would have been returned.</span></span>

<span data-ttu-id="418b9-131">Für ein nicht modalem Eigenschaften Blatt sollte die Nachrichten Schleife [**PSM \_ IsDialogMessage**](psm-isdialogmessage.md) verwenden, um Nachrichten an das Eigenschaften Blatt zu übergeben, und [**PSM \_ getcurrentpagehwnd**](psm-getcurrentpagehwnd.md) , um zu bestimmen, wann das Dialogfeld zerstört werden soll.</span><span class="sxs-lookup"><span data-stu-id="418b9-131">For a modeless property sheet, your message loop should use [**PSM\_ISDIALOGMESSAGE**](psm-isdialogmessage.md) to pass messages to the property sheet dialog box, and [**PSM\_GETCURRENTPAGEHWND**](psm-getcurrentpagehwnd.md) to determine when to destroy the dialog box.</span></span> <span data-ttu-id="418b9-132">Wenn der Benutzer auf die Schaltfläche **OK** oder **Abbrechen** klickt, gibt **PSM \_ getcurrentpagehwnd** den Wert **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="418b9-132">When the user clicks the **OK** or **Cancel** button, **PSM\_GETCURRENTPAGEHWND** returns **NULL**.</span></span> <span data-ttu-id="418b9-133">Sie können dann den Wert abrufen, den ein modales Eigenschaften Blatt von [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) erhalten hätte, indem Sie eine **PSM \_ GetResult** -Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="418b9-133">You can then retrieve the value that a modal property sheet would have received from [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) by sending a **PSM\_GETRESULT** message.</span></span>

> [!Note]  
> <span data-ttu-id="418b9-134">Diese Meldung wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="418b9-134">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="418b9-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="418b9-135">Requirements</span></span>



| <span data-ttu-id="418b9-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="418b9-136">Requirement</span></span> | <span data-ttu-id="418b9-137">Wert</span><span class="sxs-lookup"><span data-stu-id="418b9-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="418b9-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="418b9-138">Minimum supported client</span></span><br/> | <span data-ttu-id="418b9-139">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="418b9-139">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="418b9-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="418b9-140">Minimum supported server</span></span><br/> | <span data-ttu-id="418b9-141">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="418b9-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="418b9-142">Header</span><span class="sxs-lookup"><span data-stu-id="418b9-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="418b9-143"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="418b9-143"><dt>Prsht.h</dt></span></span> </dl> |



 

