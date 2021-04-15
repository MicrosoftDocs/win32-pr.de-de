---
title: EM_EXLIMITTEXT Meldung (RichEdit. h)
description: Legt eine Obergrenze für den Text fest, der vom Benutzer in ein Rich-Edit-Steuerelement eingefügt oder eingefügt werden kann.
ms.assetid: 66fcdbb9-99ac-4122-b89c-be4aef80fbae
keywords:
- Windows-Steuerelemente für EM_EXLIMITTEXT Meldung
topic_type:
- apiref
api_name:
- EM_EXLIMITTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c4ebb554e3aa3139a66ca63970356e1261a23f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477598"
---
# <a name="em_exlimittext-message"></a><span data-ttu-id="bff6f-104">EM \_ exlimittext-Nachricht</span><span class="sxs-lookup"><span data-stu-id="bff6f-104">EM\_EXLIMITTEXT message</span></span>

<span data-ttu-id="bff6f-105">Legt eine Obergrenze für den Text fest, der vom Benutzer in ein Rich-Edit-Steuerelement eingefügt oder eingefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="bff6f-105">Sets an upper limit to the amount of text the user can type or paste into a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="bff6f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bff6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bff6f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bff6f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bff6f-108">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="bff6f-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bff6f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bff6f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bff6f-110">Gibt die maximale Menge an Text an, die eingegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="bff6f-110">Specifies the maximum amount of text that can be entered.</span></span> <span data-ttu-id="bff6f-111">Wenn dieser Parameter NULL ist, wird das Standard Maximum verwendet, das 64 KB groß ist.</span><span class="sxs-lookup"><span data-stu-id="bff6f-111">If this parameter is zero, the default maximum is used, which is 64K characters.</span></span> <span data-ttu-id="bff6f-112">Ein COM-Objekt zählt als einzelnes Zeichen.</span><span class="sxs-lookup"><span data-stu-id="bff6f-112">A COM object counts as a single character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bff6f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bff6f-113">Return value</span></span>

<span data-ttu-id="bff6f-114">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="bff6f-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bff6f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bff6f-115">Remarks</span></span>

<span data-ttu-id="bff6f-116">Das durch die **EM \_ exlimittext** -Nachricht festgelegte Text Limit schränkt nicht die Menge an Text ein, die Sie in ein Rich-Edit-Steuerelement mithilfe der [**EM- \_ StreamIn**](em-streamin.md) -Nachricht streamen können, wobei *LPARAM* auf SF Text festgelegt ist \_ .</span><span class="sxs-lookup"><span data-stu-id="bff6f-116">The text limit set by the **EM\_EXLIMITTEXT** message does not limit the amount of text that you can stream into a rich edit control using the [**EM\_STREAMIN**](em-streamin.md) message with *lParam* set to SF\_TEXT.</span></span> <span data-ttu-id="bff6f-117">Allerdings wird die Menge des Texts, den Sie in ein Rich-Edit-Steuerelement streamen können, mithilfe der **EM- \_ StreamIn** -Nachricht mit *LPARAM* , die auf SF RTF festgelegt ist, eingeschränkt \_ .</span><span class="sxs-lookup"><span data-stu-id="bff6f-117">However, it does limit the amount of text that you can stream into a rich edit control using the **EM\_STREAMIN** message with *lParam* set to SF\_RTF.</span></span>

<span data-ttu-id="bff6f-118">Bevor **EM \_ exlimittext** aufgerufen wird, ist der Standard Grenzwert für die Text Menge, die ein Benutzer eingeben kann, 32.767 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="bff6f-118">Before **EM\_EXLIMITTEXT** is called, the default limit to the amount of text a user can enter is 32,767 characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="bff6f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bff6f-119">Requirements</span></span>



| <span data-ttu-id="bff6f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bff6f-120">Requirement</span></span> | <span data-ttu-id="bff6f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="bff6f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bff6f-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bff6f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bff6f-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bff6f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bff6f-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bff6f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bff6f-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bff6f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bff6f-126">Header</span><span class="sxs-lookup"><span data-stu-id="bff6f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bff6f-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bff6f-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bff6f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bff6f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bff6f-129">**EM- \_ StreamIn**</span><span class="sxs-lookup"><span data-stu-id="bff6f-129">**EM\_STREAMIN**</span></span>](em-streamin.md)
</dt> </dl>

 

 





