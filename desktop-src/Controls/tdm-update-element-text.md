---
title: TDM_UPDATE_ELEMENT_TEXT (Commctrl.h)
description: 'TDM_UPDATE_ELEMENT_TEXT Meldung: Aktualisiert ein Textelement in einem Aufgabendialogfeld.'
ms.assetid: 2df446c8-db87-42b5-b5bd-40fadbf9d45b
keywords:
- TDM_UPDATE_ELEMENT_TEXT Meldung Windows-Steuerelemente
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
ms.openlocfilehash: c155b426b92645c0b9cdbabe00c44ffa722b89f3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085808"
---
# <a name="tdm_update_element_text-message"></a><span data-ttu-id="5b422-104">TDM \_ UPDATE ELEMENT TEXT \_ \_ message</span><span class="sxs-lookup"><span data-stu-id="5b422-104">TDM\_UPDATE\_ELEMENT\_TEXT message</span></span>

<span data-ttu-id="5b422-105">Aktualisiert ein Textelement in einem Aufgabendialogfeld.</span><span class="sxs-lookup"><span data-stu-id="5b422-105">Updates a text element in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="5b422-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b422-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b422-107">*wParam* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5b422-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b422-108">Gibt das zu aktualisierende Element an.</span><span class="sxs-lookup"><span data-stu-id="5b422-108">Indicates the element to update.</span></span> <span data-ttu-id="5b422-109">(Eine Abbildung der Elemente finden Sie unter [Informationen zu Taskdialogfeldern.)](task-dialogs-overview.md) Dieser Parameter muss einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="5b422-109">(For an illustration of the elements, see [About Task Dialogs](task-dialogs-overview.md).) This parameter must be one of the following values:</span></span>



| <span data-ttu-id="5b422-110">Wert</span><span class="sxs-lookup"><span data-stu-id="5b422-110">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="5b422-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5b422-111">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <span data-ttu-id="5b422-112"><dt>**\_TDE-INHALT**</dt></span><span class="sxs-lookup"><span data-stu-id="5b422-112"><dt>**TDE\_CONTENT**</dt></span></span> </dl>                                         | <span data-ttu-id="5b422-113">Inhalt.</span><span class="sxs-lookup"><span data-stu-id="5b422-113">Content.</span></span><br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <span data-ttu-id="5b422-114"><dt>**ERWEITERTE \_ \_ TDE-INFORMATIONEN**</dt></span><span class="sxs-lookup"><span data-stu-id="5b422-114"><dt>**TDE\_EXPANDED\_INFORMATION**</dt></span></span> </dl> | <span data-ttu-id="5b422-115">Erweiterte Informationen.</span><span class="sxs-lookup"><span data-stu-id="5b422-115">Expanded information.</span></span><br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <span data-ttu-id="5b422-116"><dt>**\_TDE-FUßZEILE**</dt></span><span class="sxs-lookup"><span data-stu-id="5b422-116"><dt>**TDE\_FOOTER**</dt></span></span> </dl>                                            | <span data-ttu-id="5b422-117">Fußzeilentext.</span><span class="sxs-lookup"><span data-stu-id="5b422-117">Footer text.</span></span><br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <span data-ttu-id="5b422-118"><dt>**TDE \_ \_ MAIN-ANWEISUNG**</dt></span><span class="sxs-lookup"><span data-stu-id="5b422-118"><dt>**TDE\_MAIN\_INSTRUCTION**</dt></span></span> </dl>             | <span data-ttu-id="5b422-119">Main-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="5b422-119">Main instruction.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="5b422-120">*lParam* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5b422-120">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b422-121">Zeiger auf eine Unicode-Zeichenfolge, die den neuen Text enthält.</span><span class="sxs-lookup"><span data-stu-id="5b422-121">Pointer to a Unicode string that contains the new text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b422-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5b422-122">Return value</span></span>

<span data-ttu-id="5b422-123">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5b422-123">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b422-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b422-124">Remarks</span></span>

<span data-ttu-id="5b422-125">Um Clipping zu vermeiden, darf der neue Text nicht mehr als der vorhandene Text sein.</span><span class="sxs-lookup"><span data-stu-id="5b422-125">To avoid clipping, the new text must be no longer than the existing text.</span></span> <span data-ttu-id="5b422-126">Das Festlegen des Texts auf eine kürzere Zeichenfolge führt nicht dazu, dass die Größe des Dialogfelds geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5b422-126">Setting the text to a shorter string does not cause the dialog box to resize.</span></span>

<span data-ttu-id="5b422-127">Wenn der **pszExpandedInformation-Member** der [**TASKDIALOGCONFIG-Struktur,**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) der zum Erstellen des Aufgabendialogfelds verwendet wurde, **NULL** war und Sie eine **TDM \_ UPDATE ELEMENT \_ \_ TEXT-Nachricht** mit TDE \_ EXPANDED INFORMATION \_ senden, geschieht nichts.</span><span class="sxs-lookup"><span data-stu-id="5b422-127">If the **pszExpandedInformation** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog was **NULL**, and you send a **TDM\_UPDATE\_ELEMENT\_TEXT** message with TDE\_EXPANDED\_INFORMATION, nothing will happen.</span></span>

<span data-ttu-id="5b422-128">Das obige Gilt gilt auch für die Fußzeile und die \_ TDE-FUßZEILE.</span><span class="sxs-lookup"><span data-stu-id="5b422-128">The above also applies to the footer and TDE\_FOOTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b422-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b422-129">Requirements</span></span>



| <span data-ttu-id="5b422-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b422-130">Requirement</span></span> | <span data-ttu-id="5b422-131">Wert</span><span class="sxs-lookup"><span data-stu-id="5b422-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b422-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5b422-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5b422-133">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5b422-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5b422-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5b422-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5b422-135">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5b422-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5b422-136">Header</span><span class="sxs-lookup"><span data-stu-id="5b422-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b422-137"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="5b422-137"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b422-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5b422-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b422-139">**TDM \_ \_ SET-ELEMENTTEXT \_**</span><span class="sxs-lookup"><span data-stu-id="5b422-139">**TDM\_SET\_ELEMENT\_TEXT**</span></span>](tdm-set-element-text.md)
</dt> </dl>

 

 





