---
description: Die Add-Methode fügt der Auflistung einen Eigenschafts Schlüssel hinzu.
ms.assetid: 640ef1c4-2843-48dd-a30a-9a2ef9de35b9
title: 'Iportabledevicekeycollection:: Add-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e43fea25a08969b2ae8169884d51ddc46f8c7136
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370782"
---
# <a name="iportabledevicekeycollectionadd-method"></a><span data-ttu-id="0e00c-103">Iportabledevicekeycollection:: Add-Methode</span><span class="sxs-lookup"><span data-stu-id="0e00c-103">IPortableDeviceKeyCollection::Add method</span></span>

<span data-ttu-id="0e00c-104">Die **Add** -Methode fügt der Auflistung einen Eigenschafts Schlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="0e00c-104">The **Add** method adds a property key to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e00c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e00c-105">Syntax</span></span>


```C++
HRESULT Add(
  [in] REFPROPERTYKEY Key
);
```



## <a name="parameters"></a><span data-ttu-id="0e00c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e00c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e00c-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e00c-107">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e00c-108">Ein **refpropertykey** , der der Auflistung hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0e00c-108">A **REFPROPERTYKEY** to add to the collection.</span></span> <span data-ttu-id="0e00c-109">Diese Methode kopiert den Schlüssel in die Auflistung, sodass Sie die lokale Variable freigeben können, nachdem Sie diese Methode aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="0e00c-109">This method copies the key to the collection, so you can release the local variable after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e00c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e00c-110">Return value</span></span>

<span data-ttu-id="0e00c-111">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="0e00c-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0e00c-112">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0e00c-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0e00c-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0e00c-113">Return code</span></span>                                                                                   | <span data-ttu-id="0e00c-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e00c-114">Description</span></span>                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0e00c-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0e00c-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0e00c-116">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0e00c-116">The method succeeded.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="0e00c-117"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="0e00c-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0e00c-118">Es ist nicht genügend Arbeitsspeicher verfügbar, um der Sammlung den Schlüssel hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="0e00c-118">There is not enough memory available to add the key to the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="0e00c-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0e00c-119">Examples</span></span>

<span data-ttu-id="0e00c-120">Ein Beispiel für die Verwendung dieser Methode finden Sie unter [Abrufen von Eigenschaften für ein einzelnes Objekt](retrieving-properties-for-a-single-object.md).</span><span class="sxs-lookup"><span data-stu-id="0e00c-120">For an example of how to use this method, see [Retrieving Properties for a Single Object](retrieving-properties-for-a-single-object.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e00c-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e00c-121">Requirements</span></span>



| <span data-ttu-id="0e00c-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e00c-122">Requirement</span></span> | <span data-ttu-id="0e00c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="0e00c-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e00c-124">Header</span><span class="sxs-lookup"><span data-stu-id="0e00c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0e00c-125"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e00c-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="0e00c-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0e00c-126">Library</span></span><br/> | <dl> <span data-ttu-id="0e00c-127"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e00c-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e00c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e00c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e00c-129">**Iportabledevicekeycollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0e00c-129">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="0e00c-130">Abrufen von Content-Object-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0e00c-130">Retrieving Content-Object Properties</span></span>](retrieving-content-object-properties.md)
</dt> <dt>

[<span data-ttu-id="0e00c-131">Abrufen von Eigenschaften für ein einzelnes Objekt</span><span class="sxs-lookup"><span data-stu-id="0e00c-131">Retrieving Properties for a Single Object</span></span>](retrieving-properties-for-a-single-object.md)
</dt> <dt>

[<span data-ttu-id="0e00c-132">Abrufen der von einem Gerät unterstützten Renderingfunktionen</span><span class="sxs-lookup"><span data-stu-id="0e00c-132">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




