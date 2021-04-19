---
description: Die Add-Methode fügt der Auflistung ein Element hinzu.
ms.assetid: e9e8975f-f9b8-4940-b967-020cf3812582
title: 'Iportabledevicepropvariantcollection:: Add-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d9d5b4ee664d2fbbcc78550b1af5a48874d153d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373846"
---
# <a name="iportabledevicepropvariantcollectionadd-method"></a><span data-ttu-id="0515e-103">Iportabledevicepropvariantcollection:: Add-Methode</span><span class="sxs-lookup"><span data-stu-id="0515e-103">IPortableDevicePropVariantCollection::Add method</span></span>

<span data-ttu-id="0515e-104">Die **Add** -Methode fügt der Auflistung ein Element hinzu.</span><span class="sxs-lookup"><span data-stu-id="0515e-104">The **Add** method adds an item to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0515e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0515e-105">Syntax</span></span>


```C++
HRESULT Add(
  [in] const PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="0515e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0515e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0515e-107">*pValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0515e-107">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0515e-108">Zeiger auf ein neues **PROPVARIANT** -Objekt, das der Auflistung hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0515e-108">Pointer to a new **PROPVARIANT** object to add to the collection.</span></span> <span data-ttu-id="0515e-109">Diese Methode kopiert die **PROPVARIANT** in die Auflistung. Daher sollten Sie Ihre lokale Kopie der Variablen freigeben, indem Sie **propvariantclear** aufrufen, nachdem Sie diese Methode aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="0515e-109">This method copies the **PROPVARIANT** to the collection, so you should release your local copy of the variable by calling **PropVariantClear** after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0515e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0515e-110">Return value</span></span>

<span data-ttu-id="0515e-111">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="0515e-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0515e-112">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0515e-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0515e-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0515e-113">Return code</span></span>                                                                          | <span data-ttu-id="0515e-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0515e-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0515e-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0515e-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0515e-116">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0515e-116">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0515e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0515e-117">Remarks</span></span>

<span data-ttu-id="0515e-118">Wenn VarType für *pValue den Wert* VT \_ Vector oder VT \_ UI1 aufweist, wird das Festlegen und Abrufen eines Puffers, **der NULL** oder NULL ist, nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0515e-118">When the VARTYPE for *pValue* is VT\_VECTOR or VT\_UI1, setting and retrieving a **NULL** or zero-sized buffer is not supported.</span></span> <span data-ttu-id="0515e-119">Beispielsweise sind weder pValue. Caub. pelems = **null** noch pValue. Caub. celems = 0 zulässig.</span><span class="sxs-lookup"><span data-stu-id="0515e-119">For example, neither pValue.caub.pElems = **NULL** nor pValue.caub.cElems = 0 are allowed.</span></span>

<span data-ttu-id="0515e-120">Wenn ein Aufrufer versucht, ein Element eines anderen in der Auflistung enthaltenen VarType hinzuzufügen, und der PROPVARIANT-Wert nicht automatisch von dieser Schnittstelle geändert werden kann, schlägt diese Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="0515e-120">If a caller tries to add an item of a different VARTYPE contained in the collection and the PROPVARIANT value cannot be changed by this interface automatically, this method will fail.</span></span> <span data-ttu-id="0515e-121">Um den Sammlungstyp manuell zu ändern, nennen Sie [**iportabledevicepropvariantcollection:: ChangeType**](iportabledevicepropvariantcollection-changetype.md).</span><span class="sxs-lookup"><span data-stu-id="0515e-121">To change the collection type manually, call [**IPortableDevicePropVariantCollection::ChangeType**](iportabledevicepropvariantcollection-changetype.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0515e-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0515e-122">Examples</span></span>

<span data-ttu-id="0515e-123">Ein Beispiel für die Verwendung dieser Methode finden Sie unter [Abrufen eines Objekt Bezeichners aus einem persistenten eindeutigen Bezeichner](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md) .</span><span class="sxs-lookup"><span data-stu-id="0515e-123">For an example of how to use this method, see [Retrieving an Object Identifier from a Persistent Unique Identifier](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="0515e-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0515e-124">Requirements</span></span>



| <span data-ttu-id="0515e-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0515e-125">Requirement</span></span> | <span data-ttu-id="0515e-126">Wert</span><span class="sxs-lookup"><span data-stu-id="0515e-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0515e-127">Header</span><span class="sxs-lookup"><span data-stu-id="0515e-127">Header</span></span><br/>  | <dl> <span data-ttu-id="0515e-128"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="0515e-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="0515e-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0515e-129">Library</span></span><br/> | <dl> <span data-ttu-id="0515e-130"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0515e-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0515e-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0515e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0515e-132">**Iportabledevicepropvariantcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0515e-132">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="0515e-133">Verschieben von Inhalt auf dem Gerät</span><span class="sxs-lookup"><span data-stu-id="0515e-133">Moving Content on the Device</span></span>](moving-content-on-the-device.md)
</dt> <dt>

[<span data-ttu-id="0515e-134">Abrufen eines Objekt Bezeichners aus einem persistenten eindeutigen Bezeichner</span><span class="sxs-lookup"><span data-stu-id="0515e-134">Retrieving an Object Identifier from a Persistent Unique Identifier</span></span>](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> </dl>

 

 




