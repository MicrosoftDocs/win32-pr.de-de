---
title: EM_GETFILELINECOUNT Meldung (kommstrg. h)
description: Ruft die Anzahl der Zeilen in einem mehrzeiligen Bearbeitungs Steuerelement ab, unabhängig davon, wie Linien auf dem Bildschirm angezeigt werden.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- Windows-Steuerelemente für EM_GETFILELINECOUNT Meldung
topic_type:
- apiref
api_name:
- EM_GETFILELINECOUNT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: bf48b3abeb10b98bf0c22a7dd2ef93c73a2a59c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104834"
---
# <a name="em_getfilelinecount-message-commctrlh"></a><span data-ttu-id="15678-104">EM_GETFILELINECOUNT Meldung (kommstrg. h)</span><span class="sxs-lookup"><span data-stu-id="15678-104">EM_GETFILELINECOUNT message (CommCtrl.h)</span></span>

<span data-ttu-id="15678-105">Ruft die Anzahl der Zeilen in einem mehrzeiligen Bearbeitungs Steuerelement ab, unabhängig davon, wie Linien auf dem Bildschirm angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="15678-105">Gets the number of lines in a multiline edit control, independently of how lines are displayed on the screen.</span></span>

## <a name="parameters"></a><span data-ttu-id="15678-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="15678-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15678-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="15678-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15678-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="15678-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="15678-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="15678-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15678-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="15678-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15678-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="15678-111">Return value</span></span>

<span data-ttu-id="15678-112">Der Rückgabewert ist eine ganze Zahl, die die Gesamtzahl der Textzeilen im mehrzeiligen Bearbeitungs Steuerelement angibt, unabhängig davon, wie Linien auf dem Bildschirm angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="15678-112">The return value is an integer specifying the total number of text lines in the multiline edit control, independently of how lines are displayed on the screen.</span></span> <span data-ttu-id="15678-113">Wenn das Steuerelement keinen Text hat, ist der Rückgabewert 1.</span><span class="sxs-lookup"><span data-stu-id="15678-113">If the control has no text, the return value is 1.</span></span> <span data-ttu-id="15678-114">Der Rückgabewert ist nie kleiner als 1.</span><span class="sxs-lookup"><span data-stu-id="15678-114">The return value will never be less than 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="15678-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15678-115">Remarks</span></span>

<span data-ttu-id="15678-116">Die **EM \_ getfilelinecount** -Nachricht Ruft die Gesamtanzahl von Textzeilen ab, unabhängig davon, wie Zeilen auf dem Bildschirm angezeigt werden, nicht nur die Anzahl der zurzeit sichtbaren Zeilen.</span><span class="sxs-lookup"><span data-stu-id="15678-116">The **EM\_GETFILELINECOUNT** message retrieves the total number of text lines, independently of how lines are displayed on the screen, not just the number of lines that are currently visible.</span></span>

<span data-ttu-id="15678-117">Der Zeilenumbruch ändert nicht die Anzahl der Zeilen, die von dieser Nachricht zurückgegeben werden, da diese Nachricht unabhängig davon funktioniert, wie Zeilen auf dem Bildschirm angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="15678-117">Word-wrap does not change the number of lines this message returns, as this message works independently of how lines are displayed on the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="15678-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15678-118">Requirements</span></span>



| <span data-ttu-id="15678-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15678-119">Requirement</span></span> | <span data-ttu-id="15678-120">Wert</span><span class="sxs-lookup"><span data-stu-id="15678-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15678-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="15678-121">Minimum supported client</span></span><br/> | <span data-ttu-id="15678-122">Nur Windows 10, 1809 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15678-122">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="15678-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="15678-123">Minimum supported server</span></span><br/> | <span data-ttu-id="15678-124">Nur Windows Server 2019 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15678-124">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="15678-125">Header</span><span class="sxs-lookup"><span data-stu-id="15678-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="15678-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="15678-126"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15678-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15678-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="15678-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="15678-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="15678-129">**EM \_ getfileline**</span><span class="sxs-lookup"><span data-stu-id="15678-129">**EM\_GETFILELINE**</span></span>](em-getfileline.md)
</dt> <dt>

[<span data-ttu-id="15678-130">**EM \_ filelinelength**</span><span class="sxs-lookup"><span data-stu-id="15678-130">**EM\_FILELINELENGTH**</span></span>](em-filelinelength.md)
</dt> <dt>

[<span data-ttu-id="15678-131">**" \_ Getfilelinecount" Bearbeiten**</span><span class="sxs-lookup"><span data-stu-id="15678-131">**Edit\_GetFileLineCount**</span></span>](/windows/win32/api/commctrl/nf-commctrl-edit_getfilelinecount)
</dt> </dl>

 

 





