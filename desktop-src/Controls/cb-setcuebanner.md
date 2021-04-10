---
title: CB_SETCUEBANNER Meldung (Winuser. h)
description: Legt den Hinweis Banner Text fest, der für das Bearbeitungs Steuerelement eines Kombinations Felds angezeigt wird.
ms.assetid: 4b2b5042-ba64-4e3f-adeb-9aea66773b0e
keywords:
- Windows-Steuerelemente für CB_SETCUEBANNER Meldung
topic_type:
- apiref
api_name:
- CB_SETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5799b1b1be5e938ce1e234948a1f7d878122f30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040594"
---
# <a name="cb_setcuebanner-message"></a><span data-ttu-id="faa4b-104">CB- \_ setcuebanner-Meldung</span><span class="sxs-lookup"><span data-stu-id="faa4b-104">CB\_SETCUEBANNER message</span></span>

<span data-ttu-id="faa4b-105">Legt den Hinweis Banner Text fest, der für das Bearbeitungs Steuerelement eines Kombinations Felds angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="faa4b-105">Sets the cue banner text that is displayed for the edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="faa4b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="faa4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="faa4b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="faa4b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="faa4b-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="faa4b-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="faa4b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="faa4b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="faa4b-110">Ein Zeiger auf einen null-terminierten Unicode-Zeichen folgen Puffer, der den Text enthält.</span><span class="sxs-lookup"><span data-stu-id="faa4b-110">A pointer to a null-terminated Unicode string buffer that contains the text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="faa4b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="faa4b-111">Return value</span></span>

<span data-ttu-id="faa4b-112">Gibt 1 zurück, wenn erfolgreich, oder andernfalls einen Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="faa4b-112">Returns 1 if successful, or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="faa4b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="faa4b-113">Remarks</span></span>

<span data-ttu-id="faa4b-114">Das Hinweis Banner ist Text, der im Bearbeitungs Steuerelement eines Kombinations Felds angezeigt wird, wenn keine Auswahl vorliegt.</span><span class="sxs-lookup"><span data-stu-id="faa4b-114">The cue banner is text that is displayed in the edit control of a combo box when there is no selection.</span></span>

## <a name="requirements"></a><span data-ttu-id="faa4b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="faa4b-115">Requirements</span></span>



| <span data-ttu-id="faa4b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="faa4b-116">Requirement</span></span> | <span data-ttu-id="faa4b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="faa4b-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="faa4b-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="faa4b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="faa4b-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="faa4b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="faa4b-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="faa4b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="faa4b-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="faa4b-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="faa4b-122">Header</span><span class="sxs-lookup"><span data-stu-id="faa4b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="faa4b-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="faa4b-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faa4b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="faa4b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faa4b-125">Kombinations Feld-Features</span><span class="sxs-lookup"><span data-stu-id="faa4b-125">Combo Box Features</span></span>](combo-box-features.md)
</dt> </dl>

 

 





