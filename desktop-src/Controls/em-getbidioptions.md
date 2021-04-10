---
title: EM_GETBIDIOPTIONS Meldung (RichEdit. h)
description: Gibt den aktuellen Zustand der bidirektionalen Optionen im Rich Edit-Steuerelement an.
ms.assetid: 055581c0-ae59-4601-a3e9-416705af429a
keywords:
- Windows-Steuerelemente für EM_GETBIDIOPTIONS Meldung
topic_type:
- apiref
api_name:
- EM_GETBIDIOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fade63ac94007bedbf58642dc7a9451eb158fc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104048"
---
# <a name="em_getbidioptions-message"></a><span data-ttu-id="f8c03-104">EM \_ getbidioptions-Meldung</span><span class="sxs-lookup"><span data-stu-id="f8c03-104">EM\_GETBIDIOPTIONS message</span></span>

<span data-ttu-id="f8c03-105">Gibt den aktuellen Zustand der bidirektionalen Optionen im Rich Edit-Steuerelement an.</span><span class="sxs-lookup"><span data-stu-id="f8c03-105">Indicates the current state of the bidirectional options in the rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f8c03-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8c03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8c03-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8c03-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8c03-108">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="f8c03-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f8c03-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8c03-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8c03-110">Eine [**bidioptions**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) -Struktur, die den aktuellen Zustand der bidirektionalen Optionen im Rich Edit-Steuerelement empfängt.</span><span class="sxs-lookup"><span data-stu-id="f8c03-110">A [**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) structure that receives the current state of the bidirectional options in the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8c03-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8c03-111">Return value</span></span>

<span data-ttu-id="f8c03-112">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f8c03-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8c03-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8c03-113">Remarks</span></span>

<span data-ttu-id="f8c03-114">Diese Meldung legt die Werte der **wmask** -und **weffects** -Elemente auf den Wert des aktuellen Status der bidirektionalen Optionen im Rich Edit-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="f8c03-114">This message sets the values of the **wMask** and **wEffects** members to the value of the current state of the bidirectional options in the rich edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8c03-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8c03-115">Requirements</span></span>



| <span data-ttu-id="f8c03-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8c03-116">Requirement</span></span> | <span data-ttu-id="f8c03-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f8c03-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f8c03-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f8c03-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f8c03-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8c03-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f8c03-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f8c03-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f8c03-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8c03-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f8c03-122">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="f8c03-122">Redistributable</span></span><br/>          | <span data-ttu-id="f8c03-123">Rich Edit 3,0</span><span class="sxs-lookup"><span data-stu-id="f8c03-123">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="f8c03-124">Header</span><span class="sxs-lookup"><span data-stu-id="f8c03-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8c03-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8c03-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8c03-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8c03-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="f8c03-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="f8c03-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f8c03-128">**Bidioptions**</span><span class="sxs-lookup"><span data-stu-id="f8c03-128">**BIDIOPTIONS**</span></span>](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[<span data-ttu-id="f8c03-129">**EM \_ setbidioptions**</span><span class="sxs-lookup"><span data-stu-id="f8c03-129">**EM\_SETBIDIOPTIONS**</span></span>](em-setbidioptions.md)
</dt> </dl>

 

 





