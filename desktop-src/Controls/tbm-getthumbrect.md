---
title: TBM_GETTHUMBRECT Meldung (kommstrg. h)
description: Ruft die Größe und Position des umgebenden Rechtecks für den Schieberegler in einer TrackBar ab.
ms.assetid: f53fd7af-36f8-4490-aa95-f1fa20f34efb
keywords:
- Windows-Steuerelemente für TBM_GETTHUMBRECT Meldung
topic_type:
- apiref
api_name:
- TBM_GETTHUMBRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dce1bba8af9a65f297aa0515c1103c50daa1626d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040631"
---
# <a name="tbm_getthumbrect-message"></a><span data-ttu-id="de30a-104">TBM- \_ getthumbrect-Nachricht</span><span class="sxs-lookup"><span data-stu-id="de30a-104">TBM\_GETTHUMBRECT message</span></span>

<span data-ttu-id="de30a-105">Ruft die Größe und Position des umgebenden Rechtecks für den Schieberegler in einer TrackBar ab.</span><span class="sxs-lookup"><span data-stu-id="de30a-105">Retrieves the size and position of the bounding rectangle for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="de30a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="de30a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de30a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="de30a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="de30a-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="de30a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="de30a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="de30a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de30a-110">Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="de30a-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="de30a-111">Die Meldung füllt diese-Struktur mit dem umgebenden Rechteck des Schiebe leisten-Schiebereglers in Client Koordinaten des TrackBar-Fensters.</span><span class="sxs-lookup"><span data-stu-id="de30a-111">The message fills this structure with the bounding rectangle of the trackbar's slider in client coordinates of the trackbar's window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de30a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de30a-112">Return value</span></span>

<span data-ttu-id="de30a-113">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="de30a-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="de30a-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de30a-114">Requirements</span></span>



| <span data-ttu-id="de30a-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de30a-115">Requirement</span></span> | <span data-ttu-id="de30a-116">Wert</span><span class="sxs-lookup"><span data-stu-id="de30a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="de30a-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de30a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="de30a-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de30a-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="de30a-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de30a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="de30a-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de30a-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="de30a-121">Header</span><span class="sxs-lookup"><span data-stu-id="de30a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="de30a-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="de30a-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

