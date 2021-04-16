---
title: EM_SETCARETINDEX Meldung (kommstrg. h)
description: Legt den NULL basierten Indexwert der Position der Einfügemarke in einem Bearbeitungs Steuerelement fest.
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- Windows-Steuerelemente für EM_SETCARETINDEX Meldung
topic_type:
- apiref
api_name:
- EM_SETCARETINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: ea0c49ebad91532e82dc7e96facb62f38b2abfa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478579"
---
# <a name="em_setcaretindex-message"></a><span data-ttu-id="9f997-104">EM \_ setcaretindex-Meldung</span><span class="sxs-lookup"><span data-stu-id="9f997-104">EM\_SETCARETINDEX message</span></span>

<span data-ttu-id="9f997-105">Legt den NULL basierten Indexwert der Position der Einfügemarke in einem Bearbeitungs Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="9f997-105">Sets the zero-based index value of the position of the caret in an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9f997-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f997-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f997-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9f997-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f997-108">Der neue null basierte Indexwert der Position der Einfügemarke.</span><span class="sxs-lookup"><span data-stu-id="9f997-108">The new zero-based index value of the position of the caret.</span></span>

</dd> <dt>

<span data-ttu-id="9f997-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f997-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9f997-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="9f997-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f997-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f997-111">Return value</span></span>

<span data-ttu-id="9f997-112">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9f997-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f997-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f997-113">Remarks</span></span>

<span data-ttu-id="9f997-114">Wenn der Index außerhalb des Bereichs des Texts in einem Bearbeitungs Steuerelement liegt, wird der Index so angepasst, dass er in den Textbereich passt.</span><span class="sxs-lookup"><span data-stu-id="9f997-114">If the index is out of the range of the text in an edit control, the index will be adjusted to fit inside the range of the text.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f997-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f997-115">Requirements</span></span>



| <span data-ttu-id="9f997-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f997-116">Requirement</span></span> | <span data-ttu-id="9f997-117">Wert</span><span class="sxs-lookup"><span data-stu-id="9f997-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f997-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9f997-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9f997-119">Nur Windows 10, 1809 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f997-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9f997-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9f997-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9f997-121">Nur Windows Server 2019 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f997-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9f997-122">Header</span><span class="sxs-lookup"><span data-stu-id="9f997-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f997-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f997-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f997-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f997-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="9f997-125">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="9f997-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9f997-126">**EM \_ getcaretindex**</span><span class="sxs-lookup"><span data-stu-id="9f997-126">**EM\_GETCARETINDEX**</span></span>](em-getcaretindex.md)
</dt> </dl>

 

 





