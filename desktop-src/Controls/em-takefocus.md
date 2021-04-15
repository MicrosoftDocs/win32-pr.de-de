---
title: EM_TAKEFOCUS Meldung (kommstrg. h)
description: Erzwingt, dass ein einzeilige Bearbeitungs Steuerelement den Tastaturfokus erhält. Sie können diese Nachricht explizit oder mithilfe des-Makros " \_ Take TakeFocus bearbeiten" senden.
ms.assetid: 27470857-4219-4426-bc69-e1271afc6ffb
keywords:
- Windows-Steuerelemente für EM_TAKEFOCUS Meldung
topic_type:
- apiref
api_name:
- EM_TAKEFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e4abdf926cdd337760b5cf151c3f8ee08cb418b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476827"
---
# <a name="em_takefocus-message"></a><span data-ttu-id="f69c1-105">EM- \_ Fokus Meldung</span><span class="sxs-lookup"><span data-stu-id="f69c1-105">EM\_TAKEFOCUS message</span></span>

<span data-ttu-id="f69c1-106">\[Zur internen Verwendung vorgesehen. wird nicht für die Verwendung in Anwendungen empfohlen.</span><span class="sxs-lookup"><span data-stu-id="f69c1-106">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="f69c1-107">Diese Meldung wird möglicherweise in zukünftigen Versionen von Windows nicht mehr unterstützt.\]</span><span class="sxs-lookup"><span data-stu-id="f69c1-107">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="f69c1-108">Erzwingt, dass ein einzeilige Bearbeitungs Steuerelement den Tastaturfokus erhält.</span><span class="sxs-lookup"><span data-stu-id="f69c1-108">Forces a single-line edit control to receive keyboard focus.</span></span> <span data-ttu-id="f69c1-109">Sie können diese Nachricht explizit oder mithilfe des-Makros [**" \_ Take TakeFocus bearbeiten**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus) " senden.</span><span class="sxs-lookup"><span data-stu-id="f69c1-109">You can send this message explicitly or by using the [**Edit\_TakeFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f69c1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f69c1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f69c1-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f69c1-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f69c1-112">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="f69c1-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f69c1-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f69c1-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f69c1-114">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="f69c1-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f69c1-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f69c1-115">Return value</span></span>

<span data-ttu-id="f69c1-116">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f69c1-116">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="f69c1-117">Überlegungen zur Sicherheit</span><span class="sxs-lookup"><span data-stu-id="f69c1-117">Security Considerations</span></span>

<span data-ttu-id="f69c1-118">Die Verwendung dieser Nachricht kann die Sicherheit des Programms beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="f69c1-118">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="f69c1-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f69c1-119">Remarks</span></span>

<span data-ttu-id="f69c1-120">Diese Meldung wird ignoriert, wenn das Bearbeitungs Steuerelement kein einzeilige Bearbeitungs Steuerelement ist.</span><span class="sxs-lookup"><span data-stu-id="f69c1-120">This message is ignored if the edit control is not a single-line edit control.</span></span>

<span data-ttu-id="f69c1-121">Wenn das Bearbeitungs Steuerelement zuvor eine [**EM \_ nosetfocus**](em-nosetfocus.md) -Nachricht empfangen hat, scheint das Bearbeitungs Steuerelement den Fokus zu haben, ohne es tatsächlich zu haben. andernfalls erhält das Bearbeitungs Steuerelement den Fokus.</span><span class="sxs-lookup"><span data-stu-id="f69c1-121">If the edit control previously received an [**EM\_NOSETFOCUS**](em-nosetfocus.md) message, the edit control will appear to have the focus without actually having it; otherwise, the edit control will receive focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="f69c1-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f69c1-122">Requirements</span></span>



| <span data-ttu-id="f69c1-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f69c1-123">Requirement</span></span> | <span data-ttu-id="f69c1-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f69c1-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f69c1-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f69c1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f69c1-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f69c1-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f69c1-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f69c1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f69c1-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f69c1-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f69c1-129">Header</span><span class="sxs-lookup"><span data-stu-id="f69c1-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f69c1-130"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f69c1-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f69c1-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f69c1-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="f69c1-132">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="f69c1-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f69c1-133">**" \_ TakeFocus" Bearbeiten**</span><span class="sxs-lookup"><span data-stu-id="f69c1-133">**Edit\_TakeFocus**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus)
</dt> <dt>

[<span data-ttu-id="f69c1-134">**EM \_ nosetfocus**</span><span class="sxs-lookup"><span data-stu-id="f69c1-134">**EM\_NOSETFOCUS**</span></span>](em-nosetfocus.md)
</dt> </dl>

 

 





