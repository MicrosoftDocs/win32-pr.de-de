---
description: Die Add-Methode fügt der Auflistung ein Element hinzu.
ms.assetid: 3b06abc4-f0ab-4b02-b3a7-360615f86a2a
title: 'Iportabledevicevaluescollection:: Add-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 1f423ac7243c8d16fa75978ae5c9bcf04136bb05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365393"
---
# <a name="iportabledevicevaluescollectionadd-method"></a><span data-ttu-id="615de-103">Iportabledevicevaluescollection:: Add-Methode</span><span class="sxs-lookup"><span data-stu-id="615de-103">IPortableDeviceValuesCollection::Add method</span></span>

<span data-ttu-id="615de-104">Die **Add** -Methode fügt der Auflistung ein Element hinzu.</span><span class="sxs-lookup"><span data-stu-id="615de-104">The **Add** method adds an item to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="615de-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="615de-105">Syntax</span></span>


```C++
HRESULT Add(
  [in] IPortableDeviceValues *pValues
);
```



## <a name="parameters"></a><span data-ttu-id="615de-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="615de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="615de-107">*pvalues* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="615de-107">*pValues* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="615de-108">Zeiger auf eine **iportabledecovicevalues** -Schnittstelle, die der Auflistung hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="615de-108">Pointer to an **IPortableDeviceValues** interface to add to the collection.</span></span> <span data-ttu-id="615de-109">Die Schnittstelle wird nicht tatsächlich kopiert, aber die **adressf** wird darauf aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="615de-109">The interface is not actually copied, but **AddRef** is called on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="615de-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="615de-110">Return value</span></span>

<span data-ttu-id="615de-111">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="615de-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="615de-112">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="615de-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="615de-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="615de-113">Return code</span></span>                                                                                   | <span data-ttu-id="615de-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="615de-114">Description</span></span>                                                                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="615de-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="615de-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="615de-116">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="615de-116">The method succeeded.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="615de-117"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="615de-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="615de-118">Es ist nicht genügend Arbeitsspeicher verfügbar, um den Wert der Auflistung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="615de-118">There is not enough memory available to add the value to the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="615de-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="615de-119">Requirements</span></span>



| <span data-ttu-id="615de-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="615de-120">Requirement</span></span> | <span data-ttu-id="615de-121">Wert</span><span class="sxs-lookup"><span data-stu-id="615de-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="615de-122">Header</span><span class="sxs-lookup"><span data-stu-id="615de-122">Header</span></span><br/>  | <dl> <span data-ttu-id="615de-123"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="615de-123"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="615de-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="615de-124">Library</span></span><br/> | <dl> <span data-ttu-id="615de-125"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="615de-125"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="615de-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="615de-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="615de-127">**Iportableabvicevaluescollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="615de-127">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




