---
title: EM_SELECTIONTYPE Meldung (RichEdit. h)
description: Bestimmt den Auswahltyp für ein Rich-Edit-Steuerelement.
ms.assetid: a4200e32-1056-47bd-be47-5fabaf99c058
keywords:
- Windows-Steuerelemente für EM_SELECTIONTYPE Meldung
topic_type:
- apiref
api_name:
- EM_SELECTIONTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0deb62ac3bf774c72bb076f6fce9aa8c77b423f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518683"
---
# <a name="em_selectiontype-message"></a><span data-ttu-id="8f00a-104">EM \_ SelectionType-Meldung</span><span class="sxs-lookup"><span data-stu-id="8f00a-104">EM\_SELECTIONTYPE message</span></span>

<span data-ttu-id="8f00a-105">Bestimmt den Auswahltyp für ein Rich-Edit-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="8f00a-105">Determines the selection type for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8f00a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f00a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f00a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8f00a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f00a-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="8f00a-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8f00a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8f00a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f00a-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="8f00a-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f00a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8f00a-111">Return value</span></span>

<span data-ttu-id="8f00a-112">Wenn die Auswahl leer ist, ist SEL Empty der Rückgabewert \_ .</span><span class="sxs-lookup"><span data-stu-id="8f00a-112">If the selection is empty, the return value is SEL\_EMPTY.</span></span>

<span data-ttu-id="8f00a-113">Wenn die Auswahl nicht leer ist, ist der Rückgabewert ein Satz von Flags, der einen oder mehrere der folgenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="8f00a-113">If the selection is not empty, the return value is a set of flags containing one or more of the following values.</span></span>



| <span data-ttu-id="8f00a-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="8f00a-114">Return code</span></span>                                                                                     | <span data-ttu-id="8f00a-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8f00a-115">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="8f00a-116"><dt>**SEL- \_ Text**</dt></span><span class="sxs-lookup"><span data-stu-id="8f00a-116"><dt>**SEL\_TEXT**</dt></span></span> </dl>        | <span data-ttu-id="8f00a-117">Text.</span><span class="sxs-lookup"><span data-stu-id="8f00a-117">Text.</span></span><br/>                            |
| <dl> <span data-ttu-id="8f00a-118"><dt>**SEL- \_ Objekt**</dt></span><span class="sxs-lookup"><span data-stu-id="8f00a-118"><dt>**SEL\_OBJECT**</dt></span></span> </dl>      | <span data-ttu-id="8f00a-119">Mindestens ein COM-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8f00a-119">At least one COM object.</span></span><br/>         |
| <dl> <span data-ttu-id="8f00a-120"><dt>**SEL \_ multichar**</dt></span><span class="sxs-lookup"><span data-stu-id="8f00a-120"><dt>**SEL\_MULTICHAR**</dt></span></span> </dl>   | <span data-ttu-id="8f00a-121">Mehr als ein Textzeichen.</span><span class="sxs-lookup"><span data-stu-id="8f00a-121">More than one character of text.</span></span><br/> |
| <dl> <span data-ttu-id="8f00a-122"><dt>**SEL- \_ Multiobject**</dt></span><span class="sxs-lookup"><span data-stu-id="8f00a-122"><dt>**SEL\_MULTIOBJECT**</dt></span></span> </dl> | <span data-ttu-id="8f00a-123">Mehr als ein COM-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8f00a-123">More than one COM object.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="8f00a-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8f00a-124">Remarks</span></span>

<span data-ttu-id="8f00a-125">Diese Meldung ist während der Verarbeitung der [**WM- \_ Größe**](/windows/desktop/winmsg/wm-size) für das übergeordnete Element eines untersten Rich-Edit-Steuer Elements nützlich.</span><span class="sxs-lookup"><span data-stu-id="8f00a-125">This message is useful during [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) processing for the parent of a bottomless rich edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f00a-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f00a-126">Requirements</span></span>



| <span data-ttu-id="8f00a-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8f00a-127">Requirement</span></span> | <span data-ttu-id="8f00a-128">Wert</span><span class="sxs-lookup"><span data-stu-id="8f00a-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8f00a-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8f00a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8f00a-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8f00a-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8f00a-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8f00a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8f00a-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8f00a-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8f00a-133">Header</span><span class="sxs-lookup"><span data-stu-id="8f00a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f00a-134"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f00a-134"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f00a-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f00a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f00a-136">**WM- \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="8f00a-136">**WM\_SIZE**</span></span>](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

