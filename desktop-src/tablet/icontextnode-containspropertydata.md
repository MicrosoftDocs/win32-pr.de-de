---
description: Bestimmt, ob das icontextnode-Objektdaten enthält, die unter dem angegebenen Bezeichner gespeichert sind.
ms.assetid: ac3a85a2-abf8-4ac4-8779-d9fda89497d4
title: 'Icontextnode:: ContainsPropertyData-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.ContainsPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fc45e1ebe519e5988ad73e1481c68e9e9811ba04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485115"
---
# <a name="icontextnodecontainspropertydata-method"></a><span data-ttu-id="ca09d-103">Icontextnode:: ContainsPropertyData-Methode</span><span class="sxs-lookup"><span data-stu-id="ca09d-103">IContextNode::ContainsPropertyData method</span></span>

<span data-ttu-id="ca09d-104">Bestimmt, ob das [**icontextnode**](icontextnode.md) -Objektdaten enthält, die unter dem angegebenen Bezeichner gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="ca09d-104">Determines whether the [**IContextNode**](icontextnode.md) object contains data stored under the specified identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca09d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca09d-105">Syntax</span></span>


```C++
HRESULT ContainsPropertyData(
  [in]  const GUID         *pPropertyDataId,
  [out]       VARIANT_BOOL *pbContains
);
```



## <a name="parameters"></a><span data-ttu-id="ca09d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca09d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca09d-107">*ppropertydataid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca09d-107">*pPropertyDataId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca09d-108">Der Bezeichner für die Daten.</span><span class="sxs-lookup"><span data-stu-id="ca09d-108">The identifier for the data.</span></span>

</dd> <dt>

<span data-ttu-id="ca09d-109">*pbenthält* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ca09d-109">*pbContains* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca09d-110">**Variant \_ TRUE** , wenn das [**icontextnode**](icontextnode.md) -Objektdaten enthält, die unter dem angegebenen Bezeichner gespeichert sind. Andernfalls ist der Wert **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="ca09d-110">**VARIANT\_TRUE** if the [**IContextNode**](icontextnode.md) object contains data stored under the specified identifier; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca09d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca09d-111">Return value</span></span>

<span data-ttu-id="ca09d-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ca09d-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ca09d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca09d-113">Remarks</span></span>

<span data-ttu-id="ca09d-114">Zusätzlich zu den anwendungsspezifischen Daten können Sie mit dieser Methode auch bestimmen, ob dieser [**icontextnode**](icontextnode.md) andere interne Daten enthält (siehe Eigenschaften des [Analysis-Hinweises](analysis-hint-properties.md) und [Kontext Knoten Eigenschaften](context-node-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="ca09d-114">In addition to application-specific data, you can also use this method to determine whether this [**IContextNode**](icontextnode.md) contains other internal data (see [Analysis Hint Properties](analysis-hint-properties.md) and [Context Node Properties](context-node-properties.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca09d-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca09d-115">Requirements</span></span>



| <span data-ttu-id="ca09d-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca09d-116">Requirement</span></span> | <span data-ttu-id="ca09d-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ca09d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca09d-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ca09d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ca09d-119">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ca09d-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ca09d-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ca09d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ca09d-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ca09d-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ca09d-122">Header</span><span class="sxs-lookup"><span data-stu-id="ca09d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca09d-123"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ca09d-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ca09d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ca09d-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca09d-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca09d-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ca09d-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca09d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca09d-127">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="ca09d-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="ca09d-128">**Icontextnode:: AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="ca09d-128">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="ca09d-129">**Icontextnode:: GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="ca09d-129">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="ca09d-130">**Icontextnode:: GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="ca09d-130">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="ca09d-131">**Icontextnode:: loadpropertiesdata**</span><span class="sxs-lookup"><span data-stu-id="ca09d-131">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="ca09d-132">**Icontextnode:: RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="ca09d-132">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="ca09d-133">**Icontextnode:: savepropertiesdata**</span><span class="sxs-lookup"><span data-stu-id="ca09d-133">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="ca09d-134">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="ca09d-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




