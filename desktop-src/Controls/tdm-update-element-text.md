---
title: TDM_UPDATE_ELEMENT_TEXT Meldung (kommstrg. h)
description: Aktualisiert ein Textelement in einem Aufgaben Dialogfeld.
ms.assetid: 2df446c8-db87-42b5-b5bd-40fadbf9d45b
keywords:
- Windows-Steuerelemente für TDM_UPDATE_ELEMENT_TEXT Meldung
topic_type:
- apiref
api_name:
- TDM_UPDATE_ELEMENT_TEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6dac6787c68d0cbe619bbf28fa1a6383606e99f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106245"
---
# <a name="tdm_update_element_text-message"></a><span data-ttu-id="cfa52-104">TDM- \_ Aktualisierungs \_ Element- \_ Text Nachricht</span><span class="sxs-lookup"><span data-stu-id="cfa52-104">TDM\_UPDATE\_ELEMENT\_TEXT message</span></span>

<span data-ttu-id="cfa52-105">Aktualisiert ein Textelement in einem Aufgaben Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="cfa52-105">Updates a text element in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="cfa52-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cfa52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfa52-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cfa52-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfa52-108">Gibt das zu Aktualisier Endes Element an.</span><span class="sxs-lookup"><span data-stu-id="cfa52-108">Indicates the element to update.</span></span> <span data-ttu-id="cfa52-109">(Eine Abbildung der Elemente finden Sie unter [Informationen zu Aufgaben Dialogfeldern](task-dialogs-overview.md).) Dieser Parameter muss einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="cfa52-109">(For an illustration of the elements, see [About Task Dialogs](task-dialogs-overview.md).) This parameter must be one of the following values:</span></span>



| <span data-ttu-id="cfa52-110">Wert</span><span class="sxs-lookup"><span data-stu-id="cfa52-110">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="cfa52-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cfa52-111">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <span data-ttu-id="cfa52-112"><dt>**TDE- \_ Inhalt**</dt></span><span class="sxs-lookup"><span data-stu-id="cfa52-112"><dt>**TDE\_CONTENT**</dt></span></span> </dl>                                         | <span data-ttu-id="cfa52-113">Inhalt.</span><span class="sxs-lookup"><span data-stu-id="cfa52-113">Content.</span></span><br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <span data-ttu-id="cfa52-114"><dt>**\_Erweiterte Informationen zu TDE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cfa52-114"><dt>**TDE\_EXPANDED\_INFORMATION**</dt></span></span> </dl> | <span data-ttu-id="cfa52-115">Erweiterte Informationen.</span><span class="sxs-lookup"><span data-stu-id="cfa52-115">Expanded information.</span></span><br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <span data-ttu-id="cfa52-116"><dt>**TDE- \_ Fußzeile**</dt></span><span class="sxs-lookup"><span data-stu-id="cfa52-116"><dt>**TDE\_FOOTER**</dt></span></span> </dl>                                            | <span data-ttu-id="cfa52-117">FooterText.</span><span class="sxs-lookup"><span data-stu-id="cfa52-117">Footer text.</span></span><br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <span data-ttu-id="cfa52-118"><dt>**TDE- \_ Haupt \_ Anweisung**</dt></span><span class="sxs-lookup"><span data-stu-id="cfa52-118"><dt>**TDE\_MAIN\_INSTRUCTION**</dt></span></span> </dl>             | <span data-ttu-id="cfa52-119">Main-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="cfa52-119">Main instruction.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="cfa52-120">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cfa52-120">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfa52-121">Zeiger auf eine Unicode-Zeichenfolge, die den neuen Text enthält.</span><span class="sxs-lookup"><span data-stu-id="cfa52-121">Pointer to a Unicode string that contains the new text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfa52-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cfa52-122">Return value</span></span>

<span data-ttu-id="cfa52-123">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="cfa52-123">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfa52-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cfa52-124">Remarks</span></span>

<span data-ttu-id="cfa52-125">Der neue Text darf nicht länger als der vorhandene Text sein, um das Abschneiden zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="cfa52-125">To avoid clipping, the new text must be no longer than the existing text.</span></span> <span data-ttu-id="cfa52-126">Wenn Sie den Text auf eine kürzere Zeichenfolge festlegen, wird die Größe des Dialog Felds nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="cfa52-126">Setting the text to a shorter string does not cause the dialog box to resize.</span></span>

<span data-ttu-id="cfa52-127">Wenn der **pszexpandedinformation** -Member der [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) -Struktur, die zum Erstellen des Aufgaben Dialogfelds verwendet wurde, **null** war und Sie eine **TDM- \_ Aktualisierungs \_ Element- \_ Text** Nachricht mit erweiterten TDE- \_ Informationen senden \_ , geschieht nichts.</span><span class="sxs-lookup"><span data-stu-id="cfa52-127">If the **pszExpandedInformation** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog was **NULL**, and you send a **TDM\_UPDATE\_ELEMENT\_TEXT** message with TDE\_EXPANDED\_INFORMATION, nothing will happen.</span></span>

<span data-ttu-id="cfa52-128">Das obige gilt auch für die Fußzeile und den TDE- \_ Fußzeile.</span><span class="sxs-lookup"><span data-stu-id="cfa52-128">The above also applies to the footer and TDE\_FOOTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfa52-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfa52-129">Requirements</span></span>



| <span data-ttu-id="cfa52-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cfa52-130">Requirement</span></span> | <span data-ttu-id="cfa52-131">Wert</span><span class="sxs-lookup"><span data-stu-id="cfa52-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cfa52-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cfa52-132">Minimum supported client</span></span><br/> | <span data-ttu-id="cfa52-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cfa52-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cfa52-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cfa52-134">Minimum supported server</span></span><br/> | <span data-ttu-id="cfa52-135">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cfa52-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cfa52-136">Header</span><span class="sxs-lookup"><span data-stu-id="cfa52-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfa52-137"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfa52-137"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfa52-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfa52-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfa52-139">**TDM \_ - \_ Element \_ Text festlegen**</span><span class="sxs-lookup"><span data-stu-id="cfa52-139">**TDM\_SET\_ELEMENT\_TEXT**</span></span>](tdm-set-element-text.md)
</dt> </dl>

 

 





