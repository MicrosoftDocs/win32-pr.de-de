---
description: Ruft den Typ des angegebenen Strichs ab.
ms.assetid: bbd0bc23-89f9-4033-bc32-f9bd737c960c
title: 'Iinkanalyzer:: GetStrokeType-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetStrokeType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d9358b2583f31fd26310ea880470f36404021fec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214659"
---
# <a name="iinkanalyzergetstroketype-method"></a><span data-ttu-id="37182-103">Iinkanalyzer:: GetStrokeType-Methode</span><span class="sxs-lookup"><span data-stu-id="37182-103">IInkAnalyzer::GetStrokeType method</span></span>

<span data-ttu-id="37182-104">Ruft den Typ des angegebenen Strichs ab.</span><span class="sxs-lookup"><span data-stu-id="37182-104">Retrieves the type of the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="37182-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="37182-105">Syntax</span></span>


```C++
HRESULT GetStrokeType(
  [in]  LONG       lStrokeId,
  [out] StrokeType *pStrokeType
);
```



## <a name="parameters"></a><span data-ttu-id="37182-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="37182-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37182-107">*lstrokeid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="37182-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37182-108">Der Strich Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="37182-108">The stroke identifier.</span></span>

</dd> <dt>

<span data-ttu-id="37182-109">*pstroketype* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="37182-109">*pStrokeType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37182-110">Die Klassifizierung des angegebenen Strichs.</span><span class="sxs-lookup"><span data-stu-id="37182-110">The classification of the specified stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37182-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="37182-111">Return value</span></span>

<span data-ttu-id="37182-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="37182-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="37182-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37182-113">Remarks</span></span>

<span data-ttu-id="37182-114">Wenn der Typ des Strichs der [**StrokeType**](stroketype.md) -Wert \_ nicht klassifiziert ist, klassifiziert [**iinkanalyzer**](iinkanalyzer.md) den Strich während der frei Hand Analyse.</span><span class="sxs-lookup"><span data-stu-id="37182-114">If the stroke's type is the [**StrokeType**](stroketype.md) value StrokeType\_Unclassified, the [**IInkAnalyzer**](iinkanalyzer.md) classifies the stroke during ink analysis.</span></span> <span data-ttu-id="37182-115">Andernfalls verwendet **iinkanalyzer** den Typ, der auf dem Strich festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="37182-115">Otherwise, the **IInkAnalyzer** uses the type set on the stroke.</span></span>

<span data-ttu-id="37182-116">Der Wert von "Stroke Type" wird von [**iinkanalyzer**](iinkanalyzer.md) nicht als Teil der Ink-Analyse festgelegt.</span><span class="sxs-lookup"><span data-stu-id="37182-116">The [**IInkAnalyzer**](iinkanalyzer.md) does not set the stroke type value as part of ink analysis.</span></span> <span data-ttu-id="37182-117">Verwenden Sie die [**iinkanalyzer:: SetStrokeType-Methode**](iinkanalyzer-setstroketype.md) oder die [**iinkanalyzer:: SetStrokesType-Methode**](iinkanalyzer-setstrokestype.md), um den strichentyp anzugeben oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="37182-117">To specify or change the stroke type, use [**IInkAnalyzer::SetStrokeType Method**](iinkanalyzer-setstroketype.md) or [**IInkAnalyzer::SetStrokesType Method**](iinkanalyzer-setstrokestype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="37182-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37182-118">Requirements</span></span>



| <span data-ttu-id="37182-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37182-119">Requirement</span></span> | <span data-ttu-id="37182-120">Wert</span><span class="sxs-lookup"><span data-stu-id="37182-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37182-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37182-121">Minimum supported client</span></span><br/> | <span data-ttu-id="37182-122">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37182-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="37182-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37182-123">Minimum supported server</span></span><br/> | <span data-ttu-id="37182-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="37182-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="37182-125">Header</span><span class="sxs-lookup"><span data-stu-id="37182-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="37182-126"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="37182-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="37182-127">DLL</span><span class="sxs-lookup"><span data-stu-id="37182-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37182-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37182-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="37182-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37182-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37182-130">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="37182-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="37182-131">**Iinkanalyzer:: SetStrokeType-Methode**</span><span class="sxs-lookup"><span data-stu-id="37182-131">**IInkAnalyzer::SetStrokeType Method**</span></span>](iinkanalyzer-setstroketype.md)
</dt> <dt>

[<span data-ttu-id="37182-132">**Iinkanalyzer:: SetStrokesType-Methode**</span><span class="sxs-lookup"><span data-stu-id="37182-132">**IInkAnalyzer::SetStrokesType Method**</span></span>](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[<span data-ttu-id="37182-133">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="37182-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




