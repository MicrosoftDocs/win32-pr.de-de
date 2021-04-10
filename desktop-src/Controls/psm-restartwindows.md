---
title: PSM_RESTARTWINDOWS Meldung (prsht. h)
description: Gibt an, dass Windows neu gestartet werden muss, damit die Änderungen wirksam werden.
ms.assetid: 5bf634ee-7408-45df-adb6-c5b947f6c47b
keywords:
- Windows-Steuerelemente für PSM_RESTARTWINDOWS Meldung
topic_type:
- apiref
api_name:
- PSM_RESTARTWINDOWS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb12126ae0a2b9187a941ccc1aff53186a0cda7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858820"
---
# <a name="psm_restartwindows-message"></a><span data-ttu-id="e5ea4-104">PSM- \_ restartwindows-Meldung</span><span class="sxs-lookup"><span data-stu-id="e5ea4-104">PSM\_RESTARTWINDOWS message</span></span>

<span data-ttu-id="e5ea4-105">Gibt an, dass Windows neu gestartet werden muss, damit die Änderungen wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="e5ea4-105">Indicates that Windows needs to be restarted for the changes to take effect.</span></span>

## <a name="parameters"></a><span data-ttu-id="e5ea4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5ea4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5ea4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e5ea4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5ea4-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="e5ea4-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e5ea4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e5ea4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5ea4-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="e5ea4-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5ea4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e5ea4-111">Return value</span></span>

<span data-ttu-id="e5ea4-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="e5ea4-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5ea4-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5ea4-113">Remarks</span></span>

<span data-ttu-id="e5ea4-114">Eine Anwendung sollte diese Nachricht nur als Antwort auf den Benachrichtigungs Code " [PSN \_ Apply](psn-apply.md) " oder " [PSN \_ killactive](psn-killactive.md) " senden.</span><span class="sxs-lookup"><span data-stu-id="e5ea4-114">An application should send this message only in response to the [PSN\_APPLY](psn-apply.md) or [PSN\_KILLACTIVE](psn-killactive.md) notification code.</span></span> <span data-ttu-id="e5ea4-115">Sie können die **PSM- \_ restartwindows** -Nachricht explizit oder mithilfe des " [**propsheet \_ restartwindows**](/windows/desktop/api/Prsht/nf-prsht-propsheet_restartwindows) "-Makros senden.</span><span class="sxs-lookup"><span data-stu-id="e5ea4-115">You can send the **PSM\_RESTARTWINDOWS** message explicitly or by using the [**PropSheet\_RestartWindows**](/windows/desktop/api/Prsht/nf-prsht-propsheet_restartwindows) macro.</span></span>

<span data-ttu-id="e5ea4-116">Diese Meldung bewirkt, dass die [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) -Funktion den ID \_ psrestartwindows-Wert zurückgibt, jedoch nur, wenn der Benutzer auf die Schaltfläche " **OK** " klickt, um das Eigenschaften Blatt zu schließen.</span><span class="sxs-lookup"><span data-stu-id="e5ea4-116">This message causes the [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) function to return the ID\_PSRESTARTWINDOWS value, but only if the user clicks the **OK** button to close the property sheet.</span></span> <span data-ttu-id="e5ea4-117">Es ist Aufgabe der Anwendung, Windows neu zu starten. Dies kann mithilfe der [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) -Funktion erfolgen.</span><span class="sxs-lookup"><span data-stu-id="e5ea4-117">It is the application's responsibility to restart Windows, which can be done by using the [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) function.</span></span>

> [!Note]  
> <span data-ttu-id="e5ea4-118">Diese Meldung wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e5ea4-118">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e5ea4-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5ea4-119">Requirements</span></span>



| <span data-ttu-id="e5ea4-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e5ea4-120">Requirement</span></span> | <span data-ttu-id="e5ea4-121">Wert</span><span class="sxs-lookup"><span data-stu-id="e5ea4-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e5ea4-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e5ea4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e5ea4-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e5ea4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e5ea4-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e5ea4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e5ea4-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e5ea4-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e5ea4-126">Header</span><span class="sxs-lookup"><span data-stu-id="e5ea4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5ea4-127"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5ea4-127"><dt>Prsht.h</dt></span></span> </dl> |



 

