---
title: PSM_REBOOTSYSTEM Meldung (prsht. h)
description: Gibt an, dass das System neu gestartet werden muss, damit die Änderungen wirksam werden. Sie können die PSM- \_ rebootsystem-Nachricht explizit oder mithilfe des propsheet \_ rebootsystem-Makros senden.
ms.assetid: 461fce3c-183a-4b9b-8eab-ed2838d9f866
keywords:
- Windows-Steuerelemente für PSM_REBOOTSYSTEM Meldung
topic_type:
- apiref
api_name:
- PSM_REBOOTSYSTEM
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14f5018dc3845d699561740ccd9cbb0a9c793f15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476059"
---
# <a name="psm_rebootsystem-message"></a><span data-ttu-id="35af2-105">PSM- \_ rebootsystemmeldung</span><span class="sxs-lookup"><span data-stu-id="35af2-105">PSM\_REBOOTSYSTEM message</span></span>

<span data-ttu-id="35af2-106">Gibt an, dass das System neu gestartet werden muss, damit die Änderungen wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="35af2-106">Indicates the system needs to be restarted for the changes to take effect.</span></span> <span data-ttu-id="35af2-107">Sie können die **PSM- \_ rebootsystem** -Nachricht explizit oder mithilfe des [**propsheet \_ rebootsystem**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="35af2-107">You can send the **PSM\_REBOOTSYSTEM** message explicitly or by using the [**PropSheet\_RebootSystem**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="35af2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="35af2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35af2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="35af2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35af2-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="35af2-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="35af2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="35af2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35af2-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="35af2-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35af2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35af2-113">Return value</span></span>

<span data-ttu-id="35af2-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="35af2-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="35af2-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35af2-115">Remarks</span></span>

<span data-ttu-id="35af2-116">Eine Anwendung sollte diese Nachricht nur als Antwort auf die Benachrichtigungs Meldung " [PSN \_ Apply](psn-apply.md) " oder " [PSN \_ killactive](psn-killactive.md) " senden.</span><span class="sxs-lookup"><span data-stu-id="35af2-116">An application should send this message only in response to the [PSN\_APPLY](psn-apply.md) or [PSN\_KILLACTIVE](psn-killactive.md) notification message.</span></span>

<span data-ttu-id="35af2-117">Diese Meldung bewirkt, dass die [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) -Funktion den \_ psrebootsystem-ID-Wert zurückgibt, jedoch nur, wenn der Benutzer auf die Schaltfläche **OK** klickt, um das Eigenschaften Blatt zu schließen.</span><span class="sxs-lookup"><span data-stu-id="35af2-117">This message causes the [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) function to return the ID\_PSREBOOTSYSTEM value, but only if the user clicks the **OK** button to close the property sheet.</span></span> <span data-ttu-id="35af2-118">Es liegt in der Verantwortung der Anwendung, das System neu zu starten. Dies kann mithilfe der [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) -Funktion erfolgen.</span><span class="sxs-lookup"><span data-stu-id="35af2-118">It is the application's responsibility to reboot the system, which can be done by using the [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) function.</span></span>

<span data-ttu-id="35af2-119">Diese Nachricht ersetzt alle [**PSM- \_ restartwindows**](psm-restartwindows.md) -Meldungen, die vor oder nach der Nachricht liegen.</span><span class="sxs-lookup"><span data-stu-id="35af2-119">This message supersedes all [**PSM\_RESTARTWINDOWS**](psm-restartwindows.md) messages that precede or follow it.</span></span>

> [!Note]  
> <span data-ttu-id="35af2-120">Diese Meldung wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="35af2-120">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="35af2-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35af2-121">Requirements</span></span>



| <span data-ttu-id="35af2-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35af2-122">Requirement</span></span> | <span data-ttu-id="35af2-123">Wert</span><span class="sxs-lookup"><span data-stu-id="35af2-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="35af2-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="35af2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="35af2-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35af2-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="35af2-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="35af2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="35af2-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35af2-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="35af2-128">Header</span><span class="sxs-lookup"><span data-stu-id="35af2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="35af2-129"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="35af2-129"><dt>Prsht.h</dt></span></span> </dl> |



 

