---
title: TDM_SET_ELEMENT_TEXT (Commctrl.h)
description: 'TDM_SET_ELEMENT_TEXT Meldung: Aktualisiert ein Textelement in einem Aufgabendialogfeld.'
ms.assetid: e3f15805-5d48-4549-9959-69ec01345e57
keywords:
- TDM_SET_ELEMENT_TEXT Meldung Windows-Steuerelemente
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
ms.openlocfilehash: c6d0c8830a6d8a1057ab283a9e096434a6184151
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104028"
---
# <a name="tdm_set_element_text-message"></a><span data-ttu-id="8cf7e-104">TDM \_ SET \_ ELEMENT \_ TEXT-Meldung</span><span class="sxs-lookup"><span data-stu-id="8cf7e-104">TDM\_SET\_ELEMENT\_TEXT message</span></span>

<span data-ttu-id="8cf7e-105">Aktualisiert ein Textelement in einem Aufgabendialogfeld.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-105">Updates a text element in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="8cf7e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cf7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cf7e-107">*wParam* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8cf7e-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cf7e-108">Gibt das zu aktualisierende Element an.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-108">Indicates the element to update.</span></span> <span data-ttu-id="8cf7e-109">(Eine Abbildung finden Sie unter [Informationen zu Taskdialogfeldern.)](task-dialogs-overview.md) Dieser Parameter muss einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-109">(For an illustration, see [About Task Dialogs](task-dialogs-overview.md).) This parameter must be one of the following values.</span></span>



| <span data-ttu-id="8cf7e-110">Wert</span><span class="sxs-lookup"><span data-stu-id="8cf7e-110">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="8cf7e-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8cf7e-111">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <span data-ttu-id="8cf7e-112"><dt>**\_TDE-INHALT**</dt></span><span class="sxs-lookup"><span data-stu-id="8cf7e-112"><dt>**TDE\_CONTENT**</dt></span></span> </dl>                                         | <span data-ttu-id="8cf7e-113">Inhalt.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-113">Content.</span></span><br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <span data-ttu-id="8cf7e-114"><dt>**ERWEITERTE \_ \_ TDE-INFORMATIONEN**</dt></span><span class="sxs-lookup"><span data-stu-id="8cf7e-114"><dt>**TDE\_EXPANDED\_INFORMATION**</dt></span></span> </dl> | <span data-ttu-id="8cf7e-115">Erweiterte Informationen.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-115">Expanded information.</span></span><br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <span data-ttu-id="8cf7e-116"><dt>**\_TDE-FUßZEILE**</dt></span><span class="sxs-lookup"><span data-stu-id="8cf7e-116"><dt>**TDE\_FOOTER**</dt></span></span> </dl>                                            | <span data-ttu-id="8cf7e-117">Fußzeilentext.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-117">Footer text.</span></span><br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <span data-ttu-id="8cf7e-118"><dt>**TDE \_ \_ MAIN-ANWEISUNG**</dt></span><span class="sxs-lookup"><span data-stu-id="8cf7e-118"><dt>**TDE\_MAIN\_INSTRUCTION**</dt></span></span> </dl>             | <span data-ttu-id="8cf7e-119">Main-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-119">Main instruction.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="8cf7e-120">*lParam* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8cf7e-120">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cf7e-121">Der zu verwendende neue Text.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-121">The new text to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cf7e-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8cf7e-122">Return value</span></span>

<span data-ttu-id="8cf7e-123">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-123">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cf7e-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8cf7e-124">Remarks</span></span>

<span data-ttu-id="8cf7e-125">Die Größe oder das Layout des Aufgabendialogfelds kann sich ändern, um den neuen Text zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8cf7e-125">The size or layout of the task dialog may change to accommodate the new text.</span></span>

## <a name="examples"></a><span data-ttu-id="8cf7e-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8cf7e-126">Examples</span></span>

<span data-ttu-id="8cf7e-127">Der folgende Beispielcode zeigt, wie der Fußzeilentext im Aufgabendialogfeld festgelegt wird, das durch *hwnd dargestellt wird.*</span><span class="sxs-lookup"><span data-stu-id="8cf7e-127">The following example code shows how to set the footer text in the task dialog represented by *hwnd*.</span></span>


```C++
SendMessage(hwnd, TDM_SET_ELEMENT_TEXT, (WPARAM)TDE_FOOTER, (LPARAM)L"New footer text.");
```



## <a name="requirements"></a><span data-ttu-id="8cf7e-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8cf7e-128">Requirements</span></span>



| <span data-ttu-id="8cf7e-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8cf7e-129">Requirement</span></span> | <span data-ttu-id="8cf7e-130">Wert</span><span class="sxs-lookup"><span data-stu-id="8cf7e-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8cf7e-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8cf7e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8cf7e-132">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8cf7e-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8cf7e-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8cf7e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8cf7e-134">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8cf7e-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8cf7e-135">Header</span><span class="sxs-lookup"><span data-stu-id="8cf7e-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cf7e-136"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="8cf7e-136"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cf7e-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8cf7e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cf7e-138">**TDM \_ \_ UPDATE-ELEMENTTEXT \_**</span><span class="sxs-lookup"><span data-stu-id="8cf7e-138">**TDM\_UPDATE\_ELEMENT\_TEXT**</span></span>](tdm-update-element-text.md)
</dt> </dl>

 

 





