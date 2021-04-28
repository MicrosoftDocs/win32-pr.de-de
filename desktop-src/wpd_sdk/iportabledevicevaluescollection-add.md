---
description: 'IPortableDeviceValuesCollection::Add-Methode: Die Add-Methode fügt der Auflistung ein Element hinzu.'
ms.assetid: 3b06abc4-f0ab-4b02-b3a7-360615f86a2a
title: IPortableDeviceValuesCollection::Add-Methode (PortableDeviceTypes.h)
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
ms.openlocfilehash: 765100e1272fc6766e9f305f37f3b699bd96beb8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083240"
---
# <a name="iportabledevicevaluescollectionadd-method"></a><span data-ttu-id="bce7a-103">IPortableDeviceValuesCollection::Add-Methode</span><span class="sxs-lookup"><span data-stu-id="bce7a-103">IPortableDeviceValuesCollection::Add method</span></span>

<span data-ttu-id="bce7a-104">Die **Add-Methode** fügt der Auflistung ein Element hinzu.</span><span class="sxs-lookup"><span data-stu-id="bce7a-104">The **Add** method adds an item to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="bce7a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bce7a-105">Syntax</span></span>


```C++
HRESULT Add(
  [in] IPortableDeviceValues *pValues
);
```



## <a name="parameters"></a><span data-ttu-id="bce7a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bce7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bce7a-107">*pValues* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="bce7a-107">*pValues* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bce7a-108">Zeiger auf eine **IPortableDeviceValues-Schnittstelle,** die der Auflistung hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bce7a-108">Pointer to an **IPortableDeviceValues** interface to add to the collection.</span></span> <span data-ttu-id="bce7a-109">Die Schnittstelle wird nicht tatsächlich kopiert, aber **AddRef** wird dafür aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="bce7a-109">The interface is not actually copied, but **AddRef** is called on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bce7a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bce7a-110">Return value</span></span>

<span data-ttu-id="bce7a-111">Die -Methode gibt ein **HRESULT zurück.**</span><span class="sxs-lookup"><span data-stu-id="bce7a-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="bce7a-112">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="bce7a-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="bce7a-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="bce7a-113">Return code</span></span>                                                                                   | <span data-ttu-id="bce7a-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bce7a-114">Description</span></span>                                                                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bce7a-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bce7a-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="bce7a-116">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bce7a-116">The method succeeded.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="bce7a-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="bce7a-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="bce7a-118">Es ist nicht genügend Arbeitsspeicher verfügbar, um den Wert zur Auflistung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="bce7a-118">There is not enough memory available to add the value to the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bce7a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bce7a-119">Requirements</span></span>



| <span data-ttu-id="bce7a-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bce7a-120">Requirement</span></span> | <span data-ttu-id="bce7a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="bce7a-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bce7a-122">Header</span><span class="sxs-lookup"><span data-stu-id="bce7a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="bce7a-123"><dt>PortableDeviceTypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="bce7a-123"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="bce7a-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bce7a-124">Library</span></span><br/> | <dl> <span data-ttu-id="bce7a-125"><dt>PortableDeviceGUIDs.lib</dt></span><span class="sxs-lookup"><span data-stu-id="bce7a-125"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bce7a-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bce7a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bce7a-127">**IPortableDeviceValuesCollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="bce7a-127">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




