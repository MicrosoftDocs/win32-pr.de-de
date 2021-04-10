---
title: EM_DISPLAYBAND Meldung (RichEdit. h)
description: Zeigt einen Teil des Inhalts eines Rich-Edit-Steuer Elements an, wie zuvor für ein Gerät mithilfe der EM- \_ Format Bereichs Nachricht formatiert.
ms.assetid: 845513d0-f32b-418c-8255-a5caf2d56215
keywords:
- Windows-Steuerelemente für EM_DISPLAYBAND Meldung
topic_type:
- apiref
api_name:
- EM_DISPLAYBAND
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51896a9ba5603e799609ab52989681ecf7bcac4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956727"
---
# <a name="em_displayband-message"></a><span data-ttu-id="6894b-104">EM \_ DisplayBand-Meldung</span><span class="sxs-lookup"><span data-stu-id="6894b-104">EM\_DISPLAYBAND message</span></span>

<span data-ttu-id="6894b-105">Zeigt einen Teil des Inhalts eines Rich-Edit-Steuer Elements an, wie zuvor für ein Gerät mithilfe der [**EM- \_ Format Bereichs**](em-formatrange.md) Nachricht formatiert.</span><span class="sxs-lookup"><span data-stu-id="6894b-105">Displays a portion of the contents of a rich edit control, as previously formatted for a device using the [**EM\_FORMATRANGE**](em-formatrange.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="6894b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6894b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6894b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6894b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6894b-108">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="6894b-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6894b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6894b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6894b-110">Eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die den Anzeigebereich des Geräts angibt.</span><span class="sxs-lookup"><span data-stu-id="6894b-110">A [**RECT**](/previous-versions//dd162897(v=vs.85)) structure specifying the display area of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6894b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6894b-111">Return value</span></span>

<span data-ttu-id="6894b-112">Wenn der Vorgang erfolgreich ist, ist der Rückgabewert " **true**".</span><span class="sxs-lookup"><span data-stu-id="6894b-112">If the operation succeeds, the return value is **TRUE**.</span></span>

<span data-ttu-id="6894b-113">Wenn der Vorgang fehlschlägt, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="6894b-113">If the operation fails, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6894b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6894b-114">Remarks</span></span>

<span data-ttu-id="6894b-115">Text-und Component Object Model (com)-Objekte werden durch das Rechteck abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="6894b-115">Text and Component Object Model (COM) objects are clipped by the rectangle.</span></span> <span data-ttu-id="6894b-116">Der Clippingbereich muss von der Anwendung nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6894b-116">The application does not need to set the clipping region.</span></span>

<span data-ttu-id="6894b-117">Die Bandbreite ist der Prozess, mit dem eine einzelne Seite der Ausgabe mit einem oder mehreren separaten Rechtecke oder Bändern generiert wird.</span><span class="sxs-lookup"><span data-stu-id="6894b-117">Banding is the process by which a single page of output is generated using one or more separate rectangles, or bands.</span></span> <span data-ttu-id="6894b-118">Wenn alle Bänder auf der Seite platziert werden, ergibt sich ein vollständiges Bild.</span><span class="sxs-lookup"><span data-stu-id="6894b-118">When all bands are placed on the page, a complete image results.</span></span> <span data-ttu-id="6894b-119">Diese Vorgehensweise wird häufig von Raster Druckern verwendet, die nicht über genügend Arbeitsspeicher oder die Möglichkeit verfügen, eine vollständige Seite gleichzeitig zu Abbildern.</span><span class="sxs-lookup"><span data-stu-id="6894b-119">This approach is often used by raster printers that do not have sufficient memory or ability to image a full page at one time.</span></span> <span data-ttu-id="6894b-120">Zu den Bandbreiten von Geräten zählen die meisten Punktmatrix Drucker und einige Laserdrucker.</span><span class="sxs-lookup"><span data-stu-id="6894b-120">Banding devices include most dot matrix printers as well as some laser printers.</span></span>

## <a name="requirements"></a><span data-ttu-id="6894b-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6894b-121">Requirements</span></span>



| <span data-ttu-id="6894b-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6894b-122">Requirement</span></span> | <span data-ttu-id="6894b-123">Wert</span><span class="sxs-lookup"><span data-stu-id="6894b-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6894b-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6894b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6894b-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6894b-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6894b-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6894b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6894b-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6894b-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6894b-128">Header</span><span class="sxs-lookup"><span data-stu-id="6894b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6894b-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6894b-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6894b-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6894b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6894b-131">Drucken von Rich Edit-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="6894b-131">Printing Rich Edit Controls</span></span>](printing-rich-edit-controls.md)
</dt> </dl>

 

