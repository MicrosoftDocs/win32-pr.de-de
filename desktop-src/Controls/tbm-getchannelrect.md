---
title: TBM_GETCHANNELRECT Meldung (kommstrg. h)
description: Ruft die Größe und Position des umgebenden Rechtecks für den Kanal einer TrackBar ab.
ms.assetid: 353edae3-1a26-4e85-8a32-ba8b5a976d24
keywords:
- Windows-Steuerelemente für TBM_GETCHANNELRECT Meldung
topic_type:
- apiref
api_name:
- TBM_GETCHANNELRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02982e9ce417b9fcf3e16d0e14d061e3ffd97a8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949592"
---
# <a name="tbm_getchannelrect-message"></a><span data-ttu-id="8061e-104">TBM- \_ GetChannelRect-Nachricht</span><span class="sxs-lookup"><span data-stu-id="8061e-104">TBM\_GETCHANNELRECT message</span></span>

<span data-ttu-id="8061e-105">Ruft die Größe und Position des umgebenden Rechtecks für den Kanal einer TrackBar ab.</span><span class="sxs-lookup"><span data-stu-id="8061e-105">Retrieves the size and position of the bounding rectangle for a trackbar's channel.</span></span> <span data-ttu-id="8061e-106">(Der Kanal ist der Bereich, in dem der Schieberegler verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="8061e-106">(The channel is the area over which the slider moves.</span></span> <span data-ttu-id="8061e-107">Sie enthält die Hervorhebung, wenn ein Bereich ausgewählt ist.)</span><span class="sxs-lookup"><span data-stu-id="8061e-107">It contains the highlight when a range is selected.)</span></span>

## <a name="parameters"></a><span data-ttu-id="8061e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8061e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8061e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8061e-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8061e-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="8061e-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8061e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8061e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8061e-112">Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="8061e-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="8061e-113">Die Meldung füllt diese Struktur mit dem umgebenden Rechteck des Kanals in den Client Koordinaten des TrackBar-Fensters.</span><span class="sxs-lookup"><span data-stu-id="8061e-113">The message fills this structure with the channel's bounding rectangle, in client coordinates of the trackbar's window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8061e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8061e-114">Return value</span></span>

<span data-ttu-id="8061e-115">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="8061e-115">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8061e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8061e-116">Requirements</span></span>



| <span data-ttu-id="8061e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8061e-117">Requirement</span></span> | <span data-ttu-id="8061e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8061e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8061e-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8061e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8061e-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8061e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8061e-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8061e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8061e-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8061e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8061e-123">Header</span><span class="sxs-lookup"><span data-stu-id="8061e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8061e-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="8061e-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

