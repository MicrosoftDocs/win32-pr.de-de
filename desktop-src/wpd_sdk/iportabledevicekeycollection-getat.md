---
description: Die GetAt-Methode ruft einen PropertyKey aus der Auflistung nach Index ab.
ms.assetid: 9a3c5c28-39b4-4d53-a8d7-0f5a0d4d89ad
title: 'Iportabledevicekeycollection:: GetAt-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: b75285f6dcdb0961312fa1db8f5c912b771bd786
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359647"
---
# <a name="iportabledevicekeycollectiongetat-method"></a><span data-ttu-id="a71d1-103">Iportabledevicekeycollection:: GetAt-Methode</span><span class="sxs-lookup"><span data-stu-id="a71d1-103">IPortableDeviceKeyCollection::GetAt method</span></span>

<span data-ttu-id="a71d1-104">Die **GetAt** -Methode ruft einen **PropertyKey** aus der Auflistung nach Index ab.</span><span class="sxs-lookup"><span data-stu-id="a71d1-104">The **GetAt** method retrieves a **PROPERTYKEY** from the collection by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="a71d1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a71d1-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPERTYKEY *pKey
);
```



## <a name="parameters"></a><span data-ttu-id="a71d1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a71d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a71d1-107">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a71d1-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a71d1-108">**DWORD** , das den Index des abzurufenden Schlüssels enthält.</span><span class="sxs-lookup"><span data-stu-id="a71d1-108">**DWORD** that contains the index of the key to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="a71d1-109">*pkey* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a71d1-109">*pKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a71d1-110">Zeiger auf ein **PropertyKey** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="a71d1-110">Pointer to a **PROPERTYKEY** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a71d1-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a71d1-111">Return value</span></span>

<span data-ttu-id="a71d1-112">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="a71d1-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a71d1-113">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a71d1-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a71d1-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a71d1-114">Return code</span></span>                                                                                  | <span data-ttu-id="a71d1-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a71d1-115">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="a71d1-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a71d1-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="a71d1-117">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a71d1-117">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="a71d1-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="a71d1-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="a71d1-119">Der über gegebene Index lag außerhalb des zulässigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="a71d1-119">The index passed in was out of range.</span></span><br/>     |
| <dl> <span data-ttu-id="a71d1-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="a71d1-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="a71d1-121">Ein erforderliches Zeigerargument war **null**.</span><span class="sxs-lookup"><span data-stu-id="a71d1-121">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="a71d1-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a71d1-122">Examples</span></span>

<span data-ttu-id="a71d1-123">Ein Beispiel für die Verwendung dieser Methode finden Sie [unter Abrufen unterstützter Dienst Ereignisse](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="a71d1-123">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a71d1-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a71d1-124">Requirements</span></span>



| <span data-ttu-id="a71d1-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a71d1-125">Requirement</span></span> | <span data-ttu-id="a71d1-126">Wert</span><span class="sxs-lookup"><span data-stu-id="a71d1-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a71d1-127">Header</span><span class="sxs-lookup"><span data-stu-id="a71d1-127">Header</span></span><br/>  | <dl> <span data-ttu-id="a71d1-128"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="a71d1-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="a71d1-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a71d1-129">Library</span></span><br/> | <dl> <span data-ttu-id="a71d1-130"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a71d1-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a71d1-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a71d1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a71d1-132">**Iportabledevicekeycollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a71d1-132">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="a71d1-133">Abrufen unterstützter Dienst Ereignisse</span><span class="sxs-lookup"><span data-stu-id="a71d1-133">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="a71d1-134">Abrufen unterstützter Dienst Methoden</span><span class="sxs-lookup"><span data-stu-id="a71d1-134">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> </dl>

 

 




