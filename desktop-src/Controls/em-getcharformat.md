---
title: EM_GETCHARFORMAT Meldung (RichEdit. h)
description: Bestimmt die Zeichen Formatierung in einem Rich-Edit-Steuerelement.
ms.assetid: 210b8719-5ed7-49f2-bd93-8a4e1efab1e8
keywords:
- Windows-Steuerelemente für EM_GETCHARFORMAT Meldung
topic_type:
- apiref
api_name:
- EM_GETCHARFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd71db4d3a13f2acfe33c2843b0d9aad46c6f9fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040692"
---
# <a name="em_getcharformat-message"></a><span data-ttu-id="ed804-104">EM \_ getcharformat-Meldung</span><span class="sxs-lookup"><span data-stu-id="ed804-104">EM\_GETCHARFORMAT message</span></span>

<span data-ttu-id="ed804-105">Bestimmt die Zeichen Formatierung in einem Rich-Edit-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="ed804-105">Determines the character formatting in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ed804-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed804-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed804-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ed804-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed804-108">Gibt den Textbereich an, aus dem die Formatierung abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ed804-108">Specifies the range of text from which to retrieve formatting.</span></span> <span data-ttu-id="ed804-109">Dieses Argument einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="ed804-109">It can be one of the following values.</span></span>



| <span data-ttu-id="ed804-110">Wert</span><span class="sxs-lookup"><span data-stu-id="ed804-110">Value</span></span>                                                                                                                                                         | <span data-ttu-id="ed804-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ed804-111">Meaning</span></span>                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <span data-ttu-id="ed804-112"><dt>**SCF- \_ Standard**</dt></span><span class="sxs-lookup"><span data-stu-id="ed804-112"><dt>**SCF\_DEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="ed804-113">Die Standard Zeichen Formatierung.</span><span class="sxs-lookup"><span data-stu-id="ed804-113">The default character formatting.</span></span><br/>             |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <span data-ttu-id="ed804-114"><dt>**SCF- \_ Auswahl**</dt></span><span class="sxs-lookup"><span data-stu-id="ed804-114"><dt>**SCF\_SELECTION**</dt></span></span> </dl> | <span data-ttu-id="ed804-115">Die Zeichen Formatierung der aktuellen Auswahl.</span><span class="sxs-lookup"><span data-stu-id="ed804-115">The current selection's character formatting.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ed804-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ed804-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed804-117">Eine [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) -Struktur, die die Attribute des ersten Zeichens empfängt.</span><span class="sxs-lookup"><span data-stu-id="ed804-117">A [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure that receives the attributes of the first character.</span></span> <span data-ttu-id="ed804-118">Der **dwMask** -Member gibt an, welche Attribute in der gesamten Auswahl konsistent sind.</span><span class="sxs-lookup"><span data-stu-id="ed804-118">The **dwMask** member specifies which attributes are consistent throughout the entire selection.</span></span> <span data-ttu-id="ed804-119">Wenn die gesamte Auswahl z. b. entweder kursiv oder nicht kursiv formatiert ist, wird cfm \_ Italic festgelegt. wenn die Auswahl teilweise kursiv und teilweise nicht ist, wird cfm \_ Italic nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ed804-119">For example, if the entire selection is either in italics or not in italics, CFM\_ITALIC is set; if the selection is partly in italics and partly not, CFM\_ITALIC is not set.</span></span>

<span data-ttu-id="ed804-120">Microsoft Rich Edit 2,0 und höher: dieser Parameter kann ein Zeiger auf eine [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) -Struktur sein, die eine Erweiterung der [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) -Struktur ist.</span><span class="sxs-lookup"><span data-stu-id="ed804-120">Microsoft Rich Edit 2.0 and later: This parameter can be a pointer to a [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) structure, which is an extension of the [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure.</span></span> <span data-ttu-id="ed804-121">Vor dem Senden der **EM \_ getcharformat** -Meldung legen Sie den **CBSIZE** -Member der Struktur so fest, dass die Version der Struktur angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ed804-121">Before sending the **EM\_GETCHARFORMAT** message, set the structure's **cbSize** member to indicate the version of the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed804-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed804-122">Return value</span></span>

<span data-ttu-id="ed804-123">Diese Meldung gibt den Wert des **dwMask** -Members der [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) -Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="ed804-123">This message returns the value of the **dwMask** member of the [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed804-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed804-124">Requirements</span></span>



| <span data-ttu-id="ed804-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed804-125">Requirement</span></span> | <span data-ttu-id="ed804-126">Wert</span><span class="sxs-lookup"><span data-stu-id="ed804-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed804-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed804-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ed804-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed804-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ed804-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed804-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ed804-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed804-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ed804-131">Header</span><span class="sxs-lookup"><span data-stu-id="ed804-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed804-132"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed804-132"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed804-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed804-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="ed804-134">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="ed804-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ed804-135">**Charformat**</span><span class="sxs-lookup"><span data-stu-id="ed804-135">**CHARFORMAT**</span></span>](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[<span data-ttu-id="ed804-136">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="ed804-136">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 





