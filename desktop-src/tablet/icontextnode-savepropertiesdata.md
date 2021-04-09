---
description: Ruft ein Bytearray ab, das die anwendungsspezifischen und internen Eigenschaften Daten für diesen icontextnode enthält.
ms.assetid: f26d71a7-fe71-48a8-9c8f-9c4d99261df1
title: 'Icontextnode:: savepropertiesdata-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SavePropertiesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f2ac064632eb9e5dd2b94f6e75b9b2836c75996d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958974"
---
# <a name="icontextnodesavepropertiesdata-method"></a><span data-ttu-id="8b268-103">Icontextnode:: savepropertiesdata-Methode</span><span class="sxs-lookup"><span data-stu-id="8b268-103">IContextNode::SavePropertiesData method</span></span>

<span data-ttu-id="8b268-104">Ruft ein Bytearray ab, das die anwendungsspezifischen und internen Eigenschaften Daten für diesen [**icontextnode**](icontextnode.md)enthält.</span><span class="sxs-lookup"><span data-stu-id="8b268-104">Retrieves an array of bytes that contains the application-specific and internal property data for this [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8b268-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b268-105">Syntax</span></span>


```C++
HRESULT SavePropertiesData(
  [in, out] ULONG *pulPropertiesDataSize,
  [out]     BYTE  **ppbPropertiesData
);
```



## <a name="parameters"></a><span data-ttu-id="8b268-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b268-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b268-107">*pulpropertiesdatasize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8b268-107">*pulPropertiesDataSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b268-108">Die Größe des Daten Arrays, das die Eigenschaften Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="8b268-108">The size of the data array containing the property information.</span></span> <span data-ttu-id="8b268-109">Der Übergabe Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8b268-109">The value passed in is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8b268-110">*ppbpropertiesdata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8b268-110">*ppbPropertiesData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b268-111">Ein Zeiger auf ein Array von 8-Bit-Ganzzahlen ohne Vorzeichen, das die anwendungsspezifischen und internen Eigenschaften Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="8b268-111">A pointer to an 8-bit unsigned integer array that contains the application-specific and internal property data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b268-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b268-112">Return value</span></span>

<span data-ttu-id="8b268-113">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="8b268-113">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8b268-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b268-114">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="8b268-115">Um einen Speicherplatz zu vermeiden, verwenden Sie " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ", um den Arbeitsspeicher von \* *ppbpropertiesdata* freizugeben, wenn Sie die Informationen nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="8b268-115">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppbPropertiesData* when you no longer need the information.</span></span>

 

<span data-ttu-id="8b268-116">Verwenden Sie diese Methode, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="8b268-116">Use this method when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="8b268-117">Diese Methode speichert die Eigenschafts Daten, die von **iinkanalyzer** auf dem [**icontextnode**](icontextnode.md)festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="8b268-117">This method saves the property data that the **IInkAnalyzer** has set on the [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="8b268-118">Weitere Informationen zum Synchronisieren von Anwendungsdaten mit [**iinkanalyzer**](iinkanalyzer.md)finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="8b268-118">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8b268-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b268-119">Requirements</span></span>



| <span data-ttu-id="8b268-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b268-120">Requirement</span></span> | <span data-ttu-id="8b268-121">Wert</span><span class="sxs-lookup"><span data-stu-id="8b268-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b268-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b268-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8b268-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b268-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8b268-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b268-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8b268-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8b268-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8b268-126">Header</span><span class="sxs-lookup"><span data-stu-id="8b268-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b268-127"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8b268-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8b268-128">DLL</span><span class="sxs-lookup"><span data-stu-id="8b268-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b268-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b268-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8b268-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b268-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b268-131">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="8b268-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="8b268-132">**Icontextnode:: loadpropertiesdata**</span><span class="sxs-lookup"><span data-stu-id="8b268-132">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="8b268-133">**Icontextnode:: AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="8b268-133">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="8b268-134">**Icontextnode:: GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="8b268-134">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="8b268-135">**Icontextnode:: RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="8b268-135">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="8b268-136">**Icontextnode:: GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="8b268-136">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="8b268-137">**Icontextnode:: ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="8b268-137">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="8b268-138">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="8b268-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

