---
title: PSM_GETCURRENTPAGEHWND Meldung (prsht. h)
description: Ruft ein Handle für das Fenster der aktuellen Seite eines Eigenschaften Blatts ab. Sie können diese Nachricht explizit oder mithilfe des propsheet \_ getcurrentpgehwnd-Makros senden.
ms.assetid: 1f2d0af9-5853-48e7-b827-483be032b6ca
keywords:
- Windows-Steuerelemente für PSM_GETCURRENTPAGEHWND Meldung
topic_type:
- apiref
api_name:
- PSM_GETCURRENTPAGEHWND
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae9ac89e6bc60317f2caf31ea92754d10983e11a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346746"
---
# <a name="psm_getcurrentpagehwnd-message"></a><span data-ttu-id="c18e0-105">PSM \_ getcurrentpagehwnd-Meldung</span><span class="sxs-lookup"><span data-stu-id="c18e0-105">PSM\_GETCURRENTPAGEHWND message</span></span>

<span data-ttu-id="c18e0-106">Ruft ein Handle für das Fenster der aktuellen Seite eines Eigenschaften Blatts ab.</span><span class="sxs-lookup"><span data-stu-id="c18e0-106">Retrieves a handle to the window of the current page of a property sheet.</span></span> <span data-ttu-id="c18e0-107">Sie können diese Nachricht explizit oder mithilfe des [**propsheet \_ getcurrentpgehwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="c18e0-107">You can send this message explicitly or by using the [**PropSheet\_GetCurrentPageHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c18e0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c18e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c18e0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c18e0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c18e0-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="c18e0-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c18e0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c18e0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c18e0-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="c18e0-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c18e0-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c18e0-113">Return value</span></span>

<span data-ttu-id="c18e0-114">Gibt ein Handle für das Fenster der aktuellen Eigenschaften Blattseite zurück.</span><span class="sxs-lookup"><span data-stu-id="c18e0-114">Returns a handle to the window of the current property sheet page.</span></span>

## <a name="remarks"></a><span data-ttu-id="c18e0-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c18e0-115">Remarks</span></span>

<span data-ttu-id="c18e0-116">Verwenden Sie die **PSM \_ getcurrentpagehwnd** -Nachricht mit nicht modalem Eigenschaften Blatt, um zu bestimmen, wann das Dialogfeld zerstört werden soll.</span><span class="sxs-lookup"><span data-stu-id="c18e0-116">Use the **PSM\_GETCURRENTPAGEHWND** message with modeless property sheets to determine when to destroy the dialog box.</span></span> <span data-ttu-id="c18e0-117">Wenn der Benutzer auf die Schaltfläche **OK** oder **Abbrechen** klickt, gibt **PSM \_ getcurrentpagehwnd** **null** zurück, und Sie können dann die [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) -Funktion verwenden, um das Dialogfeld zu zerstören.</span><span class="sxs-lookup"><span data-stu-id="c18e0-117">When the user clicks the **OK** or **Cancel** button, **PSM\_GETCURRENTPAGEHWND** returns **NULL**, and you can then use the [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) function to destroy the dialog box.</span></span>

> [!Note]  
> <span data-ttu-id="c18e0-118">Diese Meldung wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c18e0-118">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c18e0-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c18e0-119">Requirements</span></span>



| <span data-ttu-id="c18e0-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c18e0-120">Requirement</span></span> | <span data-ttu-id="c18e0-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c18e0-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c18e0-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c18e0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c18e0-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c18e0-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c18e0-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c18e0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c18e0-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c18e0-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c18e0-126">Header</span><span class="sxs-lookup"><span data-stu-id="c18e0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c18e0-127"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="c18e0-127"><dt>Prsht.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c18e0-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c18e0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c18e0-129">**Eigenschaften Blatt**</span><span class="sxs-lookup"><span data-stu-id="c18e0-129">**PropertySheet**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 

