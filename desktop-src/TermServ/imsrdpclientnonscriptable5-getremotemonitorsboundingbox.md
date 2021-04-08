---
title: IMsRdpClientNonScriptable5 getremotemonitorsboundingbox-Eigenschaft
description: Gibt das Begrenzungs Rechteck des Remote Monitors an.
ms.assetid: 4A8794F7-1DB4-4415-8538-6B2A365B22D3
ms.tgt_platform: multiple
keywords:
- Getremotemonitorsboundingbox-Eigenschaft Remotedesktopdienste
- Getremotemonitorsboundingbox-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, getremotemonitorsboundingbox-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.GetRemoteMonitorsBoundingBox
- IMsRdpClientNonScriptable5.get_GetRemoteMonitorsBoundingBox
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f67192b78c734359fc6113969eb5eb410e1bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956757"
---
# <a name="imsrdpclientnonscriptable5getremotemonitorsboundingbox-property"></a><span data-ttu-id="8a81d-106">IMsRdpClientNonScriptable5:: getremotemonitorsboundingbox-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8a81d-106">IMsRdpClientNonScriptable5::GetRemoteMonitorsBoundingBox property</span></span>

<span data-ttu-id="8a81d-107">Gibt das Begrenzungs Rechteck des Remote Monitors an.</span><span class="sxs-lookup"><span data-stu-id="8a81d-107">Specifies the bounding rectangle of the remote monitor.</span></span>

<span data-ttu-id="8a81d-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="8a81d-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a81d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a81d-109">Syntax</span></span>


```C++
HRESULT get_GetRemoteMonitorsBoundingBox(
  [out] LONG *pLeft,
  [out] LONG *pTop,
  [out] LONG *pRight,
  [out] LONG *pBottom
);
```



## <a name="property-value"></a><span data-ttu-id="8a81d-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8a81d-110">Property value</span></span>

<span data-ttu-id="8a81d-111">Empfängt den linken Rand des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="8a81d-111">Receives the left edge of the rectangle.</span></span>

<span data-ttu-id="8a81d-112">Empfängt den oberen Rand des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="8a81d-112">Receives the top edge of the rectangle.</span></span>

<span data-ttu-id="8a81d-113">Empfängt den rechten Rand des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="8a81d-113">Receives the right edge of the rectangle.</span></span>

<span data-ttu-id="8a81d-114">Empfängt den unteren Rand des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="8a81d-114">Receives the bottom edge of the rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a81d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a81d-115">Remarks</span></span>

<span data-ttu-id="8a81d-116">Alle Koordinaten befinden sich in den virtuellen Bildschirm Koordinaten, die relativ zur oberen linken Ecke des primären Monitors sind.</span><span class="sxs-lookup"><span data-stu-id="8a81d-116">All coordinates are in virtual screen coordinates, which are relative to the upper-left corner of the primary monitor.</span></span> <span data-ttu-id="8a81d-117">Wenn dies nicht der primäre Monitor ist, können einige oder alle dieser Werte negativ sein.</span><span class="sxs-lookup"><span data-stu-id="8a81d-117">If this is not the primary monitor, some or all of these values may be negative.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a81d-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a81d-118">Requirements</span></span>



| <span data-ttu-id="8a81d-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8a81d-119">Requirement</span></span> | <span data-ttu-id="8a81d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="8a81d-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a81d-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8a81d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8a81d-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8a81d-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8a81d-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8a81d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8a81d-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8a81d-124">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="8a81d-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="8a81d-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="8a81d-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a81d-126"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="8a81d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8a81d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a81d-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a81d-128"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="8a81d-129">IID</span><span class="sxs-lookup"><span data-stu-id="8a81d-129">IID</span></span><br/>                      | <span data-ttu-id="8a81d-130">IID \_ IMsRdpClientNonScriptable5 ist als 4f 6996d5-d7b1-412c-b0ff-063718566907 definiert.</span><span class="sxs-lookup"><span data-stu-id="8a81d-130">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8a81d-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a81d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a81d-132">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="8a81d-132">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





