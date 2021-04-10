---
title: EM_NOSETFOCUS Meldung (kommstrg. h)
description: Verhindert, dass ein einzeilige Bearbeitungs Steuerelement den Tastaturfokus erhält. Sie können diese Nachricht explizit oder mithilfe des " \_ nosetfocus"-Makros bearbeiten senden.
ms.assetid: aeb5ed6b-7d4f-4c0d-a172-6cee7cab959c
keywords:
- Windows-Steuerelemente für EM_NOSETFOCUS Meldung
topic_type:
- apiref
api_name:
- EM_NOSETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b82830cda3402d2089d3421debaa7c4dbf13de5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105104"
---
# <a name="em_nosetfocus-message"></a><span data-ttu-id="86c8b-105">EM \_ nosetfocus-Nachricht</span><span class="sxs-lookup"><span data-stu-id="86c8b-105">EM\_NOSETFOCUS message</span></span>

<span data-ttu-id="86c8b-106">\[Zur internen Verwendung vorgesehen. wird nicht für die Verwendung in Anwendungen empfohlen.</span><span class="sxs-lookup"><span data-stu-id="86c8b-106">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="86c8b-107">Diese Meldung wird möglicherweise in zukünftigen Versionen von Windows nicht mehr unterstützt.\]</span><span class="sxs-lookup"><span data-stu-id="86c8b-107">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="86c8b-108">Verhindert, dass ein einzeilige Bearbeitungs Steuerelement den Tastaturfokus erhält.</span><span class="sxs-lookup"><span data-stu-id="86c8b-108">Prevents a single-line edit control from receiving keyboard focus.</span></span> <span data-ttu-id="86c8b-109">Sie können diese Nachricht explizit oder mithilfe des " [**\_ nosetfocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus) "-Makros bearbeiten senden.</span><span class="sxs-lookup"><span data-stu-id="86c8b-109">You can send this message explicitly or by using the [**Edit\_NoSetFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="86c8b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="86c8b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86c8b-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="86c8b-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86c8b-112">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="86c8b-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="86c8b-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="86c8b-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86c8b-114">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="86c8b-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86c8b-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86c8b-115">Return value</span></span>

<span data-ttu-id="86c8b-116">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="86c8b-116">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="86c8b-117">Überlegungen zur Sicherheit</span><span class="sxs-lookup"><span data-stu-id="86c8b-117">Security Considerations</span></span>

<span data-ttu-id="86c8b-118">Die Verwendung dieser Nachricht kann die Sicherheit des Programms beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="86c8b-118">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="86c8b-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86c8b-119">Remarks</span></span>

<span data-ttu-id="86c8b-120">Diese Meldung wird ignoriert, wenn das Bearbeitungs Steuerelement kein einzeilige Bearbeitungs Steuerelement ist.</span><span class="sxs-lookup"><span data-stu-id="86c8b-120">This message is ignored if the edit control is not a single-line edit control.</span></span>

<span data-ttu-id="86c8b-121">Nachdem diese Nachricht gesendet wurde, ist der Effekt permanent.</span><span class="sxs-lookup"><span data-stu-id="86c8b-121">After this message is sent, the effect is permanent.</span></span>

## <a name="requirements"></a><span data-ttu-id="86c8b-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86c8b-122">Requirements</span></span>



| <span data-ttu-id="86c8b-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86c8b-123">Requirement</span></span> | <span data-ttu-id="86c8b-124">Wert</span><span class="sxs-lookup"><span data-stu-id="86c8b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86c8b-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="86c8b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="86c8b-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86c8b-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="86c8b-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="86c8b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="86c8b-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86c8b-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="86c8b-129">Header</span><span class="sxs-lookup"><span data-stu-id="86c8b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="86c8b-130"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="86c8b-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86c8b-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86c8b-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="86c8b-132">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="86c8b-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="86c8b-133">**\_Nosetfocus bearbeiten**</span><span class="sxs-lookup"><span data-stu-id="86c8b-133">**Edit\_NoSetFocus**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus)
</dt> <dt>

[<span data-ttu-id="86c8b-134">**EM- \_ Fokus**</span><span class="sxs-lookup"><span data-stu-id="86c8b-134">**EM\_TAKEFOCUS**</span></span>](em-takefocus.md)
</dt> </dl>

 

 





