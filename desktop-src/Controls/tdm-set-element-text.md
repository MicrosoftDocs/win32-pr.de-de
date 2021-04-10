---
title: TDM_SET_ELEMENT_TEXT Meldung (kommstrg. h)
description: Aktualisiert ein Textelement in einem Aufgaben Dialogfeld.
ms.assetid: e3f15805-5d48-4549-9959-69ec01345e57
keywords:
- Windows-Steuerelemente für TDM_SET_ELEMENT_TEXT Meldung
topic_type:
- apiref
api_name:
- TDM_SET_ELEMENT_TEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2229dc269f14c9a3b0765675dcc97dc9776b72c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040945"
---
# <a name="tdm_set_element_text-message"></a><span data-ttu-id="56d21-104">TDM \_ - \_ Element \_ Text Nachricht</span><span class="sxs-lookup"><span data-stu-id="56d21-104">TDM\_SET\_ELEMENT\_TEXT message</span></span>

<span data-ttu-id="56d21-105">Aktualisiert ein Textelement in einem Aufgaben Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="56d21-105">Updates a text element in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="56d21-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="56d21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56d21-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="56d21-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56d21-108">Gibt das zu Aktualisier Endes Element an.</span><span class="sxs-lookup"><span data-stu-id="56d21-108">Indicates the element to update.</span></span> <span data-ttu-id="56d21-109">(Eine Abbildung finden Sie unter [Informationen zu Aufgaben Dialogfeldern](task-dialogs-overview.md).) Dieser Parameter muss einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="56d21-109">(For an illustration, see [About Task Dialogs](task-dialogs-overview.md).) This parameter must be one of the following values.</span></span>



| <span data-ttu-id="56d21-110">Wert</span><span class="sxs-lookup"><span data-stu-id="56d21-110">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="56d21-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="56d21-111">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <span data-ttu-id="56d21-112"><dt>**TDE- \_ Inhalt**</dt></span><span class="sxs-lookup"><span data-stu-id="56d21-112"><dt>**TDE\_CONTENT**</dt></span></span> </dl>                                         | <span data-ttu-id="56d21-113">Inhalt.</span><span class="sxs-lookup"><span data-stu-id="56d21-113">Content.</span></span><br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <span data-ttu-id="56d21-114"><dt>**\_Erweiterte Informationen zu TDE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="56d21-114"><dt>**TDE\_EXPANDED\_INFORMATION**</dt></span></span> </dl> | <span data-ttu-id="56d21-115">Erweiterte Informationen.</span><span class="sxs-lookup"><span data-stu-id="56d21-115">Expanded information.</span></span><br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <span data-ttu-id="56d21-116"><dt>**TDE- \_ Fußzeile**</dt></span><span class="sxs-lookup"><span data-stu-id="56d21-116"><dt>**TDE\_FOOTER**</dt></span></span> </dl>                                            | <span data-ttu-id="56d21-117">FooterText.</span><span class="sxs-lookup"><span data-stu-id="56d21-117">Footer text.</span></span><br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <span data-ttu-id="56d21-118"><dt>**TDE- \_ Haupt \_ Anweisung**</dt></span><span class="sxs-lookup"><span data-stu-id="56d21-118"><dt>**TDE\_MAIN\_INSTRUCTION**</dt></span></span> </dl>             | <span data-ttu-id="56d21-119">Main-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="56d21-119">Main instruction.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="56d21-120">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="56d21-120">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56d21-121">Der zu verwendende neue Text.</span><span class="sxs-lookup"><span data-stu-id="56d21-121">The new text to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56d21-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56d21-122">Return value</span></span>

<span data-ttu-id="56d21-123">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="56d21-123">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="56d21-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56d21-124">Remarks</span></span>

<span data-ttu-id="56d21-125">Die Größe oder das Layout des Aufgaben Dialogfelds kann geändert werden, um den neuen Text zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="56d21-125">The size or layout of the task dialog may change to accommodate the new text.</span></span>

## <a name="examples"></a><span data-ttu-id="56d21-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="56d21-126">Examples</span></span>

<span data-ttu-id="56d21-127">Der folgende Beispielcode zeigt, wie der FooterText im Aufgaben Dialogfeld festgelegt wird, das durch *HWND* dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="56d21-127">The following example code shows how to set the footer text in the task dialog represented by *hwnd*.</span></span>


```C++
SendMessage(hwnd, TDM_SET_ELEMENT_TEXT, (WPARAM)TDE_FOOTER, (LPARAM)L"New footer text.");
```



## <a name="requirements"></a><span data-ttu-id="56d21-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56d21-128">Requirements</span></span>



| <span data-ttu-id="56d21-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56d21-129">Requirement</span></span> | <span data-ttu-id="56d21-130">Wert</span><span class="sxs-lookup"><span data-stu-id="56d21-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56d21-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="56d21-131">Minimum supported client</span></span><br/> | <span data-ttu-id="56d21-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56d21-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="56d21-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="56d21-133">Minimum supported server</span></span><br/> | <span data-ttu-id="56d21-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56d21-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56d21-135">Header</span><span class="sxs-lookup"><span data-stu-id="56d21-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="56d21-136"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="56d21-136"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56d21-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56d21-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56d21-138">**TDM- \_ Aktualisierungs \_ Element \_ Text**</span><span class="sxs-lookup"><span data-stu-id="56d21-138">**TDM\_UPDATE\_ELEMENT\_TEXT**</span></span>](tdm-update-element-text.md)
</dt> </dl>

 

 





