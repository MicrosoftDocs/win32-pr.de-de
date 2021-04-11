---
title: EM_SETBIDIOPTIONS Meldung (RichEdit. h)
description: Die \_ Meldung "gesetbidioptions" legt den aktuellen Status der bidirektionalen Optionen im Rich Edit-Steuerelement fest.
ms.assetid: b518e423-317a-4654-9d9f-c501028e2a0a
keywords:
- Windows-Steuerelemente für EM_SETBIDIOPTIONS Meldung
topic_type:
- apiref
api_name:
- EM_SETBIDIOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84dc4b92f7a989ab5ef283b36708094a143475de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105591"
---
# <a name="em_setbidioptions-message"></a><span data-ttu-id="1531e-104">EM \_ setbidioptions-Meldung</span><span class="sxs-lookup"><span data-stu-id="1531e-104">EM\_SETBIDIOPTIONS message</span></span>

<span data-ttu-id="1531e-105">Die Meldung " **\_ gesetbidioptions** " legt den aktuellen Status der bidirektionalen Optionen im Rich Edit-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="1531e-105">The **EM\_SETBIDIOPTIONS** message sets the current state of the bidirectional options in the rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1531e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1531e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1531e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1531e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1531e-108">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1531e-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1531e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1531e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1531e-110">Zeiger auf eine [**bidioptions**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) -Struktur, die angibt, wie der Zustand der bidirektionalen Optionen im Rich Edit-Steuerelement festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="1531e-110">Pointer to a [**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) structure that indicates how to set the state of the bidirectional options in the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1531e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1531e-111">Return value</span></span>

<span data-ttu-id="1531e-112">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1531e-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1531e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1531e-113">Remarks</span></span>

<span data-ttu-id="1531e-114">Das Rich Edit-Steuerelement muss sich im nur-Text-Modus befinden, oder **EM \_ setbidioptions** führt nichts aus.</span><span class="sxs-lookup"><span data-stu-id="1531e-114">The rich edit control must be in plain text mode or **EM\_SETBIDIOPTIONS** will not do anything.</span></span>

<span data-ttu-id="1531e-115">Bei nur-Text-Steuerelementen bestimmt **EM \_ setbidioptions** automatisch die Absatz Richtung und/oder die Ausrichtung basierend auf den Kontextregeln.</span><span class="sxs-lookup"><span data-stu-id="1531e-115">In plain text controls, **EM\_SETBIDIOPTIONS** automatically determines the paragraph direction and/or alignment based on the context rules.</span></span> <span data-ttu-id="1531e-116">Diese Regeln geben an, dass die Richtung und/oder Ausrichtung vom ersten starken Zeichen im Steuerelement abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="1531e-116">These rules state that the direction and/or alignment is derived from the first strong character in the control.</span></span> <span data-ttu-id="1531e-117">Ein starkes Zeichen ist ein Zeichen, von dem die Textrichtung bestimmt werden kann (siehe Unicode-Standard Version 2,0).</span><span class="sxs-lookup"><span data-stu-id="1531e-117">A strong character is one from which text direction can be determined (see Unicode Standard version 2.0).</span></span> <span data-ttu-id="1531e-118">Die Absatz Richtung und/oder Ausrichtung wird auf das Standardformat angewendet.</span><span class="sxs-lookup"><span data-stu-id="1531e-118">The paragraph direction and/or alignment is applied to the default format.</span></span>

<span data-ttu-id="1531e-119">**EM \_ Setbidioptions** schaltet nur das Standard Absatzformat zu RTL (von rechts nach links), wenn ein RTL-Zeichen gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="1531e-119">**EM\_SETBIDIOPTIONS** only switches the default paragraph format to RTL (right to left) if it finds an RTL character,</span></span>

## <a name="requirements"></a><span data-ttu-id="1531e-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1531e-120">Requirements</span></span>



| <span data-ttu-id="1531e-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1531e-121">Requirement</span></span> | <span data-ttu-id="1531e-122">Wert</span><span class="sxs-lookup"><span data-stu-id="1531e-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1531e-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1531e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1531e-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1531e-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1531e-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1531e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1531e-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1531e-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1531e-127">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="1531e-127">Redistributable</span></span><br/>          | <span data-ttu-id="1531e-128">Rich Edit 3,0</span><span class="sxs-lookup"><span data-stu-id="1531e-128">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="1531e-129">Header</span><span class="sxs-lookup"><span data-stu-id="1531e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1531e-130"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1531e-130"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1531e-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1531e-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="1531e-132">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="1531e-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1531e-133">**Bidioptions**</span><span class="sxs-lookup"><span data-stu-id="1531e-133">**BIDIOPTIONS**</span></span>](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[<span data-ttu-id="1531e-134">**EM \_ getbidioptions**</span><span class="sxs-lookup"><span data-stu-id="1531e-134">**EM\_GETBIDIOPTIONS**</span></span>](em-getbidioptions.md)
</dt> </dl>

 

 





