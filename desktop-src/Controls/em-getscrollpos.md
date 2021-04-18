---
title: EM_GETSCROLLPOS Meldung (RichEdit. h)
description: Ruft die aktuelle Bild Lauf Position des Bearbeitungs Steuer Elements ab.
ms.assetid: 26e122da-f1b4-4694-978c-ff678dad5d9f
keywords:
- Windows-Steuerelemente für EM_GETSCROLLPOS Meldung
topic_type:
- apiref
api_name:
- EM_GETSCROLLPOS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70458abca94e483f8e202f13ecaed3df04a68366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476485"
---
# <a name="em_getscrollpos-message"></a><span data-ttu-id="dfcd5-104">EM \_ getscrollpos-Meldung</span><span class="sxs-lookup"><span data-stu-id="dfcd5-104">EM\_GETSCROLLPOS message</span></span>

<span data-ttu-id="dfcd5-105">Ruft die aktuelle Bild Lauf Position des Bearbeitungs Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="dfcd5-105">Obtains the current scroll position of the edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="dfcd5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfcd5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfcd5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dfcd5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dfcd5-108">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="dfcd5-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="dfcd5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dfcd5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dfcd5-110">Zeiger auf eine [**Punkt**](/previous-versions//dd162805(v=vs.85)) Struktur.</span><span class="sxs-lookup"><span data-stu-id="dfcd5-110">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure.</span></span> <span data-ttu-id="dfcd5-111">Nach dem Aufrufen von **EM \_ getscrollpos** enthält dieser Parameter einen Punkt im virtuellen Textbereich des Dokuments, ausgedrückt in Pixel.</span><span class="sxs-lookup"><span data-stu-id="dfcd5-111">After calling **EM\_GETSCROLLPOS**, this parameters contains a point in the virtual text space of the document, expressed in pixels.</span></span> <span data-ttu-id="dfcd5-112">Dieser Punkt ist der Punkt, der sich zurzeit in der oberen linken Ecke des Bearbeitungs Steuer Elements befindet.</span><span class="sxs-lookup"><span data-stu-id="dfcd5-112">This point will be the point that is currently located in the upper-left corner of the edit control window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfcd5-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dfcd5-113">Return value</span></span>

<span data-ttu-id="dfcd5-114">Diese Meldung gibt immer 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="dfcd5-114">This message always returns 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfcd5-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dfcd5-115">Remarks</span></span>

<span data-ttu-id="dfcd5-116">Bei den in der [**Punkt**](/previous-versions//dd162805(v=vs.85)) Struktur zurückgegebenen Werten handelt es sich um 16-Bit-Werte (auch in den 32-Bit-breiten Feldern).</span><span class="sxs-lookup"><span data-stu-id="dfcd5-116">The values returned in the [**POINT**](/previous-versions//dd162805(v=vs.85)) structure are 16-bit values (even in the 32-bit wide fields).</span></span>

## <a name="requirements"></a><span data-ttu-id="dfcd5-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dfcd5-117">Requirements</span></span>



| <span data-ttu-id="dfcd5-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dfcd5-118">Requirement</span></span> | <span data-ttu-id="dfcd5-119">Wert</span><span class="sxs-lookup"><span data-stu-id="dfcd5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dfcd5-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dfcd5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dfcd5-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dfcd5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dfcd5-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dfcd5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dfcd5-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dfcd5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dfcd5-124">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="dfcd5-124">Redistributable</span></span><br/>          | <span data-ttu-id="dfcd5-125">Rich Edit 3,0</span><span class="sxs-lookup"><span data-stu-id="dfcd5-125">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="dfcd5-126">Header</span><span class="sxs-lookup"><span data-stu-id="dfcd5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfcd5-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfcd5-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfcd5-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dfcd5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfcd5-129">**EM- \_ setscrollpos**</span><span class="sxs-lookup"><span data-stu-id="dfcd5-129">**EM\_SETSCROLLPOS**</span></span>](em-setscrollpos.md)
</dt> </dl>

 

