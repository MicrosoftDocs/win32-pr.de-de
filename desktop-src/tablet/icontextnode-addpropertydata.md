---
description: Fügt eine bestimmte anwendungsspezifische Daten hinzu.
ms.assetid: 86ba37ac-8e65-4397-8ed1-37463152bebd
title: 'Icontextnode:: AddPropertyData-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.AddPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ed318520b8ac83acbc8ed615002fababe2a4b12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129508"
---
# <a name="icontextnodeaddpropertydata-method"></a><span data-ttu-id="e8be6-103">Icontextnode:: AddPropertyData-Methode</span><span class="sxs-lookup"><span data-stu-id="e8be6-103">IContextNode::AddPropertyData method</span></span>

<span data-ttu-id="e8be6-104">Fügt eine bestimmte anwendungsspezifische Daten hinzu.</span><span class="sxs-lookup"><span data-stu-id="e8be6-104">Adds a piece of application-specific data.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8be6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8be6-105">Syntax</span></span>


```C++
HRESULT AddPropertyData(
  [in] const GUID  *pPropertyDataId,
  [in]       ULONG ulPropertyDataSize,
  [in]       BYTE  *pbPropertiesData
);
```



## <a name="parameters"></a><span data-ttu-id="e8be6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8be6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8be6-107">*ppropertydataid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8be6-107">*pPropertyDataId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8be6-108">Eine Globally Unique Identifier (GUID), die zum Identifizieren des Datentyps verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e8be6-108">A globally unique identifier (GUID) that is used to identify the type of data.</span></span>

</dd> <dt>

<span data-ttu-id="e8be6-109">*ulpropertydatasize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8be6-109">*ulPropertyDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8be6-110">Die Größe der Daten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="e8be6-110">The size of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e8be6-111">*pbpropertiesdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8be6-111">*pbPropertiesData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8be6-112">\[in ist size \_ (ulpropertydatasize)\]</span><span class="sxs-lookup"><span data-stu-id="e8be6-112">\[in, size\_is(ulPropertyDataSize)\]</span></span>

<span data-ttu-id="e8be6-113">Ein Array von 8-Bit-Ganzzahlen ohne Vorzeichen, das die hinzu zufügenden Eigenschaften Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="e8be6-113">An 8-bit unsigned integer array containing the property information to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8be6-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8be6-114">Return value</span></span>

<span data-ttu-id="e8be6-115">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e8be6-115">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e8be6-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8be6-116">Remarks</span></span>

<span data-ttu-id="e8be6-117">Verwenden Sie **icontextnode:: AddPropertyData** zum Zuordnen von Daten zu einem Kontext Knoten.</span><span class="sxs-lookup"><span data-stu-id="e8be6-117">Use **IContextNode::AddPropertyData** to associate data with a context node.</span></span> <span data-ttu-id="e8be6-118">Um die Daten zu einem späteren Zeitpunkt abzurufen, verwenden Sie [**icontextnode:: GetPropertyData**](icontextnode-getpropertydata.md).</span><span class="sxs-lookup"><span data-stu-id="e8be6-118">To retrieve the data later, use [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md).</span></span>

<span data-ttu-id="e8be6-119">Der Ink Analyzer kann den Knoten als Teil der frei Hand Analyse löschen, es sei denn, der Kontext Knoten ist bestätigt (siehe [**icontextnode:: Confirm**](icontextnode-confirm.md)).</span><span class="sxs-lookup"><span data-stu-id="e8be6-119">The ink analyzer may delete the node as part of ink analysis, unless the context node is confirmed (see [**IContextNode::Confirm**](icontextnode-confirm.md)).</span></span> <span data-ttu-id="e8be6-120">Weitere Informationen zum Synchronisieren von Anwendungsdaten mit [**iinkanalyzer**](iinkanalyzer.md)finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e8be6-120">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8be6-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8be6-121">Requirements</span></span>



| <span data-ttu-id="e8be6-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8be6-122">Requirement</span></span> | <span data-ttu-id="e8be6-123">Wert</span><span class="sxs-lookup"><span data-stu-id="e8be6-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8be6-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e8be6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e8be6-125">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8be6-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e8be6-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e8be6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e8be6-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e8be6-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e8be6-128">Header</span><span class="sxs-lookup"><span data-stu-id="e8be6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8be6-129"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e8be6-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e8be6-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e8be6-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8be6-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8be6-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e8be6-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8be6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8be6-133">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="e8be6-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="e8be6-134">**Icontextnode:: GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="e8be6-134">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="e8be6-135">**Icontextnode:: GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="e8be6-135">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="e8be6-136">**Icontextnode:: ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="e8be6-136">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="e8be6-137">**Icontextnode:: loadpropertiesdata**</span><span class="sxs-lookup"><span data-stu-id="e8be6-137">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="e8be6-138">**Icontextnode:: RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="e8be6-138">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="e8be6-139">**Icontextnode:: savepropertiesdata**</span><span class="sxs-lookup"><span data-stu-id="e8be6-139">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> </dl>

 

 




