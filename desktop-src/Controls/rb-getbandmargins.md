---
title: RB_GETBANDMARGINS Meldung (kommstrg. h)
description: Ruft die Ränder eines Bands ab.
ms.assetid: 262f4180-53f9-428f-9360-75b762470270
keywords:
- Windows-Steuerelemente für RB_GETBANDMARGINS Meldung
topic_type:
- apiref
api_name:
- RB_GETBANDMARGINS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51ab77c057073d9816d1310b1e8cb39fd374956b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956799"
---
# <a name="rb_getbandmargins-message"></a><span data-ttu-id="d20ea-104">RB \_ getbandmargin-Meldung</span><span class="sxs-lookup"><span data-stu-id="d20ea-104">RB\_GETBANDMARGINS message</span></span>

<span data-ttu-id="d20ea-105">Ruft die Ränder eines Bands ab.</span><span class="sxs-lookup"><span data-stu-id="d20ea-105">Retrieves the margins of a band.</span></span>

## <a name="parameters"></a><span data-ttu-id="d20ea-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d20ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d20ea-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d20ea-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d20ea-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="d20ea-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d20ea-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d20ea-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d20ea-110">Zeiger auf eine [**Ränder**](/windows/desktop/api/Uxtheme/ns-uxtheme-margins) -Struktur, die die abgerufenen Ränder empfängt.</span><span class="sxs-lookup"><span data-stu-id="d20ea-110">Pointer to a [**MARGINS**](/windows/desktop/api/Uxtheme/ns-uxtheme-margins) structure that receives the retrieved margins.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d20ea-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d20ea-111">Return value</span></span>

<span data-ttu-id="d20ea-112">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d20ea-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="d20ea-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d20ea-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d20ea-114">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="d20ea-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="d20ea-115">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d20ea-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d20ea-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d20ea-116">Requirements</span></span>



| <span data-ttu-id="d20ea-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d20ea-117">Requirement</span></span> | <span data-ttu-id="d20ea-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d20ea-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d20ea-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d20ea-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d20ea-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d20ea-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d20ea-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d20ea-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d20ea-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d20ea-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d20ea-123">Header</span><span class="sxs-lookup"><span data-stu-id="d20ea-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d20ea-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d20ea-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





