---
description: Gibt an, ob ein Strich im Rahmen einer Zeichnung oder beim Schreiben analysiert werden soll.
ms.assetid: 3f4c4522-ada7-4759-bca7-88b2a71f36ea
title: StrokeType-Enumeration (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StrokeType
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 3b59be130c6c7055bb7636760451dcadf5acf841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217200"
---
# <a name="stroketype-enumeration"></a><span data-ttu-id="07df8-103">StrokeType-Enumeration</span><span class="sxs-lookup"><span data-stu-id="07df8-103">StrokeType enumeration</span></span>

<span data-ttu-id="07df8-104">Gibt an, ob ein Strich im Rahmen einer Zeichnung oder beim Schreiben analysiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="07df8-104">Indicates whether a stroke should be analyzed as part of a drawing or as part of writing.</span></span>

## <a name="syntax"></a><span data-ttu-id="07df8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="07df8-105">Syntax</span></span>


```C++
typedef enum StrokeType { 
  StrokeType_Unclassified  = 0,
  StrokeType_Writing       = 1,
  StrokeType_Drawing       = 2
} StrokeType;
```



## <a name="constants"></a><span data-ttu-id="07df8-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="07df8-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="07df8-107"><span id="StrokeType_Unclassified"></span><span id="stroketype_unclassified"></span><span id="STROKETYPE_UNCLASSIFIED"></span>**StrokeType \_ nicht klassifiziert**</span><span class="sxs-lookup"><span data-stu-id="07df8-107"><span id="StrokeType_Unclassified"></span><span id="stroketype_unclassified"></span><span id="STROKETYPE_UNCLASSIFIED"></span>**StrokeType\_Unclassified**</span></span>
</dt> <dd>

<span data-ttu-id="07df8-108">Der Strich kann entweder Teil einer Zeichnung oder eines Teils eines Schreibvorgangs sein.</span><span class="sxs-lookup"><span data-stu-id="07df8-108">The stroke might be either part of a drawing or part of writing.</span></span>

</dd> <dt>

<span data-ttu-id="07df8-109"><span id="StrokeType_Writing"></span><span id="stroketype_writing"></span><span id="STROKETYPE_WRITING"></span>**Schreiben von StrokeType \_**</span><span class="sxs-lookup"><span data-stu-id="07df8-109"><span id="StrokeType_Writing"></span><span id="stroketype_writing"></span><span id="STROKETYPE_WRITING"></span>**StrokeType\_Writing**</span></span>
</dt> <dd>

<span data-ttu-id="07df8-110">Der Strich ist Teil des Schreibens.</span><span class="sxs-lookup"><span data-stu-id="07df8-110">The stroke is part of writing.</span></span>

</dd> <dt>

<span data-ttu-id="07df8-111"><span id="StrokeType_Drawing"></span><span id="stroketype_drawing"></span><span id="STROKETYPE_DRAWING"></span>**StrokeType- \_ Zeichnung**</span><span class="sxs-lookup"><span data-stu-id="07df8-111"><span id="StrokeType_Drawing"></span><span id="stroketype_drawing"></span><span id="STROKETYPE_DRAWING"></span>**StrokeType\_Drawing**</span></span>
</dt> <dd>

<span data-ttu-id="07df8-112">Der Strich ist Teil einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="07df8-112">The stroke is part of a drawing.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="07df8-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07df8-113">Examples</span></span>

<span data-ttu-id="07df8-114">Das folgende Beispiel zeigt einen Teil eines Stroke-Ereignis Handlers, der in ähnlicher Weise wie das [C++ Event Sinks-Beispiel](c---event-sinks-sample.md)implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="07df8-114">The following example shows part of a stroke event handler, implemented in a similar fashion to the [C++ Event Sinks Sample](c---event-sinks-sample.md).</span></span> <span data-ttu-id="07df8-115">Der hinzugefügte Strich wird geprüft, um festzustellen, ob der obere Rand seines umgebenden Felds unterhalb eines Rands gezeichnet wurde `drawingMargin` .</span><span class="sxs-lookup"><span data-stu-id="07df8-115">The added stroke is checked to see if the top of its bounding box has been drawn below a margin, `drawingMargin`.</span></span> <span data-ttu-id="07df8-116">Wenn dies der Fall ist, wird das [**iinkanalyzer**](iinkanalyzer.md) -Objekt, `m_spInkAnalyzer` , so festgelegt, dass der Strich als Zeichen Strich analysiert wird, anstatt als Handschrift Strich.</span><span class="sxs-lookup"><span data-stu-id="07df8-116">If so, the [**IInkAnalyzer**](iinkanalyzer.md) object, `m_spInkAnalyzer`, is set to analyze the stroke as a drawing stroke, rather than as a handwriting stroke.</span></span> <span data-ttu-id="07df8-117">`CheckHResult` eine Funktion, die eine `HRESULT` -und eine-Zeichenfolge annimmt und eine mit der-Zeichenfolge erstellte Ausnahme auslöst, wenn der `HRESULT` nicht **erfolgreich** ist.</span><span class="sxs-lookup"><span data-stu-id="07df8-117">`CheckHResult` is a function that takes an `HRESULT` and a string, and throws an exception created with the string if the `HRESULT` is not **SUCCESS**.</span></span>


```C++
IInkRectangle* bounds;
CheckHResult(pStroke->GetBoundingBox(IBBM_Default, &bounds), "IInkStrokeDisp::GetBoundingBox failed");
long top;
CheckHResult(bounds->get_Top(&top), "IInkRectangle::get_Top failed");
if (top > drawingMargin)
{
    long strokeId;
    CheckHResult(pStroke->get_ID(&strokeId), "IInkStrokeDisp::get_ID failed");
    m_pInkAnalyzer->SetStrokeType(strokeId, StrokeType_Drawing);
}
```



## <a name="requirements"></a><span data-ttu-id="07df8-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07df8-118">Requirements</span></span>



| <span data-ttu-id="07df8-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07df8-119">Requirement</span></span> | <span data-ttu-id="07df8-120">Wert</span><span class="sxs-lookup"><span data-stu-id="07df8-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07df8-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="07df8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="07df8-122">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07df8-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="07df8-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="07df8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="07df8-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="07df8-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="07df8-125">Header</span><span class="sxs-lookup"><span data-stu-id="07df8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="07df8-126"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="07df8-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07df8-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07df8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07df8-128">**Iinkanalyzer:: SetStrokeType-Methode**</span><span class="sxs-lookup"><span data-stu-id="07df8-128">**IInkAnalyzer::SetStrokeType Method**</span></span>](iinkanalyzer-setstroketype.md)
</dt> </dl>

 

 




