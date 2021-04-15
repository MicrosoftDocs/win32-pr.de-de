---
title: CB_SETEDITSEL Meldung (Winuser. h)
description: Eine Anwendung sendet eine CB \_ seteditsel-Meldung, um Zeichen im Bearbeitungs Steuerelement eines Kombinations Felds auszuwählen.
ms.assetid: 25a07341-a21c-42a9-a220-62650997757b
keywords:
- Windows-Steuerelemente für CB_SETEDITSEL Meldung
topic_type:
- apiref
api_name:
- CB_SETEDITSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a54e09697e266b4e0c4260104e90f454a5e3edfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476632"
---
# <a name="cb_seteditsel-message"></a><span data-ttu-id="72391-104">CB-nach \_ richten-Nachricht</span><span class="sxs-lookup"><span data-stu-id="72391-104">CB\_SETEDITSEL message</span></span>

<span data-ttu-id="72391-105">Eine Anwendung sendet eine **CB \_ seteditsel** -Meldung, um Zeichen im Bearbeitungs Steuerelement eines Kombinations Felds auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="72391-105">An application sends a **CB\_SETEDITSEL** message to select characters in the edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="72391-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="72391-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72391-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="72391-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="72391-108">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="72391-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="72391-109">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72391-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72391-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) von *LPARAM* gibt die Anfangsposition an.</span><span class="sxs-lookup"><span data-stu-id="72391-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of *lParam* specifies the starting position.</span></span> <span data-ttu-id="72391-111">Wenn das **LoWord** -1 ist, wird die Auswahl ggf. entfernt.</span><span class="sxs-lookup"><span data-stu-id="72391-111">If the **LOWORD** is -1, the selection, if any, is removed.</span></span>

<span data-ttu-id="72391-112">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) von *LPARAM* gibt die Endposition an.</span><span class="sxs-lookup"><span data-stu-id="72391-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of *lParam* specifies the ending position.</span></span> <span data-ttu-id="72391-113">Wenn das **HIWORD** -1 ist, wird der gesamte Text von der Anfangsposition bis zum letzten Zeichen im Bearbeitungs Steuerelement ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="72391-113">If the **HIWORD** is -1, all text from the starting position to the last character in the edit control is selected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72391-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="72391-114">Return value</span></span>

<span data-ttu-id="72391-115">Wenn die Nachricht erfolgreich ist, ist der Rückgabewert " **true**".</span><span class="sxs-lookup"><span data-stu-id="72391-115">If the message succeeds, the return value is **TRUE**.</span></span> <span data-ttu-id="72391-116">Wenn die Nachricht an ein Kombinations Feld mit dem Format " [**CBS \_ DropDownList**](combo-box-styles.md) " gesendet wird, ist es CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="72391-116">If the message is sent to a combo box with the [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="72391-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72391-117">Remarks</span></span>

<span data-ttu-id="72391-118">Die Positionen sind NULL basiert.</span><span class="sxs-lookup"><span data-stu-id="72391-118">The positions are zero-based.</span></span> <span data-ttu-id="72391-119">Das erste Zeichen des Bearbeitungs Steuer Elements befindet sich an der Nullposition.</span><span class="sxs-lookup"><span data-stu-id="72391-119">The first character of the edit control is in the zero position.</span></span> <span data-ttu-id="72391-120">Das erste Zeichen nach dem letzten ausgewählten Zeichen befindet sich an der Endposition.</span><span class="sxs-lookup"><span data-stu-id="72391-120">The first character after the last selected character is in the ending position.</span></span> <span data-ttu-id="72391-121">Wenn Sie z. b. die ersten vier Zeichen des Bearbeitungs Steuer Elements auswählen möchten, verwenden Sie die Startposition 0 und die Endposition 4.</span><span class="sxs-lookup"><span data-stu-id="72391-121">For example, to select the first four characters of the edit control, use a starting position of 0 and an ending position of 4.</span></span>

## <a name="requirements"></a><span data-ttu-id="72391-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72391-122">Requirements</span></span>



| <span data-ttu-id="72391-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72391-123">Requirement</span></span> | <span data-ttu-id="72391-124">Wert</span><span class="sxs-lookup"><span data-stu-id="72391-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72391-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="72391-125">Minimum supported client</span></span><br/> | <span data-ttu-id="72391-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72391-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="72391-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="72391-127">Minimum supported server</span></span><br/> | <span data-ttu-id="72391-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72391-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="72391-129">Header</span><span class="sxs-lookup"><span data-stu-id="72391-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="72391-130"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="72391-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72391-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72391-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="72391-132">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="72391-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="72391-133">**CB \_ geteditsel**</span><span class="sxs-lookup"><span data-stu-id="72391-133">**CB\_GETEDITSEL**</span></span>](cb-geteditsel.md)
</dt> <dt>

<span data-ttu-id="72391-134">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="72391-134">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="72391-135">**Makelparam**</span><span class="sxs-lookup"><span data-stu-id="72391-135">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

