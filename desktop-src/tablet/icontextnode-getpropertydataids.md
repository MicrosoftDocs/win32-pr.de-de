---
description: Ruft die Bezeichner ab, für die Eigenschafts Daten vorhanden sind.
ms.assetid: c9c491b7-95e2-421a-8632-f65844cd5ef9
title: 'Icontextnode:: GetPropertyDataIds-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPropertyDataIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: cdbc0ec0a613feccb4064a88f4723538439f4532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343694"
---
# <a name="icontextnodegetpropertydataids-method"></a><span data-ttu-id="886ef-103">Icontextnode:: GetPropertyDataIds-Methode</span><span class="sxs-lookup"><span data-stu-id="886ef-103">IContextNode::GetPropertyDataIds method</span></span>

<span data-ttu-id="886ef-104">Ruft die Bezeichner ab, für die Eigenschafts Daten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="886ef-104">Retrieves the identifiers for which there is property data.</span></span>

## <a name="syntax"></a><span data-ttu-id="886ef-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="886ef-105">Syntax</span></span>


```C++
HRESULT GetPropertyDataIds(
  [out] ULONG *pulGuidCount,
  [out] GUID  **ppGuids
);
```



## <a name="parameters"></a><span data-ttu-id="886ef-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="886ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="886ef-107">*pulguidcount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="886ef-107">*pulGuidCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="886ef-108">Die Anzahl der Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="886ef-108">The number of properties.</span></span>

</dd> <dt>

<span data-ttu-id="886ef-109">*ppguids* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="886ef-109">*ppGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="886ef-110">Die Bezeichner, für die Eigenschafts Daten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="886ef-110">The identifiers for which there is property data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="886ef-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="886ef-111">Return value</span></span>

<span data-ttu-id="886ef-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="886ef-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="886ef-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="886ef-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="886ef-114">Um einen Speicherplatz zu vermeiden, verwenden Sie " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ", um den Arbeitsspeicher von \* *ppguids* freizugeben, wenn Sie die Informationen nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="886ef-114">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppGuids* when you no longer need the information.</span></span>

 

<span data-ttu-id="886ef-115">Diese Methode gibt die anwendungsspezifischen Bezeichner für Eigenschaften Daten zurück, die hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="886ef-115">This method returns the application-specific identifiers for property data that has been added.</span></span> <span data-ttu-id="886ef-116">Außerdem werden die Bezeichner für die internen Eigenschaften Daten zurückgegeben, die von den Eigenschaften Konstanten für [Kontext Knoten](context-node-properties.md) beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="886ef-116">It also returns the identifiers for the internal property data, which are described by the [Context Node Properties](context-node-properties.md) constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="886ef-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="886ef-117">Requirements</span></span>



| <span data-ttu-id="886ef-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="886ef-118">Requirement</span></span> | <span data-ttu-id="886ef-119">Wert</span><span class="sxs-lookup"><span data-stu-id="886ef-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="886ef-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="886ef-120">Minimum supported client</span></span><br/> | <span data-ttu-id="886ef-121">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="886ef-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="886ef-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="886ef-122">Minimum supported server</span></span><br/> | <span data-ttu-id="886ef-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="886ef-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="886ef-124">Header</span><span class="sxs-lookup"><span data-stu-id="886ef-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="886ef-125"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="886ef-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="886ef-126">DLL</span><span class="sxs-lookup"><span data-stu-id="886ef-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="886ef-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="886ef-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="886ef-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="886ef-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="886ef-129">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="886ef-129">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="886ef-130">**Icontextnode:: GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="886ef-130">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="886ef-131">**Icontextnode:: ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="886ef-131">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="886ef-132">**Icontextnode:: RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="886ef-132">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="886ef-133">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="886ef-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

