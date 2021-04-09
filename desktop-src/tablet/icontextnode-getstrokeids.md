---
description: Ruft ein Array von bezeichern für die Striche innerhalb des icontextnode-Objekts ab.
ms.assetid: 2420afec-6859-449b-92d8-0f4327281852
title: 'Icontextnode:: GetStrokeIds-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 25592cd245eba135fa7e459ff3c5c5207fc6ff0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129500"
---
# <a name="icontextnodegetstrokeids-method"></a><span data-ttu-id="ad480-103">Icontextnode:: GetStrokeIds-Methode</span><span class="sxs-lookup"><span data-stu-id="ad480-103">IContextNode::GetStrokeIds method</span></span>

<span data-ttu-id="ad480-104">Ruft ein Array von bezeichern für die Striche innerhalb des [**icontextnode**](icontextnode.md) -Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="ad480-104">Retrieves an array of identifiers for the strokes within the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad480-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad480-105">Syntax</span></span>


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokes
);
```



## <a name="parameters"></a><span data-ttu-id="ad480-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad480-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad480-107">*pulstrokeidscount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ad480-107">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad480-108">Die Anzahl der Striche.</span><span class="sxs-lookup"><span data-stu-id="ad480-108">The number of strokes.</span></span> <span data-ttu-id="ad480-109">Der Wert, der an die Übergabe erfolgt, wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ad480-109">The value that is passed in is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ad480-110">*pplstrokes* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ad480-110">*pplStrokes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad480-111">Ein Zeiger auf das Array von Strich Bezeichners für dieses [**icontextnode**](icontextnode.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="ad480-111">A pointer to the array of stroke identifiers for this [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad480-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad480-112">Return value</span></span>

<span data-ttu-id="ad480-113">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ad480-113">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ad480-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad480-114">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="ad480-115">Um einen Speicherplatz zu vermeiden, verwenden Sie " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ", um den Arbeitsspeicher aus \* *pplstrokes* freizugeben, wenn Sie die Informationen nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="ad480-115">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**pplStrokes* when you no longer need the information.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ad480-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad480-116">Requirements</span></span>



| <span data-ttu-id="ad480-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad480-117">Requirement</span></span> | <span data-ttu-id="ad480-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ad480-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad480-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ad480-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ad480-120">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad480-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ad480-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ad480-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ad480-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad480-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ad480-123">Header</span><span class="sxs-lookup"><span data-stu-id="ad480-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad480-124"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ad480-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ad480-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ad480-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad480-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad480-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ad480-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad480-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad480-128">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="ad480-128">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="ad480-129">**Icontextnode:: getstrokeid**</span><span class="sxs-lookup"><span data-stu-id="ad480-129">**IContextNode::GetStrokeId**</span></span>](icontextnode-getstrokeid.md)
</dt> <dt>

[<span data-ttu-id="ad480-130">**Icontextnode:: getstrokecount**</span><span class="sxs-lookup"><span data-stu-id="ad480-130">**IContextNode::GetStrokeCount**</span></span>](icontextnode-getstrokecount.md)
</dt> <dt>

[<span data-ttu-id="ad480-131">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="ad480-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

