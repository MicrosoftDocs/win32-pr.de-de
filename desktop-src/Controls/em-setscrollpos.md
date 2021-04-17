---
title: EM_SETSCROLLPOS Meldung (RichEdit. h)
description: Führt einen Bildlauf für den Inhalt eines Rich-Edit-Steuer Elements zum angegebenen Punkt durch.
ms.assetid: 9ec514a4-97b1-44ab-b2ca-973b1f6fc404
keywords:
- Windows-Steuerelemente für EM_SETSCROLLPOS Meldung
topic_type:
- apiref
api_name:
- EM_SETSCROLLPOS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec41ac5255059b8d40f3a4c2e9b666815b9094fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478558"
---
# <a name="em_setscrollpos-message"></a><span data-ttu-id="1c19f-104">EM \_ setscrollpos-Meldung</span><span class="sxs-lookup"><span data-stu-id="1c19f-104">EM\_SETSCROLLPOS message</span></span>

<span data-ttu-id="1c19f-105">Führt einen Bildlauf für den Inhalt eines Rich-Edit-Steuer Elements zum angegebenen Punkt durch.</span><span class="sxs-lookup"><span data-stu-id="1c19f-105">Scrolls the contents of a rich edit control to the specified point.</span></span>

## <a name="parameters"></a><span data-ttu-id="1c19f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c19f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c19f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1c19f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1c19f-108">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1c19f-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1c19f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1c19f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1c19f-110">Ein Zeiger auf eine [**Punkt**](/previous-versions//dd162805(v=vs.85)) Struktur, die einen Punkt im virtuellen Textbereich des Dokuments in Pixel angibt.</span><span class="sxs-lookup"><span data-stu-id="1c19f-110">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure which specifies a point in the virtual text space of the document, expressed in pixels.</span></span> <span data-ttu-id="1c19f-111">Das Dokument wird gescrollt, bis sich dieser Punkt in der oberen linken Ecke des Bearbeitungs Steuer Elements befindet.</span><span class="sxs-lookup"><span data-stu-id="1c19f-111">The document will be scrolled until this point is located in the upper-left corner of the edit control window.</span></span> <span data-ttu-id="1c19f-112">Wenn Sie die Ansicht so ändern möchten, dass die obere linke Ecke der Ansicht zwei Zeilen nach unten und ein Zeichen vom linken Rand aus angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1c19f-112">If you want to change the view such that the upper left corner of the view is two lines down and one character in from the left edge.</span></span> <span data-ttu-id="1c19f-113">Sie würden einen Punkt (7, 22) übergeben.</span><span class="sxs-lookup"><span data-stu-id="1c19f-113">You would pass a point of (7, 22).</span></span>

<span data-ttu-id="1c19f-114">Das Rich Edit-Steuerelement überprüft die x-und y-Koordinaten und passt Sie ggf. an, sodass oben eine komplette Zeile angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1c19f-114">The rich edit control checks the x and y coordinates and adjusts them if necessary, so that a complete line is displayed at the top.</span></span> <span data-ttu-id="1c19f-115">Außerdem wird sichergestellt, dass der Text niemals vollständig vom Ansichts Rechteck entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="1c19f-115">It also ensures that the text is never completely scrolled off the view rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c19f-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1c19f-116">Return value</span></span>

<span data-ttu-id="1c19f-117">Diese Meldung gibt immer 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="1c19f-117">This message always returns 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c19f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c19f-118">Requirements</span></span>



| <span data-ttu-id="1c19f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c19f-119">Requirement</span></span> | <span data-ttu-id="1c19f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="1c19f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1c19f-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1c19f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1c19f-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c19f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1c19f-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1c19f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1c19f-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c19f-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1c19f-125">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="1c19f-125">Redistributable</span></span><br/>          | <span data-ttu-id="1c19f-126">Rich Edit 3,0</span><span class="sxs-lookup"><span data-stu-id="1c19f-126">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="1c19f-127">Header</span><span class="sxs-lookup"><span data-stu-id="1c19f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c19f-128"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c19f-128"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c19f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c19f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c19f-130">**EM \_ getscrollpos**</span><span class="sxs-lookup"><span data-stu-id="1c19f-130">**EM\_GETSCROLLPOS**</span></span>](em-getscrollpos.md)
</dt> </dl>

 

