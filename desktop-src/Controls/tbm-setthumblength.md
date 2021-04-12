---
title: TBM_SETTHUMBLENGTH Meldung (kommstrg. h)
description: Legt die Länge des Schiebereglers in einer TrackBar fest. Diese Meldung wird ignoriert, wenn die TrackBar nicht über den TSB- \_ FixedLength-Stil verfügt.
ms.assetid: 027fe341-a60a-4dbe-a48a-5ddaadef0b4a
keywords:
- Windows-Steuerelemente für TBM_SETTHUMBLENGTH Meldung
topic_type:
- apiref
api_name:
- TBM_SETTHUMBLENGTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d4ac33d2df43a267766e14ab95fb9729692bbee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518740"
---
# <a name="tbm_setthumblength-message"></a><span data-ttu-id="0520a-105">TBM- \_ setthumblength-Meldung</span><span class="sxs-lookup"><span data-stu-id="0520a-105">TBM\_SETTHUMBLENGTH message</span></span>

<span data-ttu-id="0520a-106">Legt die Länge des Schiebereglers in einer TrackBar fest.</span><span class="sxs-lookup"><span data-stu-id="0520a-106">Sets the length of the slider in a trackbar.</span></span> <span data-ttu-id="0520a-107">Diese Meldung wird ignoriert, wenn die TrackBar nicht über den [**TSB- \_ FixedLength**](trackbar-control-styles.md) -Stil verfügt.</span><span class="sxs-lookup"><span data-stu-id="0520a-107">This message is ignored if the trackbar does not have the [**TBS\_FIXEDLENGTH**](trackbar-control-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="0520a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0520a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0520a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0520a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0520a-110">Länge des Schiebereglers in Pixel.</span><span class="sxs-lookup"><span data-stu-id="0520a-110">Length, in pixels, of the slider.</span></span>

</dd> <dt>

<span data-ttu-id="0520a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0520a-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0520a-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="0520a-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0520a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0520a-113">Return value</span></span>

<span data-ttu-id="0520a-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="0520a-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0520a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0520a-115">Requirements</span></span>



| <span data-ttu-id="0520a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0520a-116">Requirement</span></span> | <span data-ttu-id="0520a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="0520a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0520a-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0520a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0520a-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0520a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0520a-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0520a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0520a-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0520a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0520a-122">Header</span><span class="sxs-lookup"><span data-stu-id="0520a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0520a-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="0520a-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0520a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0520a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0520a-125">**TBM \_ getthumblength**</span><span class="sxs-lookup"><span data-stu-id="0520a-125">**TBM\_GETTHUMBLENGTH**</span></span>](tbm-getthumblength.md)
</dt> </dl>

 

 





