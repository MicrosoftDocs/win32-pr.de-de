---
description: 'Erstellt die anwendungsspezifischen und internen Eigenschaften Daten für ein Bytearray, das zuvor mit icontextnode:: savepropertiesdata erstellt wurde.'
ms.assetid: 2d24d0da-16f1-4ddc-8e2e-93c312ecfa42
title: 'Icontextnode:: loadpropertiesdata-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.LoadPropertiesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc495aaa52ebfbca088f954b34f22f9d6e1e53d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354501"
---
# <a name="icontextnodeloadpropertiesdata-method"></a><span data-ttu-id="05930-103">Icontextnode:: loadpropertiesdata-Methode</span><span class="sxs-lookup"><span data-stu-id="05930-103">IContextNode::LoadPropertiesData method</span></span>

<span data-ttu-id="05930-104">Erstellt die anwendungsspezifischen und internen Eigenschaften Daten für ein Bytearray, das zuvor mit [**icontextnode:: savepropertiesdata**](icontextnode-savepropertiesdata.md)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="05930-104">Recreates the application-specific and internal property data for an array of bytes that was previously created with [**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="05930-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="05930-105">Syntax</span></span>


```C++
HRESULT LoadPropertiesData(
  [in]  ULONG        cbPropertiesDataSize,
  [in]  BYTE         *pbPropertiesData,
  [out] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a><span data-ttu-id="05930-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="05930-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05930-107">*cbpropertiesdatasize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="05930-107">*cbPropertiesDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05930-108">Die Größe des Properties-Daten Arrays.</span><span class="sxs-lookup"><span data-stu-id="05930-108">The size of the properties data array.</span></span>

</dd> <dt>

<span data-ttu-id="05930-109">*pbpropertiesdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="05930-109">*pbPropertiesData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05930-110">Das Array von 8-Bit-Ganzzahlen ohne Vorzeichen, das zu ladende Eigenschaften Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="05930-110">The 8-bit unsigned integer array containing property information to load.</span></span>

</dd> <dt>

<span data-ttu-id="05930-111">*pferfolgreich* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="05930-111">*pfSuccessful* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05930-112">**Variant \_ TRUE** , wenn die Eigenschaften Daten erfolgreich geladen wurden. Andernfalls ist der Wert **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="05930-112">**VARIANT\_TRUE** if the property data loaded successfully; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05930-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="05930-113">Return value</span></span>

<span data-ttu-id="05930-114">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="05930-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05930-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05930-115">Requirements</span></span>



| <span data-ttu-id="05930-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05930-116">Requirement</span></span> | <span data-ttu-id="05930-117">Wert</span><span class="sxs-lookup"><span data-stu-id="05930-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05930-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="05930-118">Minimum supported client</span></span><br/> | <span data-ttu-id="05930-119">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05930-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="05930-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="05930-120">Minimum supported server</span></span><br/> | <span data-ttu-id="05930-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="05930-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="05930-122">Header</span><span class="sxs-lookup"><span data-stu-id="05930-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="05930-123"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="05930-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="05930-124">DLL</span><span class="sxs-lookup"><span data-stu-id="05930-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05930-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05930-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="05930-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05930-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05930-127">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="05930-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="05930-128">**Icontextnode:: AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="05930-128">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="05930-129">**Icontextnode:: ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="05930-129">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="05930-130">**Icontextnode:: GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="05930-130">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="05930-131">**Icontextnode:: GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="05930-131">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="05930-132">**Icontextnode:: RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="05930-132">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="05930-133">**Icontextnode:: savepropertiesdata**</span><span class="sxs-lookup"><span data-stu-id="05930-133">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="05930-134">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="05930-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




