---
description: Entfernt anwendungsspezifische Daten.
ms.assetid: 41077c2f-39e3-4069-ac05-97f1785e37b7
title: 'Icontextnode:: RemovePropertyData-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.RemovePropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4c2fd5924b206ee296c066a908d2a59b02019f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526516"
---
# <a name="icontextnoderemovepropertydata-method"></a><span data-ttu-id="c654e-103">Icontextnode:: RemovePropertyData-Methode</span><span class="sxs-lookup"><span data-stu-id="c654e-103">IContextNode::RemovePropertyData method</span></span>

<span data-ttu-id="c654e-104">Entfernt anwendungsspezifische Daten.</span><span class="sxs-lookup"><span data-stu-id="c654e-104">Removes a piece of application-specific data.</span></span>

## <a name="syntax"></a><span data-ttu-id="c654e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c654e-105">Syntax</span></span>


```C++
HRESULT RemovePropertyData(
  [in] const GUID *pPropertyDataId
);
```



## <a name="parameters"></a><span data-ttu-id="c654e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c654e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c654e-107">*ppropertydataid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c654e-107">*pPropertyDataId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c654e-108">Der Bezeichner der zu entfernenden Daten.</span><span class="sxs-lookup"><span data-stu-id="c654e-108">The identifier of the data to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c654e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c654e-109">Return value</span></span>

<span data-ttu-id="c654e-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c654e-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c654e-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c654e-111">Remarks</span></span>

<span data-ttu-id="c654e-112">**E \_ InvalidArg** wird zurückgegeben, wenn der *ppropertydataid* -Parameter einer der Eigenschaften Konstanten für [Kontext Knoten](context-node-properties.md) ist.</span><span class="sxs-lookup"><span data-stu-id="c654e-112">**E\_INVALIDARG** is returned if the *pPropertyDataId* parameter is one of the [Context Node Properties](context-node-properties.md) constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="c654e-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c654e-113">Requirements</span></span>



| <span data-ttu-id="c654e-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c654e-114">Requirement</span></span> | <span data-ttu-id="c654e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c654e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c654e-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c654e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c654e-117">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c654e-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c654e-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c654e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c654e-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c654e-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c654e-120">Header</span><span class="sxs-lookup"><span data-stu-id="c654e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c654e-121"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c654e-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c654e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="c654e-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c654e-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c654e-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c654e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c654e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c654e-125">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="c654e-125">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="c654e-126">**Icontextnode:: AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="c654e-126">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="c654e-127">**Icontextnode:: ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="c654e-127">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="c654e-128">**Icontextnode:: GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="c654e-128">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="c654e-129">**Icontextnode:: GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="c654e-129">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="c654e-130">**Icontextnode:: loadpropertiesdata**</span><span class="sxs-lookup"><span data-stu-id="c654e-130">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="c654e-131">**Icontextnode:: savepropertiesdata**</span><span class="sxs-lookup"><span data-stu-id="c654e-131">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="c654e-132">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="c654e-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




