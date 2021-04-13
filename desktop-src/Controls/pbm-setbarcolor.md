---
title: PBM_SETBARCOLOR Meldung (kommstrg. h)
description: Legt die Farbe der Statusanzeige Leiste im Statusanzeige-Steuerelement fest.
ms.assetid: 4b512420-04ec-4884-ab13-4c58304b95f6
keywords:
- Windows-Steuerelemente für PBM_SETBARCOLOR Meldung
topic_type:
- apiref
api_name:
- PBM_SETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1387e69622e84990a197dc5a374d1c3449393408
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518287"
---
# <a name="pbm_setbarcolor-message"></a><span data-ttu-id="a80fe-104">PBM- \_ setbarcolor-Meldung</span><span class="sxs-lookup"><span data-stu-id="a80fe-104">PBM\_SETBARCOLOR message</span></span>

<span data-ttu-id="a80fe-105">Legt die Farbe der Statusanzeige Leiste im Statusanzeige-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="a80fe-105">Sets the color of the progress indicator bar in the progress bar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a80fe-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a80fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a80fe-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a80fe-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a80fe-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a80fe-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a80fe-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a80fe-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a80fe-110">Der **COLORREF** -Wert, der die neue Statusanzeige leisten Farbe angibt.</span><span class="sxs-lookup"><span data-stu-id="a80fe-110">The **COLORREF** value that specifies the new progress indicator bar color.</span></span> <span data-ttu-id="a80fe-111">Wenn Sie den CLR- \_ Standardwert angeben, wird in der Statusleiste die standardmäßige Statusanzeige leisten Farbe verwendet.</span><span class="sxs-lookup"><span data-stu-id="a80fe-111">Specifying the CLR\_DEFAULT value causes the progress bar to use its default progress indicator bar color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a80fe-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a80fe-112">Return value</span></span>

<span data-ttu-id="a80fe-113">Gibt die vorherige Status Indikator leisten Farbe oder CLR-Standardwert zurück, \_ Wenn die Statusanzeige leisten Farbe die Standardfarbe ist.</span><span class="sxs-lookup"><span data-stu-id="a80fe-113">Returns the previous progress indicator bar color, or CLR\_DEFAULT if the progress indicator bar color is the default color.</span></span>

## <a name="remarks"></a><span data-ttu-id="a80fe-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a80fe-114">Remarks</span></span>

<span data-ttu-id="a80fe-115">Wenn visuelle Stile aktiviert sind, hat diese Nachricht keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="a80fe-115">When visual styles are enabled, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="a80fe-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a80fe-116">Requirements</span></span>



| <span data-ttu-id="a80fe-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a80fe-117">Requirement</span></span> | <span data-ttu-id="a80fe-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a80fe-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a80fe-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a80fe-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a80fe-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a80fe-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a80fe-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a80fe-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a80fe-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a80fe-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a80fe-123">Header</span><span class="sxs-lookup"><span data-stu-id="a80fe-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a80fe-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a80fe-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





